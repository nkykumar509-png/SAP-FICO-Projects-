## 🧾 Business Scenario – Statistical Internal Order for Telephone Expenses

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


## 🎯 Objective

| Goal | Result |
|------|--------|
| Track Telephone expenses individually | Better cost visibility & decision making |
| Use Statistical Internal Order | Order used only for reporting, actual posting to cost center |
| Analyze posting reports | View transactions via KOB1 & Order report |
| Support management budgeting | Compare planned vs actual cost |****

## 🧾 SAP Posting Flow

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

