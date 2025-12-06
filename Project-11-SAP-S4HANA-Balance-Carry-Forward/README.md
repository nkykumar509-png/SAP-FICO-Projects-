Project-11: SAP S/4HANA – Foreign Currency Revaluation (F.07)

 Business Objective

To revalue foreign currency balances for customers and vendors at period end, ensuring that unrealized gain or loss due to exchange rate differences is correctly reflected in financial statements.

 Business Scenario

Musashi Auto Pvt. Ltd. deals with international customers and vendors, recording invoices in foreign currency. At month end, exchange rates may change, which affects outstanding balances.
Using F.07 Foreign Currency Valuation, the company revalues balances and posts exchange gain/loss adjustment entries.

---

 ##  SAP Configuration & Posting Steps (With T-Codes)

| Step | Description | T-Code |
|------|------------|--------|
| 01 | Customer Invoice Posting | **FB70** |
| 02 | Vendor Invoice Posting | **FB60** |
| 03 | Create Retained Earnings G/L Account | **FS00** |
| 04 | Assign Retained Earnings Account to Chart of Accounts | **OB53** |
| 05 | Display Customer Balances | **FD10N** |
| 06 | Display Vendor Balances | **FK10N** |
| 07 | Execute Foreign Currency Revaluation | **F.07** |
| 08 | Check Revaluation Spool Output | **F.07 Spool** |
| 09 | Review Revaluation Job Overview | **F.07 Job Overview** |

##  Posting Example for Testing

| Type | T-Code / Document | Amount |
|-------|-----------------------|-------:|
| Customer Invoice | **FB70** | **15,000 INR** |
| Vendor Invoice | **FB60** | **10,000 INR** |

---

##  Expected Output

✔ Successfully executed currency revaluation posting  
✔ Realized / unrealized exchange gain/loss posted correctly  
✔ Updated customer & vendor balances in **FD10N / FK10N**  
✔ Revaluation spool report reviewed in **F.07 Spool**  
✔ Revaluation job details shown in **F.07 Job Overview**

## 📁 Screenshot Attachments

| Step | Screenshot |
|------|------------|
| 01 | ![F07 Job Overview](./screenshots/F07_Job_Overview.png) |
| 02 | ![F07 Spool Display](./screenshots/F07_Spool_Display.png) |
| 03 | ![F07 Posting Results](./screenshots/F07_Posting_Results.png) |
| 04 | ![Display Customer Balances](./screenshots/FD10N_Display_Customer_Balances.png) |
| 05 | ![Display Vendor Balances](./screenshots/FK10N_Display_Vendor_Balances.png) |
| 06 | ![Assign Retained Earnings](./screenshots/OB53_Assign_Retained_Earnings.png) |
| 07 | ![Create Retained Earnings GL](./screenshots/FS00_Create_Retained_Earnings_GL.png) |
| 08 | ![Vendor Invoice Posting](./screenshots/FB60_Vendor_Invoice_Posting.png) |
| 09 | ![Customer Invoice Posting](./screenshots/FB70_Customer_Invoice_Posting.png) |
