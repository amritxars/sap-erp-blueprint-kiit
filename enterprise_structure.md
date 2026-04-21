# Enterprise Structure — NovaTrade Industries Pvt. Ltd.

## SAP Client and Company Code

| Parameter | Value |
|-----------|-------|
| Client | 100 |
| Company Code | NT01 |
| Company Name | NovaTrade Industries Pvt. Ltd. |
| Country | India |
| Currency | INR |
| Language | EN |

---

## FI Organizational Units

| Unit | ID | Description |
|------|----|-------------|
| Chart of Accounts | NTIN | NovaTrade India — 6-digit account structure |
| Fiscal Year Variant | V3 | April 1 to March 31 (12 periods + 4 special) |
| Posting Period Variant | NT01 | Controls open/close periods for NT01 |
| Field Status Variant | NT01 | Controls mandatory/optional fields per GL account |
| Credit Control Area | NT01 | Customer credit monitoring |
| Currency | INR | Indian Rupee |

---

## MM Organizational Units

| Unit | ID | Description |
|------|----|-------------|
| Plant | NT10 | New Delhi — Distribution Hub |
| Plant | NT20 | Noida — Manufacturing Plant |
| Storage Location | SL01 | Raw Material Store (under NT20) |
| Storage Location | SL02 | Finished Goods Warehouse (under NT10) |
| Storage Location | SL03 | Spare Parts & Consumables (under NT10) |
| Purchasing Organization | PO01 | Central Purchasing — covers NT10 and NT20 |
| Purchasing Group | PG01 | Electronics Procurement Team |
| Purchasing Group | PG02 | FMCG Raw Material Procurement Team |
| Valuation Area | Plant level | Valuation at plant level (Moving Average Price) |

---

## SD Organizational Units

| Unit | ID | Description |
|------|----|-------------|
| Sales Organization | SO01 | India Domestic Sales |
| Distribution Channel | DC01 | Wholesale — B2B dealer network |
| Distribution Channel | DC02 | Retail — Direct-to-consumer / e-commerce |
| Division | DV01 | Electronics Division |
| Division | DV02 | FMCG Division |
| Sales Area | SO01/DC01/DV01 | Electronics Wholesale |
| Sales Area | SO01/DC02/DV02 | FMCG Retail |
| Shipping Point | SP01 | New Delhi Dispatch Hub |
| Sales District | SD-NORTH | North India Territory |

---

## Organizational Assignments

```
Client 100
└── Company Code: NT01 (NovaTrade Industries Pvt. Ltd.)
    ├── Chart of Accounts: NTIN
    ├── Fiscal Year Variant: V3
    ├── Plant: NT10 (New Delhi)
    │   ├── Storage Location: SL02 (Finished Goods)
    │   ├── Storage Location: SL03 (Spare Parts)
    │   └── Shipping Point: SP01
    ├── Plant: NT20 (Noida)
    │   └── Storage Location: SL01 (Raw Materials)
    ├── Purchasing Organization: PO01
    │   ├── Purchasing Group: PG01
    │   └── Purchasing Group: PG02
    └── Sales Organization: SO01
        ├── Distribution Channel: DC01 (Wholesale)
        ├── Distribution Channel: DC02 (Retail)
        ├── Division: DV01 (Electronics)
        └── Division: DV02 (FMCG)
```
