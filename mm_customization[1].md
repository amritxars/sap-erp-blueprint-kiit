# MM Customization Steps — NovaTrade Industries Pvt. Ltd.

> SPRO Path: Materials Management > Purchasing / Inventory Management

---

## Step 1: Define Plants

```
T-Code: OX10 → Create Plants
T-Code: OX18 → Assign Plants to Company Code NT01
```

| Plant | Name | Location |
|-------|------|----------|
| NT10 | NovaTrade Delhi Hub | Connaught Place, New Delhi |
| NT20 | NovaTrade Noida Plant | Sector 63, Noida, UP |

**Settings per plant:**
- Country: IN
- Language: EN
- Time Zone: IST (UTC+5:30)
- Factory Calendar: IN (Indian holidays)

---

## Step 2: Storage Locations

```
T-Code: OX09 → Create Storage Locations
```

| SLoc | Plant | Description |
|------|-------|-------------|
| SL01 | NT20 | Raw Material Store |
| SL02 | NT10 | Finished Goods Warehouse |
| SL03 | NT10 | Spare Parts and Consumables |

---

## Step 3: Purchasing Organization

```
T-Code: OX08 → Create Purchasing Org PO01
T-Code: OX01 → Assign PO01 to Company Code NT01
T-Code: OX17 → Assign PO01 to Plants NT10 and NT20
T-Code: OME4 → Create Purchasing Groups
```

| PGr | Description |
|-----|-------------|
| PG01 | Electronics Procurement |
| PG02 | FMCG Raw Materials Procurement |

---

## Step 4: Material Types

```
T-Code: OMS2 → Configure Material Types
T-Code: MMNR → Define Number Ranges
```

| Type | Name | Qty Update | Value Update | Valuation |
|------|------|-----------|--------------|-----------|
| ROH | Raw Material | Yes | Yes | Moving Avg |
| FERT | Finished Product | Yes | Yes | Standard Price |
| HALB | Semi-finished | Yes | Yes | Moving Avg |
| HAWA | Trading Goods | Yes | Yes | Moving Avg |
| NLAG | Non-valuated | Yes | No | — |

---

## Step 5: Valuation and Account Determination

```
T-Code: OMWM → Set Valuation Level to Plant
T-Code: OMSK → Define Valuation Classes
T-Code: OBYC → Automatic Account Determination
```

**Key Movement Types:**
| MvT | Description | Dr | Cr |
|-----|-------------|----|----|
| 101 | Goods Receipt | Inventory | GR/IR Clearing |
| 102 | GR Reversal | GR/IR Clearing | Inventory |
| 261 | Goods Issue to Production | Consumption | Inventory |
| 601 | Delivery (PGI) | COGS | Finished Goods |

---

## Step 6: Purchase Order Configuration

```
T-Code: OMH6 → Define PO Document Types
T-Code: OMH7 → Define Number Ranges for POs
```

| PO Type | Name | Usage |
|---------|------|-------|
| NB | Standard PO | All standard procurement |
| FO | Framework Order | Long-term vendor contracts |

**Release (Approval) Strategy:**
- POs above INR 5,00,000 require manager approval
- POs above INR 25,00,000 require CFO approval
- Configured via: OMGS, OMGQ, ME29N
