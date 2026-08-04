# Lido

<!-- API-EVANGELIST-PROVENANCE:BEGIN -->
> ### About this repository
>
> **This is not our API.** This repository is an independent, third-party profile of a company's
> **publicly available** API surface, maintained by [API Evangelist](https://apievangelist.com).
> API Evangelist does not operate, host, resell, or support this company's APIs, and is not
> affiliated with or endorsed by the company unless stated on the profile.
>
> **Where the information came from.** Everything here is assembled from material a member of the
> public can reach with a browser and no credentials — the company's own website, developer portal
> and documentation, the specifications it publishes for public use (OpenAPI, AsyncAPI, JSON Schema,
> `apis.json`, `llms.txt` and similar), its public repositories, and its public status, pricing and
> changelog pages. **Nothing here is obtained by breaching a system, defeating an access control, or
> using credentials of any kind.**
>
> **The rating is an independent assessment.** The Kin Score and Agent Readiness rating are
> independently calculated scores of a company's *public* API artifacts, produced by API Evangelist
> against a published rubric. They are not certifications, endorsements, security assessments, or
> audits, and they score published artifacts — not the quality, safety, or security of the software.
>
> **Corrections, re-scores, and removal are free.** No partnership, contract, or purchase is
> required, and you do not need to justify the request.
>
> - **Something wrong?** Open an issue on this repository, or email
>   [info@apievangelist.com](mailto:info@apievangelist.com).
> - **Published something new?** Ask for a re-score and we will re-run the rating.
> - **Want the listing taken down?** Say so and we will honor it. The profile is reduced to your
>   company name, a factual description, and a link to your own site, and the company is recorded as
>   **unrated** — never scored zero for having asked.
>
> **Response times.** Acknowledgement within **one business day**; removal or restriction within
> **two business days**; corrections and re-scores within **five business days**.
>
> **On a security or compliance team?** Email
> [info@apievangelist.com](mailto:info@apievangelist.com) with *security* in the subject line and
> you will get a person, not a form. We will tell you exactly which public URLs this profile was
> built from so your team can see the same surface we did, and we will take the listing down on
> request while you work through it.
>
> Full detail: **[Where this data comes from](https://apievangelist.com/about/where-our-data-comes-from)**
<!-- API-EVANGELIST-PROVENANCE:END -->

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
