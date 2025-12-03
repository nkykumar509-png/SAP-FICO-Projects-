Project 07 – SAP FICO Withholding Tax (TDS) Implementation (End-to-End)

Module: SAP FI – AP

Version: SAP S/4HANA 2023

Scenario: TDS deduction on vendor payments

 Business Scenario

Nakkineni Solutions Pvt Ltd receives a vendor invoice from Unity Suppliers Pvt Ltd for ₹50,000 for professional services.
As per Indian Income Tax rules, TDS 10% must be deducted at the time of invoice posting.

So accounting entry should be:

Account	Debit	Credit

Expense A/c (Professional Charges)	50,000	
TDS Payable 10%		5,000
Vendor Payable		45,000

 Configuration Steps & T-Codes

Step	Activity	T-Code

1	Activate Extended Withholding Tax	SPRO
2	Create Withholding Tax Type	OBC4
3	Create Withholding Tax Code	FTXP
4	Assign Withholding Tax Type to Company Code	OBYZ
5	Assign WHT to Vendor Master	BP / XK02
6	Post Vendor Invoice with TDS	FB60
7	Display Vendor Line Items	FBL1N
8	Display TDS Balances	FAGLL03

### **1. Activate Extended Withholding Tax (SPRO)**
![SPRO_Activate_Extended_WHT](screenshots/SPRO_Activate_Extended_WHT.jpeg)

### **2. Define Withholding Tax Types (SPRO)**
![SPRO_Define_WHT_Tax_Types](screenshots/SPRO_Define_WHT_Tax_Types.jpeg)

### **3. Define Exemption Reasons (SPRO)**
![SPRO_Define_Exemption_Reasons](screenshots/SPRO_Define_Exemption_Reasons.jpeg)

### **4. Withholding Tax Country & Region (SPRO)**
![SPRO_WHT_Country_Region](screenshots/SPRO_WHT_Country_Region.jpeg)

### **5. Define Tax Calculation Rules (SPRO)**
![SPRO_Tax_Calculation_Rules](screenshots/SPRO_Tax_Calculation_Rules.jpeg)

### **6. Assign Withholding Tax Types to Company Code (SPRO)**
![SPRO_Assign_WHTTypes_to_CompanyCode](screenshots/SPRO_Assign_WHTTypes_to_CompanyCode.jpeg)

### **7. Assign G/L Accounts for TDS**
![Assign_GL_Accounts_TDS](screenshots/Assign_GL_Accounts_TDS.jpeg)

### **8. Professional Fees G/L (FS00)**
![FS00_Professional_Fees_GL](screenshots/FS00_Professional_Fees_GL.jpeg)

### **9. Contractor Fees G/L (FS00)**
![FS00_Contractor_Fees_GL](screenshots/FS00_Contractor_Fees_GL.jpeg)

### **10. TDS Payable G/L (FS00)**
![FS00_TDS_Payable_GL](screenshots/FS00_TDS_Payable_GL.jpeg)

### **11. Vendor Master Creation (BP)**
![BP_Vendor_Master_TDS](screenshots/BP_Vendor_Master_TDS.jpeg)

### **12. Vendor Withholding Tax Tab (BP)**
![BP_Withholding_Tax_Tab](screenshots/BP_Withholding_Tax_Tab.jpeg)

### **13. Vendor Invoice Posting with TDS (FB60)**
![FB60_TDS_Invoice_Posting](screenshots/FB60_TDS_Invoice_Posting.jpeg)

### **14. Document Overview (FB60)**
![FB60_Document_Overview](screenshots/FB60_Document_Overview.jpeg)

### **15. Vendor Line Items (FBL1N)**
![FBL1N_Vendor_Line_Items](screenshots/FBL1N_Vendor_Line_Items.jpeg)

### **16. TDS GL Line Item Display (FAGLL03)**
![FAGLL03_TDS_GL_Line_Items](screenshots/FAGLL03_TDS_GL_Line_Items.jpeg)
