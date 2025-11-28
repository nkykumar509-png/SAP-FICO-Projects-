# SAP S/4HANA 2023 – FI Configuration Project
# Company Name: Nakkineni Solutions Pvt Ltd
# Project Name: Basic Financial Accounting Configuration
# Module: SAP FICO (Financial Accounting)
# Version: SAP S/4HANA 2023


 **1. Project Overview**
This project demonstrates the configuration of basic Financial Accounting settings in SAP S/4HANA 2023 for the company *Nakkineni Solutions Pvt Ltd*. The objective is to establish the FI enterprise structure, master data, and perform sample financial postings.

**2. Scope of Project**
- Create Financial Accounting Organizational Structure
- Configure Global Settings
- Create General Ledger Master Records
- Perform Financial Accounting Transactions
- Validate Accounting Document Postings

**3. Enterprise Structure Configuration & T-Codes**
| Step | Description | T-Code |
|------|-------------|--------|
| 1 | Create Company | OX15 |
| 2 | Create Company Code | OX02 |
| 3 | Assign Company to Company Code | OX16 |
| 4 | Define Business Area | OX03 |
| 5 | Define Fiscal Year Variant | OB29 |
| 6 | Assign FYV to Company Code | OB37 |
| 7 | Define Posting Period Variant | OBBO |
| 8 | Assign PPV to Company Code | OBBP |
| 9 | Define Field Status Variant | OBC4 |
| 10 | Assign FSV to Company Code | OBH1 |
| 11 | Define Document Types | OBA7 |
| 12 | Define Number Ranges | FBN1 |
| 13 | Create G/L Master Records | FS00 |

**4. Sample Accounting Posting**
  Transaction Posting
**T-Code: F-02**

| Account | Debit | Credit |
|----------|---------|--------|
| Rent Expense A/c | 10,000 | |
| Bank Account | | 10,000 |

**Narration:** Being rent paid

**Display Document**
**T-Code: FB03**

 **5. Testing & Validation**
- Document successfully posted
- Accounting entries validated
- GL accounts updated correctly

## **6. Conclusion**
The basic SAP FI configuration for *Nakkineni Solutions Pvt Ltd* is completed along with sample postings and validation.

**7. Screenshot List (Capture from SAP GUI)**
| Area | T-code | Screenshot |
|-------|--------|-------------|
| Create Company | OX15 | Entry Screen |
| Create Company Code | OX02 | Data Entry |
| Assignment | OX16 | Company & Code |
| Fiscal Year | OB29 | Variant |
| Posting Period | OBBO | Config |
| Document Type | OBA7 | View |
| Number Ranges | FBN1 | Range Screen |
| G/L Master | FS00 | GL Account |
| Document Posting | F-02 | Document Entry |
| Display | FB03 | Accounting Doc |

---

 **Author**
**Nakkineni Naveen Kumar**  
SAP FICO Consultant  
Naveen Solutions Pvt Ltd


##Screenshots

### 1. Create Company (OX15)
![OX15](screenshots/OX15_Create_Company.jpeg)

### 2. Create Company Code (OX02)
![OX02](screenshots/OX02_Create_Company_Code.jpeg)

### 3. Assign Company and Company Code (OX16)
![OX16](screenshots/OX16_Assign_Company_Code.jpeg)

### 4. Define Fiscal Year Variant (OB29)
![OB29](screenshots/OB29_Fiscal_Year.jpeg)

### 5. Assign Fiscal Year Variant to Company Code (OB37)
![OB37](screenshots/OB37_Assign_FY.jpeg)

### 6. Define Posting Period Variant (OBBO)
![OBBO](screenshots/OBBO_Posting_Period.jpeg)

### 7. Assign Posting Period Variant to Company Code (OBBP)
![OBBP](screenshots/OBBP_Assign_Period.jpeg)

### 8. Define Document Types (OBA7)
![OBA7](screenshots/OBA7_Document_Types.jpeg)

### 9. Define Number Ranges (FBN1)
![FBN1](screenshots/FBN1_Number_Range.jpeg)

### 10. Create G/L Master (FS00)
![FS00](screenshots/FS00_GL_Master.jpeg)

### 11. Accounting Posting (F-02)
![F02](screenshots/F02_Posting.jpeg)

### 12. Display Document (FB03)
![FB03](screenshots/FB03_Display.jpeg)
