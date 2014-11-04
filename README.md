# Dockchains - Request For Comments

>>This is a first dump and draft

## Background

Docker containerisation is quickly becoming the preferred de facto software delivery mechanism and for the first time in the history of mankind Blockchain technology provides a universal undisputed public transaction ledger, not requiring trust in any one individual or organisation.
Problem

If you subscribe to the belief that Things are better and more economically served by general purpose SoCs (System on Chip) rather than custom designed circuitry it is not far-fetched to believe that Dockers will soon break the confines of the data center cloud and spread as fog to the edges. In any case, we will soon be facing some of the following challenges  

- scalability
  - high bandwidth costs
  - reliance on a single centralized point of failure
  - centralized authority
- data integrity and security
  - authenticity
  - publisher verification, reputation
  - tamper resistance and evidence

## Solution

We propose the establishment of a fully distributed Open Docker Store as a Public Good.

It should be

* owned by nobody
* available to everybody
* self-organizing
* handling open, closed and everything in-between

and provide

- a searchable index pre-built binary docker containers
- produced by deterministic and auditable build process
- anti-fragility by design (battle hardened containers will float to the top)
- metrics (reputation scores, crash analytics)
- a social layer (contextual issues and crowd source help)

Note: All meta data would of course be maintained as magnet links. 

## Implementation Ideas

### Smart Contracts

The way our Docker Store works and operates should be enscribed in public and fully transparent Smart Contracts.  

Note: Smart Contracts are just as efficient as digital [Panopticon](http://en.wikipedia.org/wiki/Panopticon) mechanisms - the mere knowledge of their existance and self-enforcing rules leads to compliance. 

### Ledgers

The crypto community is abuzz with competing proposals for side chains and side trees to remedy the inherent scalability issues of Bitcoin. Docker containers are simple digital assets like any other so we can take full advantage of the community solutions. We distinguish between different types of ledgers by the access rights assigned to them:

### Public Ledger

Medium term, the only stable blockchain seems to be Bitcoin why we propose a protocol built on top of Bitcoin for the Public Ledger:

- Counterparty - http://counterparty.io
- Coloured Coins - http://coloredcoins.org
  -ChromaWallet - http://chromawallet.com
  -Coinprism - https://www.coinprism.com
  -Iridis - https://github.com/owlen/iridis

### Private Ledgers

A certain organization, cloud provider would for obvious reasons prefer to keep their metadata private. What is important is that protocols are the same and open.

### Protected (Shared) Ledgers

Once an anomaly of some sort has been detected, previously private ledgers can be selectively made available (by a contract or a multisig escrow mechanism) to a closed group of aribtrators, insurers or even made public. 


### Wallet

Docker publishers will have to maintain their Docker Assets in a Wallet suitable for the protocol chosen.

A non-exhaustive list (suggestions appreciated):

- Counterwallet - https://counterwallet.io
- ChromaWallet - http://chromawallet.com

### Content Distribution

BitTorrent is as natural a choice for binary images as is git for source.

### Source Code Repository

For obvious reasons github.com is the sole contender here, at least as an aggregating hub. To simplify the design we might even have to trust them ;-) 

The unfortunately abandoned project https://github.com/gitchain/gitchain shares many of the same design goals. We should study and learn from the experiences made there and hopefully get the developer to join forces with us.

### Deterministic Build Process

The Codius Smart Contracts project is already developing Oracle technology based on 

- Google Native Client - https://code.google.com/p/nativeclient/
- Gitian - https://github.com/devrandom/gitian-builder

We share the same need for a highly trusted build process so let’s join forces with them and make sure our Docker Build use case is provided for.

## Participate

We will manage the backlog as [issues](https://github.com/dockchains/dockchains.github.io/issues), so chime in and let's build this thing!

## License

Copyright (c) 2014 [Rebaser AB](http://www.rebaser.com). See the [LICENSE](LICENSE.md) file for license rights and
limitations (MIT).







