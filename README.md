## Dockchains - Request For Comments

### Background

Docker containerisation is quickly becoming the preferred de facto software delivery mechanism and for the first time in the history of mankind Blockchain technology provides a universal undisputed public transaction ledger, not requiring trust in any one individual or organisation.
Problem

If you subscribe to the belief that Things are better and more economically served by general purpose SoCs (System on Chip) rather than custom designed circuitry it is not far-fetched to believe that Dockers will soon break the confines of the data center cloud and spread as fog to the edges. In any case, we will soon be facing some of the following challenges  

- scalability 
  -high bandwidth costs
  -reliance on a single centralized point of failure
  -centralized authority
- data integrity and security
  -authenticity
  -publisher verification, reputation
  -tamper resistance and evidence

### Solution

We propose the establishment of a fully distributed Open Docker Store as a Public Good.

It should be

- owned by nobody
- available to everybody
- self-organizing
- handling open, closed and everything in-between

and provide

- a searchable index pre-built binary docker containers
- produced by deterministic and auditable build process
- anti-fragility by design (battle hardened containers will float to the top)
- metrics (reputation scores, crash analytics)
- a social layer (contextual issues and crowd source help)

Note: All meta data would of course be maintained as magnet links. 


## Implementation Ideas

### Source Code Repository

For obvious reasons github.com is the sole contender here, at least as an aggregating hub. To simplify the design we might even have to trust them ;-) 

There are however alternatives of a true
### Public Ledger

Medium term, the only stable blockchain seems to be Bitcoin why we propose a protocol built on top of Bitcoin for the Public Ledger:

- Counterparty - http://counterparty.io
- Coloured Coins - http://coloredcoins.org
  -ChromaWallet - http://chromawallet.com
  -Coinprism - https://www.coinprism.com
  -Iridis - https://github.com/owlen/iridis

### Private Ledgers

The crypto community is abuzz with competing proposals for side chains and side trees to remedy the inherent scalability issues of Bitcoin. 
Docker containers are simple digital assets like any other so we can take full advantage of the community solutions.

### Protected Ledgers

Smart Contracts are an efficient Panopticon mechanism in that the mere knowledge of the stipulated rules makes participants comply. 

This also means that 


### Wallet

Docker publishers will have to maintain their Docker Assets in a Wallet suitable for the protocol chosen.

A non-exhaustive list (suggestions appreciated):

- Counterwallet - https://counterwallet.io
- ChromaWallet - http://chromawallet.com

### Content Distribution

BitTorrent

### Deterministic Build Process

The Codius Smart Contracts project is already developing Oracle technology based on 

- Google Native Client - https://code.google.com/p/nativeclient/
- Gitian - https://github.com/devrandom/gitian-builder

We share the same need for a highly trusted build process so let’s join forces with them and make sure our Docker Build use case is provided for.
Call to arms

This project is and will always be Open Source and licensed as <link to license> and we invite and welcome you to our <link to github repository> 








