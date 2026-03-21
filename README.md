# 🧪 Online Gift Shop Testing Project (Manual + API Testing)

## 🌐 Live Website

🔗 https://online-gift-shop-a4212.web.app/

---

## 📌 Project Overview

This project focuses on testing an **Online Gift Shop E-commerce Website** through **Manual Testing** and **API Testing (Postman)**.

The purpose of this project is to ensure that the application functions correctly, delivers a smooth user experience, and handles backend API requests properly.

Online gift shop platforms typically allow users to browse products, add items to cart, and complete purchases easily ([MobiCommerce][1]).

---

## 🎯 Objectives

* Validate core functionalities of the website
* Perform end-to-end user flow testing (Browsing → Cart → Checkout)
* Test API endpoints using Postman
* Identify bugs and usability issues
* Ensure data consistency between frontend and backend

---

## 🔍 Testing Scope

### ✅ Manual Testing

* Functional Testing
* UI/UX Testing
* Smoke Testing
* Regression Testing
* Cart Functionality Testing
* Checkout Process Testing
* Payment Scenarios:

  * Successful Payment
  * Failed Payment
  * Cancel Payment

---

### 🔗 API Testing (Postman)

* GET APIs (Fetch products, cart data)
* POST APIs (Login, Add to Cart)
* PUT/PATCH APIs (Update cart items)
* DELETE APIs (Remove items)
* Status Code Validation (200, 400, 404)
* Response Body Validation
* JSON Schema Validation
* Environment Variables Usage

---

## 🛠️ Tools & Technologies

* Postman
* Newman (CLI API Testing)
* Excel / Google Sheets (Test Cases & Bug Reports)
* Git & GitHub

---

## 📁 Project Structure

📦 project-root

┣ 📄 OGS_Test_Cases.xlsx


┣ 📂 newman_reports/


┃ ┗ 📄 Newman Execution Reports


┣ 📂 postman_collection/


┃ ┗ 📄 OGS_Collection.json


┣ 📜 README.md

---

## 📂 Folder Details

### 📄 OGS_Test_Cases.xlsx

Contains:

* Test Scenarios
* Test Steps
* Expected Results
* Actual Results
* Status (Pass/Fail)

---

### 📂 newman_reports/

* Contains CLI execution results using Newman
* Useful for automation & CI/CD integration

---

### 📂 postman_collection/

* Postman Collection JSON file
* Includes all API requests and test scripts

---

## 🚀 How to Run API Tests (Newman)

### Step 1: Install Newman

```bash
npm install -g newman
```

### Step 2: Run Collection

```bash
newman run postman_collection/OGS_Collection.json
```

### Step 3: Generate Report

```bash
newman run postman_collection/OGS_Collection.json -r cli,html
```

---

## 📊 Sample Test Scenarios

| Test Scenario  | Expected Result            | Status |
| -------------- | -------------------------- | ------ |
| Add to Cart    | Product added successfully | ✅ Pass |
| Empty Cart     | Show empty cart message    | ❌ Fail |
| Failed Payment | Show error message         | ❌ Fail |
| Cancel Payment | Cancel option available    | ❌ Fail |

---

## 🧪 API Test Example (Postman)

```javascript
pm.test("Status code is 200", function () {
    pm.response.to.have.status(200);
});

pm.test("Response contains product ID", function () {
    var jsonData = pm.response.json();
    pm.expect(jsonData._id).to.exist;
});
```

---

## 🐞 Bug Reporting

Each bug includes:

* Bug ID
* Severity & Priority
* Steps to Reproduce
* Expected Result
* Actual Result
* Status

---

## 📈 Key Learnings

* Real-world testing workflow
* Writing structured test cases
* API testing using Postman
* Using Newman for automation
* Bug tracking and reporting
* Understanding frontend-backend interaction

---

## 💡 Future Improvements

* Automation testing using Selenium
* CI/CD integration (GitHub Actions + Newman)
* Performance testing (JMeter)
* Security testing basics

---

## 🤝 Conclusion

This project demonstrates hands-on experience in **Software Quality Assurance (SQA)** including both manual and API testing.

It reflects practical knowledge required for entry-level QA Engineer roles.

---

## 👨‍💻 Author

**Mahmudul Hasan Sarkar**

* 🔗 GitHub: https://github.com/Mahmud256

