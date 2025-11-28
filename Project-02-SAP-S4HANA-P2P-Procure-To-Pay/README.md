PROJECT 2 – P2P (PROCURE TO PAY) CYCLE DOCUMENTATION

Company: Nakkineni Solutions Pvt Ltd

Module: SAP FICO / MM Integration

Version: SAP S/4HANA 2023

Project Name: End-to-End Procure to Pay Cycle


---

1. Project Overview

The Procure-to-Pay (P2P) cycle represents the complete procurement process for materials or services purchased from a vendor.
This project covers vendor creation, purchase order, goods receipt, invoice posting, and vendor payment for Nakkineni Solutions Pvt Ltd.


---

2. Business Scenario

Nakkineni Solutions Pvt Ltd purchases Office Furniture worth ₹50,000 from vendor Delhi Traders Pvt Ltd.

End-to-End steps:

1. Create Vendor


2. Create Purchase Order


3. Goods Receipt


4. Invoice Posting


5. Vendor Payment


6. Accounting Document Validation




---

3. Steps & T-Codes Used

Step No.	Business Process	T-Code

1	Create Vendor Master	FK01 / XK01
2	Create Purchase Order	ME21N
3	Goods Receipt	MIGO
4	Invoice Verification	MIRO
5	Vendor Payment	F-53
6	Display Accounting Document	FB03



---

4. Configuration Involved

Configuration	T-Code

Define Vendor Account Group	OBD3
Number Ranges for Vendors	XKN1
Assign Number Ranges	OBAS
Reconciliation Account Setup	FS00



---

5. Accounting Flow

Stage	Debit	Credit

PO (ME21N)	No Accounting Entry	
MIGO Goods Receipt	Inventory (₹50,000)	GR/IR Clearing A/c
MIRO Invoice	GR/IR Clearing A/c	Vendor
F-53 Payment	Vendor	Bank



---

6. Example Posting

📍 Invoice Posting (MIRO)

Account	Debit	Credit

GR/IR Clearing A/c	50,000	
Vendor – Delhi Traders		50,000


📍 Payment Posting (F-53)

Account	Debit	Credit

Vendor – Delhi Traders	50,000	
Bank Account		50,000



---

7. Screenshot List for Upload

Step	T-Code	Screenshot

Create Vendor	FK01	Vendor Master Data
Purchase Order	ME21N	PO Created
Goods Receipt	MIGO	Material Document
MIRO Invoice	MIRO	Accounting Document
Payment	F-53	Payment Document
Display Document	FB03	Ledger Posting

8. Conclusion

The P2P cycle for Nakkineni Solutions Pvt Ltd has been successfully completed with full financial integration between MM and FI modules, validating procurement and vendor payment processes.


---

Author

Nakkineni Naveen Kumar
SAP FICO Consultant
Nakkineni Solutions Pvt Ltd
