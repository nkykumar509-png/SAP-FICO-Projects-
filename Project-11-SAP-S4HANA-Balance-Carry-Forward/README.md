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

## Screenshots

| No. | Description | Markdown Code |
|-----|-------------|---------------|
| 1 | Customer Invoice Posting (FB70) | `![FB70 Customer Invoice Posting](screenshots/FB70_Customer_Invoice_Posting.png.jpeg)` |
| 2 | Vendor Invoice Posting (FB60) | `![FB60 Vendor Invoice Posting](screenshots/FB60_Vendor_Invoice_Posting.png.jpeg)` |
| 3 | Create Retained Earnings G/L Account (FS00) | `![FS00 Create Retained Earnings Account](screenshots/FS00_Create_Retained_Earnings_Account.png.jpeg)` |
| 4 | Assign Retained Earnings Account to Chart of Accounts (OB53) | `![OB53 Assign Retained Earnings Account](screenshots/OB53_Assign_Retained_Earnings_Account.png.jpeg)` |
| 5 | Display Customer Balances (FD10N) | `![FD10N Display Customer Balances](screenshots/FD10N_Display_Customer_Balances.png.jpeg)` |
| 6 | Display Vendor Balances (FK10N) | `![FK10N Display Vendor Balances](screenshots/FK10N_Display_Vendor_Balances.png.jpeg)` |
| 7 | Foreign Currency Revaluation – Posting Result (F.07) | `![F07 Posting Result](screenshots/F07_Posting_Result.png.jpeg)` |
| 8 | Foreign Currency Revaluation – Spool Output (F.07) | `![F07 Spool Output](screenshots/F07_Spool_Output.png.jpeg)` |
| 9 | Foreign Currency Revaluation – Job Overview (F.07) | `![F07 Job Overview](screenshots/F07_Job_Overview.png.jpeg)` |
