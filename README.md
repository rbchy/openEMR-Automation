# OpenEMR Automation – BDD Cucumber Test Framework

A comprehensive UI automation framework for testing the OpenEMR electronic medical record (EMR) system using Behavior-Driven Development (BDD) principles. This project demonstrates industry-best practices in test automation architecture and healthcare application quality assurance.

**Live Application:** [demo.openemr.io](http://demo.openemr.io/b/openemr/interface/login/login.php)

## 🛠️ Technology Stack

| Component | Technology |
|-----------|-----------|
| **Language** | Java |
| **Automation Tool** | Selenium WebDriver |
| **BDD Framework** | Cucumber (Gherkin) |
| **Test Runner** | TestNG |
| **Build Tool** | Maven |
| **IDE** | Eclipse / IntelliJ IDEA |

## 📁 Project Structure

```
openEMR-Automation/
│
├── src/test/java/
│   ├── features/         # BDD feature files (Gherkin syntax)
│   ├── steps/            # Step definition implementations
│   ├── hooks/            # Setup & teardown logic (Before/After)
│   └── runner/           # TestNG test runner classes
│
├── src/main/java/
│   └── pages/            # Page Object Model (POM) classes
│
├── pom.xml               # Maven dependencies & plugins
├── testng.xml            # TestNG suite configuration
└── README.md             # This file
```

## 🎯 Test Coverage

### 🔐 Authentication
- Valid/invalid login scenarios
- Session management and logout validation
- Error message verification

### 👤 Patient Management
- Create and add new patient records
- Search and retrieve patient information
- Update patient details

### 🗂️ Navigation & Dashboard
- Access application modules (Patients, Calendar, Messages, etc.)
- Verify page transitions and navigation workflows
- Module-specific functionality testing

### 🧾 Form & Data Handling
- Input validation and error handling
- Dynamic field interaction
- Dropdown and select element management

### ✅ UI Validation
- Element visibility and state verification
- Text assertions and content validation
- Layout and responsiveness checks

## ✨ Framework Features

- ✅ **BDD Implementation** – Cucumber with Gherkin syntax for readable test scenarios
- ✅ **Page Object Model (POM)** – Maintainable and scalable code structure
- ✅ **Reusable Components** – Step definitions and hooks for code reusability
- ✅ **Dynamic Locators** – Parameterized element locators for flexible UI interaction
- ✅ **TestNG Integration** – Flexible test execution and reporting
- ✅ **Maven Build Management** – Automated dependency management and builds

## 📋 Prerequisites

Before running the tests, ensure the following are installed:

- **Java Development Kit (JDK)** – Version 8 or higher
- **Maven** – Latest stable version
- **IDE** – Eclipse or IntelliJ IDEA
- **Browser Driver** – ChromeDriver (or appropriate driver for your browser)

## ▶️ Running the Tests

### Option 1: Maven Command Line
```bash
# Run all tests
mvn clean test

# Run tests with specific TestNG suite
mvn test -DsuiteXmlFile=testng.xml
```

### Option 2: IDE (Eclipse / IntelliJ)
1. Right-click on the test runner class
2. Select **Run As** → **TestNG Test**

### Option 3: Direct TestNG Execution
```bash
java -cp <classpath> org.testng.TestNG testng.xml
```

## 🔐 Important Notes

⚠️ **Healthcare Data Sensitivity**
- Test scenarios simulate realistic healthcare workflows
- Always use demo/test data provided by OpenEMR
- Never use real patient information in testing
- Focus on data validation, secure authentication, and UI reliability

## 📈 Roadmap & Future Enhancements

- [ ] Advanced Reporting (Extent Reports / Allure Reports)
- [ ] CI/CD Integration (Jenkins / GitHub Actions)
- [ ] Parallel Test Execution
- [ ] Cross-Browser Testing Support
- [ ] Data-Driven Testing (Excel/JSON/Database)
- [ ] REST API Testing (REST Assured)
- [ ] Database Validation Queries
- [ ] Performance Testing Integration

## 🤝 Contributing

Contributions are welcome! Please feel free to:
1. Fork the repository
2. Create a feature branch
3. Commit your changes
4. Submit a pull request

## 👨‍💻 Author

**Ranajit B. Chowdhury**  
Software QA Engineer | Automation Testing Specialist  
Expertise: Test Automation, BDD, Selenium, Healthcare Applications

## 📄 License

This project is provided as-is for educational and professional QA automation purposes.

---

**Last Updated:** April 2026