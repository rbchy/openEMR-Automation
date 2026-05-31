# OpenEMR Automation — BDD Cucumber Test Framework

![Java](https://img.shields.io/badge/Java-8+-orange?logo=java)
![Selenium](https://img.shields.io/badge/Selenium-WebDriver-43B02A?logo=selenium)
![Cucumber](https://img.shields.io/badge/Cucumber-BDD-brightgreen?logo=cucumber)
![TestNG](https://img.shields.io/badge/TestNG-Runner-red)
![Maven](https://img.shields.io/badge/Maven-Build-C71A36?logo=apache-maven)
![License](https://img.shields.io/badge/License-Educational-lightgrey)

**Author:** Ranajit Baran Chowdhury — QA Automation Engineer
**Email:** chyranajit@gmail.com
**GitHub:** [@ranajitchowdhury](https://github.com/ranajitchowdhury)

A production-grade UI automation framework for testing the **OpenEMR** electronic medical record system using **Behavior-Driven Development (BDD)** principles. This project demonstrates industry-best practices in test automation architecture and healthcare application quality assurance.

🌐 **Live Application:** [demo.openemr.io](http://demo.openemr.io/b/openemr/interface/login/login.php)

---

## 🛠️ Technology Stack

| Component | Technology | Purpose |
|-----------|-----------|---------|
| **Language** | Java 8+ | Core programming language |
| **Automation** | Selenium WebDriver | Browser interaction & UI control |
| **BDD Framework** | Cucumber (Gherkin) | Human-readable test scenarios |
| **Test Runner** | TestNG | Test execution & reporting |
| **Build Tool** | Maven | Dependency management & builds |
| **IDE** | Eclipse / IntelliJ IDEA | Development environment |

---

## 📁 Project Structure

```
openEMR-Automation/
│
├── src/test/java/
│   ├── features/              ← BDD feature files (Gherkin syntax)
│   │   ├── Login.feature
│   │   ├── PatientManagement.feature
│   │   ├── Navigation.feature
│   │   └── FormValidation.feature
│   ├── steps/                 ← Step definition implementations
│   │   ├── LoginSteps.java
│   │   ├── PatientSteps.java
│   │   └── CommonSteps.java
│   ├── hooks/                 ← Browser setup & teardown
│   │   └── Hooks.java
│   └── runner/                ← TestNG runner configuration
│       └── TestRunner.java
│
├── src/main/java/
│   └── pages/                 ← Page Object Model (POM) classes
│       ├── LoginPage.java
│       ├── DashboardPage.java
│       ├── PatientPage.java
│       └── NavigationPage.java
│
├── pom.xml                    ← Maven dependencies & plugins
├── testng.xml                 ← TestNG suite configuration
└── README.md
```

---

## 🎯 Test Coverage

### 🔐 Authentication
- Valid and invalid login scenario validation
- Session management and timeout handling
- Logout verification and redirect confirmation
- Error message display for incorrect credentials

### 👤 Patient Management
- Create and add new patient records
- Search and retrieve patient by name or ID
- Update existing patient details
- Data integrity validation after CRUD operations

### 🗂️ Navigation & Dashboard
- Access all application modules — Patients, Calendar, Messages
- Verify page transitions and navigation workflows
- Module-specific functionality and element visibility

### 🧾 Form & Data Handling
- Input field validation — required, optional, and format checks
- Dynamic field interaction (dropdowns, date pickers, checkboxes)
- Error message verification on invalid input submission

### ✅ UI Validation
- Element visibility and state verification
- Text content assertions and label validation
- Layout consistency and responsive rendering checks

---

## ✨ Framework Features

| Feature | Description |
|---------|-------------|
| ✅ BDD with Cucumber | Gherkin syntax for readable, stakeholder-friendly test scenarios |
| ✅ Page Object Model | Maintainable and scalable code separation by page |
| ✅ Reusable Step Definitions | Shared steps across feature files to reduce duplication |
| ✅ TestNG Integration | Flexible test grouping, parallel execution, and XML-based suites |
| ✅ Maven Build | Automated dependency management with a single `pom.xml` |
| ✅ Hooks (Before/After) | Clean browser setup and teardown per scenario |
| ✅ Dynamic Locators | Parameterized locators for flexible and resilient UI interaction |

---

## 📋 Prerequisites

Ensure the following are installed before running the tests:

- ✅ **JDK 8 or higher** — configured in system PATH
- ✅ **Maven** — latest stable version
- ✅ **IDE** — Eclipse or IntelliJ IDEA
- ✅ **ChromeDriver** — version matching your installed Chrome browser
- ✅ **Git** — for cloning the repository

---

## ⚙️ Installation & Setup

**1. Clone the repository:**
```bash
git clone https://github.com/ranajitchowdhury/openEMR-Automation.git
cd openEMR-Automation
```

**2. Install dependencies:**
```bash
mvn clean install -DskipTests
```

**3. Verify ChromeDriver path in `Hooks.java`:**
```java
System.setProperty("webdriver.chrome.driver", "path/to/chromedriver");
```

---

## ▶️ Running the Tests

### Option 1 — Maven Command Line
```bash
# Run all tests
mvn clean test

# Run with specific TestNG suite
mvn test -DsuiteXmlFile=testng.xml
```

### Option 2 — IDE (Eclipse / IntelliJ)
1. Right-click `TestRunner.java`
2. Select **Run As → TestNG Test**

### Option 3 — Tag-based Execution
```bash
# Run only login tests
mvn test -Dcucumber.filter.tags="@Login"

# Run only smoke tests
mvn test -Dcucumber.filter.tags="@Smoke"
```

---

## 🏷️ Tags

| Tag | Description |
|-----|-------------|
| `@Smoke` | Critical path — build verification |
| `@Regression` | Full regression suite |
| `@Login` | Authentication scenarios |
| `@Patient` | Patient management flows |
| `@Navigation` | Dashboard and module navigation |
| `@Validation` | Form and input validation checks |

---

## 🏗️ Framework Architecture

```
Feature Files (Gherkin)
        ↓
Step Definitions (steps/)
        ↓
Page Object Model (pages/)
        ↓
Selenium WebDriver
        ↓
Chrome / Firefox Browser
        ↓
OpenEMR Application (demo.openemr.io)
```

### Design Patterns Applied
- **Page Object Model (POM)** — locators and actions isolated per page class
- **BDD (Cucumber)** — Given/When/Then for non-technical stakeholder readability
- **Factory Pattern** — WebDriver instantiation managed centrally
- **Hooks** — `@Before` / `@After` for consistent browser lifecycle management

---

## ⚠️ Healthcare Data Notice

> This framework tests a **demo instance** of OpenEMR. All test data is synthetic and generated for automation purposes only.

- ✅ Use only the demo credentials provided by OpenEMR
- ✅ Never use real patient information in any test scenario
- ✅ Respect HIPAA guidelines even in test environments
- ✅ Focus on UI reliability, secure authentication, and data validation

---

## 📈 Roadmap & Future Enhancements

- [ ] Allure Reports — rich HTML reporting with screenshots
- [ ] CI/CD Integration — Jenkins / GitHub Actions pipeline
- [ ] Parallel Test Execution — multi-threaded TestNG configuration
- [ ] Cross-Browser Testing — Firefox, Edge, and Safari support
- [ ] Data-Driven Testing — Excel / JSON / Database input sources
- [ ] REST API Testing — REST Assured for backend validation
- [ ] Database Validation — MySQL query-level assertions
- [ ] Performance Testing — JMeter integration

---

## 🤝 Contributing

Contributions are welcome!

1. Fork the repository
2. Create your branch: `git checkout -b feature/improvement`
3. Commit your changes: `git commit -m 'Add improvement'`
4. Push to the branch: `git push origin feature/improvement`
5. Open a Pull Request

---

## 📄 License

This project is provided as-is for **educational and professional QA automation** purposes.

---

## 👤 Author

**Ranajit Baran Chowdhury**
Software Programmer & QA Automation Engineer
- 📧 Email: chyranajit@gmail.com
- 🐙 GitHub: [@ranajitchowdhury](https://github.com/ranajitchowdhury)

---

**Version:** 1.0.0
**Last Updated:** May 2026
