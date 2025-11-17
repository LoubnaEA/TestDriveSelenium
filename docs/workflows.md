
# Salesforce Generic Workflows 

This document describes the **generic Salesforce-inspired workflows** implemented in the TestDriveSelenium project.  
The workflows are automated using **Robot Framework**, following **data-driven testing (DDT)** principles.

--- 

### 🟪 Login Workflow
Steps :
1. Open the login page  
2. Enter username & password (from config.yaml)  
3. Validate successful login (check landing page, welcome message, user profile)
  
→ To ensure correct authentication for all subsequent workflows.  
→ To verify UI elements and error handling on login.  

### 🟪 Opportunity Management
Steps :  
1. Navigate to the Opportunities module  
2. Create a new Opportunity using data from `opportunity_data.csv`  
3. Validate creation and stage (prospecting, qualification, etc.)  
4. Update or delete opportunity if needed (multi-row DDT scenario)

→ To demonstrate **data-driven testing** for multiple opportunities.  
→ To verify business rules and UI validation messages.    

### 🟪 Case Management
Steps :
1. Create a new case in the Case module  
2. Assign and update status  
3. Validate case resolution and notifications  
  
→ To automate basic CRM case workflows.   
→ To ensure **multi-step processes** are handled correctly.    

### 🟪 Notes  
All workflows are **generic and anonymized**.  
Designed to demonstrate **automation design**, **maintainability**, **POM/DDT best practices**.  

