# Architectural foundation of **`TestDriveSelenium`**

The design focuses on robustness, modularity, maintainability and alignment with engineering-grade automation standards.  
It enforces strict separation of concerns, predictable behavior, seamless integration into CI/CD pipelines.  


### Principles & Objectives
**Strict separation of layers** : pages, tests, configuration, utilities, data.  
**Maintainability and testability** : modular, decoupled, predictable components.     
**UI test robustness** : encapsulated WebDriver interactions and stable synchronization strategies.   
**Extensibility** : adding new modules, pages, environments or test types without refactoring.  
**CI/CD readiness** : headless execution, clean logs, structured artifacts, reproducible runs.   


### High-Level Architecture (5 core layers)

**1. Test Layer (pytest-based)**  
Located in `tests/` 
  * Contains scenario definitions only   
  * Organized by functional domains (e.g., `ui/login`, `ui/search`)  
  * Follows the **Arrange / Act / Assert** pattern   
  * Contains no business logic or WebDriver logic  

**2. Page Layer (Page Object Model)**  
Located in `pages/`
  * Defines screens and interactive components  
  * Contains :
    * element locators  
    * user actions  
    * light validation (e.g., visibility checks)  
  * Fully decoupled from test logic  

**3. Tools & Utilities Layer**  
Located in `tools/`
  * **waits.py** : synchronization strategies  
  * **selenium_wrapper.py** : WebDriver lifecycle, error handling, screenshots  
  * **logger.py** : unified logging interface  
  * Provides stable cross-cutting primitives  

**4. Configuration Layer**     
Located in `config/`
  * Environment-specific YAML files (dev/qa/prod) with fallback  
  * **driver_options.py** : creation and configuration of WebDrivers  
  * Supports CLI overrides (`--env=qa`, `--headless`, etc.)  
  * No hardcoded configuration within tests  

**5. Test Data Layer**    
Located in `data/`
  * JSON/CSV datasets used for data‑driven testing  
  * **testdata_builder.py** for dynamic data generation  
  * Completely separated from logic and tests  

### Selenium Architecture

**1. WebDriver Wrapper**  
Objectives : Centralize Selenium interactions, normalize error handling, improve maintainability   

Expected capabilities :
* driver lifecycle management  
* automatic screenshots on failure  
* detailed logging  
* wrapped operations (`click`, `send_keys`, `wait_for`)  

**2. Synchronization & Waits**
* Explicit waits only  
* No hard `sleep` usage  
* Synchronization handled in `tools/waits.py`  
* Designed to withstand UI response variability  

### Test Execution Model

**1. Local Execution**
* `pytest -m ui --env=qa --headed`
* Drivers managed by `scripts/download_drivers.py`  

**2. CI/CD Execution**  
* Headless mode by default  
* Captures logs, screenshots, artifacts  
* Supports distributed execution  

**3. Tagging & Grouping**
* `@pytest.mark.smoke`  
* `@pytest.mark.critical_path`  
* `@pytest.mark.regression`  

### Extensibility Model
The architecture supports effortless addition of :
* new test modules  
* new pages and components  
* additional environments  
* new test types (API, light performance)  
* customized synchronization rules  

### Quality Gates & Best Practices
Actions fully encapsulated within page objects.    
No business logic in test files.    
Stable, centralized locators.    
Externalized test data only.    
Configuration decoupled from code.  
Logs and artifacts are mandatory.    
CI pipelines must be reproducible.    

