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



---

📍 Steps Performed

1. GST Configuration

Step	T-Code	Screenshot

Define Condition Types	OBYZ	OBYZ_Condition_Types.png.jpeg
Define / Assign Calculation Procedure	OBYZ	OBYZ_Calculation_Procedure.png.jpeg
Assign Country to Calculation Procedure	OBCN	OBCN_Assign_Country_To_Procedure.png.jpeg



---

2. GL Accounts for GST

Step	T-Code	Screenshot

Create Input GST GL Accounts	FS00	FS00_Input_GST_GL_Accounts.png.jpeg
Create Output GST GL Accounts	FS00	FS00_Output_GST_GL_Accounts.png.jpeg
Purchase A/C	FS00	FS00_Purchase_Account.png.jpeg
Sales A/C	FS00	FS00_Sales_Account.png.jpeg



---

3. Assign GST GLs to Tax Keys

Step	T-Code	Screenshot

Assign Input CGST	OB40	OB40_Assign_Input_CGST_GL.png.jpeg
Assign Input SGST	OB40	OB40_Assign_Input_SGST_GL.png.jpeg
Assign Input IGST	OB40	OB40_Assign_Input_IGST_GL.png.jpeg
Assign Output CGST	OB40	OB40_Assign_Output_CGST_GL.png.jpeg
Assign Output SGST	OB40	OB40_Assign_Output_SGST_GL.png.jpeg
Assign Output IGST	OB40	OB40_Assign_Output_IGST_GL.png.jpeg



---

4. Tax Code Creation

Step	T-Code	Screenshot

Maintain GST Tax Code	FTXP	FTXP_Input_Output_GST_Tax_Code.png.jpeg



---

5. Master Data

Step	Type	Screenshot

Vendor Master	BP	BP_Vendor_Master.png.jpeg
Customer Master	BP	BP_Customer_Master.png.jpeg



---

6. Transaction Postings

Step	T-Code	Screenshot

Vendor Invoice Posting (GST Input)	FB60	FB60_Vendor_Invoice_Posting.png.jpeg
GST Calculation details	FB60	FB60_GST_Calculation_Details.png.jpeg
Display Vendor Line Items	FBL1N	FBL1N_Vendor_Line_Item_Display.png.jpeg
Customer Invoice Posting (GST Output)	FB70	FB70_Customer_Invoice_Posting.png.jpeg
GST Calculation details	FB70	FB70_GST_Calculation_Details.png.jpeg
Display Customer Line Items	FBL5N	FBL5N_Customer_Line_Item_Display.png.jpeg
Accounting Document Display	FB03	FB03_Accounting_Document_Display.png.jpeg

---

 Result

✔ GST successfully configured in SAP S/4HANA
✔ FB60 & FB70 invoices posted with correct GST calculations
✔ Accounting entries reflected in FBL1N & FBL5N
✔ Complete End-to-End GST cycle implemented


---

 Skills Covered

GST Configuration

Automatic Account Determination

FS00 GL Creation

BP Master Data

FB60 Vendor Invoice

FB70 Customer Invoice

FBL1N / FBL5N Reporting
