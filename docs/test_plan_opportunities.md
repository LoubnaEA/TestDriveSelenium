# Test Plan - Salesforce Opportunities

Automated UI tests implemented with **Selenium WebDriver** and **Robot Framework**, using a **data-driven approach (DDT)** to separate test logic from test data.  
The workflows are inspired by generic Salesforce CRM behaviour, focusing on maintainability and realistic automation design.

---

### 🟪 In Scope
- **Login workflows**
- **Navigation to Opportunity module**
- **Opportunity creation and field validation**  
- **Multi-persona workflow**  
- **Case management** (basic navigation)

**Out of Scope**
- API testing  
- Performance testing  
- End-to-end Salesforce implementation  
- Backend validations

### 🟪 Data-Driven Approach (DDT)
Test inputs are stored in external files and consumed dynamically by Robot Framework.    
- **Data sources** :  
  `resources/data/opportunity_data.csv`  
  `resources/data/config.yaml`   
- **Advantages** :   
  - Test logic remains generic   
  - Easy maintenance and scaling   
  - Supports multi-persona scenarios  

### 🟪 Test Strategy
- **Keyword-driven structure** using reusable business and Gherkin-style keywords  
- **Page Object Model (POM)** principles applied to keyword organization  
- **CSV-driven loops** for multiple Opportunity test rows  
- **Clear separation** :
  - Test suites → *scripts/*  
  - Keywords → *resources/keywords/*  
  - Data → *resources/data/*  

### 🟪 Environment
**Browser** : Chrome (latest stable)  
**Tools** : Robot Framework, Selenium WebDriver  
**Execution command** : robot scripts/SF_Opportunity_Create.robot  

### 🟪 Risks & Assumptions
- **Risks** :
  - UI changes may break locators
  - Slow page loads may impact stability
- **Assumptions** :
  - Valid credentials available
  - Stable internet connection
  - WebDriver installed

### 🟪 References
- **Selenium WebDriver Documentation**, official reference for browser automation :  
  [https://www.selenium.dev/documentation/](https://www.selenium.dev/documentation/)  
- **Robot Framework User Guide**, official guide for syntax, keywords, data-driven testing :   
  [https://robotframework.org/robotframework/latest/RobotFrameworkUserGuide.html](https://robotframework.org/robotframework/latest/RobotFrameworkUserGuide.html)
- **Project Guidelines**, best practices applied in this repo (POM, DDT, naming conventions) :  
  `docs/guidelines.md`
- **Workflow Documentation**, salesforce-inspired workflows and step-by-step scenarios :  
  `docs/workflows.md`
- **Related Repositories**, internal references demonstrating connected processes :
  - [DeploymentPlaybook](https://github.com/LoubnaEA/DeploymentPlaybook) - Deployment & verification procedures
  - [TestTrekker](https://github.com/LoubnaEA/TestTrekker) - Test plans & workflows

