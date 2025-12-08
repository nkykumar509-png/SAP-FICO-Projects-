##  Project-14: SAP S/4HANA – Controlling (CO-CCA) – Cost Center Accounting

###  Business Scenario
Musashi Auto Pvt. Ltd. wants to manage internal expenses by department and analyze planned vs actual costs. Cost Center Accounting helps track overheads such as Stationary, Administration, and Petrol expenses and provides variance reporting to support decision-making and budgeting control.

---

##  SAP Configuration Steps (With T-Codes)

| Step | Configuration Activity | T-Code |
|------|------------------------|--------|
| 01 | Maintain Controlling Area | **OKKP** |
| 02 | Assign Company Code to Controlling Area | **OKKP** |
| 03 | Maintain Planning Version | **OKEQ** |
| 04 | Create Number Range for CO Documents | **KANK** |
| 05 | Create Primary Cost GL (Stationary Expense) | **FS00** |
| 06 | Create Secondary Cost Element | **FS00** |
| 07 | Create Cost Center Group | **OKEON** |
| 08 | Create Cost Center | **KS01** |
| 09 | Post Expense to Cost Center | **F-02** |
| 10 | Display Document Entry View | **FB03 / F-02 Display** |
| 11 | Cost Center Planning | **KP06** |
| 12 | Actual/Plan/Variance Report | **S_ALR_87013611** |

---

##  Posting Example for Testing

| Type | T-Code / Document | Amount | Cost Center |
|------|-------------------|---------|-------------|
| Stationary Expense Posting | **F-02** | **10,000 INR** | **MU2001 – Administration** |

---

##  Expected Output
✔ CO document automatically generated  
✔ Expense posted to cost center MU2001  
✔ Actual vs Planned variance calculated  
✔ Expense visible in KP06 planning report  
✔ Cost variance report visible in **S_ALR_87013611**  

---

##  Business Outcome
📍 Transparent control of internal business expenses  
📍 Improved planning & budgeting accuracy  
📍 Enhanced financial decision-making for management  
📍 Clear visibility of department-wise variances  


![OKKP Maintain Controlling Area](screenshots/01_OKKP_Maintain_Controlling_Area.png)
![Assign Company Code to CO Area](screenshots/02_OKKP_Assign_Company_Code.png)
![Maintain Planning Version OKEQ](screenshots/03_OKEQ_Maintain_Version.png)
![CO Number Range KANK](screenshots/04_KANK_Number_Range_CO.png)
![Primary Cost GL FS00](screenshots/05_FS00_Stationary_GL.png)
![Secondary Cost Element FS00](screenshots/06_FS00_Secondary_Cost_Element.png)
![Create Cost Center Group OKEON](screenshots/07_OKEON_Cost_Center_Group.png)
![KS01 Create Cost Center](screenshots/08_KS01_Create_Cost_Center.png)
![Expense Posting F-02](screenshots/09_F02_Post_To_Cost_Center.png)
![Display Document Entry View](screenshots/10_F02_Display_Document_Data_Entry.png)
![Cost Center Planning KP06](screenshots/11_KP06_Planning_Costs.png)
![Cost Center Actual Plan Variance](screenshots/12_SALR_87013611_Cost_Center_Report.png)
