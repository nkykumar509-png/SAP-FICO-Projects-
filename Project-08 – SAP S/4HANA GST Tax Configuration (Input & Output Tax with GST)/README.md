Project 08 – GST Configuration & Supplier/Customer Invoice Posting (FB60 / FB70)

SAP FICO – GST End-to-End Configuration with FB60 & FB70 Posting

 Business Scenario

Musashi Auto Pvt. Ltd. (MUPL) is implementing GST in SAP S/4HANA.
The requirement is to configure GST condition types and calculation procedure, maintain GST GL accounts, assign tax codes, and post business transactions:

Vendor Invoice with GST using FB60

Customer Invoice with GST using FB70


The GST structure includes:

CGST 9%

SGST 9%

IGST 18%



-GST Configuration Steps (with T-Codes)

Step No.	Configuration Activity	T-Code	Purpose

01	Define GST Condition Types	OBYZ	Create GST tax condition types
02	Define & Maintain Calculation Procedure	OBYZ	Structure calculation sequence
03	Assign Country to Calculation Procedure	OBCN	Link procedure with country India
04	Maintain Tax Codes	FTXP	Create GST tax codes (Input & Output)
05	Create Input GST GL Accounts	FS00	CGST, SGST, IGST Input accounts
06	Create Output GST GL Accounts	FS00	CGST, SGST, IGST Output accounts
07	Create Purchase / Sales Account	FS00	Revenue & expense posting
08	Assign GL Accounts to Tax Keys	OB40	Automatic account posting
09	Create Vendor Master	BP	Supplier record
10	Create Customer Master	BP	Customer record
11	Vendor Invoice Posting	FB60	Input tax calculation
12	Customer Invoice Posting	FB70	Output tax calculation
13	Vendor Line Item Display	FBL1N	Check accounting effect
14	Customer Line Item Display	FBL5N	Review posting impact
15	Display Accounting Document	FB03	Review FI document



---

 Screenshot File List (To Attach in Report)

Screenshot Description	File Name

Define Condition Types	OBYZ_Condition_Types.png.jpeg
Calculation Procedure	OBYZ_Calculation_Procedure.png.jpeg
Assign Country to Procedure	OBCN_Assign_Country_To_Procedure.png.jpeg
Input & Output GST Tax Code	FTXP_Input_Output_GST_Tax_Code.png.jpeg
Input GST GL Accounts	FS00_Input_GST_GL_Accounts.png.jpeg
Output GST GL Accounts	FS00_Output_GST_GL_Accounts.png.jpeg
Purchase Account	FS00_Purchase_Account.png.jpeg
Sales Account	FS00_Sales_Account.png.jpeg
OB40 – Assign Input CGST	OB40_Assign_Input_CGST_GL.png.jpeg
OB40 – Assign Input SGST	OB40_Assign_Input_SGST_GL.png.jpeg
OB40 – Assign Input IGST	OB40_Assign_Input_IGST_GL.png.jpeg
OB40 – Assign Output CGST	OB40_Assign_Output_CGST_GL.png.jpeg
OB40 – Assign Output SGST	OB40_Assign_Output_SGST_GL.png.jpeg
OB40 – Assign Output IGST	OB40_Assign_Output_IGST_GL.png.jpeg
Vendor Master BP	BP_Vendor_Master.png.jpeg
Customer Master BP	BP_Customer_Master.png.jpeg
Vendor Invoice Posting FB60	FB60_Vendor_Invoice_Posting.png.jpeg
GST Calculation FB60	FB60_GST_Calculation_Details.png.jpeg
Customer Invoice FB70	FB70_Customer_Invoice_Posting.png.jpeg
GST Calculation FB70	FB70_GST_Calculation_Details.png.jpeg
Vendor Line Item	FBL1N_Vendor_Line_Item_Display.png.jpeg
Customer Line Item	FBL5N_Customer_Line_Item_Display.png.jpeg
Accounting Document FB03	FB03_Accounting_Document_Display.png.jpeg



---

🎯 Result

✔ GST fully configured
✔ Automatic GST GL postings working correctly
✔ Vendor & customer invoices processed
✔ Reporting & reconciliation validated

