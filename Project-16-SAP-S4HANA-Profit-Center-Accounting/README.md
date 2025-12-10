PROJECT-16 – SAP S/4HANA: PROFIT CENTER ACCOUNTING (PCA)

##  Objective

| Goal                           | Result                                               |
|--------------------------------|------------------------------------------------------|
| Create Profit Center Hierarchy | Organize business units under controlling area MUPL |
| Create Profit Center Groups    | Production, Administration, Service                  |
| Create Profit Centers          | MU1101, MU2201, MU3301 created successfully          |
| Assign Profit Center to Cost Center | MU1001 assigned to MU1101                     |
| Post FI Document with Cost Center | Profit Center picked automatically               |
| Display Profit Center Report   | View plan/actual/variance                            |

##  SAP Configuration & Posting Flow – Profit Center Accounting (PCA)

| Step | Activity                                      | T-Code       | Purpose |
|------|------------------------------------------------|--------------|---------|
| 01   | Maintain Standard Hierarchy for PCA            | KCH1 / KCH2  | Define main hierarchy for controlling area |
| 02   | Define Standard Hierarchy Assignment           | OKEON        | Assign hierarchy to controlling area |
| 03   | Create Profit Center Group                     | KE51         | Create Production / Admin / Service Groups |
| 04   | Create Profit Centers                          | KE51 / KE52  | Maintain PC master data (MU1101, MU2201, etc.) |
| 05   | Assign Profit Center to Cost Center            | KS02         | Make cost center reportable by PCA |
| 06   | Post FI Document with Cost Center              | FB50         | Profit center flows automatically |
| 07   | Display / Change Profit Center                 | KE52         | Edit master data if required |
| 08   | Post Supplier Invoice                          | FB60         | Supplier posting updates Profit Center |
| 09   | Display Profit Center Report                   | S_ALR_87013326 | View PCA actuals / balances |

##  Business Example

| Doc No | G/L      | Description         | Amount       | Cost Center | Profit Center | Posting Type |
|--------|-----------|----------------------|--------------|-------------|----------------|----------------|
| 1022   | 400602    | Stationary Expense   | 100,000 INR  | MU1001      | MU1101         | Debit (FB50)   |
| 1022   | 200101    | HDFC Bank A/c        | 100,000 INR  | —           | —              | Credit (FB50)  |
| Invoice| 400602    | Office Expense       | 10,000 INR   | —           | MU1101         | Debit (FB60)   |

Screenshots

### Define Standard Hierarchy  
**T-Code:** KCH2 / KCH1  
![Define Standard Hierarchy](./screenshots/profit_center/Define_Standard_Hierarchy.png.jpeg)

---

### KE51 – Create Profit Center Group  
**T-Code:** KE51  
![KE51 Create Profit Center Group](./screenshots/profit_center/KE51_Create_Profit_Center_Group.png.jpeg)

---

### KE52 – Create / Change Profit Center  
**T-Code:** KE52 / KE51  
![KE52 Create Profit Center](./screenshots/profit_center/KE52_Create_Profit_Center.png.jpeg)

---

### KS02 – Assign Profit Center to Cost Center  
**T-Code:** KS02  
![KS02 Assign Profit Center to Cost Center](./screenshots/profit_center/KS02_Assign_Profit_Center_to_Cost_Center.png.jpeg)

---

### FB50 – Post FI Document (Stationary / Expense)  
**T-Code:** FB50  
![FB50 Post FI Document](./screenshots/profit_center/FB50_Post_FI_Document.png.jpeg)

---

### FB03 – Display FI Document / Verify Profit Center  
**T-Code:** FB03  
![FB50 Display Document](./screenshots/profit_center/FB50_Display_Document.png.jpeg)

---

### FB60 – Post Supplier Invoice (Office Expense)  
**T-Code:** FB60  
![FB60 Post Supplier Invoice](./screenshots/profit_center/FB60_Post_Supplier_Invoice.png.jpeg)

---

### S_ALR_87013326 – Profit Center Report (Actual / Plan / Variance)  
**T-Code:** S_ALR_87013326  
![S_ALR_87013326 Profit Center Report](./screenshots/profit_center/S_ALR_87013326_Profit_Center_Report.png.jpeg)

##  Final Notes / What i Achieved

| Achievement                                       | Status |
|---------------------------------------------------|--------|
| Profit Center hierarchy successfully created      | ✔      |
| Profit Center groups structured correctly         | ✔      |
| Profit Centers MU1101, MU2201, MU3301 created     | ✔      |
| Cost Center MU1001 assigned to Profit Center MU1101 | ✔    |
| FI posting automatically updated Profit Center    | ✔      |
| PCA report executed successfully                  | ✔      |
