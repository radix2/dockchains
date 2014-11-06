# Dockchains - Request For Comments

>>This is a first dump and draft

## Background

Docker containerisation is quickly becoming the preferred de facto software delivery mechanism and for the first time in the history of mankind emerging Blockchain technologies are progressing towards a universal undisputed public transaction ledger, not requiring trust in any one individual or organisation.

>> Note: The implementation ideas below are highly preliminary, more of a collection of possibly relevant technologies and projects to be inspired by.

## Problem

If you subscribe to the belief that Things are better and more economically served by general purpose SoCs (System on Chip) rather than custom designed circuitry it is not far-fetched to believe that Dockers will soon break the confines of the data center cloud and spread as fog to the edges. In any case, we will soon be facing some of the following challenges:

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

Note: To simplify things (and not require container consumers to have to participate in the financial aspects of cryptocurrency), we limit ourselves to many-to-many distribution of *free* pre-packaged containers. Most importantly this means that we limit the attack surface of the ecosystem (if consumers end up needing to actually hold currency, at least it should be in very limited amounts) and the attackers ROI.

## Implementation Ideas

### Smart Contracts

The way our Docker Store works and operates should be enscribed in public and fully transparent Smart Contracts.  

Note: Smart Contracts are just as efficient as digital [Panopticon](http://en.wikipedia.org/wiki/Panopticon) mechanisms - the mere knowledge of their existance and self-enforcing rules leads to compliance. 

### Ledgers

The crypto community is abuzz with competing proposals for side chains and tree chains ([[1]](#ref1) to remedy the inherent scalability issues of Bitcoin. Docker containers are simple digital assets like any other so we can take full advantage of the community solutions. We distinguish between different types of ledgers by the access rights assigned to them:

### Public Ledger

Medium term, the only stable blockchain seems to be Bitcoin why we propose a protocol built on top of Bitcoin for the Public Ledger:

- Counterparty - http://counterparty.io
- MasterCoin - http://www.mastercoin.org
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
- other

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

## Participate/Contribute

The first thing to slap into shape is this very document. Pull requests are eagerly requested.

### Stay in sync

Fork this repo, clone the fork, and add the original repo as a remote called `upstream`:

```
$ git clone https://github.com/username/dockchains.github.io.git
$ cd dockchains.github.io
$ git remote add upstream https://github.com/dockchains/dockchains.github.io.git
```

Pull from `upstream` frequently to keep your local copy up to date:

```
$ git pull upstream 
```

Now you might need to merge conflicting local changes. If you are IDE less:

```
$ git mergetool
```

### Pull request

Best explained [here](https://help.github.com/articles/using-pull-requests/)

### Dev Process

We will manage the backlog as plain and simple [issues](https://github.com/dockchains/dockchains.github.io/issues) in combination with the [wiki](https://github.com/dockchains/dockchains.github.io/wiki).

## References

<a name="ref1">[1]</a> Peter Todd on TreeChains - [Bitcoin-development mailing list post](http://www.mail-archive.com/bitcoin-development@lists.sourceforge.net/msg04388.html)

<a name="ref2">[2]</a> Codius Smart Contracts by Ripple Labs - [Project page](http://codius.org)

## License

Copyright (c) 2014 [Rebaser AB](http://www.rebaser.com). See the [LICENSE](https://github.com/dockchains/dockchains.github.io/blob/master/LICENSE) file for license rights and
limitations (MIT).
