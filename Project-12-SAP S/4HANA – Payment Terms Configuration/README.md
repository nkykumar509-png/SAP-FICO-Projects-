Project-12: SAP S/4HANA – Payment Terms Configuration

 Business Scenario

Musashi Auto Pvt. Ltd wants to automate due-date calculation and cash discount for vendor payments and customer invoices.
They require:

2% discount if paid within 10 days

Net due within 30 days

System should automatically calculate baseline date, due date, and discount in FB60 / FB70 postings.

---

 SAP Configuration Steps (with T-Codes)

Step No	Activity Description	T-Code

1	Define Payment Terms	OBB8
2	Define Baseline Date Rules	OBB8
3	Add Installment Payment if required	OBB9 (Optional)
4	Assign Payment Terms to Vendor Master	BP
5	Assign Payment Terms to Customer Master	BP
6	Vendor Invoice Entry	FB60
7	Customer Invoice Entry	FB70
8	Display Discount & Due-Date Calculation	FBL1N / FBL5N


Posting Example for Testing

Type	T-Code / Document	Amount	Payment Terms

Vendor Invoice	FB60	20,000 INR	2% 10 Days / Net 30
Customer Invoice	FB70	15,000 INR	2% 10 Days / Net 30

 Expected Output

✔ System calculates discount automatically
✔ Due-date calculated based on baseline date rules
✔ Discount value visible in FBL1N / FBL5N
✔ Correct posting to cash discount GL (if configured in OBXR / OBXB)

---

📝 Business Outcome

📌 Automated payment cycle
📌 Improves cash flow management
📌 Minimizes manual errors
📌 Discount benefits for early payment
