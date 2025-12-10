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

##  Business Example

| Doc No | G/L      | Description         | Amount       | Cost Center | Profit Center | Posting Type |
|--------|-----------|----------------------|--------------|-------------|----------------|----------------|
| 1022   | 400602    | Stationary Expense   | 100,000 INR  | MU1001      | MU1101         | Debit (FB50)   |
| 1022   | 200101    | HDFC Bank A/c        | 100,000 INR  | —           | —              | Credit (FB50)  |
| Invoice| 400602    | Office Expense       | 10,000 INR   | —           | MU1101         | Debit (FB60)   |

##  Final Notes / What i Achieved

| Achievement                                       | Status |
|---------------------------------------------------|--------|
| Profit Center hierarchy successfully created      | ✔      |
| Profit Center groups structured correctly         | ✔      |
| Profit Centers MU1101, MU2201, MU3301 created     | ✔      |
| Cost Center MU1001 assigned to Profit Center MU1101 | ✔    |
| FI posting automatically updated Profit Center    | ✔      |
| PCA report executed successfully                  | ✔      |
