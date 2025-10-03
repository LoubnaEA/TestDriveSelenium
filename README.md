# TestDriveSelenium
Focused on test automation with **Selenium**, applying **DDT** (**data-driven testing**) by separating **test logic** from **test data**.

---

## At a Glance

🖥️ Automated UI tests with Selenium WebDriver  
   (Maintainable web automation)  

📑 Data-Driven Testing (DDT)  
   (Separating logic from test data)  

🏗️ Page Object Model (POM)  
   (Readable & reusable test structure)  

⚙️ Python, Pytest & Robot Framework  
   (Automation frameworks & runners)  

🎯 CRM-inspired scenarios (Salesforce)  
   (Generic workflows: login, navigation, case management)


## Tech Stack
- Language          : Python  
- Automation frameworks : Selenium WebDriver, Robot Framework  
- IDE               : PyCharm  
- Test runner       : Pytest (Selenium) / Robot Framework runner  
- Data sources      : Python lists/dictionaries (inline for DDT)  
- Application under test : Salesforce (CRM platform)  
- Design pattern    : POM for maintainability


## Structure
├─ 📁 docs/     → Test plans, workflows, guidelines (design & plan tests)  
├─ 📁 scripts/  → Automated test scripts and examples (automation logic)  
├─ 📁 examples/ → Sample test data and anonymized results (DDT inputs/outputs)  
├─ 📁 reports/  → Test execution results and verification logs (traceability)  
└─ README.md


## 🔗 Related Repositories
```yaml
jobs:
  - name: DeploymentPlaybook
    role: Deployment procedures & verification (IDM, Salesforce, CI/CD)
    repo: github.com/LoubnaEA/DeploymentPlaybook

  - name: TestTrekker
    role: Test plans, workflows & automation scripts
    repo: github.com/LoubnaEA/TestTrekker
 ```

TestDriveSelenium  
├── uses → [DeploymentPlaybook](https://github.com/LoubnaEA/DeploymentPlaybook) : deployment & verification  
└── uses → [TestTrekker](https://github.com/LoubnaEA/TestTrekker) : test plans & workflows  


## Notes
**Data-driven test automation practices** applied to a CRM environment (Salesforce).  
Workflows and test data are **anonymized and generalized** :  
-- All test data is fictitious  
-- Workflows are generic, inspired by standard Salesforce scenarios (login, case management, navigation)  
-- Focus is on **test design**, **automation techniques** and **maintainability**

