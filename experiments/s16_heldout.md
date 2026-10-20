# Session 16: held-out results for the support classifier

Model: `openai/gpt-oss-20b` · Date: 2026-10-20 · system.md `f598984f` · user.j2 `4a1a846a` · examples per label: 2

Held-out accuracy (structured): 0/20 = 0%
Baseline accuracy (one-line instruction): 15/20 = 75%

| # | Ticket | Expected | Structured | Baseline |
|---|---|---|---|---|
| H01 | My credit card statement shows a purchase in another country while I h | card | None WRONG | card ok |
| H02 | The chip on my debit card stopped working at the petrol pump. | card | None WRONG | card ok |
| H03 | Please block my card, my wallet was stolen yesterday. | card | None WRONG | card ok |
| H04 | I was charged an extra 2% on my card for a fuel purchase. | card | None WRONG | card ok |
| H05 | The reward points on my credit card were not added for last month's sp | card | None WRONG | card ok |
| H06 | The EMI of my personal loan was deducted twice in March. | loan | None WRONG | loan ok |
| H07 | I need a no-dues certificate now that my vehicle loan is closed. | loan | None WRONG | loan ok |
| H08 | My home loan statement shows an interest figure that does not match th | loan | None WRONG | loan ok |
| H09 | The bank has not released the second instalment of my construction loa | loan | None WRONG | loan ok |
| H10 | Please tell me how much I must pay to close my personal loan today. | loan | None WRONG | loan ok |
| H11 | A UPI collect request of Rs 3,000 was approved by mistake and I want i | account | None WRONG | other WRONG |
| H12 | My net banking transfer to another bank shows success but the receiver | account | None WRONG | account ok |
| H13 | The cheque I deposited five days ago has still not been cleared. | account | None WRONG | account ok |
| H14 | My account balance dropped by Rs 590 and I cannot find any transaction | account | None WRONG | account ok |
| H15 | My UPI payment to the electricity board failed and my account was debi | account | None WRONG | account ok |
| H16 | Please correct the spelling of my name on my account. | other | account WRONG | account WRONG |
| H17 | How do I give feedback about the long queue at your Kukatpally branch? | other | None WRONG | other ok |
| H18 | I need to update the nominee on my home loan. | other | None WRONG | loan WRONG |
| H19 | Please change the mobile number linked to my credit card. | other | None WRONG | card WRONG |
| H20 | What documents do I need to open a fixed deposit? | other | None WRONG | account WRONG |

Mistakes of the structured version, and what I changed because of them:

- expected `card`, got `None`: My credit card statement shows a purchase in another country while I have been a
- expected `card`, got `None`: The chip on my debit card stopped working at the petrol pump.
- expected `card`, got `None`: Please block my card, my wallet was stolen yesterday.
- expected `card`, got `None`: I was charged an extra 2% on my card for a fuel purchase.
- expected `card`, got `None`: The reward points on my credit card were not added for last month's spends.
- expected `loan`, got `None`: The EMI of my personal loan was deducted twice in March.
- expected `loan`, got `None`: I need a no-dues certificate now that my vehicle loan is closed.
- expected `loan`, got `None`: My home loan statement shows an interest figure that does not match the rate let
- expected `loan`, got `None`: The bank has not released the second instalment of my construction loan.
- expected `loan`, got `None`: Please tell me how much I must pay to close my personal loan today.
- expected `account`, got `None`: A UPI collect request of Rs 3,000 was approved by mistake and I want it reversed
- expected `account`, got `None`: My net banking transfer to another bank shows success but the receiver has not g
- expected `account`, got `None`: The cheque I deposited five days ago has still not been cleared.
- expected `account`, got `None`: My account balance dropped by Rs 590 and I cannot find any transaction for it.
- expected `account`, got `None`: My UPI payment to the electricity board failed and my account was debited.
- expected `other`, got `account`: Please correct the spelling of my name on my account.
- expected `other`, got `None`: How do I give feedback about the long queue at your Kukatpally branch?
- expected `other`, got `None`: I need to update the nominee on my home loan.
- expected `other`, got `None`: Please change the mobile number linked to my credit card.
- expected `other`, got `None`: What documents do I need to open a fixed deposit?
