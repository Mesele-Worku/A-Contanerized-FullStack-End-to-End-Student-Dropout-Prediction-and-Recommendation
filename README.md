# 📦 Student Dropout Prediction App (Full-Stack)

This is a full-stack application that predicts student dropout risk using a machine learning model. It includes:

- 🌐 **Frontend**: React (Vite or CRA) + Nginx
- 🧠 **ML API**: Flask + XGBoost
- 🚀 **Backend**: Node.js + Express
- 🐳 **Containerized**: Using Docker & Docker Compose

---

## 📁 Project Structure

```
project/
├── client/              # React frontend
├── server/              # Node.js backend
├── ML_API/              # Flask ML service
├── docker-compose.yml   # Compose setup
└── README.md            # You're here
```

---

## ⚙️ Requirements

- Docker & Docker Compose

### ✅ Install Docker

[Download Docker Desktop](https://www.docker.com/products/docker-desktop)

Verify installation:

```bash
docker -v
docker-compose -v
```

---

## 🔐 Environment Variables

### 1. `client/.env`

```
VITE_LEX_BOT_ID=your-lex-bot-id
VITE_LEX_BOT_ALIAS_ID=your-alias-id
VITE_AWS_REGION=us-east-1
VITE_AWS_IDENTITY_POOL_ID=us-east-1:xxxx
```

### 2. `ML_API/.env`

```
AWS_ACCESS_KEY_ID=your-access-key
AWS_SECRET_ACCESS_KEY=your-secret-key
MAIL_FROM=you@example.com
MAIL_TO=student@example.com
AWS_REGION=us-east-1
```

> ❗ Do NOT commit your `.env` files. They should be listed in `.gitignore`.

---

## 🐳 Running the App with Docker

### 1. Build All Containers

```bash
docker-compose build
```

### 2. Start All Services

```bash
docker-compose up
```

### 3. Stop Services

```bash
docker-compose down
```

---

## 🚀 Access the App

- **Frontend**: http://localhost:3000
- **Backend**: http://localhost:4000
- **ML API**: http://localhost:5000

---

## 🔄 Updating the App

If you change the code:

```bash
docker-compose up --build
```

---

## 🧪 Testing the API

```bash
curl -X POST http://localhost:4000/api/predict   -H "Content-Type: application/json"   -d '{
    "lecture_watch_pct": 80,
    "checklist_pct": 90,
    "attended_live_class": 1,
    "attended_group_discussion": 1,
    "qa_participation_pct": 75,
    "student_email": "test@example.com",
    "student_name": "Test Student"
  }'
```

---

## 📘 Educational Resource

This project includes a full educational guide that explains how to containerize the application step-by-step with comments:

> **File**: `Containerize Apps Guide.txt`

Use this as a learning reference or to onboard collaborators.

---

## 📄 License

Educational Use Only

---

## 🙌 Contributing

Pull requests are welcome. Please make sure any contributions follow the existing style and include proper testing.

---

## 💬 Contact

For questions or collaboration:

- Email: meselew2112@gmail.com
- LinkedIn: [Mesele Worku](https://linkedin.com/in/mesele-worku)
