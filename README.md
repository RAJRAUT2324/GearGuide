# GearGuide | AI Predictive Maintenance Ecosystem

GearGuide is a high-fidelity industrial monitoring system that combines machine learning, 3D digital twins, and LLM-powered technical reasoning to predict and explain equipment failures before they occur.

## 🚀 Key Features

### 1. Sentinel AI Command Center
- **Neural Diagnostics**: Real-time failure probability analysis using Random Forest and Neural Network ensembles.
- **Grok-3 Reasoning**: Automated root cause analysis and technical briefings powered by Groq LLMs.
- **Mission Briefings**: Detailed PDF reports generated automatically for maintenance teams.

### 2. Inventory Machine Dashboard (VajraNet)
- **3D Digital Twin**: Real-time 3D floor visualization with health-coded machine nodes.
- **Onboarding Workflow**: Smart machine registration with auto-fill nomenclature and warranty tracking.
- **Telemetry Drill-down**: Detailed vibration and temperature gradients for individual assets.

### 3. Industrial Data Ingestion
- **PDF Archive**: Indexing and searching legacy maintenance logs using FAISS vector storage.
- **Sensor Simulation**: High-fidelity data stream for demonstration and training.

---

## 🛠️ Installation & Execution

### Prerequisites
- Node.js (v18+)
- Python (v3.10+)
- Git
- MongoDB

---

## 1. Clone the Repository

```bash
git clone https://github.com/RAJRAUT2324/GearGuide.git
cd GearGuide
```

---

## 2. AI Service (Python Backend)

### Windows (PowerShell)

```powershell
cd ai_service

python -m venv .venv

.venv\Scripts\Activate.ps1

pip install -r requirements.txt

python main.py
```

### Linux/macOS

```bash
cd ai_service

python3 -m venv .venv

source .venv/bin/activate

pip install -r requirements.txt

python main.py
```

---

## 3. Node Backend (Proxy & API)

```bash
cd backend

npm install

node server.js
```

The backend runs on the configured `PORT` environment variable.

---

## 4. Frontend (React + Vite)

```bash
cd frontend

npm install

npm run dev
```

---

## ⚠️ Environment Variables

Create `.env` files using the provided `.env.example` templates.

### `ai_service/.env`

```env
GROQ_API_KEY=your_groq_api_key
ML_DATABASE_URL=sqlite:///ml_database.db
```

### `backend/.env`

```env
PORT=5000
MONGO_URI=mongodb://127.0.0.1:27017/gearguide
JWT_SECRET=your_jwt_secret
```

---

## Backend Environment Variables

| Variable | Description |
|---|---|
| PORT | Port used by the Node backend |
| MONGO_URI | MongoDB connection string |
| JWT_SECRET | Secret key used for JWT authentication |

---

## 🏗️ Tech Stack
- **Frontend**: React, Tailwind CSS, Framer Motion, Three.js (R3F), Recharts.
- **Backend**: Node.js, Express, FastAPI, Python.
- **AI/ML**: PyTorch, Scikit-Learn, FAISS, Sentence-Transformers, Groq API.
- **Graphics**: @react-three/fiber, @react-three/drei.

---
*Created by [RAJRAUT2324](https://github.com/RAJRAUT2324)*
