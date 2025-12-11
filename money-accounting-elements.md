
# The individual elements of basic accounting

## Assets

All assets can be classified as tangible or intangible assets.

- Tangible assets are things you can point at (e.g., an [auto](autos.md) or building).
- Intangible assets are conceptual ideas that still have value (e.g., [intellectual property](legal-ip.md), [insurance](money-insurance.md)).

They can also be current or non-current.

- Current/convertible assets are used within the next 12 months and can typically be converted to cash easily:
  - Cash on hand
  - Cash in banks
  - Money owed
  - Petty cash (an obsolete concept now that bank cards exist)
  - Raw materials and stock
  - Pre-payments on insurance or rent
- Non-current/fixed assets will severely affect day-to-day operations if converted to cash:
  - Land
  - Buildings
  - Machinery
  - [Vehicles](autos.md)
- Contingent assets are *likely* future assets, such as accounts receivable.
  - A debt is certain, but collecting a debt isn't, so contingent assets are more scrutinized than contingent liabilities.

A circulating asset is what most people think of when they imagine "[business](business.md)":

1. Convert cash to goods (e.g., manufacturing materials, inventory).
2. Do something with the goods.
3. Convert the goods back to cash again, hopefully more than the first time.

The point of sale is the location where a transaction occurs, and accounting treats the exchange as having at least 2 transactions, which often represent informally on a receipt:

1. The customer providing payment or promise of payment for the product (debit an asset, credit Sales).
2. If applicable, they will have to move the money from the point of sale to another location (debit Bank Account, credit Undeposited Funds).
3. The company providing the product from inventory or a service rendered from a worker (debit a liability or Cost of Goods Sold, credit an asset).
4. If applicable, sales tax (debit Tax Expense, credit a tax liability).
5. If, for some reason the payment doesn't go through, the vendor may charge a Not Sufficient Funds (NSF) fee for the inconvenience.

Whenever there's cash on hand, there *will* be errors.

- If there aren't any errors *at all*, it's likely the workers are being *very* particular about keeping records because they're trying to steal from the company.
- The best way to address the problem is to make sure via [company policy](mgmt-5_communication.md) that the errors are the safest *type* of error (e.g., collected cash but didn't record it).

### Accounts receivable (A/R)

While the customer needs grace to work with their finances, managing A/R is absolutely critical to maintain cash flows, and some things are still "receivable" even when the company only uses cash receipts:

- Bills sent for rendered services.
- Outstanding [loans](money-2_debt.md) which need to be paid by other entities.
- Written arrears for clients/customers to make future payments.

A/R uses some shorthand terms when invoicing for specific, common arrangements:

- Payment in advance - customer must make a deposit or payment before starting work (e.g., 50% payment in advance).
- Due upon receipt - typically, customer must make payment by the following business day after receiving the invoice.
- Pay on delivery - the customer must pay when the product is delivered.
- Net # - various terms that give a set number of days before payment is due (e.g., Net 7 means the buyer has a week to pay it).
  - The most common are Net 7, Net 10, Net 30, Net 60, and Net 90
  - It's not uncommon to start with Net 7 for new customers and give Net 90 to loyal, long-time customers.
- X% # Net # - customer receives a percentage discount if the invoice is paid with a certain number of days, or the full amount is due in a longer number of days (e.g., 2% 10 Net 30).
- Line of Credit Pay - customers can pay the invoices over a longer routine period of time, such as monthly or quarterly.
- End of Month (EOM) - due at the end of the month, irrespective of when the invoice was created.
- Cost, Insurance and Flight (CIF) - The seller agrees to pay shipping, insurance and freight charges *before* the item is delivered.

People sometimes don't pay their bills, so organizations need a procedure for managing them:

1. Before it happens, the [contract](people-contracts.md) should *clearly* indicate late fees and the consequences for what should happen.
2. Try to contact them about the unpaid debt.
3. Write off the debt as Bad Debt Expense.
4. Make a record to prevent them from abuse the situation again.

When there are many entities to manage, a debt-by-debt solution is impractical, so they use an Aging of Receivables to accurately track the likelihood of non-payment:

1. Make a chart that breaks apart the late payments into time-based categories.
   - e.g., 1-30 days, 31-60 days, 61-90 days, 91+ days
2. Assign progressively increasing percentages for each section.
   - e.g., 1-30 is 5%, 31-60 is 10%, 61-90 is 15%, 91+ is 20%.
3. Keep track of every account within each category.
4. During the adjusting phase, use the applicable percentage of each category to create the posted Bad Debt Expense.

### Depreciation/amortization

The value of assets goes down over time, so accountants must clarify that deterioration of value.

- If it's a fixed asset, it depreciates.
- If it's an intangible asset, it amortizes.

The value of fixed assets are typically assessed at their replacement cost, minus their scrap value.

While accountants typically only amortize on a straight-line basis (the first example here), they can choose from multiple ways to depreciate a fixed asset.

1. Straight-line depreciation - the most common and simplest:
   - (Asset Cost - Scrap Value) / Asset's Useful Life
   - The depreciation rate doesn't change over the life of the asset.
   - While it spreads the expense evenly across accounting periods and easy to automate in most software, determining the useful life of the asset takes lots of guessing and a miscalculation could over-value the asset for several years.
2. Declining balance depreciation - an accelerated method that depreciates assets more in their earlier years:
   - Asset Value x Straight Line Depreciation Percentage
3. Double declining balance depreciation - an accelerated method when assets are *very* productive in their early years:
   - Asset Value x Straight Line Depreciation Percentage x 2
   - It writes off an asset's value the quickest, but the calculations are more complex than other methods and typically use a depreciation schedule to only have to calculate it once.
4. Sum of the years' digits depreciation - an alternate accelerated depreciation method:
   - (Remaining Asset Life / Sum of the Years' Digits) x (Asset Cost - Scrap Value)
     - The sum of the years' digits is calculated by adding the digits together (e.g., 5 years is 5+4+3+2+1).
   - Not as fast a devaluation as double declining balance, but faster than straight line.
   - Gives control over the depreciation expense recorded each month, but also is *the* most difficult depreciation method to calculate.
5. Units of production depreciation - defined by how many of items something can produce:
   - (Number of Units Produced / Asset Life in Units) x (Asset Cost - Scrap Value)
   - It's easy to calculate and more accurate than straight-line, but requires keeping an accurate record of the number of items it produces (which will likely vary month-to-month).

While *every* long-term asset could technically be depreciated, many items are simply easier to expense for tax reasons than bother with depreciating (e.g., brooms, computers, etc.).

Typically, the amortization of a loan is from how the *bank* sees it, since [debt payments](money-2_debt.md) are accounts receivable to them.

### Inventory tracking

Accountants can track expenses for inventory in several ways. This reflects as "cost of goods sold":

- Average Cost Method - Find the average cost of all current inventory (Total Inventory / Number of Items), then make that the value of each inventory item. This one isn't used much because it requires more calculation.
- First In, First Out (FIFO) - As inventory is depleted, use the earliest inventory's costs. The IRS likes this one, but many organizations don't because it typically reduces income (and tax payments) the least.
- Last In, First Out (LIFO) - As inventory is depleted, use the latest inventory's costs. This can easily lower profit, which can reduce tax payment.
- Highest In, First Out (HIFO) - As inventory is depleted, select the most expensive inventory's costs. This only applies to very specific circumstances, but is the best way to reduce tax payment if it's permissible in tax law.

Manufacturing plants have extra categories of each inventory item:

- Raw Materials - The incoming items as they're shipped into the factory.
- Finished Goods - The items ready to be sent out of the factory.
- Work in Process (WIP) - When there are multiple stages to the product, WIP indicates the items as they're worked into increasing states of completion.

Inventory shrinkage is when inventory is gone, but was *not* sold.

- Theft is the most likely way inventory goes missing, with damage being a close second likelihood.
  - Theft is very difficult to manage and requires a combination of [good hiring practices](mgmt-3_teams.md), locks, and security cameras.
- Inventory obsolescence is when it can't be sold anymore (e.g., out-of-style clothing, rotten food).

One specific way to track the health of a business is through the inventory turnover rate.

- Tracking the time between each individual item being bought and sold (or at least an average across products) can detect issues with inventory.
- If it's too high, shrink is almost guaranteed, meaning the company will lose assets.
- If it's too low, *any* [logistical bump](logistics.md) could disrupt timely delivery, meaning the company will lose [clientele](marketing.md).
- The easiest (and most intensive) way to track inventory is to use a perpetual inventory system that updates on *every* transaction (which typically needs [computers with scanners](computers-ocr.md) to assist).

## Liabilities

A liability involves anything an organization owes:

- Current liabilities are due within the next year:
  - Principal and interest on loans in the next year
  - Lines of credit with suppliers
  - Wages owed
  - Taxes payable
  - Bank fees
- Non-current liabilities are long-term:
  - Mortgage
  - Pension obligations
  - Principal and interest on loans beyond a year out
  - Bonds and long-term loans
  - Deferred tax liabilities
  - Lease payments that aren't due for more than a year
- Contingent liabilities are things an organization *might* owe.

One of the more frequent uses of accounting reports is to indicate assets a company can use to leverage/gear further financing.

- A company can have deficits and a negative net worth many times, but fails the first time it runs out of money.

Any money that needs to be put aside for a future liability is an encumbrance or provision.

- Sometimes, the money can go into a sinking fund to repay a debt or replace a wasting asset.
- The amount of unsecured debt a company owes if it's liquidated is its subordinated debt.

A [loan](money-2_debt.md) can be compound or simple interest:

- Simple interest loans charge periodic interest on the principal (e.g., an unpaid 3% on $100 is $103 on Month 1, $106 on Month 2, $109 on Month 3).
- A compound interest loan charges interest on the principal *and* interest (e.g., an unpaid 3% on $100 is $103 on Month 1, $106.09 on Month 2, $109.27 on Month 3).
- Compound interest is subtle, but over time it creates exponential (and [some would say extortionate](money-2_debt.md)) costs on unpaid debts.

### Accounts payable (A/P)

Even if an organization stays *very* diligent to paying all its bills, an organization will always have some form of owed payments that are "payable" to other entities:

- [Payroll](business.md) (the most common)
  - Alongside payroll, there's also withholding for tax and benefits (e.g., health [insurance](money-insurance.md))
  - For convenient payroll calculations, 3 minutes is equal to 0.05 hours
- Outstanding [loan](money-2_debt.md) principal or interest to be paid to other entities.
- Subscriptions which expect payment *after* delivery.
- Trade Payable, which is when a vendor has given goods or services but hasn't been paid yet.

Often, not tracking liabilities can cause loans to go into default and further troubles for an organization.

Sometimes, charges need to be reversed, usually for defective goods or poor service.

- The [Visa/Mastercard](politics-monopolies.md) duopoly means many payments have guaranteed transaction fees.
- A chargeback is reversing the payment, which may still incur transaction fees.
- Rebates give a partial refund for services that were overpaid or partly used and then canceled.
- Credit notes cancel a customer's debt.

Debts can be secured (with some form of collateral) or unsecured (with a promise and wishful thinking).

- Unsecured debt is essentially impossible for the lienholder to ensure it will be paid.
- While most secured debt is against the object in question (e.g., an [automotive](autos.md) for an auto loan), it can be collateralized on essentially anything the lienholder will [agree to](people-contracts.md), typically with a refinancing agreement.

### Bonds

While anyone can borrow money from a bank, sometimes a company does *not* want to use a bank, so they'll issue bonds instead.

- A bond is a specific [debt instrument](money-2_debt.md) that allows large organizations like governments and corporations to borrow a *lot* of money from many people.

In its most straightforward use, a bond's structure is relatively straightforward to understand:

1. An organization issues bonds with an interest rate and maturity, typically in $1,000 or $100 denominations (e.g., 10,000 bonds at a $1,000 face value).
2. Those bonds will have a certain number of years to maturity, with an interest rate (e.g., $1,000 face value, with a 4% yield to maturity in 3 years).
3. The bond price will be whatever the investor originally pays (e.g., a $1,000 bond with a 4% yield to maturity in 3 years is $889).
4. Before the bond matures, the investor can take back their money without interest.
5. At the bond's maturity, the investor can redeem that bond at any time, and the organization must make a balloon payment of the entire amount.

This gets *much* more complex, though:

- Some bonds are callable *before* the maturity date. In that situation, the yield-to-call will be lower than the yield-to-maturity (e.g., 1.7% instead of 4%).
- Bonds can be sold at par, but also can be sold at a premium or discount. This can happen from [market conditions](money-economics.md) for the bond, as well as the [reputation](people-image-why.md) of the organization.
- The organization can use a coupon rate, which is where the organization pays a set percentage of interest every year (e.g., a 4% coupon rate on $1,000 pays $40 a year).
- If the coupon rate is the same as the yield rate, the organization will simply pay back the original amount when it's called.

Like any other debt obligation, bonds can be secured or unsecured:

- Secured bonds collateralize an asset. A mortgage-backed security (MBS), for example, will collateralize the title of the borrower's [home](home-buy.md).
- Unsecured bonds by companies are called debentures. In the event of a liquidation, unsecured creditors will only get whatever assets are left over *after* the secured investors.

Short-term bonds are 1-3 years' maturity, medium-term are typically 10 years, and long-term are over an even longer period of time.

## Equity

Assets deals with things that "exist", and liabilities deals with things that are "owed", but equity is strictly conceptual.

- Since [investors](money-investing.md) often make [decisions](people-decisions.md) from [optics](people-image-why.md) (or are taken in by [fashions](trends.md) they [don't understand](understanding.md)), there are *many* complex domains within equity that have very little practical explanation.
- The only 2 ways to increase profits are to increase revenues or decrease expenses.

There are a few forms a business can take. They are either taxed *before* the owner receives money, or it's pass-through to the owners:

- A sole proprietorship is a person's individual business (pass-through).
- A partnership is the shared business of several individuals (pass-through).
- A Limited Liability Company or Limited Liability Partnership (LLC/LTD or LLP) is a legal (not accounting) demarcation to protect the business owners from [liability](legal-safety.md).
- A corporation is a living, separate legal entity that's incorporated on a specific date, and comes in a few forms:
  - A C corporation can be publicly traded (*not* pass-through).
  - An S corporation has many more filing requirements and can't be publicly traded (pass-through).

In a publicly traded company, the shares are owned by whoever is willing to pay for them, and the majority stakeholder typically has decision-making power over the company.

A company can also perform a share repurchase, where it buys back the shareholders' shares of stock.

### Income

A company that succeeds in an accounting period will have money left over, and it has several options:

1. Save it as Retained Earnings, typically by placing it in a reserve account (i.e., make a [self-insurance](money-insurance.md) policy).
   - It's taxable, but reinforces Operating activity.
   - A not-for-profit organization can't technically make a profit.
2. Reinvest the money into more assets (e.g., buy new equipment).
   - Often *not* taxable, and can be an Investing activity.
3. Pay down liabilities.
   - Not taxable, like a Financing activity, but boring to [executives](mgmt-1_why.md).
4. Use the money as [collateral](money-2_debt.md) to get *more* liabilities.
   - Not taxable, a direct Financing activity, but exposes more [risk](safety-riskmgmt.md) to the company.
5. Send the money out as Owner's Draw (to the owner) or Dividends (to the shareholder).
   - Taxable, and lowers the company's net worth, but is how people who own the company get paid.

Calculating total earnings isn't always simple:

- Gross income is the total earnings after subtracting loss from profit.
- EBITDA: earnings before interest, tax, depreciation, and amortization.
- EBITA: earnings before interest, tax, and amortization.
- EBIT: earnings before interest and tax.
- Net income comes *after* removing expenses, interest, tax, depreciation, and amortization from revenue.
- The quality of earnings is *actual* earnings that come from higher sales or lower costs, and can't be attributed to accounting anomalies.

### Expenses

Overhead is the cost of keeping the organization running that's *not* tied to production or sales.

- The break-even point is the precise number of units that must be sold in an accounting period to return a profit.
- Quantity to sell = total fixed costs / (selling price per unit - variable cost per unit).
- An example helps the most to illustrate the concept:
  - It takes $10,000 to run the organization in a given month.
  - That same month, the company's product can sell for $100 and costs $50 to make.
  - If the company sold 100 units (making $10,000), it would cover the overhead, but not the per-unit price.
  - To make a profit of $0, they would need to sell 200 units (10,000 / [100 - 50]).

Operating risk is when fixed operating expenses are high enough that they may interfere with profitability.

### Paying out

If the organization isn't owned by a singular entity, the owners each own a percentage of the earnings.

- The company's stock is a fractional "sharing" of that company.
  - Preferred stock is paid dividends first and has priority with company assets (e.g., with a liquidation), but the shareholders don't have voting rights.
  - Common stock is secondary on dividends and receiving assets, but shareholders have voting rights.
- The rights to [manage the organization](mgmt-1_why.md) are often *not* evenly matched with the income they'd receive (e.g., board members can't own common stock).

Often, the language of the corporate bylaws dictate how stakeholders can be paid.

- Frequently, the leadership leaving can trigger a golden parachute, leaving that executive *very* wealthy even as they leave the organization.

### Equity games

A stock split divides the shares evenly (e.g., 2:1 or 3:1).

- This means every shareholder has twice or thrice the shares, at 1/2 or 1/3 the value.
- Nothing technically "changes", but our [bias](mind-bias.md) means it can influence people to buy more stock.

For various reasons that affect equity, a business can be carved out into different domains:

- Some portions of a business are cost centers (often e.g., accounting, [IT](computers.md)) and others are profit centers (e.g., sales, [marketing](marketing.md)).
- Segment reporting divides out various divisions of a business to create specialized reports.

While a dividend is considered income that goes to the shareholders, a share repurchase/buyback is considered an expense.

- Therefore, net income can be reduced by buying company shares back from shareholders.

The nominal value of a share, when it's first issued, establishes its initial public offering (IPO).

- That IPO value *will* move around (meaning its value isn't *that* utterly important), but it generally represents a dramatic shift in the way a company operates and indicates the first time the public can purchase it.
- The listing requirements for IPOs are a [legal domain](glossary-legal.md) that falls *way* outside the range of accounting.

### Stock markets

The complexity of stock markets comes through a proliferation of third parties.

- Market makers are individuals or entities that arrange [two-sided transactions](people-contracts.md) to buy or sell securities and make a profit between the bid (buying) and ask (selling) price.
- The National Best Bid and Offer (NBBO) represents the highest bid and lowest ask for a security, making it the tightest bid-ask spread.
- Payment for Order Flow (PFOF) is a small commission the market makers make when
