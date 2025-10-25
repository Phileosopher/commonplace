
# Accounting explained

Accounting is the language of business.

- Accountants track the numerical history of transactions, then express the most relevant information in reports.

Understanding how accounting works allows you to understand where the transactions flow from.

- Most of the system is automated with spreadsheets or accounting software, so most people only need to maintain conceptual awareness of how it works.

Accounting isn't strictly a discipline of math.

- [Math](math.md) uses complex calculations, and accounting doesn't use anything above [algebra](math-algebra.md).
- Accounting, does, however, use large *columns* of numbers.
- In that sense, accountants create [databases](database.md) more than performing mathematical calculations.

## Mindset

Accounting is a distinct trade with a few idiosyncratic details.

These details are *not* intuitive, but they're not difficult to explain.

### Double entry

On the back-end, *all* accounting uses the double-entry accounting system.

- The system uses a T-ledger, with the numbers written on the left and right sides.

1. *Every* account in the account ledger only sits within 3 possible domains:
   - Assets - things you have
   - Liabilities - things you owe
   - Equity - things left over as profit/loss (i.e., Assets - Liabilities)
2. All transactions have 2 sides to it:
   - A debit ("debir" or "Dr") on the left side.
   - A credit ("credir" or "Cr") on the right side.
   - The idea is that every transaction on the left side has an equal amount on the right:
     - All the debits of a transaction will equal all the credits.
   - There is *no* inherent meaning to debits or credits without the account it's related to.
     - Debits are *typically* used for assets and expenses, and credits are *typically* used for liabilities and income, but it reverses when the books are closed and there are counter-balancing accounts to many of them.
   - In general, if you have to anchor a concept, think of how the number goes up:
     - If it's assets, debit means up.
     - If it's a liability, credit means up.
     - If it's equity, credit *generally* means up, but then debit means up when equity zeroes out at the end of the period.
3. The debits and credits have meaning relative to their placement in the account ledger:
   - Assets - debit means it goes up, credit means it goes down (e.g., a bank's debit/credit card is relative to *them*).
   - Liabilities - debit means it goes down, credit means it goes up (e.g., getting a new loan will be a new credit).
   - Equity - debit goes to Expenses, credit goes to Revenue.
4. Every transaction traces movement between the accounts:
   - Getting a $1,000 loan - Debit $1,000 to Loan Expense, Credit $1,000 to Outstanding Loans.
   - Buying $200 of inventory - Debit $200 to Inventory, Credit $200 from Cash.
   - Selling $100 of inventory for $150
     - Debit $100 to Cost of Goods Sold, Credit $100 from Inventory.
     - Debit $150 to Cash, Credit $150 to Sales Revenue.
5. At the end of the period, make closing entries to the Equity accounts to zero them out for a new period:
   - Debit all Revenue accounts to make them $0, Credit the same amount to Retained Earnings.
   - Credit all Expense accounts to make them $0, Debit the same amount to Retained Earnings.

The essence of double entry is that absolutely *everything* must be rigorously organized and micromanaged.

- Since all debit and credit transactions add up to zero, it's patently obvious at the transaction level when something is wrong.
- Every single thing's philosophical status (i.e., its [purpose](purpose.md) or [essence](values.md)) is represented by an account.
- Every time there's a change to that thing, it's affecting something else (i.e., a different account) and must be recorded as well.
  - If it's trading one "thing" for another "thing" (e.g., buying inventory), it's asset-with-asset.
  - If it's trading a "thing" for a [future promise](people-contracts.md) (e.g., getting a loan) or fulfilling that promise, it's asset-with-liability.
  - If it's an account *outside* the organization (e.g., a bank account) it's reproduced precisely the same as an asset or liability.
  - If it's strictly conceptual (e.g., a donation or making money), it's an equity account (income if it makes more money and expense if it loses money).

### Accounting philosophy

Accountants live dogmatically by Generally Accepted Accounting Principles (GAAP).

- Any accountant who doesn't abide by GAAP is violating the [rules](people-rules.md) that govern *any* accounting, and is setting up their organization and themselves for a bad time in the future.
- GAAP has 4 assumptions, 4 principles, and 4 constraints.

Assumption 1 - Accounting Entity

- The organization is [logically separate](logic.md) from its owners and other organizations.
- As much as possible, revenue and expenses for the entity aren't affiliated with personal expenses.
- Without it, the [boundaries](people-boundaries.md) between entities gets complicated or nonexistent and opens everything up to abuse and fraud.

Assumption 2 - Going Concern/Continuity

- Except for a 100% liquidation, the organization will keep operating indefinitely into the unforeseeable future.
- This assumption validates several methods:
  - Whether an asset is fixed vs. current
  - Short-term vs. long-term liabilities
  - Capital and revenue expenditures
  - The changes in value of an asset (Capitalization, Depreciation, and Amortization)
- Without it, there will be no means of [projecting](imagination.md) what to do in the farther future.

Assumption 3 - Monetary Unit Principle

- The unit of record must be a stable currency.
  - The [FASB](http://www.fasb.org/) accepts the nominal value of the US Dollar, unadjusted for inflation.
- That currency is as fixed as possible to accurately reflect value compared to everything else.
  - In other words, the USD is the standard of currency because everyone uses it as the standard of currency.
  - Barring a major upset in the world [economic](economics.md) system (this was written in 2023) even other *currencies* are pegged to the dollar.
- Without it, there's no clear, measurable [certainty](understanding-certainty.md) on the value of anything relative to other items or periods.

Assumption 4 - Time-Period Principle

- An entity's economic actions are divided evenly into artificial, fixed, equally sized periods.
- As much as possible, attach revenue and expenses together in the same periods using cut-off procedures.
- The time divisions are typically monthly, quarterly or yearly but can go down to weekly, daily or hourly if needed.
- Without it, there's no clear way to define how an organization performed during a period of time relative to other periods.

Principle 1 - Historical Cost Principle

- The costs of most Assets and Liabilities must be based on how much they paid, and not fair market value.
- While it conflicts with [marketing](marketing.md) (and [investors](money-investing.md), to an extent), it avoids [subjective](image.md) or [biased](mind-bias.md) values based on [the market](economics.md).
- This principle doesn't always apply: most [debts](money-2_debt.md) and [securities](money-investing.md) report at market values.
- Without it, the value of things can be over-stated, meaning extreme dissatisfaction and potential complications later on when the value is more accurately determined (instead of simply dissatisfaction right now).

Principle 2 - Revenue Recognition Principle

- Organizations must either record when they receive revenue (Cash Basis) or when they earn it (Accrual Basis).
- Most organizations, for various [legal](legal-safety.md) and [contractual](people-6_contracts.md) reasons, *can't* use a Cash Basis.
- Without this distinction, the cash flow becomes hard to clearly track.

Principle 3 - Matching Principle

- As long as it's reasonable, expenses *must* match with revenues.
- Expenses are recognized when they contribute to revenue, *not* when they've incurred.
  - Expenses *can* be charged to the current period, but only if they can't trace directly to revenue.
- This principle allows more accurate analysis of profitability and performance (e.g., Depreciation, Cost of Goods Sold).
- Without it, it's difficult to determine and measure the relationship between various business activities.

Principle 4 - Full Disclosure Principle

- Preparing and using information costs money, so analyzing the tradeoffs determines which information should be disclosed.
  - Accountants can store their information in the main body of financial statements, in the notes, or as supplementary information.
- The disclosed information should provide enough knowledge for all organizational [decisions](people-decisions.md), but shouldn't become unreasonably expensive.
- Without it, accountants would endlessly peruse the record keeping and drive a company out of business.

Constraint 1 - Objectivity Principle

- Financial statements that accountants provide to the organization must use objective evidence.
- A massive aspect of accounting involves documenting and recording evidence of already-existing information.
- Without it, the organization wouldn't be durable to the criticism and audits of other entities.

Constraint 2 - Materiality Principle

- An item should only be reported if it might affect a reasonable individual's decision.
- Without it, accountants would gather endless useless information.

Constraint 3 - Consistency Principle

- From period to period, an organization must use the same accounting principles and methods.
- Like the Time Period Principle, there's no clear way to define without it how an organization performed during a period of time relative to other periods.

Constraint 4 - Conservatism Principle

- When accountants must decide, they should pick the solution that *least* overstates assets and income.
- Like the Historical Cost Principle, the value of over-stating things means extreme dissatisfaction and potential complications later on when the value is more accurately determined (rather than simply dissatisfaction right now).

## The accounting cycle

The routine of accounting breaks each period into an 8-step accounting cycle:

1. Identify transactions - this can require a human accountant, but can be largely automated.
   - It's simply a matter of detecting movement of anything with value:
     - Selling or returning a product.
     - Purchasing supplies.
     - Exchanging assets.
     - Borrowing or paying off a [debt](money-2_debt.md).
     - Depositing from or paying the organization's owners.
     - Losses from natural disasters or theft, or collecting an [insurance payment](money-insurance.md).
   - Cash basis looks only at events that have happened, while Accrual basis looks at [promises of events happening](people-6_contracts.md) as well.
2. Journal entries - use [language](language.md) to articulate chronologically what happened.
   - The first accounting documentation is in the journal.
   - Each journal entry always affects at least 2 accounts (as shown above).
3. Posting - record the same information from the journals to the General Ledger.
   - It's effectively the same information, but [classified](organization.md) by account and without the [story](stories.md) of what happened.
4. Trial balance - calculate the total balances at the end of the period.
   - This is a redundant step that [ensures](understanding-certainty.md) the debits and credits are clearly balanced before moving forward.
5. Worksheet - for any discrepancies in the trial balance, make corrections (adjustments) on a worksheet.
   - This step isn't necessary in a small cash-basis organization, but things rarely stay simple in a large organization.
   - Adjustments also account for one-time payments that affect multiple periods:
     - Depreciation divides out the deterioration of multi-year (long-term) assets.
     - One-time payments for longer-term assets (e.g., [insurance](money-insurance.md)) are divided out to accurately match expenses with revenues.
   - At the end, take another trial balance to ensure the adjustments balance out the accounts.
6. Adjusting journal entries - post any worksheet adjustments as journal entries to the affected accounts.
   - This step is the cumulative effort of the worksheet stage.
7. Financial statements - produce all the financial statements (more detail below).
8. Close the books - zero out the revenue and expense accounts (as shown above).
   - This phase is also usually where stock dividends and other adjusting equity accounts are managed (more detail below).

Now that [computers](computers.md) can error-check everything and fix errors automatically, the cycle isn't *completely* critical, but accountants like its redundancy because it gives more possibilities of catching errors.

For the sake of convenience, accountants [organize](organization.md) the accounts by numbering them with an approximate convention:

- 1000-1999 Asset accounts
- 2000-2999 Liability accounts
- 3000-3999 Equity accounts
- 4000-4999 Revenue accounts
- 5000-5999 Cost of Goods Sold accounts
- 6000-6999 Expense accounts
- 7000-7999 Other Revenue accounts (e.g., interest income)
- 8000-8999 Other Expense accounts (e.g., income taxes)

## Reporting

Four major reports are *very* commonplace.

- These "financials" are top-level descriptions of the organization.
- However, other reports can drill into as much detail as the interested parties care to go.

The **Income Statement** shows financial performance over time.

- They're the most important because they most significantly reflect [performance](results.md).
- At the beginning of the period, the Income Statement balance is zero.
  - Every cycle, the books close and set the balance back to zero.
- Revenue - Expenses = Income (i.e., Profit or Loss)
- Broadly, Expenses are grouped into two categories:
  1. Operating Revenue & Expenses, which are directly associated with the organization's operations.
  2. Non-Operating Revenue & Expenses, which is everything else not directly related to the organization's operations.

The **Balance Sheet** shows a financial position on a specific date.

- It breaks out the above-stated Asset, Liability, and Equity accounts for a given date.
  - At the end of each year, Net Earnings/Income are added to Retained Earnings on the Balance Sheet.
- It's the easiest to produce, since it's basically the General Ledger without all the details.

The **Statement of Cash Flows** shows how money flows in and out of various activities.

- There are 3 major activity groups:
  1. Operating activities - keeps the organization going.
  2. Investing activities - manages assets to keep operating activities going.
  3. Financing activities - expands and grows the organization through loans, others' [investments](money-investing.md), or donations.
- Without computer assistance, Cash Flow Statements are tedious to generate.

The **Statement of Changes in Equity** shows the changes in equity across a period.

- Equity is the organization's net worth, *not* its actual value.
- Statement of Changes in Equity isn't very useful for internal decisions *nearly* as much as for [investors](money-investing.md), so it's usually not bundled with the other three.

The statements could best be described by comparing the organization to a fruit-bearing tree:

- The Balance Sheet is a slice of the tree's trunk, which is the foundation of what produces the fruit.
  - The Equity/Net Worth/Accumulated Retained Earnings section of the Balance Sheet approximates the value of the organization.
- The Income Statement is the fruit gathered for a window of time.
  - Some years are lean with little or no Net Income, and others are strong with plenty of Net Income.
- The Cash Flow Statement shows where the cash traveled in the organization.
  - It shows how much of the Income Statement produced a yield (Operating/Investing Activities) and how much the Balance Sheet helped grow the organization (Financing Activities).

Typically, the reports are often bundled together into an Annual Report.

- Beyond the standard reports, they can include forecasts that try to [predict future financial periods](imagination.md).

Most [managerial](mgmt-1_why.md) accounting involves creating specialized reports to fit the needs of the people who influence a large company.

- To create the reports, most of the data on graphs is smoothed out to show lines that indicate [a trend](trends.md) instead of jagged points.

Some financial statements are required by the Securities and Exchange Commission (SEC) to more clearly clarify equity-based information for owners:

- Proxy Statements help shareholders make informed decisions about matters that will be addressed at a stockholder meeting.
- Prospectus provide details about an investment's offering (i.e., stocks, bonds, mutual funds) to the public.
- A Confirmation indicates a legally affirmed indication of a completed [trade](people-6_contracts.md).

Even when a company is liquidated or merged into another company, the financials must still reflect those periods of time and what happened.

## Endless details

Beyond the above, accounting is a world of endless details.

- More than anything else, accounting looks at each small thing from the bottom-up.
- Unless someone is on [the autism spectrum](https://books2read.com/autism/), they're *not* qualified to work well as an accountant.

This is by no means exhaustive, but is thorough enough to cover important components.

Assets and liabilities can be classified as short-term or long-term.

- Short-term is expected to have use for less than 12 months (e.g., supplies, short-term loan).
- Long-term is expected to last longer than 12 months (e.g., autos, mortgage).

Many accounts are kept at zero (zero-based):

- All equity accounts are zero at the beginning of the period, and must become zero again at the end.
- Beyond the accounts that show on financials, accountants typically create suspense accounts, which are intermediate-stage holding containers for complex accounting procedures.

Throughout the record keeping, accountants often plug small numbers to correct rounding errors.

- While some accountants can become insanely petty over a $0.01 discrepancy, it's often caused by a typographical error.

[Finding errors](https://adequate.life/fix/) is a *massive* part of the labor that goes into accounting:

- Errors of omission mean it wasn't entered at all.
- Entry reversal swaps a credit entry with a debit.
- Transposition errors swap digits inside numbers (meaning the discrepant amount can be divided by 9).
- Rounding errors adapt the number to an approximate value, and can create a snowball effect later (e.g., 2.9 becomes 3).
  - The [two-based number system](math-cs.md) of computers means computer-based accounting is *always* at risk of rounding errors.
- Errors of commission mean it was entered correctly to the correct account, but the value is wrong (e.g., applied payment to the wrong invoice).
- Error of principle (aka "input error") means it doesn't conform to GAAP.

There are some ways to make error-searching easier:

- If the discrepant amount is divisible by 9, two numbers were probably transposed.
- If the discrepant amount is divisible by 2, the erroneous number probably had an extra digit.
- If the discrepant amount is divisible by 10, a decimal may have been misplaced.
- When the error matches a common transaction amount, it may have been entered twice or omitted.

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

1. Before it happens, the [contract](people-6_contracts.md) should *clearly* indicate late fees and the consequences for what should happen.
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

[Continued](money-accounting-2.md)
