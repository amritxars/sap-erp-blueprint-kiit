# SAP Transaction Code (T-Code) Quick Reference
## NovaTrade Industries Pvt. Ltd.

---

## Configuration T-Codes (SPRO / IMG)

### FI — Financial Accounting

| T-Code | Description | Phase |
|--------|-------------|-------|
| SPRO | SAP Project Reference Object (IMG entry point) | Config |
| OX15 | Define Company | Config |
| OX02 | Create Company Code | Config |
| OX16 | Assign Company Code to Company | Config |
| OB13 | Create Chart of Accounts | Config |
| OBD4 | Define Account Groups | Config |
| OB62 | Assign Chart of Accounts to Company Code | Config |
| OB29 | Define Fiscal Year Variant | Config |
| OB37 | Assign Fiscal Year Variant to Company Code | Config |
| OBBO | Create Posting Period Variant | Config |
| OBBP | Assign Posting Period Variant to Company Code | Config |
| OBA7 | Define Document Types | Config |
| FBN1 | Define Number Ranges for Documents | Config |
| OBA4 | Define Tolerance Groups for Employees | Config |
| OBA3 | Define Tolerance Groups for Customers/Vendors | Config |
| FTXP | Define Tax Codes (GST) | Config |

### MM — Materials Management

| T-Code | Description | Phase |
|--------|-------------|-------|
| OX10 | Define Plant | Config |
| OX18 | Assign Plant to Company Code | Config |
| OX09 | Define Storage Location | Config |
| OX08 | Define Purchasing Organization | Config |
| OX01 | Assign Purchasing Org to Company Code | Config |
| OX17 | Assign Purchasing Org to Plant | Config |
| OME4 | Define Purchasing Groups | Config |
| OMS2 | Configure Material Types | Config |
| MMNR | Define Number Ranges for Materials | Config |
| OMWM | Set Valuation Level | Config |
| OMSK | Define Valuation Classes | Config |
| OBYC | Configure Automatic Account Determination | Config |
| OMH6 | Define PO Document Types | Config |
| OMH7 | Define Number Ranges for POs | Config |

### SD — Sales & Distribution

| T-Code | Description | Phase |
|--------|-------------|-------|
| OVX5 | Define Sales Organization | Config |
| OVX3 | Assign Sales Org to Company Code | Config |
| OVXI | Define Distribution Channel | Config |
| OVXB | Define Division | Config |
| OVXK | Assign Distribution Channel to Sales Org | Config |
| OVXA | Assign Division to Sales Org | Config |
| OVXG | Define Sales Area | Config |
| VOFA | Define Billing Types | Config |
| OVLK | Define Delivery Types | Config |
| V/08 | Define Pricing Procedure | Config |
| VKOA | Revenue Account Determination | Config |

---

## Business Transaction T-Codes

### MM Transactions

| T-Code | Description |
|--------|-------------|
| ME51N | Create Purchase Requisition |
| ME52N | Change Purchase Requisition |
| ME53N | Display Purchase Requisition |
| ME41 | Create Request for Quotation (RFQ) |
| ME47 | Maintain Quotation |
| ME49 | Compare Price Quotations |
| ME21N | Create Purchase Order |
| ME22N | Change Purchase Order |
| ME23N | Display Purchase Order |
| ME29N | Release (Approve) Purchase Order |
| MIGO | Goods Movement (GR/GI/Transfer Posting) |
| MIRO | Logistics Invoice Verification |
| MMBE | Stock Overview |
| MB52 | Warehouse Stocks of Material |
| MB5S | Display GR/IR Balances |
| ME2M | Purchase Orders by Material |
| ME2N | Purchase Orders by PO Number |

### FI Transactions

| T-Code | Description |
|--------|-------------|
| F-02 | Enter General Ledger Posting |
| FB50 | Enter G/L Account Document |
| F-43 | Enter Vendor Invoice |
| F-53 | Post Vendor Payment |
| F110 | Automatic Payment Run |
| F-28 | Post Incoming Payment |
| F-32 | Clear Customer Open Items |
| FB03 | Display Document |
| FBL1N | Vendor Line Items Report |
| FBL5N | Customer Line Items Report |
| FBL3N | G/L Account Line Items |
| FS10N | G/L Account Balance Display |
| S_ALR_87012291 | G/L Account Balances |
| S_ALR_87012085 | Accounts Payable Aging |
| S_ALR_87012168 | Accounts Receivable Aging |
| S_ALR_87012284 | Financial Statements (P&L / Balance Sheet) |

### SD Transactions

| T-Code | Description |
|--------|-------------|
| VA11 | Create Sales Inquiry |
| VA21 | Create Sales Quotation |
| VA01 | Create Sales Order |
| VA02 | Change Sales Order |
| VA03 | Display Sales Order |
| VA05 | List of Sales Orders |
| VL01N | Create Outbound Delivery |
| VL02N | Change Outbound Delivery (incl. PGI) |
| VF01 | Create Billing Document |
| VF02 | Change Billing Document |
| VF03 | Display Billing Document |
| VF05 | List of Billing Documents |
| VT01N | Create Shipment |
| S_ALR_87012186 | Customer Sales Analysis |
