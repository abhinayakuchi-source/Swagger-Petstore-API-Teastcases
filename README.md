# 🐾 Swagger Petstore API Testing

## 📌 Project Overview

This project demonstrates **REST API Testing** using the **Swagger Petstore API**.

The project was developed as part of a **Full Stack Development Training Program** to gain practical experience in API testing, REST APIs, HTTP methods, request and response validation, positive testing, negative testing, CRUD operations, and test-case documentation.

The main objective is to design structured test cases for the Swagger Petstore API and document the expected behavior of different API endpoints.

---

## 🔗 API Under Test

**Swagger Petstore**

Official Swagger UI:

https://petstore.swagger.io/

### Base URL

```text
https://petstore.swagger.io/v2
```

Swagger Petstore provides an interactive Swagger/OpenAPI interface through which API endpoints can be viewed, tested, and executed.

---

# 🎯 Project Objectives

The main objectives of this project are:

* Understand REST API testing.
* Understand API endpoints.
* Understand HTTP request methods.
* Understand HTTP status codes.
* Prepare structured API test cases.
* Identify request parameters.
* Identify request headers.
* Prepare request bodies.
* Validate expected API responses.
* Perform positive testing.
* Perform negative testing.
* Test valid and invalid input values.
* Understand CRUD operations.
* Understand API error handling.
* Document API testing activities professionally.
* Gain practical experience with Swagger/OpenAPI documentation.

---

# 🧪 Testing Scope

The following Swagger Petstore modules are covered:

### 🐾 Pet API

Testing operations related to:

* Finding pets by status
* Finding pets by tags
* Finding a pet by ID
* Adding a new pet
* Updating a pet
* Updating pet information using form data
* Deleting a pet
* Uploading a pet image

### 🏪 Store API

Testing operations related to:

* Retrieving store inventory
* Placing an order
* Retrieving an order
* Deleting an order

### 👤 User API

Testing operations related to:

* Creating a user
* Creating multiple users
* Retrieving a user
* Updating a user
* Deleting a user
* Logging in
* Logging out

---

# 🔧 HTTP Methods Covered

| HTTP Method | Purpose                             |
| ----------- | ----------------------------------- |
| GET         | Retrieve data                       |
| POST        | Create data or perform an operation |
| PUT         | Update existing data                |
| DELETE      | Delete data                         |

---

# 📚 API Testing Concepts Covered

## 1. API

API stands for **Application Programming Interface**.

An API allows two software applications to communicate with each other.

In this project, requests are sent to the Swagger Petstore API and the API returns responses.

---

## 2. REST API

REST stands for **Representational State Transfer**.

REST APIs use HTTP methods such as:

* GET
* POST
* PUT
* DELETE

Swagger Petstore is a RESTful API that uses these HTTP methods to perform operations on pets, orders, and users.

---

## 3. Endpoint

An endpoint is a specific URL through which an API operation can be accessed.

Example:

```text
GET /pet/{petId}
```

The complete URL is:

```text
https://petstore.swagger.io/v2/pet/{petId}
```

---

## 4. Request

An API request is sent from the client to the server.

A request can contain:

* HTTP method
* URL
* Path parameters
* Query parameters
* Headers
* Request body

---

## 5. Response

The server sends a response after processing the request.

A response can contain:

* Status code
* Response headers
* Response body

---

## 6. Status Code

HTTP status codes indicate the result of an API request.

Common status codes include:

| Status Code | Meaning                 |
| ----------- | ----------------------- |
| 200         | OK / Successful request |
| 201         | Created                 |
| 400         | Bad Request             |
| 404         | Not Found               |
| 405         | Method Not Allowed      |
| 500         | Internal Server Error   |

The expected status code for each test case is documented in the Excel sheet.

---

## 7. Request Headers

Headers provide additional information about the request.

Example:

```text
Accept: application/json
```

For JSON request bodies:

```text
Content-Type: application/json
```

Some operations may use an API key:

```text
api_key: special-key
```

---

## 8. Request Body

A request body contains the data sent to the API.

Example:

```json
{
  "id": 1,
  "name": "Doggie",
  "status": "available"
}
```

Request bodies are mainly used with POST and PUT operations.

---

## 9. JSON

JSON stands for **JavaScript Object Notation**.

It is a commonly used format for exchanging data between clients and servers.

Example:

```json
{
  "id": 1,
  "name": "Doggie",
  "status": "available"
}
```

---

# 🔄 CRUD Operations

CRUD stands for:

* **Create**
* **Read**
* **Update**
* **Delete**

These operations are commonly implemented using HTTP methods.

| CRUD Operation | HTTP Method | Example    |
| -------------- | ----------- | ---------- |
| Create         | POST        | Add Pet    |
| Read           | GET         | Get Pet    |
| Update         | PUT         | Update Pet |
| Delete         | DELETE      | Delete Pet |

---

# 🧪 Types of Testing Covered

## Positive Testing

Positive testing verifies that the API works correctly when valid input is provided.

Examples:

* Valid pet ID
* Valid user
* Valid order
* Valid pet status
* Valid request body

Example:

```text
GET /v2/pet/1
```

Expected result:

```text
HTTP 200 OK
```

---

## Negative Testing

Negative testing verifies how the API behaves when invalid or unexpected input is provided.

Examples:

* Invalid ID
* Non-existing ID
* Invalid status
* Missing required fields
* Invalid username
* Invalid login credentials
* Invalid order ID

Negative testing helps verify validation and error handling.

---

# 📊 Test Case Documentation

The project contains an Excel test-case document:

```text
Swagger_Petstore_API_Test_Cases.xlsx
```

The test-case sheet contains the following columns:

| Column               | Description                        |
| -------------------- | ---------------------------------- |
| Test Case ID         | Unique identifier of the test case |
| API Name             | Name of the API operation          |
| Method               | HTTP method                        |
| Endpoint             | API endpoint                       |
| Description          | Purpose of the test case           |
| Request Headers      | Headers required for the request   |
| Request Body         | Request payload                    |
| Expected Status Code | Expected HTTP status code          |
| Expected Response    | Expected API response              |

The sheet intentionally excludes the following execution-result columns:

* Actual Status Code
* Actual Response
* Test Result

These columns can be added later when the test cases are actually executed.

---

# 📋 Test Case Summary

A total of **38 test cases** have been prepared.

| Module    | Number of Test Cases |
| --------- | -------------------: |
| Pet API   |                   18 |
| Store API |                    8 |
| User API  |                   12 |
| **Total** |               **38** |

---

# 🐾 Pet API

The Pet API is used to manage pet information.

## Main Pet Operations

```text
GET    /pet/findByStatus
GET    /pet/findByTags
GET    /pet/{petId}
POST   /pet
PUT    /pet
POST   /pet/{petId}
DELETE /pet/{petId}
POST   /pet/{petId}/uploadImage
```

### Pet Test Scenarios

| Test Case | Scenario                            | Method |
| --------- | ----------------------------------- | ------ |
| TC_001    | Find Pets by Status - Available     | GET    |
| TC_002    | Find Pets by Status - Pending       | GET    |
| TC_003    | Find Pets by Status - Invalid       | GET    |
| TC_004    | Find Pets by Tags                   | GET    |
| TC_005    | Find Pets by Multiple Tags          | GET    |
| TC_006    | Find Pet by ID                      | GET    |
| TC_007    | Find Pet by Invalid ID              | GET    |
| TC_008    | Find Pet by Non-Existing ID         | GET    |
| TC_009    | Add New Pet                         | POST   |
| TC_010    | Add Pet with Missing Required Field | POST   |
| TC_011    | Update Existing Pet                 | PUT    |
| TC_012    | Update Pet with Invalid ID          | PUT    |
| TC_013    | Update Non-Existing Pet             | PUT    |
| TC_014    | Update Pet Using Form Data          | POST   |
| TC_015    | Delete Pet                          | DELETE |
| TC_016    | Delete Pet with Invalid ID          | DELETE |
| TC_017    | Delete Non-Existing Pet             | DELETE |
| TC_018    | Upload Pet Image                    | POST   |

---

# 🏪 Store API

The Store API manages pet store orders and inventory.

## Main Store Operations

```text
GET    /store/inventory
POST   /store/order
GET    /store/order/{orderId}
DELETE /store/order/{orderId}
```

### Store Test Scenarios

| Test Case | Scenario                     | Method |
| --------- | ---------------------------- | ------ |
| TC_019    | Get Inventory                | GET    |
| TC_020    | Place Order                  | POST   |
| TC_021    | Place Invalid Order          | POST   |
| TC_022    | Get Order by ID              | GET    |
| TC_023    | Get Order with Invalid ID    | GET    |
| TC_024    | Get Non-Existing Order       | GET    |
| TC_025    | Delete Order                 | DELETE |
| TC_026    | Delete Order with Invalid ID | DELETE |

---

# 👤 User API

The User API is used for user management and authentication operations.

## Main User Operations

```text
POST /user
POST /user/createWithArray
POST /user/createWithList
GET  /user/{username}
PUT  /user/{username}
DELETE /user/{username}
GET  /user/login
GET  /user/logout
```

### User Test Scenarios

| Test Case | Scenario                          | Method |
| --------- | --------------------------------- | ------ |
| TC_027    | Create User                       | POST   |
| TC_028    | Create Multiple Users Using Array | POST   |
| TC_029    | Create Multiple Users Using List  | POST   |
| TC_030    | Get User by Username              | GET    |
| TC_031    | Get Non-Existing User             | GET    |
| TC_032    | Update User                       | PUT    |
| TC_033    | Update Non-Existing User          | PUT    |
| TC_034    | Delete User                       | DELETE |
| TC_035    | Delete Non-Existing User          | DELETE |
| TC_036    | Login User                        | GET    |
| TC_037    | Login with Invalid Credentials    | GET    |
| TC_038    | Logout User                       | GET    |

---

# 🔍 Sample Positive Test Case

## Find Pet by ID

### Test Case ID

```text
TC_006
```

### API

```text
Find Pet by ID
```

### Method

```text
GET
```

### Endpoint

```text
/v2/pet/{petId}
```

Example:

```text
/v2/pet/1
```

### Description

Verify that pet details can be retrieved using a valid pet ID.

### Expected Status Code

```text
200
```

### Expected Response

Pet details should be returned in JSON format.

---

# ❌ Sample Negative Test Case

## Find Pet Using Invalid ID

### Test Case ID

```text
TC_007
```

### API

```text
Find Pet by Invalid ID
```

### Method

```text
GET
```

### Endpoint

```text
/v2/pet/abc
```

### Description

Verify that the API handles an invalid pet ID correctly.

### Expected Status Code

```text
400
```

### Expected Response

An appropriate invalid-ID error response should be returned.

---

# 📦 Sample Request Body

## Add Pet

```json
{
  "id": 1,
  "name": "Doggie",
  "category": {
    "id": 1,
    "name": "Dogs"
  },
  "photoUrls": [
    "https://example.com/dog.jpg"
  ],
  "tags": [
    {
      "id": 1,
      "name": "friendly"
    }
  ],
  "status": "available"
}
```

---

# 👤 Sample User Request

```json
{
  "id": 1,
  "username": "user1",
  "firstName": "John",
  "lastName": "Doe",
  "email": "john@example.com",
  "password": "password",
  "phone": "1234567890",
  "userStatus": 1
}
```

---

# 🛠️ Tools Used

| Tool             | Purpose                                   |
| ---------------- | ----------------------------------------- |
| Swagger UI       | API documentation and API execution       |
| Swagger Petstore | API under test                            |
| Microsoft Excel  | Test case preparation                     |
| GitHub           | Version control and project documentation |

---

# 🚀 How to Execute the Test Cases

## Step 1: Open Swagger Petstore

Open:

```text
https://petstore.swagger.io/
```

---

## Step 2: Select the API Module

Choose one of the available modules:

```text
Pet
Store
User
```

---

## Step 3: Select an Endpoint

For example:

```text
GET /pet/{petId}
```

---

## Step 4: Click "Try it out"

Swagger UI provides the option to enter parameters and request information.

---

## Step 5: Enter Test Data

Example:

```text
petId = 1
```

---

## Step 6: Execute

Click:

```text
Execute
```

---

## Step 7: Observe the Response

Check:

* Response Code
* Response Body
* Response Headers
* Response Time

---

## Step 8: Compare With Expected Result

Compare the actual response with the expected status code and expected response documented in the Excel test-case sheet.

---

# 🔄 API Testing Workflow

```text
Read API Documentation
        ↓
Identify API Endpoint
        ↓
Identify HTTP Method
        ↓
Identify Parameters
        ↓
Prepare Test Data
        ↓
Prepare Request
        ↓
Execute API
        ↓
Capture Response
        ↓
Validate Status Code
        ↓
Validate Response Body
        ↓
Compare With Expected Result
        ↓
Mark Test Result
```

---

# 🧪 Test Case Design Process

The test cases were designed using the following approach:

### 1. Identify the API

Understand the purpose of the endpoint.

### 2. Identify the HTTP Method

Determine whether the endpoint uses:

```text
GET
POST
PUT
DELETE
```

### 3. Identify Inputs

Identify:

* Path parameters
* Query parameters
* Headers
* Request body

### 4. Create Positive Scenarios

Use valid input values.

### 5. Create Negative Scenarios

Use invalid or unexpected input values.

### 6. Define Expected Results

Specify:

* Expected status code
* Expected response

### 7. Execute and Validate

Execute the request and compare the actual result with the expected result.

---

# 🔐 Authentication and API Key

The Swagger Petstore API includes authentication-related operations.

User authentication operations include:

```text
GET /user/login
GET /user/logout
```

Some operations may also use an API key.

Example:

```text
api_key: special-key
```

---

# 📁 Project Structure

```text
Swagger-Petstore-API-Testing/
│
├── README.md
│
└── Swagger_Petstore_API_Test_Cases.xlsx
```

---

# 📄 Excel Test Case File

The Excel file contains the prepared test cases for the Swagger Petstore API.

### Included Columns

```text
Test Case ID
API Name
Method
Endpoint
Description
Request Headers
Request Body
Expected Status Code
Expected Response
```

### Excluded Columns

The following columns have been intentionally omitted from the GitHub version:

```text
Actual Status Code
Actual Response
Test Result
```

This keeps the GitHub test-case document focused on **test-case design and expected results**.

---

# 📊 Expected Test Result Concept

During actual execution, the test result can be determined using:

```text
Actual Status Code == Expected Status Code
             AND
Actual Response matches Expected Response
             ↓
           PASS
```

Otherwise:

```text
           FAIL
```

---

# 🧠 Important API Testing Concepts Learned

This project provides practical understanding of:

* API
* REST API
* Swagger
* OpenAPI
* API Endpoint
* HTTP Methods
* HTTP Status Codes
* Request
* Response
* Request Headers
* Request Body
* Path Parameters
* Query Parameters
* JSON
* CRUD Operations
* Positive Testing
* Negative Testing
* Input Validation
* Error Handling
* Response Validation
* API Documentation
* Test Case Design
* Test Execution
* Test Result
* Swagger UI

---

# 📈 Future Enhancements

This project can be extended by:

* Executing all test cases using Swagger UI.
* Executing test cases using Postman.
* Adding actual response data.
* Adding actual status codes.
* Recording Pass/Fail results.
* Creating Postman collections.
* Adding automated API tests.
* Using JavaScript with Newman.
* Using Java with REST Assured.
* Integrating API tests into CI/CD pipelines.
* Generating automated test reports.
* Adding authentication and authorization test scenarios.
* Performing performance testing.
* Performing security testing.

---

# ⚠️ Important Note

This repository contains **API test-case preparation and documentation** for the Swagger Petstore API.

The GitHub Excel version intentionally contains the **expected test information only**.

The following execution-result fields are not included:

```text
Actual Status Code
Actual Response
Test Result
```

These fields should be completed after actual API execution.

Therefore, this project primarily demonstrates **API test-case design, documentation, positive testing, negative testing, and expected-result definition**.

---

# 🎓 Learning Outcomes

After completing this project, the following practical skills were developed:

* Understanding REST APIs
* Reading Swagger/OpenAPI documentation
* Identifying API endpoints
* Working with HTTP methods
* Preparing API requests
* Working with JSON
* Understanding request headers
* Understanding request parameters
* Understanding request bodies
* Validating HTTP status codes
* Validating API responses
* Designing positive test cases
* Designing negative test cases
* Understanding CRUD operations
* Preparing professional test-case documentation
* Understanding API testing workflow
* Working with Swagger UI

---

# 🌐 Useful Links

### Swagger Petstore

https://petstore.swagger.io/

### Swagger Petstore API Base URL

https://petstore.swagger.io/v2

---

# 📌 Project Information

```text
Project Name     : Swagger Petstore API Testing
Project Type     : REST API Testing
Training         : Full Stack Development Training
API              : Swagger Petstore
API Specification: Swagger / OpenAPI
Format           : JSON
Documentation    : Microsoft Excel
Repository       : GitHub
Modules          : Pet, Store, User
Test Cases       : 38
Testing Types    : Positive and Negative Testing
```

---

# 👩‍💻 Author

**Abhinaya Kuchi**

B.Tech – Artificial Intelligence and Data Science

Full Stack Development Training Project

---

# ⭐ Conclusion

The Swagger Petstore API Testing project demonstrates a structured approach to REST API testing.

The project covers the **Pet, Store, and User** modules and includes **38 test cases** covering valid and invalid scenarios.

The test cases document the API name, HTTP method, endpoint, description, request headers, request body, expected status code, and expected response.

This project provides a strong foundation for moving from manual API testing toward **Postman-based testing and automated API testing frameworks**.

---

## ⭐ Keywords

```text
API Testing
REST API
Swagger
OpenAPI
Swagger Petstore
Postman
HTTP Methods
GET
POST
PUT
DELETE
JSON
CRUD
Test Cases
Positive Testing
Negative Testing
API Validation
Software Testing
Full Stack Development
Manual Testing
API Documentation
```
