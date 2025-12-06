## Project-08 – SAP S/4HANA – GST Configuration (India)

### Business Scenario

Configure Goods & Services Tax (GST) in SAP S/4HANA for an Indian company code (MUPL) and verify end-to-end postings:

- Vendor invoice with input GST via **FB60**
- Customer invoice with output GST via **FB70**
- Automatic GST postings using **OB40**
- Reporting of vendor and customer line items via **FBL1N / FBL5N**

GST structure used:

| Tax Type | Example Rate |
|---------|--------------|
| CGST    | 9%           |
| SGST    | 9%           |
| IGST    | 18%          |

---

### GST Configuration Steps (with T-Codes)

| Step | Configuration Activity                         | T-Code | Purpose                                               |
|------|------------------------------------------------|--------|-------------------------------------------------------|
| 01   | Define GST Condition Types                     | OBYZ   | Create GST tax condition types                        |
| 02   | Define / Maintain Calculation Procedure        | OBYZ   | Build GST calculation schema                          |
| 03   | Assign Country to Calculation Procedure        | OBCN   | Link procedure TAXINN to country IN                   |
| 04   | Maintain GST Tax Codes (Input / Output)        | FTXP   | Define GST tax codes for purchases and sales          |
| 05   | Create Input GST GL Accounts                   | FS00   | Input CGST / SGST / IGST GLs                          |
| 06   | Create Output GST GL Accounts                  | FS00   | Output CGST / SGST / IGST GLs                         |
| 07   | Create Purchase Account                        | FS00   | Expense account for GST-relevant purchases            |
| 08   | Create Sales Account                           | FS00   | Revenue account for GST-relevant sales                |
| 09   | Assign Input GST GLs to Tax Keys               | OB40   | Automatic posting – input CGST / SGST / IGST          |
| 10   | Assign Output GST GLs to Tax Keys              | OB40   | Automatic posting – output CGST / SGST / IGST         |
| 11   | Create Vendor Master                           | BP     | Supplier master data with company code MUPL           |
| 12   | Create Customer Master                         | BP     | Customer master data with company code MUPL           |
| 13   | Post Vendor Invoice with GST                   | FB60   | Vendor invoice + input GST calculation                |
| 14   | Post Customer Invoice with GST                 | FB70   | Customer invoice + output GST calculation             |
| 15   | Display Accounting Document                    | FB03   | Check FI document and GST postings                    |
| 16   | Vendor Line Item Display                       | FBL1N  | Verify vendor open item / cleared item with GST       |
| 17   | Customer Line Item Display                     | FBL5N  | Verify customer open item / cleared item with GST     |

---

### Screenshot File List (as used in this project)

| Screenshot Description                     | File Name                                       |
|-------------------------------------------|-------------------------------------------------|
| Define Condition Types                    | OBYZ_Condition_Types.png.jpeg                   |
| Define Calculation Procedure              | OBYZ_Calculation_Procedure.png.jpeg             |
| Assign Country to Procedure               | OBCN_Assign_Country_To_Procedure.png.jpeg       |
| Input & Output GST Tax Code               | FTXP_Input_Output_GST_Tax_Code.png.jpeg         |
| Input GST GL Accounts                     | FS00_Input_GST_GL_Accounts.png.jpeg             |
| Output GST GL Accounts                    | FS00_Output_GST_GL_Accounts.png.jpeg            |
| Purchase Account                          | FS00_Purchase_Account.png.jpeg                  |
| Sales Account                             | FS00_Sales_Account.png.jpeg                     |
| OB40 – Assign Input CGST GL              | OB40_Assign_Input_CGST_GL.png.jpeg              |
| OB40 – Assign Input IGST GL              | OB40_Assign_Input_IGST_GL.png.jpeg              |
| OB40 – Assign Input SGST GL              | OB40_Assign_Input_SGST_GL.png.jpeg              |
| OB40 – Assign Output CGST GL             | OB40_Assign_Output_CGST_GL.png.jpeg             |
| OB40 – Assign Output IGST GL             | OB40_Assign_Output_IGST_GL.png.jpeg             |
| OB40 – Assign Output SGST GL             | OB40_Assign_Output_SGST_GL.png.jpeg             |
| Vendor Master (BP)                        | BP_Vendor_Master.png.jpeg                       |
| Customer Master (BP)                     | BP_Customer_Master.png.jpeg                     |
| Vendor Invoice Posting (FB60)             | FB60_Vendor_Invoice_Posting.png.jpeg            |
| GST Calculation Details – Vendor (FB60)   | FB60_GST_Calculation_Details.png.jpeg           |
| Customer Invoice Posting (FB70)           | FB70_Customer_Invoice_Posting.png.jpeg          |
| GST Calculation Details – Customer (FB70) | FB70_GST_Calculation_Details.png.jpeg           |
| Vendor Line Item Display                  | FBL1N_Vendor_Line_Item_Display.png.jpeg         |
| Customer Line Item Display                | FBL5N_Customer_Line_Item_Display.png.jpeg       |
| Accounting Document Display (FB03)        | FB03_Accounting_Document_Display.png.jpeg       |

---

### Outcome

- GST configuration completed successfully for company code **MUPL**  
- Automatic GST postings triggered via **OB40**  
- Vendor and customer invoices posted with correct input/output GST  
- Line item reports (**FBL1N / FBL5N**) and accounting document (**FB03**) validated
