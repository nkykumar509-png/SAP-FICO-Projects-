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
