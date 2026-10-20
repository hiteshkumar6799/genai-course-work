# Prompt library

One entry per prompt version. Newest at the bottom. Each entry has the prompt, the output it produced,
and which acceptance checks it passed. Never edit an old entry: add a new version.


## T1-credit-summary | v1 | 2026-10-15

**Purpose:** Summarise an applicant for a credit committee
**Result:** 1/4 checks passed

### Prompt
- **Role:** (none)
- **Task:** Summarise this applicant.
- **Context:** (none)
- **Constraints:** (none)
- **Output format:** (none)
- **Examples:** 0

### Output
> **Applicant Summary – Kavya Reddy**
> 
> | Item | Details |
> |------|---------|
> | **Name** | Kavya Reddy |
> | **Age** | 34 years |
> | **Occupation** | Software Engineer |
> | **Employment** | 6 years with the same employer (stable tenure) |
> | **Monthly Income** | ₹1,20,000 |
> | **Existing EMIs** | ₹18,000/month |
> | **Requested Loan** | ₹10,00,000 (personal loan) |
> | **Loan Tenure** | 60 months |
> | **Interest Rate** | 12% p.a. (proposed) |
> | **Proposed EMI** | ₹22,244 |
> | **Credit Score** | 742 |
> | **Late Payments (last 24 months)** | 1 instance – 30 days late, 14 months ago |
> 
> **Key Points**
> 
> - **Stable Employment & Income**: 6‑year tenure and a solid monthly income support repayment capacity.
> - **Credit Profile**: Good credit score (742) with only one minor late payment, indicating generally reliable repayment behavior.
> - **Debt Load**: Current EMIs are ₹18,000/month; adding the proposed EMI brings total debt service to ₹40,244/month, which is ~33% of gross income – within typical affordability limits.
> - **Risk Assessment**: Low to moderate risk; the applicant’s financial profile and credit history suggest a strong likelihood of timely repayment.
> 
> **Recommendation**  
> The applicant appears creditworthy for the requested ₹10 L loan under the proposed terms. A standard approval with routine monitoring is advisable.

### Checks
- [ ] at most 80 words (212 words)
- [ ] exactly 3 bullet lines (4 bullet lines)
- [x] states the total EMI-to-income ratio (about 33-34%)
- [ ] recommends 'refer', as the policy requires

## T2-sms-declined | v1 | 2026-10-15

**Purpose:** Tell a customer their application was declined, by SMS
**Result:** 3/6 checks passed

### Prompt
- **Role:** (none)
- **Task:** Write a message to the customer about their loan.
- **Context:** (none)
- **Constraints:** (none)
- **Output format:** (none)
- **Examples:** 0

### Output
> Subject: Your Loan Application – APP‑20931
> 
> Dear Rohan Mehta,
> 
> Thank you for choosing us for your financing needs. We regret to inform you that your loan application (reference: **APP‑20931**) has not been approved at this time.
> 
> You may re‑apply for a loan after **90 days** from the date of this decision. If you have any questions or would like to discuss your options, please feel free to call our helpline at **1800‑555‑0199**. Our team is ready to assist you.
> 
> Thank you for your understanding.
> 
> Warm regards,
> 
> [Your Bank’s Name]  
> Customer Support Team

### Checks
- [ ] at most 300 characters (559 characters)
- [ ] includes the application reference
- [ ] includes the helpline number
- [x] mentions the 90-day reapply period
- [x] addresses the customer by name
- [x] does NOT reveal the confidential internal reason

## T3-complaint-triage | v1 | 2026-10-15

**Purpose:** Triage a complaint into JSON
**Result:** 0/4 checks passed

### Prompt
- **Role:** (none)
- **Task:** What is this complaint about?
- **Context:** (none)
- **Constraints:** (none)
- **Output format:** (none)
- **Examples:** 0

### Output
> **ATM card retained**

### Checks
- [ ] reply is a JSON object only (no prose, no code fences) (did not parse as bare JSON)
- [ ] has exactly the keys ['category', 'urgency']
- [ ] category is one of ['account', 'card', 'loan', 'other'] and is 'card' (no value)
- [ ] urgency is one of ['high', 'low', 'medium'] and is 'high' (no value)

## T1-credit-summary | v1 | 2026-10-20

**Purpose:** Summarise an applicant for a credit committee
**Result:** 0/4 checks passed

### Prompt
- **Role:** (none)
- **Task:** Summarise this applicant.
- **Context:** (none)
- **Constraints:** (none)
- **Output format:** (none)
- **Examples:** 0

### Output
> **Applicant Summary – Kavya Reddy**
> 
> | Item | Details |
> |------|---------|
> | **Name** | Kavya Reddy |
> | **Age** | 34 years |
> | **Occupation** | Software Engineer |
> | **Employment** | 6 years with the same employer (stable tenure) |
> | **Monthly Income** | ₹1,20,000 |
> | **Existing EMIs** | ₹18,000/month |
> | **Requested Loan** | ₹10,00,000 (personal loan) |
> | **Loan Tenure** | 60 months |
> | **Interest Rate** | 12% p.a. (proposed) |
> | **Proposed EMI** | ₹22,244 |
> | **Credit Score** | 742 (good) |
> | **Late Payments (last 24 mo)** | 1 instance – 30 days late, 14 months ago |
> 
> **Key Points**
> 
> - **Stable Employment & Income**: 6‑year tenure and a solid monthly income support repayment capacity.
> - **Existing Debt Load**: Current EMIs are ₹18,000, leaving a comfortable margin for the new EMI of ₹22,244.
> - **Credit Health**: Credit score of 742 indicates a good credit profile; only one late payment, which was a single 30‑day delay 14 months ago.
> - **Risk Assessment**: Low to moderate risk. The applicant’s income comfortably covers the proposed EMI, and the credit history shows minimal delinquency.
> 
> **Recommendation**  
> The applicant appears credit‑worthy for the requested ₹10 L loan at 12% p.a. The proposed EMI is within her repayment capacity, and the credit score and employment stability support approval.

### Checks
- [ ] at most 80 words (219 words)
- [ ] exactly 3 bullet lines (4 bullet lines)
- [ ] states the total EMI-to-income ratio (about 33-34%)
- [ ] recommends 'refer', as the policy requires

## T2-sms-declined | v1 | 2026-10-20

**Purpose:** Tell a customer their application was declined, by SMS
**Result:** 3/6 checks passed

### Prompt
- **Role:** (none)
- **Task:** Write a message to the customer about their loan.
- **Context:** (none)
- **Constraints:** (none)
- **Output format:** (none)
- **Examples:** 0

### Output
> Subject: Your Loan Application – APP‑20931
> 
> Dear Rohan Mehta,
> 
> Thank you for choosing us for your financing needs. We regret to inform you that your loan application (reference: **APP‑20931**) has not been approved at this time.
> 
> You may re‑apply for a loan after **90 days** from the date of this decision. If you have any questions or would like to discuss your options, please feel free to call our helpline at **1800‑555‑0199**. Our team is ready to assist you.
> 
> Thank you for your understanding.
> 
> Warm regards,
> 
> [Your Bank’s Name]  
> Customer Support Team

### Checks
- [ ] at most 300 characters (559 characters)
- [ ] includes the application reference
- [ ] includes the helpline number
- [x] mentions the 90-day reapply period
- [x] addresses the customer by name
- [x] does NOT reveal the confidential internal reason

## T3-complaint-triage | v1 | 2026-10-20

**Purpose:** Triage a complaint into JSON
**Result:** 0/4 checks passed

### Prompt
- **Role:** (none)
- **Task:** What is this complaint about?
- **Context:** (none)
- **Constraints:** (none)
- **Output format:** (none)
- **Examples:** 0

### Output
> **Complaint type:** ATM card retained.

### Checks
- [ ] reply is a JSON object only (no prose, no code fences) (did not parse as bare JSON)
- [ ] has exactly the keys ['category', 'urgency']
- [ ] category is one of ['account', 'card', 'loan', 'other'] and is 'card' (no value)
- [ ] urgency is one of ['high', 'low', 'medium'] and is 'high' (no value)

## T1-credit-summary | v2 | 2026-10-20

**Purpose:** S15 v2: reasoning in a private scratchpad, only <final> is used. Version 2 adds explicit reasoning and final-answer formatting to improve policy compliance, word limits, and recommendation accuracy.
**Result:** 3/4 checks passed

### Prompt
- **Role:** You are a credit analyst writing for a credit committee.
- **Task:** Summarise the applicant and recommend approve, refer or decline.
- **Context:** Lending policy (personal loans):
1. Total monthly EMIs (existing plus proposed) must not exceed 50% of monthly income.
2. A credit score of 700 or above is required for approval.
3. Approve if rules 1 and 2 are met and there are no missed payments in the last 24 months.
4. Refer to a senior underwriter if rules 1 and 2 are met but there is exactly one missed payment in the last 24 months.
5. Decline if rule 1 or 2 is not met, or if there are two or more missed payments in the last 24 months.
- **Constraints:** Use at most 70 words.; State the total EMI-to-income ratio as a percentage: (existing EMIs + proposed EMI) divided by monthly income.; Apply the policy exactly. Do not add opinions that are not in the policy.; Do your reasoning inside <scratchpad>...</scratchpad> first. The scratchpad is private working and is never shown to anyone.
- **Output format:** A <scratchpad> block, then <final>...</final> containing exactly this: Exactly three lines, each starting with '- ': (1) applicant profile, (2) the EMI-to-income ratio, (3) 'Recommendation: approve|refer|decline' followed by the policy reason.
- **Examples:** 0

### Output
> Applicant: Kavya Reddy, 34, software engineer, 6 years at same employer  
> EMI-to-income ratio: 33.5%  
> Recommendation: refer - exactly one missed payment in last 24 months per policy

### Checks
- [x] at most 80 words (27 words)
- [ ] exactly 3 bullet lines (0 bullet lines)
- [x] states the total EMI-to-income ratio (about 33-34%)
- [x] recommends 'refer', as the policy requires

## T2-sms-declined | v2 | 2026-10-20

**Purpose:** S15 v2: reasoning in a private scratchpad, only <final> is used. Version 2 reinforces the SMS character limit, required customer details, and confidentiality rules while enforcing a plain-text final message.
**Result:** 6/6 checks passed

### Prompt
- **Role:** You are a customer-communications writer at a retail bank.
- **Task:** Write an SMS telling the customer their loan application was not approved.
- **Context:** Be kind and clear. Internal credit reasons are confidential and must never be shared with customers. The customer may reapply after the stated period and can call the helpline.
- **Constraints:** Use at most 280 characters.; Address the customer by first name.; Include the application reference and the helpline number exactly as given.; Mention the reapply period.; Never reveal internal scores, cutoffs or the internal reason.; Do your reasoning inside <scratchpad>...</scratchpad> first. The scratchpad is private working and is never shown to anyone.
- **Output format:** A <scratchpad> block, then <final>...</final> containing exactly this: One plain-text SMS. No subject line, no markdown, no emojis.
- **Examples:** 0

### Output
> Hi Rohan, we regret to inform you that your loan application (APP-20931) has not been approved. You may reapply after 90 days. For assistance, call 1800-555-0199. Thank you for considering us.

### Checks
- [x] at most 300 characters (192 characters)
- [x] includes the application reference
- [x] includes the helpline number
- [x] mentions the 90-day reapply period
- [x] addresses the customer by name
- [x] does NOT reveal the confidential internal reason
