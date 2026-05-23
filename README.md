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

## 🛠️ Prerequisites

- **Node.js**: v18 or newer
- **Python**: v3.10 or newer
- **Git**
- **MongoDB**: local `mongod` service or a MongoDB Atlas connection string

> The backend will start with a local fallback connection to `mongodb://127.0.0.1:27017/gearguide`, but setting `MONGO_URI` in `.env` is recommended for predictable local development.

---

## ▶️ Quick Start

### 1. AI Service (Python)

#### Windows PowerShell
```powershell
cd ai_service
python -m venv .venv
.\.venv\Scripts\Activate.ps1
pip install -r requirements.txt
copy .env.example .env
python main.py
```

#### Windows Git Bash, macOS, or Linux
```bash
cd ai_service
python -m venv .venv
source .venv/Scripts/activate  # Git Bash on Windows
# or
source .venv/bin/activate       # macOS/Linux
pip install -r requirements.txt
cp .env.example .env
python main.py
```

### 2. Backend (Node.js)

#### 1) Create your backend environment file
```bash
cd backend
cp .env.example .env
```

#### 2) Install dependencies and start the server
```bash
npm install
node server.js
```

The backend listens on **http://localhost:5000** by default. If you set `PORT` in `.env`, that value is used instead.

#### Backend requirements
- `MONGO_URI`: optional, defaults to `mongodb://127.0.0.1:27017/gearguide`
- `JWT_SECRET`: required for signed auth tokens; use a long random value
- `PORT`: optional, defaults to `5000`

If you do not have MongoDB running locally, either:
1. Start a local MongoDB server (`mongod`), or
2. Set `MONGO_URI` to your MongoDB Atlas connection string.

### 3. Frontend (React + Vite)

```bash
cd frontend
npm install
npm run dev
```

The frontend dev server typically runs on **http://localhost:5173**.

---

## 🔐 Environment Variables

Use the example files below to create your local `.env` files. These files are ignored by Git so your secrets stay local.

### `ai_service/.env.example`
```env
GROQ_API_KEY=your_groq_api_key_here
```

### `backend/.env.example`
```env
MONGO_URI=mongodb://127.0.0.1:27017/gearguide
JWT_SECRET=replace-with-a-long-random-secret
PORT=5000
```

> If you are using a MongoDB Atlas cluster, replace `MONGO_URI` with your connection string.

---

## 🧭 OS-Specific Notes

### Windows
- Use **PowerShell** for `Activate.ps1`.
- If PowerShell blocks the activation script, run:
  ```powershell
  Set-ExecutionPolicy -Scope Process -ExecutionPolicy Bypass
  ```
- If you use **Git Bash**, use `source .venv/Scripts/activate`.

### macOS / Linux
- Use `source .venv/bin/activate` to activate the Python virtual environment.

---

## 🏗️ Tech Stack
- **Frontend**: React, Tailwind CSS, Framer Motion, Three.js (R3F), Recharts.
- **Backend**: Node.js, Express, Mongoose, JWT authentication.
- **AI/ML**: PyTorch, Scikit-Learn, FAISS, Sentence-Transformers, Groq API.
- **Graphics**: @react-three/fiber, @react-three/drei.

---

## 🤝 Contributing

1. Fork the repository.
2. Create a branch for your change.
3. Follow the setup instructions above.
4. Open a pull request with a clear summary of your changes.

---
*Created by [RAJRAUT2324](https://github.com/RAJRAUT2324)*
