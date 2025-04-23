
# CRUD Postman QA Automation 

**`crud-postman-qa-automation`** is an automated testing project designed to validate CRUD (Create, Read, Update, Delete) operations using **Postman** and **Newman**. This project focuses on automating API tests to ensure that the application's backend services function correctly for all basic data operations, while integrating reporting for easy tracking.

---

## 📁 Project Structure

```
crud-postman-qa-automation/
│
├── api-tests/
│   ├── crud-api-tests.json        # Postman Collection
│   └── report/                    # Newman HTML Report
│
└── README.md                      # This file
```

---

## 🚀 How to Run the Tests

### ✅ 1. API Test (Postman + Newman)

```bash
npm run api-test
```

This generates a report at:

```
api-tests/report/report.html
```

---

## ⚙️ CI with GitHub Actions

Whenever a push is made to `main`, GitHub Actions automatically:

- Runs the CRUD API tests
- Generates a visual HTML report
- Uploads the report as a downloadable artifact

See it under the [Actions](https://github.com/Hyokenhi/crud-postman-qa-automation/actions) tab.

---

## 👤 Author

**Cristian Camilo Delgado**  
👨‍💻 Software Programming Technician - SENA  
🚀 Passionate about automation and continuous learning, seeking a career in QA Automation.  
💡 Committed to improving software quality through disciplined, efficient, and effective testing practices.

📬 Contact: [LinkedIn](https://www.linkedin.com/in/Hyokenhi/) | GitHub: [@Crisweisk](https://github.com/Hyokenhi)

---

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.
