
## Peak pod - Matt Levine

The most basic [move](https://www.bloomberg.com/opinion/articles/2021-10-07/matt-levine-s-money-stuff-looking-for-tether-s-money) in [finance](https://www.bloomberg.com/opinion/articles/2022-11-28/ftx-s-blockfi-rescue-didn-t-work) is the [slicing](https://www.bloomberg.com/opinion/articles/2023-01-18/slicing-cash-flows-for-better-ratings) of cash flows. You have a thing with some uncertain payoff: It will surely be worth at least $X, but it could be worth as much as $Y. You put the thing in a box and sell claims on the box to different people who want different things. You sell $X worth of senior claims to people who want safety, promising to pay them back first: The box will surely be worth at least $X, so their claims are very safe. And then you sell some junior claims to other people who want risk: The box could be worth as much as $Y, in which case you'd pay off the $X of senior claims and have money left over for the junior claims. Those claims are risky (they could go to zero), but also more lucrative (they could be worth a lot); they promise a higher expected return in exchange for taking more risk. And of course you could slice more finely: Issue one set of super-safe senior claims, another set of pretty safe mezzanine claims, a set of risky junior claims, etc. And an important way to come up with new financial businesses is to notice some financial thing with some fluctuating value and decompose it into a safe part and a risky part. 

One way to think about multi-manager, multi-strategy [hedge funds](https://www.bloomberg.com/opinion/articles/2023-11-08/the-coffee-futures-got-stale) (or "pod shops") is that they are a way to turn _investing skill_ into this sort of tractable, tranche-able financial asset. The rough theory is:

1. Some people can, with hard work and native skill, identify which stocks (bonds, commodities, etc.) are better and which are worse, within some narrow sector, with some reasonably high success rate. Not through any sort of magic market intuition but through deep study and specialization: If you spend your life studying the biotech industry, you might have somewhat better-than-chance odds of picking which biotech stocks will outperform and which will underperform.
2. If they just went out and bought the five stocks they thought were the best, they'd have a good chance of making a lot of money, but there'd be risks too. Perhaps there would be a general stock market crash, or a collapse in the biotech industry; they might have accurately picked the best stocks but those stocks would still go down.
3. But you can hire them and isolate their skill: Make them buy the best stocks in their sector, short the worst stocks in their sector, and keep a neutral exposure to the stock market, the sector and other factors, so that they only make (or lose) money if their favorite stocks outperform (or underperform) their least-favorite stocks due to their pure stock-picking skill. 
4. And you can also hire other specialists in other sectors, and other asset classes, and make all of them hedge, so that you have a diversified portfolio that has no exposure to the broad stock market, to individual sectors, to factors, etc., but is exposed only to their collective investing skill.
5. And you fire the ones who mess up, so the overall skill level remains high.
6. And then you decompose what they are doing into (1) a very large, very boring, very safe portfolio and (2) a smaller and more volatile stream of payoffs for their investing skill.

If you do this right, you can have them build a very large portfolio with not very much risk. They can bet on a lot of things, and bet against a lot of other things, and those things are highly correlated with each other. Like, they make $1 billion of bets that blue widgets will go up, and they make $1 billion of bets that green widgets will go down, and historically blue and green widget prices have moved in lockstep. That's a total of $2 billion of bets, but they cancel each other out. If blue widgets go down 20% (and they lose $200 million on their long bet), then probably green widgets will also go down 20% (and they make $200 million on their short bet), so there's still $2 billion. But the idea is that they know something the market doesn't, and actually blue widgets will go up by 5 percentage points more (or down by 5 percentage points less) than green widgets, and so they'll make $50 million on this bet. Of course they could be wrong; maybe blue widgets will _underperform_ green ones and the bet will lose money. Not the whole $2 billion amount of the bet - blue and green widgets are pretty fungible - but, you know, maybe $50 million.

And you can kind of abstractly do some math like "this bet requires $2 billion, and we hope it will pay back like $2.05 billion, but even if we're wrong it should pay back $2 billion, or $1.95 billion at absolute worst." And then you can go out and sell, say, $1.9 billion of senior claims on this bet, saying "we'll pay you back the $1.9 billion no matter what." And then you raise, say, $100 million of junior claims on this bet, saying "we hope to pay you back $150 million on your $100 million investment, but if we're wrong you eat the losses."

Traditionally the people buying the senior claims are prime brokerage desks at big investment banks, and they can check all of this: They can look at the actual trades that you're doing and say "ah yes, historically, blue and green widget prices have been highly correlated, so the chances of losing much of this $2 billion is slim, and the chances of eating into our $1.9 billion are close to zero." And they can check  your track record, too, and say "yeah these guys usually make money and always pay back their senior claims so it's fine." Also they hold your collateral - the blue widgets you're long, the green widgets you're short - and if the trade does start to collapse they can probably shut it down before you lose too much money (and, thus, before _they_ lose any money). 

And then traditionally the people buying the junior claims are your hedge fund investors, who are betting that you really do have all this investing skill, that you really can turn their $100 million into $150 million much more often than you turn it into $50 million. And then traditionally you yourself, and your employees, have some sort of super-junior claim, where you get paid a big chunk of the upside if the bets pay off.

Now, another important move in finance is to worry about this slicing of cash flows. The traditional worries are:

1. The safe senior claims: Are they really that safe? Do we really _know_ that this trade can't lose a lot of money and cut into the $1.9 billion senior claim? What if blue widgets fall 10% and green widgets go up 10%? Then this strategy loses $200 million, the junior claims are wiped out and the lenders lose money.
2. The risky junior claims: Boy, they sure look risky! In the example above, the total portfolio lost 10% of its value, but the junior claims lost 100% of their value. Seems risky.
3. The interplay between them: If you have a $2 billion portfolio and it loses 10% of its value for some temporary reason, you might just hold onto it until the prices recover. But if you have a $2 billion portfolio with 95% leverage and it loses 10% of its value, your lender - a bank prime brokerage - will seize the collateral and sell it as quickly as possible, which means (1) you permanently lose all of your equity and also (2) your lender's sale might further drive down prices and cause more problems.

Here's a [Bloomberg News story about "peak pod"](https://www.bloomberg.com/news/articles/2023-11-30/ken-griffin-s-citadel-hedge-fund-rivals-draw-scrutiny-over-crowding-leverage):

> Multimanager funds like [Ken] Griffin's Citadel have come to dominate the hedge fund industry, riding a steady run of outperformance to oversee more than $1 trillion, including a healthy dose of leverage. But the explosive growth has led the industry giants to pile into many of the same trades.
>
> That has built unease among regulators, investors and traders over these so-called pod shops. …
>
> Overcrowding in some bets, increased market volatility, an expensive talent war and lower returns this year have prompted market participants to question whether the world of high finance is approaching peak pod. ...
>
> "There's some overcrowding and concern about the amount of leverage at individual firms and collectively," John Jackson, head of hedge fund research at investment consultant Mercer, said during a recent Capital Allocators podcast. And because they typically cut risk very quickly "we are worried about the potential snowball effect." …
>
> Clients are now fixated on leverage and the risk of "platform de-grossing" - or stampede selling - Goldman Sachs said in an earlier report. …
>
> Much of the increased regulatory focus has been in Treasury markets, where leverage tends to be the highest. Hedge funds in aggregate had estimated leverage of 56-to-1 on $553 billion of Treasury repo borrowing as of December 2022, according to a September research note by Federal Reserve staffers Ayelen Banegas and Phillip Monin.
>
> That's why many of the big firms incurred larger-than-expected losses during the early days of the Covid-19 pandemic. They were caught in the so-called basis trade, which is designed to profit from small differences between Treasury futures and the cash market. Considered a safe arbitrage bet if held to maturity, it can occasionally go haywire, as it did in March 2020. 

If you are [long $1 billion of Treasury bonds and short $1 billion of Treasury futures](https://www.bloomberg.com/opinion/articles/2023-09-14/people-are-worried-about-the-basis-trade), your chances of losing even 2% of your money are low enough - because Treasury bonds and Treasury futures are almost the same thing - that a bank will lend you 98% of the money you need to do that trade. But they are not zero! Sometimes bad stuff happens.

But the other problem is the crowded trades. "Of the $90.7 billion that Citadel held in US stocks at the end of September, 93% was in shares Millennium also holds," says the article. The essential bet of the multi-manager pod shops is that investing skill is (1) real, repeatable and identifiable and (2) not correlated to broad markets: Picking the better things and shorting the worse things should work whether the stock market is up and down. But the risk is that investing skill might be _correlated with everyone else's investing skill._ If you hire people who are really good at knowing which stocks are good and which are bad, and then your four biggest competitors hire similarly skilled people, they might all pick the same good stocks and short the same bad stocks. And then if their bets blow up, they all blow up at once.

## First-loss funds - Matt Levine

Here's another way to [slice the returns from hedge-fund skill](https://www.bloomberg.com/news/articles/2023-11-30/hedge-fund-to-back-traders-who-risk-their-own-money-if-bets-fail):

> Andrew Lubin, previously the chief executive officer of the London unit of SAC Capital Advisors, and Tim Pearey, former CEO of Odey Asset Management, said they have started a hedge fund that provides capital to traders if they put in their own cash and agree to lose their money first when bets fail.
>
> Such arrangements, known as first-loss funds, are a niche part of the $4 trillion hedge fund industry and offer traders an opportunity to hold on to more of their profits in exchange for taking on the bulk of the risk. Traders signing up for Lubin and Pearey's London-based AB Asset Scale could keep as much as 60% of the profits they generate, higher than traditional industry payouts of 20% at major multi-strategy hedge funds. ...
>
> Such platforms frequently hire and fire traders whose performance has dropped or when a trading strategy they run falls out of favour. Lubin and Pearey said they are looking to pick talented traders affected by this churn.
>
> The first-loss funds provide as much as nine times the capital of a hedge fund or a trader, with their money being housed in a separately managed account. The arrangement, which provides a significant boost to assets under management, requires any losses to accrue to the trader's own invested capital first. …
>
> Losses of up to 10% will be absorbed by the trader's own capital with the fund aiming to liquidate their bets when declines hit 8.5%, according to an investor document seen by Bloomberg.

I like it. The traditional way to get fired from a multi-manager fund is to have too big a drawdown, to lose, say, 5% or 10% of your allocated capital. If you work at a big multi-strategy fund and then are "affected by this churn," the natural inferences to draw are:

1. You have investing skill (that's why the pod shop hired you), but
2. You sometimes lose 10% of your capital (that's why they fired you).

So someone else should be willing to hire you to run their money, but only if you take the risk of losing 10% of your capital.
