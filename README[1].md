# SAP ERP Blueprint — NovaTrade Industries Pvt. Ltd.

> **KIIT University | SAP ERP Curriculum | Project Submission | 2024–25**

A comprehensive SAP ERP enterprise structure blueprint and customization guide for a fictitious Indian mid-size company — **NovaTrade Industries Pvt. Ltd.** — covering three core SAP functional modules: **FI (Financial Accounting)**, **MM (Materials Management)**, and **SD (Sales & Distribution)**.

---

## About This Project

This project simulates a real-world SAP implementation engagement. It was prepared as part of the SAP ERP curriculum at KIIT University and follows the standard SAP ASAP/Activate implementation methodology.

**Company:** NovaTrade Industries Pvt. Ltd. (fictitious)  
**Industry:** Consumer Electronics & FMCG  
**Headquarters:** New Delhi, India  
**SAP Client:** 100 | **Company Code:** NT01  

---

## Repository Structure

```
sap-erp-blueprint-novatrade/
│
├── README.md                          ← You are here
│
├── docs/
│   ├── SAP_Blueprint_NovaTrade_KIIT.docx   ← Full project report (Word)
│   ├── enterprise_structure.md             ← Org unit definitions (FI, MM, SD)
│   └── customization_steps.md             ← Step-by-step SPRO config guide
│
├── diagrams/
│   ├── org_chart.svg                  ← Enterprise structure hierarchy
│   ├── p2p_flow.svg                   ← Procure-to-Pay process flow
│   ├── o2c_flow.svg                   ← Order-to-Cash process flow
│   └── fi_integration.svg             ← FI-MM-SD cross-module integration
│
├── config-scripts/
│   ├── fi_customization.md            ← FI module SPRO steps
│   ├── mm_customization.md            ← MM module SPRO steps
│   ├── sd_customization.md            ← SD module SPRO steps
│   └── tcode_reference.md             ← Full T-code quick reference
│
└── assets/
    └── (supporting images, screenshots)
```

---

## Modules Covered

| Module | Full Name | Key Org Units |
|--------|-----------|---------------|
| **FI** | Financial Accounting | Company Code NT01, Chart of Accounts NTIN, Fiscal Year Variant V3 |
| **MM** | Materials Management | Plants NT10/NT20, Purchasing Org PO01, Storage Locations SL01–SL03 |
| **SD** | Sales & Distribution | Sales Org SO01, Distribution Channels DC01/DC02, Divisions DV01/DV02 |

---

## Key Process Flows

### Procure-to-Pay (P2P) — SAP MM
`PR (ME51N)` → `RFQ (ME41)` → `PO (ME21N)` → `GR (MIGO)` → `Invoice (MIRO)` → `Payment (F110)`

### Order-to-Cash (O2C) — SAP SD
`Inquiry (VA11)` → `Quotation (VA21)` → `Order (VA01)` → `Delivery (VL01N)` → `PGI (VL02N)` → `Billing (VF01)` → `Payment (F-28)`

---

## Cross-Module Integration

| Event | Source | Auto-Posting in FI |
|-------|--------|--------------------|
| Goods Receipt | MM | Dr. Inventory / Cr. GR/IR Clearing |
| Invoice Verification | MM | Dr. GR/IR / Cr. Vendor Payable |
| Post Goods Issue | SD | Dr. COGS / Cr. Finished Goods |
| Customer Billing | SD | Dr. Accounts Receivable / Cr. Revenue |

---

## Diagrams

### Enterprise Structure
![Enterprise Structure](diagrams/org_chart.svg)

### Procure-to-Pay Flow
![P2P Flow](diagrams/p2p_flow.svg)

### Order-to-Cash Flow
![O2C Flow](diagrams/o2c_flow.svg)

### FI-MM-SD Integration
![FI Integration](diagrams/fi_integration.svg)

---

## How to Use This Repository

1. Read the **full project report** in `docs/SAP_Blueprint_NovaTrade_KIIT.docx`
2. Browse the **customization steps** in `config-scripts/` for each module
3. Refer to `config-scripts/tcode_reference.md` for a quick T-code lookup
4. All process flow diagrams are in `diagrams/` as SVG (scalable, zoomable)

---

## Technologies & Tools

- **SAP ERP** — FI, MM, SD modules (SPRO / IMG configuration)
- **SAP ASAP Methodology** — Blueprint phase documentation
- **Microsoft Word** — Project report generation
- **SVG** — Process flow and architecture diagrams

---

## Submission Details

| Field | Value |
|-------|-------|
| Institution | KIIT University, Bhubaneswar |
| Course | SAP ERP Fundamentals |
| Submission Type | Option A — Full Company Blueprint |
| Academic Year | 2024–25 |

---

*This is an academic project. NovaTrade Industries Pvt. Ltd. is a fictitious company created solely for educational purposes.*
