# Docker Installation (Linux / WSL)

Follow the instructions below to install **Docker and Docker Compose v2**.  
These steps work on **Linux and WSL**.

## 1. Update the system

```bash
sudo apt update
sudo apt upgrade -y
```

## 2. Install Docker

```bash
sudo apt install docker.io -y
```

## 3. Allow Docker to run without sudo

```bash
sudo usermod -aG docker $USER
newgrp docker
```

## 4. Install Docker Compose v2

```bash
sudo apt install docker-compose-v2 -y
```

## 5. Verify installation

```bash
docker --version
docker compose version
```

## 6. project run
```docker compose up```


# 🏥 Diagnostic Management System  

A **Full-Stack Medical Appointment Booking & Management Platform** built with modern web technologies.  
This system allows patients to book appointments, doctors to manage schedules, and admins to oversee the entire platform.

---

## 🚀 Features Overview

### 🔐 Core User Roles
- **Patients / Users** – Book appointments, manage profiles  
- **Doctors** – Manage availability, appointments, and profiles  
- **Admins** – Oversee doctors, appointments, and system management  

---

## 👥 User Management
- User Registration & Login with **JWT Authentication**
- Role-Based Authorization (Admin / Doctor / User)
- Doctor Registration & Profile Management
- User Profile Updates with Image Upload (**Cloudinary**)
- Doctor Details:
  - Specialty
  - Experience
  - Consultation Fees
  - Qualifications

---

## 📅 Appointment System
- 📌 Book Appointments (Select doctor, date, and time slot)
- 🗓 Doctor Availability Management
- 📊 Appointment Status:
  - Pending
  - Completed
  - Cancelled
- 📝 Appointment Notes (Admin/Doctor)
- 📜 Appointment History (Per user & doctor)
- ❌ Cancel Appointments (User, Doctor, Admin)

---

## 💳 Payment Processing

Integrated Secure Payment Gateways:

- 🇮🇳 **Razorpay** (India)
- 🌍 **Stripe** (International)
- 🇧🇩 **Aamarpay** (Bangladesh)

Features:
- Payment Verification
- Order Status Tracking
- Success / Failed / Cancel Page Handling

---

## 📊 Dashboard Features

### 🛠 Admin Dashboard
- View all appointments
- Manage doctors
- Monitor statistics

### 👨‍⚕️ Doctor Dashboard
- View scheduled appointments
- Track earnings

### 👤 User Dashboard
- View appointment history
- Manage profile

---

# 🛠 Tech Stack

### Frontend
- React (Vite)
- Tailwind CSS

### Backend
- Node.js
- Express.js
- MongoDB
- Mongoose ODM

### Authentication
- JWT (Role-Based Access Control)

### Storage
- Cloudinary (Image Upload)

### File Upload
- Multer Middleware

---

# 📁 Project Structure

```
diagnostic-management-system/
│
├── admin/        # Admin panel interface
├── frontend/     # User-facing React application
└── backend/      # API server (controllers, routes, middleware)
```

---

# ⚙️ How to Run the Project

## 1️⃣ Clone the Repository

```bash
git clone <your-repo-url>
cd diagnostic-management-system
```

---

## 2️⃣ Setup Backend

```bash
cd backend
npm install
```

### Create `.env` file inside `backend/`

```env
MONGO_URI=your_mongodb_connection_string
JWT_SECRET=your_jwt_secret_key

CLOUDINARY_CLOUD_NAME=your_cloudinary_cloud_name
CLOUDINARY_API_KEY=your_cloudinary_api_key
CLOUDINARY_API_SECRET=your_cloudinary_api_secret

RAZORPAY_KEY_ID=your_razorpay_key_id
RAZORPAY_KEY_SECRET=your_razorpay_key_secret

STRIPE_SECRET_KEY=your_stripe_secret_key

AAMARPAY_STORE_ID=your_aamarpay_store_id
AAMARPAY_STORE_PASSWORD=your_aamarpay_store_password
```

### Start Backend Server

```bash
npm start
```

---

## 3️⃣ Setup Frontend

```bash
cd ../frontend
npm install
npm start
```

Access User Interface:

http://localhost:5173

---

## 4️⃣ Setup Admin Panel

```bash
cd ../admin
npm install
npm run dev
```

Access Admin Panel:

http://localhost:5174

### 🔑 Admin Login Credentials

Email: admin@example.com  
Password: greatstack123  

---

# 🔒 Security Features
- JWT Authentication
- Role-Based Access Control
- Secure Payment Verification
- Protected API Routes
- Environment Variable Configuration

---

# 📌 Project Highlights

✔ Scalable Architecture  
✔ Secure Authentication & Authorization  
✔ Multi-Gateway Payment Integration  
✔ Cloud Image Storage  
✔ Clean & Responsive UI (Tailwind CSS)  
✔ Full Role-Based Dashboard System  

---

# 📄 License
This project is built for educational and development purposes.  
You may modify and use it as needed.
