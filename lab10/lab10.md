# CST8912 – Cloud Solution Architecture  
## Lab 10 

**Student Name:** Jigarkumar Patel    

---

# Task 1 – SQL Alerts and Email Notification (Logic App)

For this task, I used an Azure Logic App connected with an Azure SQL Database and Outlook email. The database already contained three records with email addresses, subjects, and message body text. I verified the table data first using a SQL query.

## SQL Data Verification

I opened the query editor in Azure SQL Database and ran a SELECT query on the Alerts table. The table showed three rows with different subjects and message body values.

![SQL Table View](pictures/1.png)

---

## Logic App Structure

The Logic App was already created and contains the following main flow:
- A Recurrence trigger to run automatically
- Get rows (V2) action to read data from the Alerts table
- A For each loop to process each row

This ensures that every record in the database is checked during each run.

![Logic App Designer Flow](pictures/1.2.png)

---

## Logic App Run History

After running the Logic App, I checked the run history section. All executions showed a successful status, which confirms that the workflow is running properly without errors.

![Logic App Run History](pictures/1.3.png)

---

## Email Notification Output

When the Logic App runs, it sends emails using the data from the SQL table. The subject and body of the email match the values stored in the database. The email below shows that the message body was successfully delivered.

![Email Received](pictures/1.4.png)

---

This confirms that the SQL data is being read correctly and that the Logic App is able to send emails based on the database records.
