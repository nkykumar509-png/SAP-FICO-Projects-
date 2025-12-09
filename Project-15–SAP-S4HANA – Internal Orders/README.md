Statistical Internal Order for Telephone Expenses

Business Scenario 

In an organization, certain overhead expenses such as telephone bills, electricity bills, office maintenance etc., must be monitored and controlled effectively.
To track such indirect expenses, SAP S/4HANA provides Statistical Internal Orders.

In this project, the company Musashi Auto Pvt. Ltd. (MUPL) wants to track Telephone Expenses separately for analysis purposes.
Although the internal order is used for reporting, the actual cost should still post to the cost center, meaning the internal order must be statistical (not real order).

| Business Requirement | Description |
|----------------------|-------------|
| Purpose | Track overhead expenses like telephone bills separately |
| Company Name | Musashi Auto Pvt. Ltd. (MUPL) |
| Expense Tracked | Telephone Expenses |
| Internal Order Type | Statistical |
| Internal Order No. | 1000540 |
| Cost Center | MU2001 |
| Primary Cost Element | 400607 – Telephone Expense |
| Posting Method | FI Posting (F-02) |
| Expected Reporting | KOB1 / S_ALR_87013019 |

##  Business Example

| Document No. | G/L Account | Description | Amount | Cost Center | Order | Posting Method |
|--------------|-------------|-------------|--------|-------------|--------|----------------|
| 1019 | 400607 | Telephone Expenses | 100,000 INR | MU2001 | 1000540 | F-02 (Debit) |
| 1019 | 200101 | HDFC Bank A/c | 100,000 INR | — | — | F-02 (Credit) |

Objective
Result

Track Telephone expenses individually	Better cost visibility & decision making
Use Statistical Internal Order	Order only for reporting, cost center receives actual cost
Analyze posting report	View expenses in KOB1 and Cost order report
Support management budgeting	Helps compare planned vs actual cost later

##  SAP Posting Flow

| Step | Activity | T-Code |
|-------|----------|---------|
| 01 | Define Internal Order Type (Statistical) | KOT2_OPA |
| 02 | Maintain Number Range for Order | KANK |
| 03 | Create Statistical Internal Order | KO01 |
| 04 | Display Internal Order | KO03 |
| 05 | Create Primary Cost Element (Telephone Expense) | FS00 / KA01 |
| 06 | Post Telephone Expense to Internal Order | F-02 |
| 07 | Display Actual Cost Line Items | KOB1 |
| 08 | Display Cost Center / Order Report | S_ALR_87013019 |
| 09 | Try Settlement (System Message – Cannot settle statistical order) | KO88 |
## 📊 Expected Output

| Result | Status |
|--------|--------|
| Telephone expense posted successfully | ✔ |
| Internal Order is Statistical (No Settlement Allowed) | ✔ |
| Cost visible in Cost Center MU2001 | ✔ |
| Posting shown in Order Report KOB1 | ✔ |
| Variance & reporting available | ✔ |

## 📂 Screenshot References – Statistical Internal Order (Telephone Expenses)

### 🧾 FS00 – Create Telephone Expense G/L
**T-Code:** FS00  
![FS00_Create_Telephone_Expenses](./screenshots/FS00_Create_Telephone_Expenses.png.jpeg)

---

### 🧾 KOT2 – Create Internal Order Type (Statistical Order)
**T-Code:** KOT2_OPA  
![KOT2_Create_Order_Type](./screenshots/KOT2_Create_Order_Type.png.jpeg)

---

### 🧾 KO01 – Create Statistical Internal Order
**T-Code:** KO01  
![KO01_Create_Statistical_Order](./screenshots/KO01_Create_Statistical_Order.png.jpeg)

---

### 🧾 KO03 – Display Internal Order
**T-Code:** KO03  
![KO03_Display_Internal_Order](./screenshots/KO03_Display_Internal_Order.png.jpeg)

---

### 🧾 KO02 – Change Internal Order (Control / Edit Master)
**T-Code:** KO02  
![KO02_Change_Internal_Order](./screenshots/KO02_Change_Internal_Order.png.jpeg)

---

### 🧾 FB60 – Vendor Invoice Posting for Telephone Expense
**T-Code:** FB60  
![FB60_Post_Telephone_Invoice](./screenshots/FB60_Post_Telephone_Invoice.png.jpeg)

---

### 🧾 FB60 – Display Document / Invoice Overview
**T-Code:** FB03 / FB60 Document Overview  
![FB60_Display_Invoice](./screenshots/FB60_Display_Invoice.png.jpeg)

---

### 🧾 KOB1 – Display Actual Cost Document Line Items
**T-Code:** KOB1  
![KOB1_Display_Cost_Line_Items](./screenshots/KOB1_Display_Cost_Line_Items.png.jpeg)

---

### 🧾 S_ALR_87013019 – Internal Order Cost Report
**T-Code:** S_ALR_87013019  
![S_ALR_87013019_Cost_Order_Report](./screenshots/S_ALR_87013019_Cost_Order_Report.png.jpeg)
