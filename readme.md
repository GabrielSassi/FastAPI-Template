# FastAPI Template

Minimal, reusable **FastAPI starter project** with:

* Basic API structure
* Health endpoint
* Docker support
* Azure DevOps CI
* Simple test setup

Designed for **quick project bootstrap** with zero architecture overhead.

---

## 📦 Project structure

```
fastapi-template/
├─ app/
│  ├─ __init__.py
│  └─ main.py
├─ tests/
│  └─ test_main.py
├─ requirements.txt
├─ Dockerfile
├─ azure-pipelines.yml
├─ .gitignore
└─ README.md
```

---

## 🚀 Run locally

### 1️⃣ Create virtual environment

```bash
python -m venv .venv
```

Activate:

**Windows**

```bash
.venv\Scripts\activate
```

**Mac/Linux**

```bash
source .venv/bin/activate
```

---

### 2️⃣ Install dependencies

```bash
python -m pip install -r requirements.txt
```

---

### 3️⃣ Run API

```bash
uvicorn app.main:app --reload
```

Open:

* API → http://localhost:8000
* Docs → http://localhost:8000/docs
* Health → http://localhost:8000/health

---

## 🐳 Run with Docker

### Build image

```bash
docker build -t fastapi-template .
```

### Run container

```bash
docker run -p 8000:8000 fastapi-template
```

Access API:

```
http://localhost:8000
```

> Note: Docker uses `0.0.0.0` internally but you must connect via `localhost`.

---

## ✅ Tests

```bash
pytest
```

---

## 🔧 Azure DevOps CI

Pipeline runs:

* Dependency install
* Tests

Triggered on push to `main`.

---

## 🎯 Template usage workflow

1. Create new repo from this template
2. Clone
3. Create endpoints
4. Ship

Keep the template simple — complexity belongs to the project, not the starter.

---

## 🧠 Design philosophy

* Minimal surface area
* Fast experimentation
* Docker-first runtime
* CI-ready
* No premature architecture

---

## 📄 License

Internal template — adapt as needed.