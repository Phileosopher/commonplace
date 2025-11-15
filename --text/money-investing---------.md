
## Banks - Matt Levine

### Oh McKinsey

The basic analysis of banking is:

1. A bank owns a pile of assets: loans, bonds, etc. Say they are worth $100 today.
2. The bank is funded mostly by senior claims on those assets: bank deposits and other forms of debt that really should get paid back. Say the bank has $90 of debt outstanding against its $100 of assets.
3. The bank also has a little sliver of equity: its shareholders have the residual claim on those assets, after the senior claims paid back. Here the bank has $10 of equity; depositors and other creditors are entitled to the first $90 of the bank's assets, but anything left over — currently $10 — goes to the shareholders.
4. The shareholders, therefore, have a close-to-the-money [_call option_ on the bank's assets](https://link.mail.bloombergbusiness.com/click/34992007.275818/aHR0cHM6Ly9lbi53aWtpcGVkaWEub3JnL3dpa2kvTWVydG9uX21vZGVs/60e87ce39a995a4b1a2deb96B1ce28125): If the assets turn out to be worth more than $90, the shareholders get the excess, but if they turn out to be worth less than $90, the shareholders get nothing. In particular, if the assets turn out to be worth zero — if all $100 of assets turn out to be fake and the bank is worthless — then the shareholders only lose their $10; the other $90 of the losses fall on the depositors. (Or the deposit insurance fund, the taxpayers, etc.)
5. This option is more valuable if volatility is higher. If the bank's assets have a 50/50 chance of ending up worth $98 or $102, then the shareholders will get back either $8 or $12 after paying off the debt, for an expected value of $10. (And the depositors will always get back their $90.) If the bank's assets have a 50/50 chance of ending up worth $70 or $130, then the shareholders will get back either $0 or $40, for an expected value of $20. And the depositors will get back $90 in the good case, but only $70 — a catastrophe, a bank failure — in the bad case.
6. The bank's executives have fiduciary duties to shareholders, and probably own a lot of stock themselves, so they want to make the stock more valuable.
7. Again, the theoretically correct way to make the stock more valuable is to make the assets more volatile, to make the bank riskier, to increase the value of the shareholders' option.
8. Everything _else_ about banks — bank regulation, prudential supervision, capital and liquidity requirements, deposit insurance, rules about bonuses and clawbacks, bank culture and training, speeches by politicians, depictions of banks in popular culture — is about mitigating this essential problem. The essential problem is that, if you look at a bank's capital structure with some financial sophistication but also some naivety, you will say "wait the bank works for the shareholders, the shareholders have an at-the-money option on the assets, and the way to increase shareholder value is to increase the volatility of those assets."

Many stories about banks are that story, the story of someone looking at a bank's balance sheet with financial sophistication and also naivety and saying "hey what about some more risk?" Here's a great one [from Bloomberg's Todd Gillespie](https://link.mail.bloombergbusiness.com/click/34992007.275818/aHR0cHM6Ly93d3cuYmxvb21iZXJnLmNvbS9uZXdzL2FydGljbGVzLzIwMjQtMDQtMDkvYWZ0ZXItbWNraW5zZXktbXVzaW5ncy10ZXhhcy1iYW5rLWFpbXMtdG8tZXNjYXBlLWZhdGUtb2Ytcml2YWxzP2NtcGlkPUJCRDA0MTAyNF9NT05FWVNUVUZGJnV0bV9tZWRpdW09ZW1haWwmdXRtX3NvdXJjZT1uZXdzbGV0dGVyJnV0bV90ZXJtPTI0MDQxMCZ1dG1fY2FtcGFpZ249bW9uZXlzdHVmZg/60e87ce39a995a4b1a2deb96B43cf0e22):

> A cadre of McKinsey & Co. consultants strode into a meeting with Houston's most prominent local bank to dwell on the problem bedeviling thousands of regional banks: How to stay relevant.
> 
> "The thing that I laugh at, though, is they had a chart," said Steve Stephens, the CEO of Amegy Bank, recalling the presentation to the board of its parent company in late 2022. McKinsey's message was that banks such as Amegy could find a lucrative business niche, like the so-called specialty regional banks that it spotlighted in slides, he said.
> 
> "Well, that was First Republic, Silicon Valley Bank and Signature," said Stephens, all of which collapsed last year. "It's specialization that got them."

This was good advice, that McKinsey gave him! [[4]](imap://dave%40stucky%2Etech@mail.stucky.tech:993/fetch%3EUID%3E.INBOX%3E4899#footnote-4)  Find a niche, specialize, make a big bet: Diversification makes you safer but reduces the variance of your returns; specialization increases the variance and thus the likelihood of making a lot of money for shareholders. Also the likelihood of going to zero.

[4] To be fair: "A representative for McKinsey declined to comment. That 2022 presentation was meant to provide an overview on the trends shaping the banking industry and the three failed banks were highlighted among about two dozen firms to showcase how investors were valuing them, according to another person who saw the deck and declined to be identified discussing private information."

NOTE: THIS IDEA IS A VERY VALUABLE ASPECT OF EXPLAINING WHY FINANCIAL REGULATIONS ARE SO PSYCHOTIC; MAKE SURE TO PARSE AND SUMMARIZE THIS ENTIRE ARTICLE!!!

## Adverse Selection - Matt Levine

### The Harvard of trading

I think that, if you had only five minutes with a world-class trader, and you asked her "teach me the essentials of trading," probably she would spend the five minutes on adverse selection. The essential lesson is that, if you are being offered a trade, that probably means it's a bad trade; your job is to understand that thoroughly so you can figure out the exceptions. There are many ways to teach this lesson, but my favorite probably comes from a reader email [I quoted last October](https://link.mail.bloombergbusiness.com/click/35377662.266794/aHR0cHM6Ly93d3cuYmxvb21iZXJnLmNvbS9vcGluaW9uL2FydGljbGVzLzIwMjMtMTAtMTIvZnR4LWhhZC1tYW55LWJhZC1zcHJlYWRzaGVldHM_Y21waWQ9QkJEMDUxNDI0X01PTkVZU1RVRkYmdXRtX21lZGl1bT1lbWFpbCZ1dG1fc291cmNlPW5ld3NsZXR0ZXImdXRtX3Rlcm09MjQwNTE0JnV0bV9jYW1wYWlnbj1tb25leXN0dWZm/60e87ce39a995a4b1a2deb96B328a4bcc), when I was writing a lot about Sam Bankman-Fried's coin flipping at Jane Street:

> This was a Susquehanna interview question 25 years ago! They made me do the math on 1000 coin flips. EV(heads) (easy), standard deviation (slightly harder), then they offered me a +EV bet on the outcome. I said "let's go."
> 
> They said "Wrong. If we're offering it to you, you shouldn't take it."
> 
> I said "We just did the math."
> 
> They said "We have a guy on the floor of the Amex who can flip 55% heads."

The point here is that Susquehanna International Group employed a guy who was really good at flipping coins so they land heads, _so that_ Susquehanna's traders didn't get too cocky about their bets. "I've done the math and this trade has positive expected value," they will say, but then they'll pause and remember the coin-flip guy and think "if this trade really has positive expected value, why is it being offered to me," and they think a bit harder about it and become better traders.

This lesson applies beyond individual trades. For instance, there is the structure of the investment management industry. Agustin Lebron, a former Jane Street trader, has a very good book called [_The Laws of Trading_](https://link.mail.bloombergbusiness.com/click/35377662.266794/aHR0cHM6Ly93d3cubGF3c29mdHJhZGluZy5jb20v/60e87ce39a995a4b1a2deb96B9d8d5873), in which he says:

> The profitable trades that exist in the world are either (a) the ones you're intimately involved in running, or (b) the ones that are inaccessible to you. There is no (c). And what's funny about the situation in trading is that, if we were talking about just about any other industry, the very notion of a (c) would be laughable. Imagine if someone who's good at manufacturing cars came to you and said: "Hey. I'm a profitable car-maker. If you like, I'll let you take all the profit from my car-making skill in exchange for a small fee for me." You would rightly suspect they're trying to pull one over on you. So why is the situation different in trading?

Similarly! At Bloomberg Businessweek, [Alice Kantor profiles IM Academy](https://link.mail.bloombergbusiness.com/click/35377662.266794/aHR0cHM6Ly93d3cuYmxvb21iZXJnLmNvbS9uZXdzL2ZlYXR1cmVzLzIwMjQtMDUtMTQvdGhlLXN0b2NrLW1hcmtldC1tdWx0aWxldmVsLW1hcmtldGluZy1jb21wYW55LWZvci10ZWVucz9jbXBpZD1CQkQwNTE0MjRfTU9ORVlTVFVGRiZ1dG1fbWVkaXVtPWVtYWlsJnV0bV9zb3VyY2U9bmV3c2xldHRlciZ1dG1fdGVybT0yNDA1MTQmdXRtX2NhbXBhaWduPW1vbmV5c3R1ZmY/60e87ce39a995a4b1a2deb96Bc83039a9), a multilevel marketing scheme for stock and commodities trading. At the object level, this seems like a bad trading school:

> During the pandemic, IM grew from a small New York operation into a global phenomenon by selling the promise that it could teach anyone, particularly teens and twentysomethings, how to become a savvy retail investor. For a one-time $275 fee and $250 a month, members had access to online courses and coaches providing trading strategies—the "Yale of forex, the Harvard of trading," as a salesman described IM in a marketing video. When young people weren't being invited by their friends to become budding stock market mavens, they might encounter Instagram videos showing how others had gotten rich with the IM method or hear about celebrity members, including fashion model Blac Chyna and professional boxer Floyd Mayweather Jr. 

But at the meta level, it provides a helpful lesson in adverse selection. [[2]](imap://dave%40stucky%2Etech@mail.stucky.tech:993/fetch%3EUID%3E.INBOX%3E5653#footnote-2)  The thing that IM Academy teaches, if you are paying attention, is "if they know so much about how to make money in financial markets, why would they teach me how to do it for just $250 a month?" 

NOTE: THE ASPECT OF ADVERSE SELECTION HAS WISDOM TO IT! YOU SHOULD BE HUNTING FOR THE TRADES, NOT THE OTHER WAY AROUND UNLESS THERE'S ANOTHER REASON
