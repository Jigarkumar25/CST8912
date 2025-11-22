# CST8912 – Cloud Solution Architecture  
## Lab 9 – Azure SQL Database Security Features

**Student Name:** Jigarkumar Patel    

---

## Task 1 – Deploy an Azure SQL Database

### Steps Performed
- Created resource group **CST8912demo**  
- Deployed Azure SQL Database named **db8912**  
- Created SQL server **db8912demo123** in **West US**  
- Enabled Public endpoint and allowed Azure services plus client IP  
- Loaded sample data for testing  
- Confirmed database is **Online**

### Screenshot – SQL Database Overview
![SQL Database Overview](pictures/1.png)

---

## Task 2 – Configure Advanced Data Protection

### Steps Performed
1. Opened SQL Server and went to **Microsoft Defender for Cloud**  
2. Enabled **Microsoft Defender for SQL**  
3. Reviewed **Recommendations** and **Security Alerts**  
4. Confirmed Defender is active at server level

### Screenshot – Microsoft Defender Enabled
![Microsoft Defender](pictures/2.1.png)

### Screenshot – Recommendations View
![Defender Recommendations](pictures/2.2.png)

---

## Task 3 – Configure Data Classification

### Steps Performed
1. Opened **Data Discovery & Classification** on db8912  
2. Reviewed detected sensitive columns  
3. Accepted all **15 recommended classifications**  
4. Saved changes  
5. Verified updated classification overview

### Screenshot – Sensitive Columns Identified
![Sensitive Columns](pictures/3.1.png)

### Screenshot – Classification Overview Updated
![Classification Overview](pictures/3.2.png)

---

## Task 4 – Configure Auditing

### Steps Performed
1. Enabled **Server Level Auditing**  
2. Created new storage account for audit logs  
3. Set **Retention = 5 days**  
4. Database auditing inherited server settings  
5. Used Query Editor to:
   - Attempt wrong password  
   - Log in successfully  
   - Run SQL query  
6. Viewed audit logs and verified events

### Screenshot – Server Auditing Enabled
![Server Auditing](pictures/4.1.png)

### Screenshot – Query Executed to Generate Logs
![Query Editor](pictures/4.2.png)

### Screenshot – Audit Log Records
![Audit Logs](pictures/4.3.png)

---

## Task 5 – Clean Up Resources

### Steps Performed
- Deleted SQL database **db8912**  
- Deleted SQL server **db8912demo123**  
- Deleted audit storage account  
- Deleted resource group **CST8912demo**

### Screenshot – Cleanup Confirmation
![Cleanup](pictures/5.png)

---
