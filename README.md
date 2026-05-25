# Lido

Lido — Ethereum liquid staking protocol (stETH / wstETH); #1 liquid staking provider by TVL.

## Overview

Lido is the leading liquid staking protocol on Ethereum. Users deposit ETH and receive stETH, a rebasing ERC-20 that earns daily staking rewards, or its wrapped non-rebasing form wstETH that flows freely across DeFi. The protocol is governed by the Lido DAO via the LDO token, with on-chain Aragon voting, off-chain Snapshot signaling, and a Dual Governance timelock giving stETH holders a dynamic veto over the DAO.

Lido's validator set is delegated across multiple Staking Modules — the Curated Module of professional node operators, Simple DVT (Obol + SSV), the permissionless Community Staking Module backed by bonded stETH, and stVaults for tailored modular setups. With over $18B TVL and 8.8M+ ETH staked, Lido is the #1 liquid staking provider by total value locked.

Lido previously operated on Polygon (stMATIC, sunset June 2025) and Solana (stSOL, sunset February 2024); the protocol is now Ethereum-only.

## Public HTTP APIs

| API | Purpose | Base URL |
| --- | --- | --- |
| Lido APR API | Latest and 7-day SMA stETH staking APR | `https://eth-api.lido.fi/v1/protocol/steth/apr/` |
| Reward History API | Per-address stETH reward history with fiat conversion | `https://reward-history-backend.lido.fi/` |
| Withdrawals API | Estimated withdrawal queue finalization times | `https://wq-api.lido.fi/v2/request-time` |
| Keys API | Node operator validator keys across staking modules | `https://github.com/lidofinance/lido-keys-api` |

A mirror of each public API runs on the Hoodi testnet (`*.testnet.fi`).

## Open Source

- Core smart contracts: [lidofinance/core](https://github.com/lidofinance/core) (Solidity, GPL-3.0)
- Community Staking Module: [lidofinance/community-staking-module](https://github.com/lidofinance/community-staking-module)
- Dual Governance: [lidofinance/dual-governance](https://github.com/lidofinance/dual-governance)
- TypeScript SDK: [`@lidofinance/lido-ethereum-sdk`](https://www.npmjs.com/package/@lidofinance/lido-ethereum-sdk) (MIT)
- Lido Oracle: [lidofinance/lido-oracle](https://github.com/lidofinance/lido-oracle) (Python daemon)
- Validator monitoring: [lidofinance/ethereum-validators-monitoring](https://github.com/lidofinance/ethereum-validators-monitoring)
- CLI: [lidofinance/lido-cli](https://github.com/lidofinance/lido-cli)
- Staking widget: [lidofinance/ethereum-staking-widget](https://github.com/lidofinance/ethereum-staking-widget)
- Subgraph: [lidofinance/lido-subgraph](https://github.com/lidofinance/lido-subgraph)
- LIPs: [lidofinance/lido-improvement-proposals](https://github.com/lidofinance/lido-improvement-proposals)

## Resources

- Website: <https://lido.fi>
- Staking app: <https://stake.lido.fi>
- Documentation: <https://docs.lido.fi>
- Governance forum: <https://research.lido.fi>
- Blog: <https://blog.lido.fi>
- GitHub org: <https://github.com/lidofinance>
- Bug bounty (Immunefi): <https://immunefi.com/bug-bounty/lido/>
- Audits: <https://github.com/lidofinance/audits>

## APIs.json

This repository follows the [APIs.json](https://apisjson.org/) specification. See [`apis.yml`](./apis.yml).
