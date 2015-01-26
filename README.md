# Dockchains - RFC

## Background

Docker containerisation is quickly becoming the preferred de facto software delivery mechanism and for the first time in the history of mankind emerging Blockchain technologies are progressing towards acceptance as universally undisputed public transaction ledgers, not requiring trust in any one individual or organisation (but to some extent in the improbablity of collusion).

>> Note: The implementation ideas below are highly preliminary, more of a collection of possibly relevant technologies and projects to be inspired by.

While the problems and solutions outlined below are universal we believe that the right place to start is amongst the alpha geeks in the developer community. The design patterns emerging here will serve as a foundation aka platform for a redesign of the internet.

## Problem

If you subscribe to the belief that "Things" will be built using general purpose programmable SoCs (System on Chip) rather than custom designed processors or sensors they will easily be powerful enough to run lightweight versions of Linux and by extension Docker containers. 

The Internet of Everything will soon be facing some of the following challenges:

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
* handling open source, closed and everything in-between

and provide

- a searchable index of pre-built binary docker containers
- an auditable and deterministic build process
- anti-fragility by design (battle hardened containers will float to the top)
- a publisher identity system
- metrics (reputation scores, crash analytics)
- a social layer (contextual issues and crowd source help)

Note: All meta data would of course also be maintained according to Named Data Networking principles.

## Implementation Ideas

### Distributed Autonomous Corporation

Note: Not only decentralized but *distributed*, the distinction will be explained below.

Stan Larimer of Invictus Corporation is one of the foremost proponents of the revival of Nick Szabos ideas and captures their defining qualities as

- They are corporations – they are free and independent persons (but don’t have legal personality).
- They are autonomous – once up to speed, they no longer need (or heed) their creators.
- They are distributed – there are no central points of control or failure that can be attacked.
- They are transparent – their books and business rules are auditable by all.
- They are confidential – customer information is securely (and incorruptibly) protected.
- They are trustworthy – because no interaction with them depends on trust.
- They are fiduciaries – acting solely in their customers’ and shareholders’ interests.
- They are self-regulating – they robotically obey their own rules.
- They are incorruptible – no one can exercise seductive or coercive influence over them.
- They are sovereign – over their digital resources (but don't have legal capacity).[5]

### Identity

Before entering into smart contracts as peers we need to establish an identity system on which to base them. Identity is just metadata and does not apply only to people but organizations and any data. Several interesting initiatives based on crypto and different degrees of decentralization have been proposed:  

- [onename.com](http://onename.com) 
- [namecoin](http://namecoin.info)
- Chris Ellis - The World Citizenship project [5](#ref5)

Identity is not only a valuable scarce object but "uniquely unique", and it's value therefor asymptotically infinite. Yet, until now there has been no viable identity protocol layer for the Internet. Due to the challenges involved in maintaining a Public Key Infrastructure (the challenge lies in enabling the general public (pun unintended) to hold and protect their private keys in a secure and scalable way). Instead we have had to exchange our most valuable asset, that which defines us, for communication services. It is not only easier to centralize identity managment, it's also a simple and lucrative business model. Not only is this a bad idea in the first place but in the name of convenience we have had to sacrifice security (relying mostly upon simple username/password credentials).

### Smart Contracts 

Read more - [3](#ref3)
As noted above, the rules for how our Docker Store works and operates should be enscribed in a Smart Contract.  

Note: Smart Contracts are just as efficient as digital [Panopticon](http://en.wikipedia.org/wiki/Panopticon) mechanisms - the mere knowledge of their existance and self-enforcing rules leads to compliance. 

### Ledgers

The crypto community is abuzz with competing proposals for side chains and tree chains ([[1]](#ref1) to remedy the inherent scalability issues of Bitcoin. Docker containers are simple digital assets like any other so we can take full advantage of the community solutions. We distinguish between different types of ledgers by the access rights assigned to them:

### Public Ledger

There is an abundance of competing blockchain designs

- Counterparty - http://counterparty.io
- MasterCoin - http://www.mastercoin.org
- Coloured Coins - http://coloredcoins.org
  - ChromaWallet - http://chromawallet.com
  - Coinprism - https://www.coinprism.com
  - Iridis - https://github.com/owlen/iridis

### Private Ledgers

A certain organization, cloud provider would for obvious reasons prefer to keep their metadata private. What is important is that the protocols are the same and open.

### Protected (Shared) Ledgers

Once an anomaly of some sort has been detected, previously private ledgers can be selectively made available (by a contract or a multisig escrow mechanism) to a closed group of arbibtrators, insurers or even made public. 

### Wallet

Docker publishers will have to maintain their Docker Assets in a Wallet suitable for the protocol chosen.

A non-exhaustive list (suggestions appreciated):

- Counterwallet - https://counterwallet.io
- ChromaWallet - http://chromawallet.com
- other

### Content Distribution

BitTorrent and maybe even the proprietary but free BitTorrent Sync product would be as natural a choice for binary images as is git for source.

### Source Code Repository

For obvious reasons github.com (or one of it's clones) is the sole contender here, at least as an aggregating hub. To simplify the design we might even have to trust them ;-) 

The unfortunately abandoned project https://github.com/gitchain/gitchain shares many of the same design goals as Project Dockchains. We should study and learn from the experiences made there.

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
$ git clone https://github.com/radix2/dockchains.git
$ cd dockchains
$ git remote add upstream https://github.com/radix2/dockchains.git
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

<a name="ref1">[1]</a> TreeChains, Peter Todd  - [Bitcoin-development mailing list post](http://www.mail-archive.com/bitcoin-development@lists.sourceforge.net/msg04388.html)

<a name="ref2">[2]</a> Codius Smart Contracts, Ripple Labs - [Project page](http://codius.org)

<a name="ref3">[3]</a> The Idea of Smart Contracts, Nick Szabo - [Blog post](http://szabo.best.vwh.net/smart_contracts_idea.html)

<a name="ref4">[4]</a> DAOs, DACs, DAs and More: An Incomplete Terminology Guide, Vitalik Buterin, Ethereum.org [Blog post](https://blog.ethereum.org/2014/05/06/daos-dacs-das-and-more-an-incomplete-terminology-guide/)

<a name="ref5">[5]</a> World Citizenship, Chris Ellis - [Github repo](https://github.com/MrChrisJ/World-Citizenship)

## License

Copyright (c) 2014 [Rebaser AB](http://www.rebaser.com). See the [LICENSE](https://github.com/dockchains/dockchains.github.io/blob/master/LICENSE) file for license rights and
limitations (MIT).
