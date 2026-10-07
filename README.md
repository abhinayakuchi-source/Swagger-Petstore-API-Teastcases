# 🐾 Swagger Petstore API Testing

## 📌 Project Overview

This project is a **REST API Testing project** based on the **Swagger Petstore API**.

The project focuses on understanding and testing REST APIs using Swagger UI and documenting test cases in Excel.

The testing covers three major API categories:

* 🐾 Pet API
* 🏪 Store API
* 👤 User API

A total of **38 structured test cases** were prepared covering API functionality, HTTP methods, request and response validation, status codes, positive testing, negative testing, CRUD operations, and different input scenarios.

---
# 📊 Excel Test Cases

> ### 📥 [Download the Swagger Petstore API Test Cases Excel File](./Swagger_Petstore_API_Test_Cases.xlsx)

The Excel file contains **38 structured API test cases** covering:

* 🐾 Pet API — 18 test cases
* 🏪 Store API — 8 test cases
* 👤 User API — 12 test cases
* ✅ Positive testing
* ❌ Negative testing
* 🔄 CRUD operations
* 🌐 HTTP methods
* 🔢 Expected status codes
* 📋 Expected API responses
* 📝 Request headers and request bodies
* 🔍 API request and response validation

**Note:** The GitHub Excel version contains the test-case design and expected results. The execution-result columns **Actual Status Code, Actual Response, and Test Result** are excluded from this version.

## 🎯 Project Objectives

The main objectives of this project are:

* Understand the fundamentals of API testing.
* Understand REST APIs and API endpoints.
* Learn different HTTP methods.
* Understand HTTP status codes.
* Understand API requests and responses.
* Work with request headers and request bodies.
* Understand JSON request and response formats.
* Perform positive and negative testing.
* Create structured API test cases.
* Validate expected API behavior.
* Test CRUD operations.
* Understand Swagger/OpenAPI documentation.
* Practice testing APIs using Swagger UI.
* Document API test cases using Microsoft Excel.
* Understand the difference between expected and actual results.
* Gain practical knowledge of manual API testing.

---

# 📚 API Testing Concepts Learned

## 1. What is an API?

**API (Application Programming Interface)** is a mechanism that allows two different software applications to communicate with each other.

For example:

```text
Client Application
       ↓
      API
       ↓
Server / Database
```

The client sends a request to the API, and the API returns a response.

---

## 2. What is API Testing?

API testing is the process of testing APIs directly to verify that they:

* Accept valid requests.
* Reject invalid requests.
* Return correct status codes.
* Return expected responses.
* Handle different input values correctly.
* Perform the expected operations.
* Handle errors properly.

API testing focuses mainly on the **backend functionality** rather than the user interface.

---

## 3. What is a REST API?

REST stands for:

**Representational State Transfer**

A REST API is an API that follows REST architectural principles and commonly uses HTTP methods to perform operations on resources.

Example:

```text
GET    /pet/1
POST   /pet
PUT    /pet
DELETE /pet/1
```

---

# 🌐 Client-Server Architecture

API communication generally follows:

```text
Client
   ↓
HTTP Request
   ↓
REST API / Server
   ↓
Processing
   ↓
HTTP Response
   ↓
Client
```

### Example

A client requests information about Pet ID `1`.

```text
GET /pet/1
```

The server processes the request and returns information about the pet.

---

# 🔗 API Endpoint

An **endpoint** is a specific URL through which a client accesses an API resource.

Example:

```text
/pet
/pet/{petId}
/store/order
/user/{username}
```

An endpoint is usually combined with an HTTP method.

Example:

```text
GET /pet/{petId}
```

Here:

* `GET` → HTTP method
* `/pet/{petId}` → API endpoint
* `{petId}` → Path parameter

---

# 📡 HTTP Methods

HTTP methods define what operation should be performed.

| Method | Purpose       |
| ------ | ------------- |
| GET    | Retrieve data |
| POST   | Create data   |
| PUT    | Update data   |
| DELETE | Delete data   |

---

## GET

Used to retrieve information.

Example:

```http
GET /pet/1
```

Purpose:

```text
Retrieve information about Pet ID 1
```

---

## POST

Used to create a new resource.

Example:

```http
POST /pet
```

A request body can contain the new pet information.

---

## PUT

Used to update an existing resource.

Example:

```http
PUT /pet
```

---

## DELETE

Used to delete a resource.

Example:

```http
DELETE /pet/1
```

---

# 🔄 CRUD Operations

CRUD stands for:

| Operation | HTTP Method |
| --------- | ----------- |
| Create    | POST        |
| Read      | GET         |
| Update    | PUT         |
| Delete    | DELETE      |

### CRUD Flow

```text
CREATE → POST
READ   → GET
UPDATE → PUT
DELETE → DELETE
```

CRUD operations are one of the important concepts tested in this project.

---

# 📥 HTTP Request

An HTTP request is sent from the client to the server.

A request can contain:

* HTTP method
* URL
* Endpoint
* Headers
* Query parameters
* Path parameters
* Request body

Example:

```text
POST /pet

Headers:
Content-Type: application/json

Body:
{
  "name": "Tommy",
  "status": "available"
}
```

---

# 📤 HTTP Response

The server sends an HTTP response back to the client.

A response can contain:

* Status code
* Response headers
* Response body

Example:

```text
Status Code: 200

Response:
{
  "id": 1,
  "name": "Tommy",
  "status": "available"
}
```

---

# 📋 Request Headers

Headers provide additional information about an HTTP request.

Example:

```text
Content-Type: application/json
```

`Content-Type` tells the server what type of data is being sent.

Common content types include:

```text
application/json
application/xml
```

---

# 📦 Request Body

The request body contains the data sent to the server.

Example:

```json
{
  "id": 101,
  "name": "Tommy",
  "status": "available"
}
```

Request bodies are commonly used with:

```text
POST
PUT
```

---

# 📄 JSON

JSON stands for:

**JavaScript Object Notation**

It is commonly used for exchanging data between clients and servers.

Example:

```json
{
  "id": 101,
  "name": "Tommy",
  "status": "available"
}
```

JSON uses:

* Objects
* Key-value pairs
* Arrays
* Strings
* Numbers
* Boolean values
* Null values

---

# 🔢 HTTP Status Codes

HTTP status codes indicate the result of an API request.

## 2xx — Success

Indicates that the request was successfully processed.

Examples:

```text
200 OK
201 Created
```

---

## 3xx — Redirection

Indicates that additional action may be required to complete the request.

---

## 4xx — Client Errors

Indicates that there is an issue with the request sent by the client.

Examples:

```text
400 Bad Request
401 Unauthorized
403 Forbidden
404 Not Found
```

---

## 5xx — Server Errors

Indicates that an error occurred on the server.

Examples:

```text
500 Internal Server Error
502 Bad Gateway
503 Service Unavailable
```

---

# 🧪 Positive Testing

Positive testing verifies that the API works correctly when valid input is provided.

Example:

```text
Valid Pet ID
Valid JSON body
Valid required fields
Valid username
```

Expected behavior:

```text
API should process the request successfully.
```

---

# ❌ Negative Testing

Negative testing verifies how an API behaves when invalid input is provided.

Examples:

```text
Invalid Pet ID
Invalid username
Missing required fields
Invalid JSON
Invalid parameter
Non-existing resource
```

The API should handle invalid requests appropriately and return a suitable error response.

---

# 🔍 Request Validation

Request validation verifies whether the request sent to the API is correct.

Things that can be checked include:

* HTTP method
* Endpoint
* Parameters
* Headers
* Request body
* Data types
* Required fields
* Valid input values

---

# ✅ Response Validation

Response validation verifies whether the API response matches the expected result.

Things that can be checked include:

* Status code
* Response body
* Response fields
* Data values
* Response format
* Error messages
* Headers

---

# 🔢 Path Parameters

A path parameter is a value included directly in the URL path.

Example:

```text
GET /pet/{petId}
```

Actual request:

```text
GET /pet/101
```

Here:

```text
petId = 101
```

Path parameters are commonly used to identify a specific resource.

---

# 🔎 Query Parameters

Query parameters are values added to the URL after `?`.

Example:

```text
/pet/findByStatus?status=available
```

Here:

```text
status=available
```

is a query parameter.

Multiple query parameters can be separated using `&`.

Example:

```text
/example?status=available&limit=10
```

---

# 🔐 Authentication and Authorization

### Authentication

Authentication verifies:

**Who are you?**

Examples:

```text
Username + Password
API Key
Token
```

### Authorization

Authorization verifies:

**What are you allowed to access or perform?**

These are different concepts:

```text
Authentication → Identity
Authorization  → Permissions
```

---

# 🔑 API Key

An API key is a value used by an API to identify or authenticate a client/application.

Example:

```text
api_key = abc123
```

Depending on the API, the key may be passed through:

* Header
* Query parameter
* Other authentication mechanism

---

# 📖 Swagger and OpenAPI

## What is Swagger?

Swagger provides tools for designing, documenting, and testing APIs.

## What is OpenAPI?

OpenAPI is a standard specification for describing REST APIs.

Swagger UI can display an OpenAPI definition in an interactive format.

---

# 🖥️ Swagger UI

Swagger UI allows developers and testers to:

* View API documentation.
* View endpoints.
* View HTTP methods.
* View parameters.
* View request body formats.
* Execute API requests.
* View API responses.
* Check status codes.
* Understand API behavior.

---

# 🌐 API Under Test

This project uses:

**Swagger Petstore API**

Swagger Petstore provides sample REST API endpoints for learning and testing API concepts.

API Documentation:

https://petstore.swagger.io/

---

# 🐾 Pet API

The Pet API is used for operations related to pets.

Important operations include:

```text
Add Pet
Update Pet
Find Pet by ID
Find Pets by Status
Find Pets by Tags
Update Pet using Form Data
Delete Pet
```

### Main endpoints

```text
POST   /pet
PUT    /pet
GET    /pet/{petId}
GET    /pet/findByStatus
GET    /pet/findByTags
POST   /pet/{petId}
DELETE /pet/{petId}
```

---

# 🏪 Store API

The Store API is used for store and order-related operations.

Important operations include:

```text
Place Order
Find Order by ID
Delete Order
Get Inventory
```

### Main endpoints

```text
POST   /store/order
GET    /store/order/{orderId}
DELETE /store/order/{orderId}
GET    /store/inventory
```

---

# 👤 User API

The User API is used for user-related operations.

Important operations include:

```text
Create User
Create Users with Array
Create Users with List
Login User
Logout User
Get User by Username
Update User
Delete User
```

### Main endpoints

```text
POST   /user
POST   /user/createWithArray
POST   /user/createWithList
GET    /user/login
GET    /user/logout
GET    /user/{username}
PUT    /user/{username}
DELETE /user/{username}
```

---

# 🧪 Test Case

A test case is a documented set of conditions and steps used to verify whether an API behaves as expected.

A test case generally contains:

```text
Test Case ID
API Name
HTTP Method
Endpoint
Description
Request Headers
Request Body
Expected Status Code
Expected Response
```

---

# 📊 Excel Test Case Documentation

The API test cases for this project are documented in Excel.

The GitHub version contains the expected-result test-case information.

### Columns included:

| Column               | Purpose                     |
| -------------------- | --------------------------- |
| Test Case ID         | Unique test case identifier |
| API Name             | API being tested            |
| Method               | HTTP method                 |
| Endpoint             | API endpoint                |
| Description          | Test scenario               |
| Request Headers      | Headers required            |
| Request Body         | Data sent to API            |
| Expected Status Code | Expected HTTP response code |
| Expected Response    | Expected API behavior       |

### Actual-result columns excluded from the GitHub documentation version:

```text
Actual Status Code
Actual Response
Test Result
```

These columns are related to recording execution results after running the test cases.

---

# 🧾 Expected vs Actual Results

## Expected Result

Defines what should happen when the API is executed.

Example:

```text
Expected Status Code: 200
Expected Response: Pet details should be returned
```

## Actual Result

Records what actually happened during execution.

Example:

```text
Actual Status Code: 200
Actual Response: Pet details received
```

## Test Result

The final comparison can be:

```text
Expected Result = Actual Result
        ↓
      PASS
```

or

```text
Expected Result ≠ Actual Result
        ↓
      FAIL
```

---

# 🧪 Test Case Categories

The test cases in this project cover:

### Functional Testing

Verifies whether the API performs the intended functionality.

### Positive Testing

Uses valid inputs.

### Negative Testing

Uses invalid inputs.

### Boundary/Invalid Input Testing

Tests unusual, invalid, missing, or unexpected values where applicable.

### Response Validation

Checks whether the API returns the expected response.

### Status Code Validation

Checks whether the correct HTTP status code is returned.

---

# 📋 Test Case Summary

The project contains:

| API       | Number of Test Cases |
| --------- | -------------------: |
| Pet API   |                   18 |
| Store API |                    8 |
| User API  |                   12 |
| **Total** |               **38** |

---

# 🐾 Pet API Test Scenarios

The Pet API test cases include scenarios such as:

1. Add a new pet with valid data.
2. Add a pet with different valid values.
3. Add a pet with missing/invalid information.
4. Update an existing pet.
5. Retrieve a pet using a valid ID.
6. Retrieve a pet using an invalid ID.
7. Retrieve pets using available status.
8. Retrieve pets using pending status.
9. Retrieve pets using sold status.
10. Search using tags.
11. Update pet information using form data.
12. Delete an existing pet.
13. Delete using an invalid/non-existing ID.
14. Validate response data.
15. Validate status codes.
16. Test valid request body.
17. Test invalid request data.
18. Verify API behavior for different input conditions.

---

# 🏪 Store API Test Scenarios

The Store API test cases include:

1. Place an order using valid information.
2. Place an order with different valid values.
3. Retrieve an existing order.
4. Retrieve an invalid/non-existing order.
5. Delete an existing order.
6. Delete an invalid/non-existing order.
7. Retrieve store inventory.
8. Validate response and status code.

---

# 👤 User API Test Scenarios

The User API test cases include:

1. Create a user with valid data.
2. Create multiple users using an array.
3. Create multiple users using a list.
4. Login with valid credentials.
5. Test login with invalid credentials.
6. Logout the user.
7. Retrieve a user using username.
8. Retrieve a non-existing user.
9. Update an existing user.
10. Delete an existing user.
11. Test invalid user input.
12. Validate status codes and responses.

---

# 📝 Sample Test Case

### Positive Test Case

```text
Test Case ID:
TC-PET-001

API:
Pet API

Method:
POST

Endpoint:
/pet

Scenario:
Add a new pet using valid information.

Request Body:
{
  "id": 101,
  "name": "Tommy",
  "status": "available"
}

Expected Result:
Pet should be created successfully and the API should return the appropriate success response.
```

---

# ❌ Sample Negative Test Case

```text
Test Case ID:
TC-PET-NEG-001

API:
Pet API

Method:
GET

Endpoint:
/pet/{petId}

Scenario:
Retrieve a pet using an invalid/non-existing ID.

Input:
Invalid Pet ID

Expected Result:
API should handle the invalid request appropriately and return a suitable error response.
```

---

# 🔄 API Testing Workflow

The API testing process followed in this project is:

```text
Understand API Documentation
          ↓
Identify Endpoints
          ↓
Identify HTTP Methods
          ↓
Understand Parameters
          ↓
Prepare Test Scenarios
          ↓
Create Test Cases
          ↓
Send API Request
          ↓
Receive API Response
          ↓
Validate Status Code
          ↓
Validate Response Body
          ↓
Compare Expected vs Actual Result
          ↓
Mark Test Result
```

---

# 🧠 Test Case Design Process

The following approach was used to design the test cases:

### Step 1 — Understand the API

Study the Swagger documentation.

### Step 2 — Identify Endpoints

List the available API endpoints.

### Step 3 — Identify HTTP Methods

Determine whether each endpoint uses:

```text
GET
POST
PUT
DELETE
```

### Step 4 — Identify Inputs

Identify:

* Path parameters
* Query parameters
* Headers
* Request body
* Required fields

### Step 5 — Create Positive Scenarios

Test valid input values.

### Step 6 — Create Negative Scenarios

Test invalid inputs and error conditions.

### Step 7 — Define Expected Results

Specify expected:

* Status code
* Response
* API behavior

### Step 8 — Execute and Validate

Send the request and compare actual behavior with expected behavior.

---

# 🧰 Tools Used

| Tool            | Purpose                                   |
| --------------- | ----------------------------------------- |
| Swagger UI      | API documentation and testing             |
| Microsoft Excel | Test case documentation                   |
| GitHub          | Project version control and documentation |
| REST API        | Backend/API testing                       |
| JSON            | Request and response data format          |

---

# 📁 Project Structure

```text
swagger-petstore-api-testcases/
│
├── README.md
│
└── Swagger_Petstore_API_Test_Cases.xlsx
```

---

# 📊 Project Deliverables

This project contains:

* API testing documentation.
* 38 structured API test cases.
* Pet API test cases.
* Store API test cases.
* User API test cases.
* Positive test scenarios.
* Negative test scenarios.
* HTTP method testing.
* Status code validation.
* Request/response validation.
* Excel-based test-case documentation.
* Swagger API testing practice.

---

# 🎓 Concepts Learned from This Project

Through this project, I gained practical understanding of:

```text
API
REST API
REST Architecture
Client-Server Communication
API Endpoint
HTTP Request
HTTP Response
HTTP Methods
GET
POST
PUT
DELETE
HTTP Status Codes
2xx
3xx
4xx
5xx
Request Headers
Request Body
Response Body
JSON
Path Parameters
Query Parameters
CRUD Operations
Authentication
Authorization
API Key
Swagger
OpenAPI
Swagger UI
API Documentation
Positive Testing
Negative Testing
Functional Testing
Input Validation
Request Validation
Response Validation
Status Code Validation
Test Case Design
Expected Result
Actual Result
Pass / Fail
Manual API Testing
Excel Test Documentation
```

---

# 💡 Important API Testing Concepts

### API Testing vs UI Testing

| API Testing                     | UI Testing                        |
| ------------------------------- | --------------------------------- |
| Tests backend/API functionality | Tests user interface              |
| No UI required                  | Requires UI                       |
| Faster execution                | Usually slower                    |
| Validates requests/responses    | Validates visual/user interaction |
| Checks status codes and data    | Checks screens and user actions   |

---

# 🔍 What Should Be Validated in API Testing?

During API testing, important validation points include:

```text
1. HTTP Method
2. Endpoint
3. Request Parameters
4. Request Headers
5. Request Body
6. Status Code
7. Response Headers
8. Response Body
9. Response Data
10. Error Handling
```

---

# ⚠️ Common API Testing Errors

Some common HTTP errors that testers should understand are:

```text
400 → Bad Request
401 → Unauthorized
403 → Forbidden
404 → Not Found
405 → Method Not Allowed
500 → Internal Server Error
```

The exact response depends on the API implementation.

---

# 🔁 Regression Testing and Retesting

## Retesting

Retesting means testing a specific failed functionality again after the defect has been fixed.

Example:

```text
API Test Failed
      ↓
Developer Fixes Issue
      ↓
Run Same Test Again
      ↓
Retesting
```

## Regression Testing

Regression testing verifies that new changes or fixes have not negatively affected existing functionality.

Example:

```text
API Updated
    ↓
Test Updated Feature
    ↓
Test Related Existing APIs
    ↓
Ensure Existing Functionality Still Works
```

---

# 🧪 Manual API Testing

This project primarily focuses on **manual API testing** using Swagger UI.

Manual testing involves:

```text
Read Documentation
       ↓
Prepare Test Case
       ↓
Enter Parameters
       ↓
Provide Request Body
       ↓
Execute API
       ↓
Observe Response
       ↓
Validate Result
       ↓
Document Result
```

---

# 📌 Important Note About Test Results

The Excel documentation uploaded to GitHub focuses on the **test-case design and expected results**.

The following execution-result columns are intentionally excluded from the GitHub documentation version:

```text
Actual Status Code
Actual Response
Test Result
```

These fields should be populated based on the **actual execution of each API request**.

Therefore, expected results should not be treated as live execution evidence unless the API was actually executed and the results were recorded.

---

# 🚀 Future Enhancements

The project can be extended by adding:

* Postman collections.
* Automated API testing.
* JavaScript API automation.
* Python API automation.
* Newman test execution.
* Response schema validation.
* JSON schema validation.
* Authentication testing.
* Automated test reports.
* CI/CD integration.
* GitHub Actions.
* Regression test automation.
* API performance testing.
* Load testing.
* More negative test cases.

---

# 🔮 Possible Automation Workflow

```text
Swagger API
     ↓
Postman Collection
     ↓
Automated Test Scripts
     ↓
Test Execution
     ↓
Assertions
     ↓
Test Report
     ↓
GitHub Actions
     ↓
CI/CD Pipeline
```

---

# 📈 Learning Outcomes

After completing this project, I gained practical knowledge of:

* Understanding REST APIs.
* Reading Swagger API documentation.
* Identifying API endpoints.
* Understanding HTTP methods.
* Working with JSON.
* Understanding API requests and responses.
* Working with parameters and headers.
* Understanding HTTP status codes.
* Performing positive testing.
* Performing negative testing.
* Designing API test cases.
* Validating API responses.
* Understanding CRUD operations.
* Documenting test cases in Excel.
* Understanding expected and actual results.
* Performing manual API testing using Swagger UI.

---

# 🔗 Useful Links

### Swagger Petstore

https://petstore.swagger.io/

### Swagger / OpenAPI

https://swagger.io/

---

# 👩‍💻 Author

**Abhinaya Kuchi**

B.Tech — Artificial Intelligence and Data Science

Prathyusha Engineering College

---

# 📌 Repository Information

**Repository Name:**

```text
swagger-petstore-api-testcases
```

**Project Type:**

```text
REST API Testing
```

**Testing Type:**

```text
Manual API Testing
```

**API Documentation:**

```text
Swagger / OpenAPI
```

**Test Cases:**

```text
38
```

**Documentation:**

```text
Microsoft Excel
```

---

# ⭐ Conclusion

This project provided practical experience in **REST API testing using Swagger Petstore**.

It helped develop an understanding of API endpoints, HTTP methods, request and response structures, JSON, parameters, headers, status codes, CRUD operations, positive and negative testing, validation, test-case design, and API documentation.

The project also demonstrates how API test scenarios can be systematically documented and organized using Excel.

---

## 🏷️ Keywords

```text
API Testing
REST API
Swagger
Swagger Petstore
OpenAPI
Manual Testing
Software Testing
QA Testing
Test Cases
HTTP
HTTP Methods
HTTP Status Codes
JSON
CRUD
Positive Testing
Negative Testing
API Validation
Request Validation
Response Validation
Swagger UI
REST API Testing
```
