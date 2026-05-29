# Hyperflow

**Enterprise-ready onchain data through one API.**

Hyperflow provides real-time and historical blockchain data through a fast, developer-friendly GraphQL API.

We are building a reliable data layer for teams that need structured blockchain data without maintaining their own full indexing stack.

## What We Build

Hyperflow indexes blockchain data and exposes it through clean APIs.

Our infrastructure is designed to support:

* Real-time blockchain data
* Historical blockchain queries
* Multi-chain indexing
* Blocks, transactions, logs, traces, and decoded events
* High-performance GraphQL access
* Enterprise-grade reliability and monitoring

## Why Hyperflow

Blockchain data infrastructure is usually fragmented.

Teams often need to combine:

* RPC providers
* Archive nodes
* Indexers
* ETL pipelines
* Databases
* Event decoders
* Internal APIs
* Monitoring tools

Hyperflow simplifies this into one data access layer.

Instead of building and maintaining custom indexing infrastructure, teams can query normalized onchain data directly.

## Core Use Cases

Hyperflow is built for teams working on:

* Blockchain analytics
* Security monitoring
* Transaction investigation
* Compliance and audit workflows
* Wallet and address intelligence
* DeFi event indexing
* Swap and liquidity analysis
* Internal dashboards
* AI agents that need reliable onchain context

## Developer Experience

Hyperflow is built for engineers.

We focus on:

* Clean GraphQL schemas
* Fast query performance
* Predictable data models
* Production-ready infrastructure
* Clear separation between raw data and parsed objects
* APIs that can be used by backend services, dashboards, and automation tools

## API

Ethereum GraphQL API:

```text
https://api.hyperflowlabs.com/ethereum/graphql
```

## Technology Direction

Hyperflow’s stack is built around high-volume blockchain ingestion and low-latency querying.

Our technical focus includes:

* EVM chain indexing
* Archive and trace data
* ClickHouse-based analytical storage
* GraphQL APIs
* Parsed event layers
* DeFi swap events
* Data freshness monitoring
* Data integrity checks
* Multi-chain expansion

## Repositories

This GitHub organization contains Hyperflow-related code, infrastructure, tools, and developer resources.

Repository access may vary depending on whether a component is:

* Public open-source
* Internal infrastructure
* Client-facing integration code
* Experimental research
* Production service code

## Engineering Principles

We care about:

* Correctness over shortcuts
* Measurable performance
* Clean APIs
* Strong typing
* Small, maintainable modules
* Clear ownership
* Automated checks
* Production observability
* Security-first development

## Development Policy

For internal repositories, pull requests should follow the organization development policy.

Expected standards:

* Every pull request should reference a tracked task or ticket.
* Pull request descriptions should explain what changed and why.
* Large files should be avoided unless justified.
* Sensitive data must never be committed.
* Production-impacting changes require review.
* CI checks must pass before merge.

## Security

Do not open public issues for security vulnerabilities.

For security-related communication, contact the Hyperflow team through the official website.

## Links

* Website: https://www.hyperflowlabs.com/
* API: https://api.hyperflowlabs.com/ethereum/graphql

---

**Hyperflow — one API for real-time and historical onchain data.**
