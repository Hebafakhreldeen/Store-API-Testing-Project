# Store API Testing Project

## 📌 Project Overview

This project demonstrates a complete *API Testing workflow* using *Postman* on the Fake Store API.

It covers:

* Authentication (Login)
* Token handling using Environment Variables
* Authorization with Bearer Token
* Full CRUD operations on Products
* End-to-End API testing scenario

---

## 🛠 Tools Used

* Postman
* Fake Store API
* Git & GitHub

---

## 🔐 Authentication

*Endpoint:*


POST /auth/login


After successful login, the JWT token is automatically saved into an Environment Variable using Postman tests.

javascript
pm.environment.set("auth_token", pm.response.json().token);


---

## 📦 Products CRUD Scenario

### 1️⃣ Get All Products


GET /products


### 2️⃣ Create Product


POST /products


✔️ Product ID is saved dynamically:

javascript
pm.environment.set("product_id", pm.response.json().id);


### 3️⃣ Get Product by ID


GET /products/{{product_id}}


### 4️⃣ Update Product


PUT /products/{{product_id}}


### 5️⃣ Delete Product


DELETE /products/{{product_id}}


---

## ▶️ How to Run the Project

1. Import the Postman Collection
2. Import the Environment file
3. Select the Environment
4. Run requests in order:

   * Login
   * Get Products
   * Create Product
   * Read / Update / Delete Product

---

## ✅ Key Testing Concepts Covered

* Environment Variables
* Token-based Authentication
* Dynamic Data Handling
* API Assertions
* End-to-End CRUD Testing

---

## 👤 Author

Heba Ashour
