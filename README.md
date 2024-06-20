# The Steelman Case Against Bitcoin Ossification

There have been many arguments made against changing bitcoin. Michael Saylor has made the argument that any changes made need to be sure to stand the test of time. That's generally a valid feeling, even shared by those who are proponents of changes to bitcoin. However, ultimately, for the legitimate proposals for changes that have passed the BIP review process and are candidates for a soft fork, the fact is, they are anything but an attack on bitcoin.

## Permissionless protocols

One of the more salient points that can be made in opposition to ossification is the fact that what the changes enable are already possible natively on bitcoin with no changes needed, and in fact are being actively worked towards by well-capitalized companies like Citrea, BitLayer, BOB, and Zulu with BitVM, and in addition to Botanix spiderchains and Mercury statechains.

It's inarguable at this point that there is substantial demand for layers that settle to bitcoin.

These "L2" protocols can introduce pretty much any rules they want with no changes needed of bitcoin as it currently is. If the market is proving that these solutions are popular and high in demand, a case could be made for "harm mitigation", in enabling unilateral exit, improving security, and reducing on-chain footprint.

Ultimately, if one sees congestion and obstacles that inhibits people to securely, permissionlessly, and trustlessly transact in and custody whatever value they entrust to bitcoin, then changes should be introduced to improve the situation.

## Some changes can be rolled back

There have been concerns around proposals such as OP_CAT that it opens up a Pandora's box of unforeseen second and third order effects. However, because it's implemented via OP_SUCCESS in TapScript, it can be rolled back in a soft fork. In the case that something truly terrible and unforeseen comes from enabling OP_CAT, anything that was previously valid can then be made invalid through a soft fork.

(This section needs more details)

## Changes that upgrade bitcoin security

Pierre Rochard said recently that while he's skeptical of changes to bitcoin, he's supportive of security improvements. One potential security improvement is the addition of quantum resistant addresses in a "QuBit" soft fork. If done right, it's hard to argue against such a change. It's likely quantum computers will reach the point where they can break bitcoin's signature security within 10 years' time. This drastically undercuts Saylor's timeframe, and even a quantum resistant address type will need to eventually be upgraded once more to an address type secured by specialized quantum security hardware.

This kind of inevitable change means ossification in all cases is undeniably a bad thing for bitcoin, and demonstrates that there are indeed cases where changes are warranted.

## MEV

MEV is a valid concern with its potential for distorting miner incentives in a way that leads to mining pool centralization. However, ultimately, there are good reasons why it won't happen that way on bitcoin. First, accounts-based chains are most vulnerable to MEV through transaction-ordering attacks. Bitcoin, with its UTXOs and PSBT swaps, can enable dexes that are relatively resistant to MEV. L2s even more so.

Additionally, AMMs are capital inefficient, and so they suffer from liquidity availability. Demand is also reduced when superior, cheaper PSBT swaps are available as an option.

(I remember a point Rijndael made about closed-set verifiers, but I can't remember)

## Motivation

The most motivating things in bitcoin are incentives and price signals. So long as fee rates eventually return to "normal" and transactions remain affordable to most, the price signal for change simply isn't there. Bearing in mind that it was not too long ago that unfilled blocks regularly be mined with plenty of room for 3-cent transactions, now transactions are nearer to $3. Should there be a 10x in the price and a 10x in demand, imagine a world where even the simplest of bitcoin transactions costs $300. Is it not worth thinking ahead for potential solutions? Imagine, say, a future where Ark has covenants that make the protocol fully trustless, and it's able to rapidly and inexpensively capitalize trustless Lightning channels with async payments to mobile wallets.

If something is valuable enough, efforts will be made towards addressing its limitations.
