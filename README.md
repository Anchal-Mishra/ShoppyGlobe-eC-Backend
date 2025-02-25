# 🛒 ShoppyGlobe E-Commerce Application

Welcome to the **ShoppyGlobe E-Commerce Application**, a powerful and scalable backend built with **Node.js** and **Express.js**, designed to handle user authentication, product management, and cart functionalities efficiently. This project leverages **MongoDB** as the database and **JWT** for secure authentication.

---

## 🚀 Features
✅ User Authentication (Register & Login)  
✅ Product Management (CRUD Operations)  
✅ Cart Functionality (Add, Get, Update, Remove Items)  
✅ Secure Authentication with JWT Middleware  
✅ Modern Tech Stack: Node.js, Express.js, MongoDB, Mongoose  

---

## 🛠 Tech Stack
- **Backend:** Node.js, Express.js
- **Database:** MongoDB, Mongoose
- **Authentication:** JWT, bcrypt.js

---

## 📌 Installation Guide
### 1️⃣ Clone the Repository
```sh
git clone  https://github.com/Anchal-Mishra/ShoppyGlobe-eC-Backend.git
cd your-repo-name
```

### 2️⃣ Install Dependencies
```sh
npm install
```

### 3️⃣ Create a `.env` File
```sh
touch .env
```
Inside `.env`, add the following:
```env
MONGODB_URI=mongodb+srv://<username>:<password>@<cluster>.mongodb.net/<dbname>?retryWrites=true&w=majority
JWT_SECRET=your_jwt_secret_key
PORT=5000
```

### 4️⃣ Start the Server
```sh
npm run dev   # Using nodemon for live reload
# or
node server.js
```

---

## 🔗 API Endpoints
### 🔐 User Authentication
#### ➤ Register User
**Endpoint:** `POST /api/auth/register`
```json
{
  "username": "john_doe",
  "email": "john@example.com",
  "password": "password123"
}
```
#### ➤ Login User
**Endpoint:** `POST /api/auth/login`
```json
{
  "email": "john@example.com",
  "password": "password123"
}
```

### 🛍️ Product Management
#### ➤ Get All Products
**Endpoint:** `GET /api/products`

#### ➤ Get Product by ID
**Endpoint:** `GET /api/product/:id`

#### ➤ Create a Product
**Endpoint:** `POST /api/product`
```json
{
  "name": "Product Name",
  "price": 99.99,
  "description": "Product description"
}
```
#### ➤ Update a Product
**Endpoint:** `PUT /api/product/:id`
```json
{
  "price": 89.99
}
```
#### ➤ Delete a Product
**Endpoint:** `DELETE /api/product/:id`

### 🛒 Cart Management
#### ➤ Add Item to Cart
**Endpoint:** `POST /api/cart`
```json
{
  "productId": "12345",
  "quantity": 2
}
```
#### ➤ Get User Cart
**Endpoint:** `GET /api/cart`

#### ➤ Update Cart Item
**Endpoint:** `PUT /api/cart/:id`
```json
{
  "quantity": 3
}
```
#### ➤ Remove Item from Cart
**Endpoint:** `DELETE /api/cart/:id`

---

## 🔒 Middleware
- `authMiddleware.js` - Protects routes using JWT authentication.

---



