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
