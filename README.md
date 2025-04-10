# 📘 RESTful Booker API Testing Project

## 👩‍💻 Author & Repository  
**Created by:** Sandhya Mohan Sankeshwar  
**GitHub Repository:** https://github.com/Suvarna-06/restful-booker-api

---

## 📝 Project Overview  
This project contains automated test cases for the [RESTful Booker API](https://restful-booker.herokuapp.com/) using **Postman**.  
It covers CRUD operations like booking creation, retrieval, updates, and deletion with both positive and negative test cases, including edge and boundary scenarios.

---

## 🛠️ Tools & Technologies Used  
- Postman – to design and run API test cases  
- Newman – for CLI execution and generating reports  
- JavaScript – for writing test scripts in Postman  
- JSON – for request and response bodies  

---

## 📋 Test Plan Summary  
The test strategy is designed to validate the following:

- ✅ Status Codes – Validate expected response status (200, 400, 403, 500)  
- ✅ Field Validations – Validate request bodies with missing/invalid data  
- ✅ Boundary Testing – Min/max values for fields like `totalprice`  
- ✅ Negative Testing – Empty, invalid, or unsupported inputs  
- 🔐 Authentication Testing – Validate secure endpoints (PUT/PATCH/DELETE) with/without proper auth  

---

## ✅ Sample Test Scenarios  

| Test Case | Description | Expected Result |
|----------|-------------|-----------------|
| TC01 | Create booking with valid data | 200 OK |
| TC02 | Invalid `firstname` (numeric) | 500 Internal Server Error |
| TC03 | Empty `firstname` | 400 Bad Request |
| TC04 | Invalid `lastname` (numeric) | 500 Internal Server Error |
| TC05 | Empty `lastname` | 400 Bad Request |
| TC06 | Special characters in `firstname` | 400 Bad Request |
| TC07 | Special characters in `lastname` | 400 Bad Request |
| TC08–TC21 | Various edge/missing data scenarios | As per test case |
| TC22–TC31 | Authenticated CRUD operations (GET/PUT/PATCH) | Valid/Invalid based on auth |

---

## ▶️ How to Execute the Tests

### 👉 Using Postman GUI:
1. Import the collection into Postman.
2. Click on “Runner” → Run all requests.
3. Observe results in the console or collection runner UI.

### 👉 Using Newman CLI:
```bash
newman run Restfulbokker_Testcase.postman_collection.json
