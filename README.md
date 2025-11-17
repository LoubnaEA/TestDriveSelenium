# TestDriveSelenium

Focused on UI test automation with **Selenium WebDriver**, applying **DDT** by separating **test logic** from **test data**. 

---

## At a Glance
- **UI Automation with Selenium WebDriver**
  - Clear separation between pages, actions and tests  
  - Behavior-oriented test scripts  
  - Scalable and maintainable folder structure  

- **Data-Driven Testing (DDT)**
  - Test logic isolated from test data  
  - Externalized inputs (CSV / JSON / Python dictionaries)  
  - Flexible scenario variations  

- **Page Object Model (POM)**
  - Centralized locators  
  - Reusable page actions  
  - Consistent naming and design conventions  

- **Python Ecosystem**
  - Selenium WebDriver  
  - Pytest  
  - Robot Framework (complementary keyword layer)

- **CRM-style Workflows**
  - Generic patterns inspired by **Salesforce** : authentication, navigation, case management  


## Tech Stack
- **Language :** Python  
- **Automation :** Selenium WebDriver  
- **Test Runners :** Pytest, Robot Framework  
- **Design Pattern :** Page Object Model (POM)  
- **Data Formats :** CSV, JSON, Python dictionaries  
- **Target Workflows :** CRM-style UI interactions  
- **IDE :** PyCharm  


## Structure  
├─ 📁 docs/ → Test plans, workflows, guidelines     
├─ 📁 scripts/ → Automated test scripts and framework logic   
├─ 📁 examples/ → Sample test data and anonymized DDT inputs  
├─ 📁 reports/ → Execution logs and result reports (traceability)   
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
Data-driven UI automation in a CRM-like environment.  
All workflows and datasets are **anonymized and generic**.  
Focus on :  
-- Test design quality  
-- Automation architecture  
-- Maintainability and scalability  

