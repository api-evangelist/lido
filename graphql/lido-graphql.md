# Lido Finance GraphQL API

## Description

Lido Finance exposes on-chain protocol data through a subgraph on The Graph protocol. The subgraph indexes Ethereum mainnet events from the Lido stETH contract, the Withdrawal Queue, the Node Operator Registry, the on-chain Oracle, and the Aragon-based Lido DAO (voting, Easy Track motions). It provides a GraphQL query interface for staking activity, reward accounting, node operator management, governance, and withdrawal queue mechanics.

## Endpoint

- **Mainnet (The Graph Hosted):** `https://api.thegraph.com/subgraphs/name/lidofinance/lido`
- **Decentralized Network:** Query via The Graph Network using subgraph ID for `lidofinance/lido`

## Documentation

- Subgraph source: https://github.com/lidofinance/lido-subgraph
- Schema source: https://github.com/lidofinance/lido-subgraph/blob/master/schema.graphql
- The Graph hosted service docs: https://thegraph.com/docs/en/querying/querying-the-graph/
- Lido integrations overview: https://docs.lido.fi/integrations/api

## Key Entity Types

| Type | Description |
|---|---|
| `LidoTransfer` | stETH ERC-20 transfer events with share and balance snapshots |
| `LidoApproval` | stETH ERC-20 approval events |
| `LidoSubmission` | ETH deposit / staking submissions with share accounting |
| `TotalReward` | Oracle-reported reward distribution including fees, APR, and share splits |
| `NodeOperatorFees` | Per-operator fee disbursements linked to a TotalReward |
| `NodeOperatorsShares` | Per-operator share allocations linked to a TotalReward |
| `NodeOperator` | Curated Module node operator records (name, reward address, key counts) |
| `NodeOperatorSigningKey` | Validator signing keys registered per node operator |
| `OracleReport` | Accounting report submitted by the Lido Oracle |
| `OracleCompleted` | Finalized oracle epoch completion events |
| `OracleMember` | Oracle committee member records |
| `OracleConfig` | Oracle configuration parameters (quorum, epochs per frame, etc.) |
| `LidoConfig` | Protocol-level configuration (insurance fund, treasury, staking limits, locator) |
| `Totals` | Running totals of pooled ETH and shares |
| `Stats` | Aggregate stats: unique holders, last oracle epoch |
| `Shares` | Per-address share balances |
| `Holder` | stETH holder records (current and anytime) |
| `CurrentFees` | Current fee basis points (treasury, insurance, operators) |
| `SharesBurn` | Share burn events (used in withdrawal finalization) |
| `WithdrawalRequested` | Withdrawal queue request events (stETH amount, shares, owner) |
| `WithdrawalClaimed` | Claimed withdrawal events (ETH released, receiver) |
| `WithdrawalsFinalized` | Batch finalization events for the withdrawal queue |
| `WithdrawalQueueConfig` | Withdrawal queue configuration (bunker mode, pause state) |
| `Voting` | Aragon DAO vote records |
| `Vote` | Individual votes cast on a Voting |
| `VotingObjection` | Objection phase votes on a Voting |
| `VotingConfig` | DAO voting configuration parameters |
| `Motion` | Easy Track motion records (EVM script, status, objection counts) |
| `Objection` | Individual objections filed against an Easy Track motion |
| `EasyTrackConfig` | Easy Track system configuration |
| `EVMScriptFactory` | Registered EVM script factory contracts |
| `Role` | ACL role assignments |
| `BeaconReport` | Individual oracle member beacon chain reports |
| `OracleExpectedEpoch` | Expected epoch tracking for oracle consensus |
| `AppVersion` | Aragon app version records |

## Example Queries

### Recent stETH submissions (deposits)
```graphql
{
  lidoSubmissions(first: 10, orderBy: blockTime, orderDirection: desc) {
    id
    sender
    amount
    shares
    totalPooledEtherAfter
    blockTime
    transactionHash
  }
}
```

### Latest oracle reward report
```graphql
{
  totalRewards(first: 1, orderBy: blockTime, orderDirection: desc) {
    id
    totalRewards
    apr
    aprBeforeFees
    feeBasis
    totalPooledEtherAfter
    totalSharesAfter
    blockTime
    transactionHash
  }
}
```

### Node operators
```graphql
{
  nodeOperators(where: { active: true }) {
    id
    name
    rewardAddress
    stakingLimit
    totalKeysTrimmed
    nonce
  }
}
```

### Recent withdrawal requests
```graphql
{
  withdrawalRequesteds(first: 10, orderBy: blockTime, orderDirection: desc) {
    requestId
    requestor
    owner
    amountOfStETH
    amountOfShares
    blockTime
    transactionHash
  }
}
```

## Notes

- The subgraph is open-source under the lidofinance GitHub organization.
- All amounts are in Wei (BigInt). APR values are BigDecimal (annualized, post-fee).
- The hosted service endpoint may have rate limits; for production use query via the decentralized Graph Network.
- The subgraph covers the Ethereum mainnet Lido V1 and V2 (post-Shapella) contract events. Polygon (stMATIC) and Solana (stSOL) subgraphs are separate and those protocols have been sunset.
- `OracleCompleted` and `OracleReport` reflect the legacy and V2 oracle accounting models respectively.
