
# What blockchain is

Computer files don't often stay the same. They're updated with new information, new [metadata](computers-files.md), things are moved around, [glitchy code is patched](computers-software-redesign.md), [updates roll out to handle changes from *other* software](computers-software-redesign.md), [databases](database.md) get cleaned up, and so on.

Naturally, across a [distributed system](computers-distsys.md) (such as cloud synchronization), this can pose extremely complicated challenges. There are a few general ways to sync:

1. Track the date/time it was last modified, then update everything else to the latest and keep date/time-sorted backups of the changes.
2. Create a [cryptographic hash](encryption.md) of the file's contents and track if anything changes, then update everything else to the latest and keep date/time-sorted backups of the changes.

So what happens if there's a discrepancy with no clear difference to make a ruling on which one is authoritative?

- File.txt (version A)
- File.txt (version B)
- Both were edited 10:22:54.565 today, with the same history of edits.

To accommodate this situation, one of the records must be wrong, but we need computer rules to automate which one is. In this case, one of the computers has a higher authority than the other, and the other file is discarded. This is known as a "centralized ledger".

Now, imagine combining the balancing of [peer-to-peer networking](computers-distsys-torrent.md) into this. Instead of 1 central server holding *all* the information, you'd need to add another layer of complexity. This is where "blockchain" comes in.

To keep track of the changes, each [database record](database.md) is divided into manageable chunks of binary information called a "block". The records are strung together by cryptographic hashes on the beginning and end of the blocks:

1. Block 1: BlockInformation - HashA
2. Block 2: HashA - BlockInformation - HashB
3. Block 3: HashB - BlockInformation - HashC
4. etc.

This sequence of blocks is arranged into a [Merkle Tree](data-structures.md) and called the "chain of custody". Each hash is pulled from that block's code, so any changes would be inherently obvious.

Each new block is "mined" as it's created, and every node gets an update of the mined block. Blockchain miners tend to be very powerful computers due to all the necessary calculations.

## Hacking blockchain

However, because of [the way encryption works](encryption.md), a hash could be theoretically reproduced. In the above example, what stops a [hacker](hacking.md) from making a fraudulent Block 2 with the same Hash A and Hash B?

- Block 1: BlockInformation - HashA
- Block 2: HashA - OtherInformation - HashB
- Block 3: HashB - BlockInformation - HashC
- etc.

However, how do we know which one is the *correct* chain of events? When Computer A cross-references from Computer B, who's to say that Computer B is reliable?

This issue is most easily clarified through the [Byzantine Generals Problem](https://en.wikipedia.org/wiki/Byzantine_fault). In short, if two generals are trying to communicate but can't directly communicate with each other, how can you verify that the communications haven't been tampered with?

In this case, since the hash is an elaborate mathematical calculation, if you add more code onto that block (called a "nonce"), the hash will change differently:

- Block 1: BlockInformation+nonce - HashA+
- Block 2: HashA+ - OtherInformation+nonce - NOTHashB
- Block 3: HashB+ - BlockInformation+nonce - HashC+
- etc.

This is called the "proof of work" concept.

Of course, this can *still* get [hacked](hacking.md) if someone's smart enough and determined enough. So, they added another layer of complexity. They'll take *multiple* blocks and slam them together, then create a hash from that with a nonce. In this case, that would mean putting Blocks 1, 2, and 3 together, then putting a nonce on it.

This makes it *very* time-intensive (upwards of years for a hacker's computer to crack).

While this is happening, the computer is also instructed to cross-reference the information with many other computers.

- Computer A checks the chain of custody with Computer B
- Computer A checks the chain of custody with Computer C
- Computer A checks the chain of custody with Computer D
- etc.
- Computer A finds out Computer C is wrong, but all the other ones are correct, so it syncs the correct information and achieves "critical consensus".

The nonces add onto other nonces, over and over, making data transfer mathematically arcane and horrifyingly inefficient. This entire setup is *very* [cybersecure](computers-cysec.md), and creates very little room for hacking or error, but uses tons of electricity and processing power.

One of the most glaringly obvious hacks against a blockchain comes through what's called a "51% attack". It requires rapidly adding enough nodes with the same fraudulent blocks that they represent over 50% of the nodes. At that point, the fully democratic system will conform everything toward the fraudulent block(s).

A 51% attack can be profoundly dangerous, as shown [in this table](https://www.crypto51.app/). The best solution for a 51% attack is to have many, many nodes, and to have new blocks constantly being created. That way, things are moving too fast and too much for a malicious agent to easily act.

## Cryptocurrency

One of the most popular blockchain implementations involves "cryptocurrency" (or simply "crypto"), where the blocks are a tradable commodity/currency. It's a fast-adopting trend for making payments and transferring money across international borders, and countries are slowly forming stock markets for it and accepting it as legal tender.

Bitcoin is by far the most popular, but it's nowhere *near* the only one. There are many of them, with new ones coming around all the time.

### NFTs

By removing the centralized ledger aspect of transfers, you can also remove the need for "trusted intermediaries". You can have a computer establish a "smart contract" with a trustworthy computer.

Each of these blocks can also become "non-fungible tokens" (NFTs), which are simply hashes that represent...something. Ethereum is the most popular NFT, but anyone can make one.

These NFTs can associate to pretty much anything:

- [Intellectual properties](legal-ip.md)
- Legal organizations
- Documentation
- Personal identification
- Social media status updates
- [Graphical assets](engineering-graphics.md) like GIFs or photos

They have no inherent value, but each one is unique compared to any other NFTs in their class, which can give value from that fact alone. It's why people paid money for NFTs of a Lebron James tweet or [CryptoPunks](https://www.larvalabs.com/cryptopunks). It's mostly the same force that drives the the [Tickle Me Elmo craze](https://en.wikipedia.org/wiki/Tickle_Me_Elmo#1996_Elmo_craze) or [tulip mania](https://en.wikipedia.org/wiki/Tulip_mania): the concept of [scarcity](money-economics.md).

### Crypto mining

Blockchain developers get to choose how new NFTs are created, based on existing rules written into the computer code. One of the means of acquiring new blocks for most NFTs is to "mine" them by instructing computers to generate more NFT tokens.

Bitcoin mining uses mathematical problems, and they're mined on a [logarithmic curve](math-algebra-cs.md). That is, they become progressively more work-intensive to mine as the years go by. Only 21,000,000 Bitcoin can ever be "mined".

Crypto mining creates a severe workload on the drive and processor hardware, so many manufacturers have tried to limit crypto mining by making it work inefficiently or voiding the warranty, and [a few have actually used individuals' computers for their own gain without permission](faang.md).

### Implementations

It's worth noting that Bitcoin, specifically, isn't really *one* crypto:

1. Back in 2014, there was a schism on Reddit's [/r/bitcoin](http://reddit.com/r/bitcoin) about how fast the blocks should become bigger.
2. The small-block faction won the argument on BTC (and on Bitcoin.org).
3. By 2017, the large-block faction dominated with a different crypto called BHC on [/r/btc](http://reddit.com/r/btc) (and on Bitcoin.com).

Another popular crypto is Ethereum, which differentiates from Bitcoin because it also has smart contracts. But, again, it's not one crypto:

1. In 2014, [a hacker](hacking.md) stole $50 million dollars of ETC from a startup that used Ethereum.
2. Though the hacker got hacked by seven other hackers, the code implied that it was possible that the hacker was entitled to the ether.
3. There was an attempt to make a soft [fork](computers-software-versionctrl.md) (that would keep it all together), but it didn't work because of a [security vulnerability](computers-cysec.md) with the consensus system, so the Ethereum Foundation had to create a hard fork called ETH.
4. ETC became Ethereum Classic, sustained on [GitHub's ethereumproject](https://github.com/ethereumproject), while the Ethereum Foundation has [Twitter's ethereumproject](https://twitter.com/ethereumproject)..

Sometimes, multiple blockchain protocols can merge together. This can be especially useful to prevent a 51% attack.

### Managing crypto

Some cryptocurrency has had *ridiculously* wild swings (e.g., BTC sometimes can move +100%/-50% month-to-month). To compensate for that, some cryptocurrency is a "stablecoin", where it attaches its value to a relatively stable non-cryptocurrency denomination (such as the US dollar in the case of Tether), often implying that someone is holding the original denomination, [though it can become complicated](https://web.archive.org/web/20211007101222/https://www.bloomberg.com/news/features/2021-10-07/crypto-mystery-where-s-the-69-billion-backing-the-stablecoin-tether).

*Further*, because of the way blockchain works, someone may own 1/500th of Block 549241, 1/1210th of Block 6493 and 1/497th of Block 82421. Other software comes in as a "crypto wallet" to make it easier to manage and transact information. Crypto wallets are a huge reason that crypto is so accessible now, but it blurs the line of the concept of who legitimately owns a blockchain element, since the crypto wallet is also a participant in holding the crypto.

Some blockchain uses a "hybrid ledger", where there's a mix between a trusted intermediary and and distributed ledger. Technically, a crypto wallet is a hybrid ledger because it's subordinate to the "master" ledger.

If, for whatever reason, someone ever loses their [private keys](encryption.md) or they're stolen, they lose access to their blockchain. The decentralized network means there's nobody who can reset your password. In 2018, it was estimated that [about 20% of BTC is gone for good](https://web.archive.org/web/20180713203135/https://www.investopedia.com/news/20-all-btc-lost-unrecoverable-study-shows/).

### Inefficient

Every time there's a new update to the ledger, *every other computer* on the P2P network gets the same data update. This means that cryptocurrency burns through a *lot* of hard drives and processors proportionally to the amount of transactions that happen over the network, especially as the blocks grow longer. Unless there's a pre-programmed "garbage collection" built into the blockchain algorithm, it can become an exponential memory problem.

Also, mining and updating crypto takes a *lot* of electrical power from all the processor use. This is a combination of the compounded proof of work concept and *every* other computer synchronizing all the changes. In the beginning of 2021, [Bitcoin consumed more electricity than the entire country of Argentina](https://web.archive.org/web/20210210142853/https://www.bbc.com/news/technology-56012952).

However, it's hard to *clearly* define a comparison because most other monetary systems are spread across many other systems (e.g., banks, payment processors, US government, etc.). This problem *can* get better with optimization, but it takes [plenty of redesign](computers-software-maintenance.md).

One of the best redesigns is to use "proof of stake" instead of proof of work. Instead of adding never-ending nonces, a computer's block changes are trusted on the network proportionally to the amount of existing blocks it already has.

### The crypto marketplace

Irrespective of the risks and complexities, the decentralized nature of cryptocurrency and NFTs allow for many varieties of [exchange trading](money-investing.md). For the most part, the industry is filled with an anti-authoritarian anarcho-capitalist culture that embraces the concept of a free market without government intervention, and is typically performed on a decentralized exchange (DEX).

What most of the crypto bros don't realize is that people are typically driven more by [use](purpose.md) than by ownership. People are generally happy to have banks hold their money if it's readily available for them later, and only resort to *not* using banks once they [distrust](trust.md) them.

Beyond directly trading, there are many clever ways to maximize returns on the margins with maximal/miner extractable value (MEV). In practice, it simply means buying something at one instant, then selling it at another when the price is a little higher. While the cryptocurrency holder can do it, anyone who successfully programs "bots" can do it as well:

- Gas golfing - optimizing the order of transactions to cut down on transaction fees, named after Ethereum's name for their fees.
- DEX arbitrage - buy a cryptocurrency at a lower price on one exchange, then sell it quickly on another exchange.
- Lending protocol liquidations - when someone takes a loan out with a lending protocol and fails to repay it, the lender can liquidate the borrower's collateral at a profit.
- Front running - scan the queue (mempool) for profitable transactions, then replicate and prioritize them over other transactions in the queue.
- Sandwich trading - find a large pending transaction on a DEX, then place a profitable trade before and after the transaction from the price change.

### Investing scams

Of course, like any new trend, people often buy what they don't understand. In that sense, the unregulated nature of cryptocurrency opens up a world of scams in the form of new blockchain implementations. This is only heightened now that investors, business people, criminals, and law enforcement are as interested as the computer geeks.

In a lot of ways, the promotional angle for many blockchain implementations rings of an [MLM](marketing-mlm.md) pitch: get rich quickly by getting in early, and pay someone else to figure everything out for you. It attracts the types of people willing to gamble while thinking they're making an investment, and adds in [the allure of technology](https://trendless.tech/trends/) to its offering.

One of the largest sources of technically-probably-legal behavior comes through how crypto is brokered. Very often, brokers will hold onto records of crypto transactions, then move them later on, with no mandatory timing to when they need to be processed or reserve to hold onto for 'just in case'. It ends up being like the over-leveraged banks that caused the bank runs that started the Great Depression.

Many crypto designers/traders use the hard-to-pin-down and probably-not-legal system of wash trading, which is a relatively simple method:

1. Make a cryptocurrency across at least a few servers.
2. Perform many, many trades (often with fees) with yourself to make it look like it's a popular cryptocurrency. Use a VPN or something else to obscure what you're actually doing.
3. Advertise to everyone that your cryptocurrency is a hugely popular cryptocurrency.
4. Once you have more users, you'll eventually reach a critical point where you have a popular (and highly profitable) cryptocurrency.

Further, some actors behind the scenes [create short squeezes](https://web.archive.org/web/20220206001711/https://www.singlelunch.com/2022/01/09/an-anatomy-of-bitcoin-price-manipulation/) by generating artificial scarcity or artificial demand increase for crypto. This is hard to prove, but often happens with a BART pattern (a spike, short spurts of of wobbling, and a return to normal).

### Regulations

Regulating cryptocurrency is complicated. [Accountants](money-accounting.md) first determined crypto was best treated as a commodity, but it's a strange one that has complicated legal ramifications. For one, commodities *usually* have a geographic location. In practice, it's more like an [algorithmically](computers-programming-algorithms.md) generated [intellectual property](legal-ip.md) than anything else.

Further, the term DeFi (decentralized finance) may apply to offerings that *rely* on blockchain without actually *being* blockchain. Some of them will tie it directly to the value of another commodity or currency, others will aggregate blockchain values (similar to mutual funds) and provide that as a service.

There are [legal](legal-safety.md) disputes over the concept of "code as law", where computer code is defined as the law itself (as opposed to the *spirit* of what the code was meant to do originally). "Code as law" would allow hackers to legally steal cryptocurrency if they can change the code of the blockchain.

Decentralized systems are a foreign concept because our human nature tends to direct our [power](power.md) into a pyramid, so it'll take quite some time for the chaos to settle about how to regulate crypto. However, crypto is *also* the platform for a *lot* of black market activity, so there's a lot of money and motivation by many people who want to subvert existing laws to keep those laws out of crypto.

Even regulating crypto isn't particularly useful without lawmakers understanding what it is. Very often, many of the black market transfers are crypto-*adjacent*, meaning they're still using money, but it rides alongside crypto to hide the paper trail.

And, since [investing](money-investing.md) is regulated based on [predictions about the future](imagination.md), any whiff of regulatory change will dramatically change the value of a blockchain implementation. The philosophical definition of [what humanity deems as having value](values.md) is critically important to understand.

One inescapable reality about cryptocurrency, however, is that it *does* create a parallel tradable commodity that works enough like money, and people can trade with it if their government's currency becomes unstable. Of course, if a government were to oppress it enough, [fear](mind-feelings-fear.md) would prevent it being anything *but* a black market activity.

The more vocal advocates for crypto often imply that the lack of central control will perfectly replace government, but crypto by itself *can't* do a few things:

- It won't protect citizens from harm *outside* their region (e.g., foreign invaders, foreign immigrants).
- It doesn't protect citizens from harm and crime *inside* their region (e.g., police, firefighting, healthcare).
- It can't provide the optional but preferable effort of building infrastructure that's part of the commons (e.g., road and rail, preserving parks, utilities like water/trash).
- It won't provide incentives for private activities beneficial to society (e.g., farming subsidies, technology grants).
- It can't provide services to the [underclass](classes.md) (e.g., healthcare, foster care, most social services).

### Privacy concerns

The [aspect of privacy](computers-cysec.md) is also a concern with some blockchain implementations. In many respects, scanning and encoding every human eyeball (like with Worldcoin) or every fingerprint creates a tremendous risk to the natural anonymity we are all accustomed to. Thus, some activists like [Edward Snowden](https://web.archive.org/web/20211101005702/https://decrypt.co/84277/snowden-slams-sam-altman-worldcoin-eyeball-scan-for-crypto) are vehemently opposed to this type of implementation.

At the same time, its effectiveness only applies to the degree that it works. Very often, databases can be corrupted, and people can [hack](hacking.md) anything that can make them money (such as, for example, using fake [biometric data](computers-cysec-authentication.md) if there's a cash reward for submitting your personal biological information).

While it's true that cryptocurrency is its own computerized accountant (instead of a bank), this comes at the risk that it's a dumb computer that has *no* intuition to [authenticate](computers-cysec-authentication.md) you versus someone else with a photo of you and your password.

### Hacks/crimes

[Every typical hacking situation](hacking.md) applies with cryptocurrency, but often with less government pushback than money-based transactions. There are often bots that will "frontrun" transactions with minor changes to glean money on the side, and it's an even more brilliant tactic if they can stay undetected during the transfer.

The claims around using cryptocurrency is that it will fix corruption, but it can't. [Human nature](humanity.md) has moral failings that have *nothing* to do with money, since everyone has consented to *money* for thousands of years. Even within the first decade of cryptocurrency, bad actors have arisen.

One of the most ubiquitous forms of using cryptocurrency is to launder money. By putting money into crypto, then bouncing around cryptocurrencies, the paper trail can be very difficult to follow.

Because of absolutely no regulation of cryptocurrency itself (as well as dicey legislation about managing it) it's not uncommon for hackers to steal it.

- [A couple stole 120,000 Bitcoin from the Hong Kong exchange Bitfinex](https://web.archive.org/web/20220208223714/https://www.reuters.com/article/us-bitfinex-hacked-hongkong-idUSKCN10E0KP).

At the same time, hacking crypto or using it for money laundering doesn't necessarily empower anyone to subvert justice:

- [The Feds arrested a couple and seized back the 120,000 Bitcoin Bitfinex hack](https://web.archive.org/web/20220208164644/https://www.washingtonpost.com/national-security/2022/02/08/bitfinex-hack-bitcoin-arrests/).

One painful reality, though, is that almost anything that *could* be done with a blockchain implementation would work just as well without one. The only exception to this is illegal activity, though [not all of it is necessarily criminal](hardship-persecution-church.md).

- [Binance has been the vehicle for $2.35 billion in illegal laundering transactions](https://www.reuters.com/investigates/special-report/fintech-crypto-binance-dirtymoney/).

It's also worth noting that hackers are the force that made blockchain in the first place, and blockchain has other clever uses:

- [This guy heats his home by mining Bitcoin](https://web.archive.org/web/20210223094016/https://blog.haschek.at/2021/how-i-heat-my-home-by-mining.html).
- One of the latest forms of combining cryptocurrency with large organizations is to create decentralized autonomous organizations (DAOs), which attempt to operate entire organizations and societies based on crypto (e.g., [CityCoins](https://www.citycoins.co)).

## Potentially useful

The adoption of cryptocurrency is inevitable, but not precisely how crypto advocates believe it will be. Depending on legislation, it'll likely become an alternate payment option or a highly illegal activity.

The [trend](trends.md) is still early enough that it's difficult to tell for sure. It may have a place as a high-risk [investment vehicle](money-investing.md), but not much else right now.

Unfortunately, as long as Ponzi schemes stay unregulated within crypto, the average person will *not* adopt it, and the longer it persists the more likely people will consider it an inherently sketchy proposal.

At the same time, cryptocurrency can very effectively serve as the de facto currency standard if a government ever collapses into anarchy in a way that preserves its nation's [internet](computers-sofware-webdev.md).
