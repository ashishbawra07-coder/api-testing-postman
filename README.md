# 🔌 API Testing with Postman & Newman

[![Newman Tests](https://github.com/ashishbawra07-coder/api-testing-postman/actions/workflows/newman.yml/badge.svg)](https://github.com/ashishbawra07-coder/api-testing-postman/actions)
[![Postman](https://img.shields.io/badge/Postman-FF6C37?style=flat&logo=postman&logoColor=white)](https://postman.com)
[![Newman](https://img.shields.io/badge/Newman-CLI-FF6C37?style=flat&logo=postman&logoColor=white)](https://www.npmjs.com/package/newman)

> Comprehensive REST API test suite using **Postman Collections** with **Newman CLI** integration for CI/CD pipelines. Covers authentication, CRUD operations, error handling, and response validation.

---

## 📌 Features

- ✅ REST API testing (GET, POST, PUT, DELETE)
- ✅ Environment-based config (Dev, QA, Staging, Prod)
- ✅ Authentication token management (auto-generate & inject)
- ✅ Pre-request scripts for dynamic test data
- ✅ Comprehensive assertions (status, schema, response time)
- ✅ Newman HTML Extra reports
- ✅ GitHub Actions CI/CD pipeline

---

## 📁 Project Structure

```
api-testing-postman/
├── .github/
│   └── workflows/
│       └── newman.yml              # CI/CD pipeline
├── collections/
│   ├── BookStore_API.postman_collection.json
│   └── Account_API.postman_collection.json
├── environments/
│   ├── qa.postman_environment.json
│   ├── staging.postman_environment.json
│   └── prod.postman_environment.json
├── reports/                        # HTML reports (git-ignored)
├── package.json
└── README.md
```

---

## 🚀 Getting Started

### Prerequisites
- Node.js 18+
- Newman CLI

### Installation
```bash
# Clone the repo
git clone https://github.com/ashishbawra07-coder/api-testing-postman.git
cd api-testing-postman

# Install dependencies
npm install
```

### Running Tests

```bash
# Run all tests in QA environment
npm test

# Run with specific environment
npm run test:staging
npm run test:prod

# Generate HTML report
npm run test:report
```

---

## 📊 Test Coverage

| Endpoint | Method | Tests |
|---|---|---|
| `/Account/v1/GenerateToken` | POST | Auth token generation, invalid credentials |
| `/Account/v1/Authorized` | POST | Authorization check |
| `/BookStore/v1/Books` | GET | List all books, schema validation |
| `/BookStore/v1/Book` | GET | Single book fetch, invalid ISBN |
| `/BookStore/v1/Books` | POST | Add book to collection |
| `/BookStore/v1/Books` | DELETE | Remove book from collection |

---

## 👤 Author

**Ashish Bawra** — QA Automation Engineer  
📧 ashishbawra07@gmail.com  
🔗 [LinkedIn](https://linkedin.com/in/ashishbawra)  
🎭 [Playwright Framework](https://github.com/ashishbawra07-coder/playwright-automation-framework)
