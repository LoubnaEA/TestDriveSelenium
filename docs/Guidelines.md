## Guidelines - Test Automation Best Practices

### Page Object Model (POM)
- Each Salesforce page/module has its own **Robot keyword file** (`keywords/`)
- Separate **locators** (XPaths, CSS) from **actions** for maintainability
- Keep keywords **high-level** (business actions) and reuse low-level Selenium keywords

### Data-Driven Testing (DDT)
- Store test data in **CSV, JSON** or **Excel** files (`resources/data/`)
- Keep test logic **generic** and feed it with external data
- Use Robot Framework’s `FOR` loops to iterate over multiple rows
- Example: test `Create-Opportunity` with 3 sets of input data

### Naming Conventions
- **Test cases** → Verb-Noun  
`Create-Opportunity`, `Validate-Login`, `Update-Case`
- **Keywords** → Action_Context  
`Click_LoginButton`, `Enter_UserCredentials`, `Verify_OpportunityStage`
- **Variables** → Uppercase with underscores  
`${LOGIN_URL}`, `${USERNAME_FIELD}`, `${PASSWORD_FIELD}`
- **Test data files** → lowercase, underscores  
`opportunity_data.csv`, `login_credentials.json`
- **Scripts** → Module/Domain + description  
`SF_Opportunity_EXO1.robot`, `login_tests.robot`
- **Directories** → lowercase  
`docs/`, `resources/`, `scripts/`, `reports/`

### Test Design
- Follow **AAA pattern** (Arrange, Act, Assert)
- Keep tests **independent** (no hidden dependencies)
- Prioritize **happy paths**, then add negative scenarios
- One test = **one validation goal**

### Maintainability
- Use **meaningful names**  
- Group reusable steps in **keywords**
- Centralize locators in a **single file** → easier updates
- Regularly clean unused test data and scripts

### Reporting & Logs
- Store Robot logs in `reports/` for each run
- Use tags (`[Tags] Smoke, Regression`) to organize test suites
- Share logs in CI/CD pipelines (Jenkins, GitHub Actions)

### Version Control (GitHub)
- Commit often, with clear messages (`Add Create-Opportunity test`)
- Use branches for new features/tests
- Keep `main` branch stable
- Document folder structure in `docs/Architecture.md`

