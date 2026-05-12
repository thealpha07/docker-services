## MERN stack Monolith Repo
A clone of comprehensive, monolithic MERN stack food delivery application featuring a customer-facing storefront, a secure admin dashboard, and full Stripe payment integration.
## Features

- User Panel
- Admin Panel
- JWT Authentication
- Password Hashing with Bcrypt
- Stripe Payment Integration
- Login/Signup
- Logout
- Add to Cart
- Place Order
- Order Management
- Products Management
- Filter Food Products
- Login/Signup
- Authenticated APIs
- REST APIs
- Role-Based Identification
- Beautiful Alerts

This repository contains three distinct micro-environments:

- **Frontend:** React application (Vite) for the customer store and cart.
    
- **Admin:** React application (Vite) for inventory and order management.
    
- **Backend:** Node.js/Express server acting as the API gateway and connecting to MongoDB.
    

---

## 🛠️ Installation & Setup

**1. Clone the repository**

Bash

```
git clone https://github.com/thealpha07/tomato-monolith.git
cd tomato-monolith
```

**2. Install dependencies** You will need to install the Node modules for all three environments independently.

Bash

```
# Install Frontend dependencies
cd frontend
npm install
cd ..

# Install Admin dependencies
cd admin
npm install
cd ..

# Install Backend dependencies
cd backend
npm install
cd ..
```

---

## 🔐 Environment Variables

This project strictly uses environment variables to maintain security and portability. You must create a `.env` file in **each** of the three main directories.

### Backend (`backend/.env`)

Create a `.env` file inside the `backend` folder and add the following keys:

Code snippet

```
# Security
JWT_SECRET=your_super_secret_jwt_string
SALT=10

# Database (Use the legacy connection string to bypass strict DNS blocks)
MONGO_URL=mongodb://<username>:<password>@cluster-shard-00.mongodb.net:27017/<db-name>?ssl=true&replicaSet=atlas-shard-0&authSource=admin

# Third-Party APIs
STRIPE_SECRET_KEY=sk_test_your_stripe_secret_key_here

# Cross-Origin
FRONTEND_URL=http://localhost:5173

```

### Frontend (`frontend/.env`)

Create a `.env` file inside the `frontend` folder:

Code snippet

```
VITE_BACKEND_URL=http://localhost:4000
```

### Admin (`admin/.env`)

Create a `.env` file inside the `admin` folder:

Code snippet

```
VITE_BACKEND_URL=http://localhost:4000
```

---

## 🏃‍♂️ Running the Application

To run the application locally, you will need to start all three servers in separate terminal windows.

**Terminal 1: Start the Backend Server**

Bash

```
cd backend
npm run dev
```

_(Server should initialize on Port 4000 and log "DB Connected")_

**Terminal 2: Start the Customer Frontend**

Bash

```
cd frontend
npm run dev
```

_(App will be available at http://localhost:5173)_

**Terminal 3: Start the Admin Panel**

Bash

```
cd admin
npm run dev
```

_(App will be available at http://localhost:5174)_

---

## 💳 Testing Payments (Stripe Sandbox)

The application is configured to use Stripe in Test Mode. To simulate a successful checkout:

- **Card Number:** `4242 4242 4242 4242`
    
- **Expiry Date:** Any future date (e.g., `12/28`)
    
- **CVC:** Any 3 digits (e.g., `123`)
  
  
#### Note: 
The credits go to the original developer and no code is owned by me. This is a clone repository for my personal learning.