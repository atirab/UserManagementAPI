# UserManagementAPI – API Testing Project

## Project Overview
This project demonstrates API testing of a User Management system using Postman and Newman.  
It covers CRUD operations, data-driven testing, and automated execution using CI/CD.

---

## Tools Used
- Postman
- Newman
- REST APIs
- JavaScript (Postman test scripts)
- GitHub Actions (CI/CD)

---

## API Endpoints Tested
- GET – Get all users
- GET – Get single user
- POST – Create user
- PUT – Update user (full)
- PATCH – Update user (partial)
- DELETE – Delete user


---

## Test Coverage
- Status code validation
- Response body validation
- Dynamic variable handling (userId)
- Data-driven testing using JSON file

---

## Project Structure
UserManagementAPI/
├─ Collections/ # Postman collection
├─ Environments/ # Postman environment
├─ TestData/ # JSON test data
├─ Reports/ # Newman reports
├─ TestCases/ # Excel test cases
├─ .github/workflows/ # CI/CD pipeline



---

## How to Run the Tests

### Using Postman
1. Import the collection and environment
2. Use Collection Runner
3. Select `UsersTestData.json` as data file
4. Run the collection

### Using Newman in command line

 newman run Collections/UserManagementAPI.postman_collection.json \
            -e Environments/QA.postman_environment.json \
            -d TestData/UsersTestData.json \
            -r cli,html,json-summary \
            --reporter-html-export Reports/run-report.html
