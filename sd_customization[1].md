# SD Customization Steps — NovaTrade Industries Pvt. Ltd.

> SPRO Path: Sales and Distribution > Basic Functions / Sales / Shipping / Billing

---

## Step 1: Sales Organization

```
T-Code: OVX5 → Create Sales Organization SO01
T-Code: OVX3 → Assign SO01 to Company Code NT01
```

- Sales Org Name: NovaTrade India Sales
- Currency: INR
- Statistics Currency: INR

---

## Step 2: Distribution Channels and Divisions

```
T-Code: OVXI → Create Distribution Channels
T-Code: OVXB → Create Divisions
T-Code: OVXK → Assign Distribution Channel to Sales Org
T-Code: OVXA → Assign Division to Sales Org
T-Code: OVXG → Define Sales Areas
```

| Channel | Name |
|---------|------|
| DC01 | Wholesale |
| DC02 | Retail |

| Division | Name |
|----------|------|
| DV01 | Electronics |
| DV02 | FMCG |

**Sales Areas:**
- SO01 / DC01 / DV01 → Electronics Wholesale
- SO01 / DC02 / DV02 → FMCG Retail

---

## Step 3: Sales Document Types

```
T-Code: VOV8 → Define Sales Document Types
```

| Type | Name | Usage |
|------|------|-------|
| OR | Standard Order | Regular B2B and B2C orders |
| RO | Rush Order | Same-day delivery requirement |
| RE | Returns | Customer return processing |
| CR | Credit Memo Request | Price adjustment in customer's favour |
| DR | Debit Memo Request | Price adjustment in company's favour |

---

## Step 4: Pricing Procedure

```
T-Code: V/06 → Define Condition Types
T-Code: V/08 → Define Pricing Procedure NTPRC
T-Code: OVKK → Assign Pricing Procedure to Sales Area
```

**Pricing Procedure NTPRC Condition Types:**

| Step | Cond Type | Name | Calc Type |
|------|-----------|------|-----------|
| 10 | PR00 | Base Price | Fixed amount |
| 20 | K007 | Customer Discount | Percentage |
| 30 | K005 | Material Discount | Percentage |
| 80 | MWST | Output Tax (GST) | Tax code |
| 90 | SKTO | Cash Discount | Percentage |

---

## Step 5: Shipping Configuration

```
T-Code: OVLK → Define Delivery Types
T-Code: OVZG → Define Shipping Points
T-Code: OVZB → Assign Shipping Point to Plant
```

| Delivery Type | Name |
|---------------|------|
| LF | Outbound Delivery |
| LR | Returns Delivery |

**Shipping Points:**
- SP01 → New Delhi Dispatch Hub → assigned to Plant NT10

**Routes:**
- RT01 → Standard Road (North India) → default transit time: 2 days

---

## Step 6: Billing

```
T-Code: VOFA → Define Billing Types
T-Code: VKOA → Revenue Account Determination
```

| Billing Type | Name |
|--------------|------|
| F2 | Invoice |
| RE | Credit Memo |
| RD | Debit Memo |
| S1 | Cancellation Invoice |

**Revenue Account Determination (VKOA):**
- Sales Revenue → GL Account 300010
- Sales Deductions → GL Account 300020
- Output Tax → GL Account 600020
