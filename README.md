# 🏥 HMIS Backend

Hospital Medical Information System (HMIS) — Backend built with **Node.js**, **Express**, **Sequelize ORM**, and **PostgreSQL**.  
This project manages patients, staff, appointments, billing, pharmacy, diagnostics, ICU beds, and more.

---

## 📂 Features
- Patient registration & management  
- Staff & department management  
- Appointment scheduling & status tracking  
- Billing and payments  
- Diagnostics test management  
- Pharmacy medicines & prescriptions  
- ICU bed allocation & monitoring  
- Basic user authentication (admin, staff, patient)  

---

## ⚙️ Tech Stack
- **Backend**: Node.js + Express  
- **Database**: PostgreSQL with Sequelize ORM  
- **Authentication**: JWT + bcrypt (password hashing)  
- **REST APIs**: Role-based endpoints (patients, staff, appointments, pharmacy, etc.)  

---

## 🚀 Getting Started

### 1️⃣ Clone the repository
```bash
git clone https://github.com/your-username/hmis-backend.git
cd hmis-backend
```

### 2️⃣ Install dependencies
```bash
npm install
```

### 3️⃣ Configure Database
Edit `config/database.js` or set environment variables:
```bash
export PG_DB=hmisdb
export PG_USER=postgres
export PG_PASS=yourpassword
export PG_HOST=localhost
```

### 4️⃣ Create Database
```bash
createdb hmisdb
```

### 5️⃣ Seed Database
⚠️ This will **drop and recreate** tables with sample data.
```bash
npm run seed
```

### 6️⃣ Run Server
```bash
npm run dev
```

Server will start at:  
👉 `http://localhost:3000`

---

## 📡 API Endpoints

### Patients
- `GET /api/patients` → List patients  
- `POST /api/patients` → Register patient  

### Appointments
- `GET /api/appointments` → List appointments  
- `POST /api/appointments` → Schedule appointment  

---

## ✅ Sample Output

### GET `/api/patients`
```json
[
  {
    "patient_id": 1,
    "first_name": "PatientFN1",
    "last_name": "PatientLN1",
    "gender": "Male",
    "dob": "1981-01-01T00:00:00.000Z",
    "contact": "8000000001",
    "email": "patient1@example.com",
    "address": "Address line 1",
    "medical_history": "No major history"
  }
]
```

### GET `/api/appointments`
```json
[
  {
    "appointment_id": 1,
    "patient_id": 1,
    "doctor_id": 1,
    "appointment_time": "2025-09-12T10:00:00.000Z",
    "status": "scheduled",
    "reason": "General consultation"
  }
]
```

---

## 👥 Default Users
| Username | Password    | Role   |
|----------|------------|--------|
| admin    | adminpass  | admin  |
| staff1   | staffpass  | staff  |
| patient1 | patientpass| patient|

---

## 📌 Next Steps
- [ ] Add full JWT-based authentication & role guards  
- [ ] Expand routes (billing, pharmacy, diagnostics)  
- [ ] Add frontend (React or Angular)  
- [ ] Deploy with Docker + Docker Compose  

---

🔗 Once you push, your repo will look like:  
👉 `https://github.com/your-username/hmis-backend`
