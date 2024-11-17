
# Tomato Project 🍅

## Overview
The **Tomato Project** is a full-stack web application designed to manage food orders seamlessly. It provides an admin dashboard for managing orders, users, and food items, along with a backend that handles data operations, API requests, and payment processing using Stripe.

---

## Features
### Frontend
- **Admin Dashboard**:
  - Add, edit, and delete food items.
  - View and manage orders.
  - User management capabilities.
- **Responsive Design**:
  - Optimized for desktop and mobile devices.
- **Modular Architecture**:
  - Reusable components and CSS styles.

### Backend
- **RESTful APIs**:
  - Endpoints for handling users, orders, cart, and food items.
- **Database Integration**:
  - MongoDB for storing persistent data.
- **Payment Gateway**:
  - Stripe integration for secure online payments.

---

## Tech Stack
### Frontend
- **Framework**: React.js
- **Build Tool**: Vite.js
- **Styling**: CSS Modules
- **Package Manager**: npm

### Backend
- **Framework**: Node.js with Express.js
- **Database**: MongoDB
- **Payment Gateway**: Stripe
- **ORM**: Mongoose for database interactions

---

## Installation and Setup

### Prerequisites
Ensure you have the following installed:
- [Node.js](https://nodejs.org/)
- [MongoDB](https://www.mongodb.com/)
- [Stripe Account](https://stripe.com/) to obtain API keys.

### Steps
1. Clone the repository:
   ```bash
   git clone https://github.com/github-adie/tomato.git
   ```

2. Install dependencies for both the frontend and backend:
   - Navigate to the **frontend** directory:
     ```bash
     cd tomato/admin
     npm install
     ```
   - Navigate to the **backend** directory:
     ```bash
     cd tomato/backend
     npm install
     ```

3. Configure environment variables:
   - Create a `.env` file in the backend directory with the following:
     ```env
     PORT=5000
     MONGO_URI=your-mongodb-uri
     STRIPE_SECRET_KEY=your-stripe-secret-key
     STRIPE_PUBLISHABLE_KEY=your-stripe-publishable-key
     ```

4. Start the servers:
   - **Frontend**:
     ```bash
     npm run dev
     ```
   - **Backend**:
     ```bash
     node server.js
     ```

5. Access the application:
   - Frontend: `http://localhost:3000`
   - Backend: `http://localhost:5000`

---

## Project Structure
```
tomato/
├── admin/                     # Frontend
│   ├── src/                   # React components, assets, and pages
│   ├── public/                # Public assets
│   ├── package.json           # Frontend dependencies
│   └── vite.config.js         # Build configuration
├── backend/                   # Backend
│   ├── controllers/           # API logic (user, order, cart, food)
│   ├── config/                # Database and Stripe configurations
│   ├── models/                # MongoDB schemas
│   ├── routes/                # API routes
│   ├── package.json           # Backend dependencies
│   ├── server.js              # Express server
│   └── .env                   # Environment variables
└── README.md                  # Project documentation
```

---

## API Endpoints
### Users
- **POST /api/users**: Create a new user.
- **GET /api/users**: Retrieve all users.

### Orders
- **POST /api/orders**: Place a new order.
- **GET /api/orders**: Get order details.

### Cart
- **POST /api/cart**: Add items to the cart.
- **GET /api/cart**: View cart items.

### Food
- **POST /api/food**: Add a new food item.
- **GET /api/food**: Retrieve food items.

### Payments
- **POST /api/payments**: Create a payment session using Stripe.
- **GET /api/payments/success**: Verify payment success.

---

## Stripe Integration
Stripe has been integrated for processing payments:
1. Backend handles payment intents using the `STRIPE_SECRET_KEY`.
2. Frontend uses `STRIPE_PUBLISHABLE_KEY` to render the Stripe payment interface.
3. Secure payments are processed via Stripe's API and verified on the backend.

---

## Usage
1. **Admin Dashboard**:
   - Log in to manage users, food items, and orders.
   - Add or update food items as needed.
2. **Order Processing**:
   - Place and manage orders.
   - View cart and order history.
3. **Payments**:
   - Complete payments via Stripe's secure interface.

---

## Contributing
Contributions are welcome! To contribute:
1. Fork the repository.
2. Create a new branch:
   ```bash
   git checkout -b feature-name
   ```
3. Commit your changes:
   ```bash
   git commit -m "Add feature description"
   ```
4. Push to your branch:
   ```bash
   git push origin feature-name
   ```
5. Open a Pull Request.

---

## License
This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.

---

## Acknowledgments
- Thanks to the open-source community for libraries and tools used in this project.
- Special thanks to [Stripe](https://stripe.com/) for providing a seamless payment gateway solution.
```
