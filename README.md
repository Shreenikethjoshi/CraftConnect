# CraftConnect

![CraftConnect Banner](https://via.placeholder.com/1200x300.png?text=CraftConnect+-+Empowering+Local+Artisans)

<div align="center">
  <img src="https://img.shields.io/badge/React-18-blue?style=for-the-badge&logo=react" alt="React" />
  <img src="https://img.shields.io/badge/Node.js-Express-green?style=for-the-badge&logo=node.js" alt="Node.js" />
  <img src="https://img.shields.io/badge/MongoDB-Mongoose-brightgreen?style=for-the-badge&logo=mongodb" alt="MongoDB" />
  <img src="https://img.shields.io/badge/Status-Active-success?style=for-the-badge" alt="Status" />
</div>

<br />

**CraftConnect** is a comprehensive e-commerce marketplace dedicated to empowering local artisans and craftsmen. By cutting out the middleman, CraftConnect provides a direct platform for creators to showcase their heritage pottery, woodwork, and handmade goods to a global audience while offering buyers a transparent, authentic shopping experience.

---

## Key Features

### For Buyers
- **Authentic Shopping:** Browse high-quality, handcrafted goods directly from the artisans.
- **Customization Requests:** Request specific modifications to products before purchasing.
- **Secure Checkout & OTP Verification:** Robust security with Razorpay integration and email OTP verification via SendGrid.
- **Order Tracking:** Track your order history and manage your cart intuitively.

### For Artisans
- **Dedicated Dashboard:** A rich, interactive workspace featuring revenue charts, stock alerts, and quick action cards.
- **Product Management:** Easily list new products, edit inventory, and upload images.
- **Order Fulfillment:** Receive and process orders, view customization requests, and update shipping statuses.
- **Split-Revenue Tracking:** Automatic, transparent calculation of earnings per order item.

### For Administrators
- **Platform Analytics:** Deep insights into global order volumes, platform growth, and revenue trends.
- **Marketplace Management:** Define taxonomies (categories), approve/reject new artisan applications, and manage platform users.
- **Customer Support Desk:** Handle support tickets, assign priorities, and communicate with users seamlessly.

---

## Technical Stack

- **Frontend:** React.js 18, Hooks, Context API, Lucide-React (Icons)
- **Backend:** Node.js, Express.js (RESTful API)
- **Database:** MongoDB with Mongoose ODM
- **Integrations:** SendGrid (Emailing), Razorpay (Payments)

---

## Getting Started

Follow these instructions to set up the project locally.

### Prerequisites
- [Node.js](https://nodejs.org/) (v16+)
- [MongoDB](https://www.mongodb.com/) (Local or Atlas URL)

### 1. Clone the repository
```bash
git clone https://github.com/Shreenikethjoshi/CraftConnect.git
cd CraftConnect
```

### 2. Backend Setup
```bash
cd Backend
npm install
```
Create a `.env` file in the `Backend` directory and add the following variables:
```env
PORT=5000
MONGODB_URI=your_mongodb_connection_string
JWT_SECRET=your_jwt_secret
SENDGRID_API_KEY=your_sendgrid_key
RAZORPAY_KEY_ID=your_razorpay_key
RAZORPAY_KEY_SECRET=your_razorpay_secret
```
Start the backend server:
```bash
npm run dev
```

### 3. Frontend Setup
```bash
cd CraftConnect
npm install
```
Create a `.env` file in the `CraftConnect` directory:
```env
REACT_APP_API_URL=http://localhost:5000/api
```
Start the React application:
```bash
npm start
```

---

## Project Structure

```text
CraftConnect/
├── Backend/                 # Node.js + Express Backend
│   ├── src/
│   │   ├── controllers/     # Route logic (admin, auth, cart, order, etc.)
│   │   ├── models/          # Mongoose Schemas (User, Product, Order, etc.)
│   │   ├── routes/          # API definitions
│   │   └── utils/           # Helper functions (email, otp, razorpay)
│   └── package.json
└── CraftConnect/            # React Frontend
    ├── src/
    │   ├── features/        # Role-based feature modules (admin, artisan, shop)
    │   ├── shared/          # Shared components (Navbar, widgets)
    │   └── utils/           # API handlers and Auth hooks
    └── package.json
```

---

## Security & Architecture Highlights

- **Role-Based Access Control (RBAC):** Distinct roles for `user`, `artisan`, and `admin`, dynamically adjusting frontend views and securing backend routes.
- **Real-Time Analytics:** Intelligent client-side grouping of data ensuring database time is accurately normalized to the user's local timezone.
- **Robust Authentication:** Multi-step OTP registration ensuring zero fake accounts, secured via bcrypt hashing and JWT session tokens.
- **Revenue Splitting Algorithm:** Complex cart processing that accurately distributes revenue to multiple artisans from a single user order.

---

> **Note for Recruiters & Developers:** This project demonstrates full-stack proficiency, including complex state management, database schema design for e-commerce, secure authentication flows, and integration with third-party payment and email services.
