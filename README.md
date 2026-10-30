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
> **Not from the company, and here with a question?** You are welcome here — we would rather be the
> front line and point you the right way than have a good report go nowhere. What this repository
> can answer is narrow, though, so it is worth knowing who you are actually looking for:
>
> - **A question about how the API works, an account, billing, or a bug in the service** — that is
>   the company's own support, not us. We profile this API; we do not operate it and cannot see
>   your account.
> - **A bug in an open-source project we only catalog** — file it on that project's own repository.
>   This has happened with a real and correct bug report that reached us instead of the people who
>   could fix it, which helped nobody.
> - **Anything about this listing itself** — the description, the tags, the rating, a missing or
>   wrong artifact — is ours. Open an issue here.
> - **Not sure, or something general about API Evangelist or APIs.io** — open an issue on the
>   [APIs.io Inbox](https://github.com/api-search/inbox) and we will route it.
>
> **This repository contains no software, and we will never ask you to download anything.** There is
> no build, release, installer, or binary here — only text and machine-readable API descriptions, so
> there is nothing here that can be "corrupt" or need "repairing". Any issue, comment, or email
> claiming otherwise and offering a download link is not from us and is hostile. Do not follow the
> link; it is a lure. Report it to GitHub and, if you like, tell us at
> [info@apievangelist.com](mailto:info@apievangelist.com) so we can take it down.
>
> **On a security or compliance team?** Email
> [info@apievangelist.com](mailto:info@apievangelist.com) with *security* in the subject line and
> you will get a person, not a form. We will tell you exactly which public URLs this profile was
> built from so your team can see the same surface we did, and we will take the listing down on
> request while you work through it.
>
> Full detail: **[Where this data comes from](https://apievangelist.com/about/where-our-data-comes-from)**
<!-- API-EVANGELIST-PROVENANCE:END -->

Lido is the leading liquid staking protocol on Ethereum, allowing anyone to stake ETH without locking it or running validator infrastructure. Stakers deposit ETH and receive stETH — a rebasing ERC-20 that earns daily staking rewards — or its non-rebasing wrapped form wstETH used widely across DeFi. Lido is governed by the Lido DAO via the LDO token, Snapshot signaling, on-chain Aragon voting, and a Dual Governance timelock that gives stETH holders a dynamic veto over the DAO. The protocol's validator set is delegated across multiple Staking Modules — the Curated Module (professional node operators), Simple DVT (distributed validator technology via Obol and SSV), the Community Staking Module (permissionless solo stakers backed by bonded stETH), and stVaults (modular tailored setups). At over $18B TVL and 8.8M+ ETH staked, Lido is the #1 liquid staking provider by total value locked. Lido previously operated on Polygon (stMATIC, sunset June 2025) and Solana (stSOL, sunset February 2024); the protocol is now Ethereum-only. Lido publishes the open-source core smart contracts, a TypeScript SDK (`@lidofinance/lido-ethereum-sdk`), a Python oracle daemon, validator monitoring tooling, frontend widgets, and three public read-only HTTP APIs for protocol APR, reward history, and withdrawal queue timing.

**Areas:** Liquid Staking · Ethereum · Staking · DeFi · stETH · wstETH · Validator · Node Operators · DAO · Governance · LDO · Oracle

## Lido on APIs.io

Everything profiled for Lido is published on APIs.io rather than in this repository. Start at the provider page — **[apis.io/providers/lido/](https://apis.io/providers/lido/)** — or go straight to one of the APIs or properties below.

### APIs (12)

- [Lido APR API](https://apis.io/apis/lido/lido-apr-api/) — Read-only HTTP API returning the latest stETH staking APR and a 7-day simple moving average APR. Used by integrators, dashboards, and DeFi protocols to…
- [Lido Reward History API](https://apis.io/apis/lido/lido-reward-history-api/) — Read-only HTTP API returning a per-address stETH reward history including USD/EUR/GBP fiat conversions, with options to filter to rewards-only, sort,…
- [Lido Withdrawals API](https://apis.io/apis/lido/lido-withdrawals-api/) — Read-only HTTP API for the Lido stETH withdrawal queue. Returns estimated finalization times for one or more withdrawal request IDs, and can forecast the…
- [Lido Keys API](https://apis.io/apis/lido/lido-keys-api/) — Service that exposes node operator validator keys from each Lido staking module (Curated, Simple DVT, CSM) for use by deposit security infrastructure,…
- [Lido Subgraph (GraphQL)](https://apis.io/apis/lido/lido-subgraph/) — GraphQL subgraph deployed to The Graph Decentralized Network that indexes Lido smart-contract events — rewards distribution, oracle reports, stETH transfers…
- [Lido APR for Eth and stEth API](https://apis.io/apis/lido/lido-apr-for-eth-and-steth-api/) — The APR for Eth and stEth API from Lido — 8 operation(s) for apr for eth and steth.
- [Lido Estimate API](https://apis.io/apis/lido/lido-estimate-api/) — The Estimate API from Lido — 1 operation(s) for estimate.
- [Lido NFT API](https://apis.io/apis/lido/lido-nft-api/) — The NFT API from Lido — 2 operation(s) for nft.
- [Lido Request Time API](https://apis.io/apis/lido/lido-request-time-api/) — The Request Time API from Lido — 3 operation(s) for request time.
- [Lido Rewards API](https://apis.io/apis/lido/lido-rewards-api/) — The Rewards API from Lido — 1 operation(s) for rewards.
- [Lido Swap rate for stETH and wstETH API](https://apis.io/apis/lido/lido-swap-rate-for-steth-and-wsteth-api/) — The Swap rate for stETH and wstETH API from Lido — 2 operation(s) for swap rate for steth and wsteth.
- [Lido Validators API](https://apis.io/apis/lido/lido-validators-api/) — The Validators API from Lido — 1 operation(s) for validators.

### Published properties

Each property below is a page on APIs.io carrying the machine-readable artifact and what it says.

#### GraphQL (1)

GraphQL schemas.

- [Lido Finance GraphQL API](https://apis.io/graphqls/lido/lido-graphql/)

#### Security (2)

Authentication, trust centre, and vulnerability disclosure.

- [Lido Domain Security](https://apis.io/security/lido/lido-domain-security/)
- [Lido Vulnerability Disclosure](https://apis.io/security/lido/lido-vulnerability-disclosure/)

## Where to find this API

Links to the company's own pages. This repository publishes no copy of their specifications — the canonical document is theirs and lives at the URLs below.

- [Website](https://lido.fi)
- [Documentation](https://docs.lido.fi)
- [Blog](https://blog.lido.fi)
- [GitHub](https://github.com/lidofinance)

## API Evangelist rating

**Kin Score 27.8** — thin · rubric 0.24.0 · scored 2026-10-17

| Facet | Score |
|---|---|
| Discoverability | 62.5 |
| Contract quality | 39.9 |
| Contract governance | 0.0 |
| Operational transparency | 18.4 |
| Developer ergonomics | 50.0 |
| Access clarity | 0.0 |

**Agent readiness 21.7** — agent-aware

| Agent-readiness dimension | Result |
|---|---|
| Spec Presence | yes |
| Agentic Access | — |
| Reversibility Documented | na |
| MCP Server | — |
| Auth Clarity | — |
| Idempotency | na |
| Error Semantics | verified |
| OpenAPI Examples | — |
| Rate Limit Signal | — |
| Event Surface Described | — |
| Agent Skills | — |
| Well Known Catalog | — |
| Consent Identity | — |
| Agent Card | — |
| Dry Run Mode | na |
| Delegated Identity | — |
| Protected Resource Metadata | — |
| Dynamic Client Registration | — |
| Agentic Commerce | — |

**Regulatory alignment 11.8** — Horizontal (data, software, accessibility, platform)

The rubric is published at [github.com/api-evangelist/kin-score](https://github.com/api-evangelist/kin-score). The per-check breakdown behind these numbers — which checks were earned, partial or missed — along with score history and how this provider compares to its peers, is available at [apis.io/providers/lido/](https://apis.io/providers/lido/).

## How this profile is made

API Evangelist profiles a company's public API surface the way a developer would find it: the website, developer portal and documentation, the specifications it publishes, its public repositories, and its pricing, status and changelog pages. From that it derives the properties above — contracts split per API, workflows, schemas, collections, governance rules, plans and rate limits — and scores them against the published [Kin Score rubric](https://github.com/api-evangelist/kin-score).

The artifacts are published on [APIs.io](https://apis.io), not in this repository. This repository is the public record for Lido: the place to say something is wrong, missing or out of date, and to ask for a re-score or a removal.

## Open an issue

- **Something about this listing** — a wrong description, a missing API, a stale artifact or a question about the rating: [open an issue on this repository](https://github.com/api-evangelist/lido/issues/new).
- **A new API, or one that is not in the catalog yet** — [submit it on APIs.io](https://apis.io/add/).
- **Anything else** — [the APIs.io inbox](https://github.com/api-search/inbox/issues/new) or [info@apievangelist.com](mailto:info@apievangelist.com).
