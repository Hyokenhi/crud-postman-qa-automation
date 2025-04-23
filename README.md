
# CRUD Postman QA Automation 🚀

**`crud-postman-qa-automation`** is an automated testing project designed to validate CRUD (Create, Read, Update, Delete) operations using **Postman** and **Newman**. This project focuses on automating API tests to ensure that the backend services function correctly for all basic data operations. It also integrates detailed reporting for easy tracking of results and performance metrics.

---

## 🔍 Project Overview

This project automates the following CRUD operations tests:

- **Create**: Validates the ability to create new data entries via API.
- **Read**: Validates that the data can be read correctly.
- **Update**: Validates that the data can be updated via API.
- **Delete**: Validates that data can be deleted from the system.

The tests are created using **Postman**, and **Newman** is used to run the tests in the command line. The project also includes automated reporting to track the success and failure of the tests.

---

## 📁 Project Structure

The project is structured as follows for easy navigation and maintenance:

```
crud-postman-qa-automation/
│
├── api-tests/
│   ├── crud-api-tests.json        # Postman Collection for CRUD operations
│   └── report/                    # Newman HTML Report
│
├── node_modules/                  # Node modules for Newman and other dependencies
├── .gitignore                     # Git ignore file
├── README.md                      # This file
├── package-lock.json              # NPM lock file for dependencies
└── package.json                   # NPM configuration file
```

---

## 🛠️ Technologies Used

- **Postman**: For creating, managing, and testing API requests.
- **Newman**: Command-line tool to run **Postman** collections, enabling automation of API testing.
- **Node.js**: JavaScript runtime used to execute the tests and manage the project dependencies.
- **NPM**: For managing dependencies and scripts.

---

## 🚀 How to Run the Tests

### ✅ 1. Clone the Repository

Clone the repository to your local machine:

```bash
git clone https://github.com/Hyokenhi/crud-postman-qa-automation.git
cd crud-postman-qa-automation
```

### ✅ 2. Install Dependencies

To install the required dependencies, run the following command:

```bash
npm install
```

### ✅ 3. Running the Tests

#### API Test (Postman + Newman)

To execute the API tests using **Newman**, run:

```bash
newman run api-tests/crud-api-tests.json -r html,mochawesome
```

This will run the **Postman** collection defined in `crud-api-tests.json` and generate the results in **HTML** and **Mochawesome** formats.

---

## ⚙️ CI/CD Integration with GitHub Actions

### Automated Test Execution

Each time you push to the `main` branch, **GitHub Actions** will automatically:

- Run the **CRUD API tests** defined in the Postman collection.
- Generate a **Mochawesome** HTML report.
- Upload the test results as an artifact for easy access.

### Workflow File (`.github/workflows/ci.yml`)

```yaml
name: CRUD Postman API Automation

on:
  push:
    branches:
      - main

jobs:
  run-tests:
    runs-on: ubuntu-latest
    steps:
      - name: Checkout code
        uses: actions/checkout@v2
      - name: Install dependencies
        run: npm install
      - name: Run Postman tests
        run: newman run api-tests/crud-api-tests.json -r html,mochawesome
      - name: Upload test reports
        uses: actions/upload-artifact@v2
        with:
          name: mochawesome-report
          path: api-tests/report/*.html
```

You can monitor the execution of your workflows under the **Actions** tab in your GitHub repository.

---

## 📝 Test Details

- **Create Test**: Automates testing for creating new data entries via the API.
- **Read Test**: Ensures that the data can be read correctly from the API.
- **Update Test**: Validates the ability to update existing data via the API.
- **Delete Test**: Ensures that the API can delete data as expected.
- **Mochawesome Reports**: Automatically generates detailed test logs, failures, and visual reports for analysis.

---

## ❗ Important Notes

- **Postman Environment**: Ensure that the **Postman environment variables** are configured correctly for your API endpoints and any authentication requirements.
  
- **Headless Mode**: Running the tests in **headless mode** (using **Newman**) is recommended for CI/CD pipelines. However, you can also run the tests in the Postman UI for manual inspection.

---

## 👤 Author

**Cristian Camilo Delgado**  
👨‍💻 Software Programming Technician - SENA  
🚀 Passionate about automation and continuous learning, seeking a career in QA Automation.  
💡 Committed to improving software quality through disciplined, efficient, and effective testing practices.

📬 Contact: [LinkedIn](https://www.linkedin.com/in/Hyokenhi/) | GitHub: [@Hyokenhi](https://github.com/Hyokenhi)

---

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.
