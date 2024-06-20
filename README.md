# The Steelman Case Against Bitcoin Ossification

There have been many arguments made against changing bitcoin. Michael Saylor has made the argument that any changes made need to be sure to stand the test of time. That's generally a valid feeling, even shared by those who are proponents of changes to bitcoin. However, ultimately, for the legitimate proposals for changes that have passed the BIP review process and are candidates for a soft fork, the fact is, they are anything but an attack on bitcoin.

## When to ossify

While there is certainly appeal to the idea of bitcoin being good enough as it is, how can we be the judge that the protocol as it is today is correct any more than we can be the judge of a change to the protocol? The best we can do is propose the best changes and seek consensus on implementing them. Ossification is itself choosing to change bitcoin by stopping a change process that was put in place partially by Satoshi and partially by his successors.

## Permissionless protocols

One of the more salient points that can be made in opposition to ossification is the fact that what the changes enable are already possible natively on bitcoin with no changes needed, and in fact are being actively worked towards by well-capitalized companies like Citrea, BitLayer, BOB, and Zulu with BitVM, and in addition to Botanix spiderchains and Mercury statechains.

It's inarguable at this point that there is substantial demand for layers that settle to bitcoin.

These "L2" protocols can introduce pretty much any rules they want with no changes needed of bitcoin as it currently is. If the market is proving that these solutions are popular and high in demand, a case could be made for "harm mitigation", in enabling unilateral exit, improving security, and reducing on-chain footprint.

This is not a question of what use cases we enable - it's a question of how risky those use cases are for bitcoin users and by extension to bitcoin itself.

Ultimately, if one sees congestion and obstacles that inhibits people to securely, permissionlessly, and trustlessly transact in and custody whatever value they entrust to bitcoin, then changes should be introduced to improve the situation.

## Some changes can be rolled back

There have been concerns around proposals such as OP_CAT that it opens up a Pandora's box of unforeseen second and third order effects. However, such opcodes can be removed in the same way as CVE-2010-5137 if they cause a critical issue via an additional soft fork. In the case that something truly terrible and unforeseen comes from enabling OP_CAT, anything that was previously valid can then be made invalid through a soft fork.

This would be a confiscatory soft fork against those already using the opcode, but this could potentially be mitigated by restricting its use through a smaller reduction in valid transactions (e.g. adding a restriction on the number of CATs in a script) rather than a complete disabling of the opcode.

## Changes that upgrade bitcoin security

Pierre Rochard said recently that while he's skeptical of changes to bitcoin, he's supportive of security improvements. One potential security improvement is the addition of quantum resistant addresses in a "QuBit" soft fork. If done right, it's hard to argue against such a change. It's likely quantum computers will reach the point where they can break bitcoin's signature security within 10 years' time. This drastically undercuts Saylor's timeframe, and even a quantum resistant address type will need to eventually be upgraded once more to an address type secured by specialized quantum security hardware.

This kind of inevitable change means ossification in all cases is undeniably a bad thing for bitcoin, and demonstrates that there are indeed cases where changes are warranted.

## Centralizing MEV (MEVil)

MEV is an important concern with its potential for distorting miner incentives in a way that leads to mining pool centralization. However, there are good reasons why it won't happen that way on bitcoin. First, accounts-based chains are most vulnerable to MEV through transaction-ordering attacks. Bitcoin, with its UTXOs and PSBT swaps, can enable dexes that are relatively resistant to MEV. L2s even more so.

It is nearly certain that AMMs are impossible on bitcoin without a fork explicitly intended to enable them (i.e. adding first class token supporting opcodes). Even if bitcoin were to add a SNARK verification opcode, each token balance check would require a separate proof circuit and data of at least hundreds of bytes and more likely kilobytes. Without a SNARK verifier, checking any token balance would require full transaction history for the token balance, including SPV proofs, and some fraud proof mechanism. Because any fork (aside from first class tokens) which enables reduced token balance proof size would also enable layered token trading, no material token trading would occur on base layer. Why pay for hundreds of bytes of token proof for each trade when you can potentially do a PSBT swap for less than 100 bytes of signature data and lift your token in to a layer where you can trade for very low fees?

Additionally, AMMs are capital inefficient, and so they suffer from liquidity availability. Demand is also reduced when superior, cheaper PSBT swaps are available as an option.

The other potential type of centralizing MEV would come from sidechain MEV leakage. If sidechains or other layers can have an open sequencer set (i.e. miners are free to join) then miners are likely to find themselves in an advantageous position with regard to selecting or sequencing second layer transactions relative to either base layer activity or off chain exchange activity. In this scenario, the existence of a sidechain that is pegged to bitcoin (i.e. where miners can be confident in their ability to realize profits in real money on bitcoin) they will naturally be incentivized to build significant infrastructure in order to maximize their ability to harvest additional bitcoin profits thanks to their superior ability to exit into bitcoin and control the contents of sidechain blocks. However, layers subject to this type of MEV will be inferior to closed sequencer set second layers with unilateral exit for participants. In a closed sequencer second layer, transactions can be faster and more reliable than in an open sequencer second layer. Moreover, the incentive to develop complex second layer software and services is much greater when a closed set of sequencers can harvest the second layer transaction fees. Finally, a closed sequencer second layer with unilateral exit offers a superior trust model to an open sequencer second layer with trust minimized exit that depends on the bitcoin mining process for trust minimization (e.g. hashrate escrow).

## Motivation

The most motivating things in bitcoin are incentives and price signals. So long as fee rates eventually return to "normal" and transactions remain affordable to most, the price signal for change simply isn't there. Bearing in mind that it was not too long ago that unfilled blocks regularly be mined with plenty of room for 3-cent transactions, now transactions are nearer to $3. Should there be a 10x in the price and a 10x in demand, imagine a world where even the simplest of bitcoin transactions costs $300. Is it not worth thinking ahead for potential solutions? Imagine, say, a future where Ark has covenants that make the protocol fully trustless, and it's able to rapidly and inexpensively capitalize trustless Lightning channels with async payments to mobile wallets.

If something is valuable enough, efforts will be made towards addressing its limitations.
