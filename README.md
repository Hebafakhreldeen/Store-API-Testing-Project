# 🛠 Store API Testing Project

## 🚀 Project Overview

This project demonstrates a **complete API testing workflow** using **Postman** on the **Fake Store API**.  
It showcases practical QA skills including authentication, token handling, dynamic environment variables, and **end-to-end CRUD testing for products**.

Key highlights:

- Authentication & Login with JWT token handling
- Authorization with Bearer Tokens
- Dynamic environment variable usage
- Full CRUD operations on products
- Response validation and assertions

---

## 📌 API Endpoints Covered

| Action | Method | Endpoint |
|--------|--------|----------|
| Login | POST | `/auth/login` |
| Get All Products | GET | `/products` |
| Create Product | POST | `/products` |
| Get Product by ID | GET | `/products/{{product_id}}` |
| Update Product | PUT | `/products/{{product_id}}` |
| Delete Product | DELETE | `/products/{{product_id}}` |

---

## 🧪 Tools & Technologies

- **Postman** (Collection, Environment, and Test Scripts)  
- **JavaScript** for Test Scripts  
- **REST API fundamentals**  
- **Git & GitHub** for version control  

---

## 🔑 Key Concepts Demonstrated

- Environment Variables for dynamic token and ID handling
- Token-based authentication
- Dynamic data validation
- Response structure and data type validation
- Chained request execution (Login → CRUD workflow)
- End-to-end API testing scenario

---

## 🧠 Example Test Scripts

### 1. Save Authentication Token

javascript
pm.test("Status code is 200", function () {
    pm.response.to.have.status(200);
});
pm.environment.set("auth_token", pm.response.json().token);
`

### 2. Save Product ID dynamically

javascript
pm.test("Save created product ID", () => {
    pm.expect(pm.response.json()).to.have.property("id");
    pm.environment.set("product_id", pm.response.json().id);
});


### 3. Validate Response Structure

javascript
pm.test("Response is JSON and contains correct structure", () => {
    pm.response.to.be.json;
    const data = pm.response.json();
    pm.expect(data).to.have.property("id");
    pm.expect(data).to.have.property("title");
});


---

## ▶️ How to Run the Project

1. Clone this repository
2. Open Postman
3. Import **Postman Collection**
4. Import **Environment Variables**
5. Select the imported environment
6. Run requests in this order:

   * Login
   * Get All Products
   * Create Product
   * Get / Update / Delete Product

---

## 📈 Expected Outcomes

* Successful login and token retrieval
* Dynamic product ID handling for chained requests
* Correct response structures and data types
* Full CRUD operations executed successfully

---

## 👩‍💻 Author

**Heba Ashour**

