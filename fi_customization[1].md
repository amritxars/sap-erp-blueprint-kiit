# FI Customization Steps — NovaTrade Industries Pvt. Ltd.

> SPRO Path: Financial Accounting > Financial Accounting Global Settings

---

## Step 1: Define Company and Company Code

```
T-Code: OX15 → Define Company
T-Code: OX02 → Create Company Code NT01
T-Code: OX16 → Assign Company Code to Company
```

**Settings for NT01:**
- Company Name: NovaTrade Industries Pvt. Ltd.
- Country: IN (India)
- Currency: INR
- Language: EN
- Address: Connaught Place, New Delhi – 110001

---

## Step 2: Chart of Accounts

```
T-Code: OB13 → Create Chart of Accounts NTIN
T-Code: OBD4 → Define Account Groups
T-Code: OB62 → Assign CoA to Company Code NT01
```

**Account Groups:**
| Group ID | Name | Range |
|----------|------|-------|
| ASSET | Assets | 100000–199999 |
| LIAB | Liabilities | 200000–299999 |
| REV | Revenue | 300000–399999 |
| COGS | Cost of Sales | 400000–499999 |
| OPEX | Operating Expenses | 500000–599999 |
| TAX | Tax Accounts | 600000–699999 |

**Retained Earnings Account:** 290000

---

## Step 3: Fiscal Year Variant

```
T-Code: OB29 → Create Fiscal Year Variant V3
T-Code: OB37 → Assign V3 to Company Code NT01
```

- 12 normal posting periods (April = Period 1, March = Period 12)
- 4 special periods (13–16) for year-end adjustments

---

## Step 4: Posting Period Variant

```
T-Code: OBBO → Create Posting Period Variant NT01
T-Code: OBBP → Assign to Company Code NT01
```

- Open all 12 periods at year start
- Close periods month-by-month after reconciliation
- Keep period 13–16 closed except during year-end close

---

## Step 5: Document Types and Number Ranges

```
T-Code: OBA7 → Define Document Types
T-Code: FBN1 → Define Number Ranges
```

| Doc Type | Name | Number Range |
|----------|------|--------------|
| SA | G/L Account Document | 0100000000–0199999999 |
| KR | Vendor Invoice | 0200000000–0299999999 |
| KZ | Vendor Payment | 0300000000–0399999999 |
| DR | Customer Invoice | 0400000000–0499999999 |
| DZ | Customer Payment | 0500000000–0599999999 |
| AB | Accounting Document | 0600000000–0699999999 |

---

## Step 6: Tolerance Groups

```
T-Code: OBA4 → Employee Tolerance Groups
T-Code: OBA3 → Customer/Vendor Tolerance Groups
```

- Max payment difference: INR 500
- Max cash discount per line: INR 1,000

---

## Step 7: GST Tax Configuration

```
T-Code: FTXP → Define Tax Codes
```

| Code | Description | Rate |
|------|-------------|------|
| I1 | Input GST 18% | 18% |
| I0 | Input GST 0% | 0% |
| O1 | Output GST 18% | 18% |
| O0 | Output GST 0% | 0% |
| I5 | Input GST 5% | 5% |
| O5 | Output GST 5% | 5% |

**GL Account Assignments:**
- Input GST: 600010
- Output GST: 600020
- GST Payable (net): 600030
