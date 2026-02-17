# Sentiment Analyzer (Mistral)

An AI-powered Sentiment Analysis web application that classifies input text as **Positive**, **Negative**, or **Neutral** using the **Mistral** model via **Ollama**.

Built with:

* ⚡ FastAPI (Backend API)
* 🎨 Streamlit (Frontend UI)
* 🧠 Mistral (Local LLM Inference)

---

## 🚀 Project Overview

This project demonstrates how to build a full-stack AI application using:

* A locally hosted Large Language Model
* A REST API backend
* An interactive web frontend

The application allows users to input a sentence and instantly receive its sentiment classification.

---

## 🎯 Features

* Classifies text as:

  * ✅ Positive
  * ❌ Negative
  * ⚪ Neutral
* Fully local LLM (No OpenAI API required)
* Simple and clean UI
* FastAPI-based REST backend
* Streamlit-based frontend
* Easy to deploy and extend

---

## 🏗️ Technology Stack

| Component     | Technology |
| ------------- | ---------- |
| LLM Model     | Mistral    |
| LLM Runtime   | Ollama     |
| Backend       | FastAPI    |
| Frontend      | Streamlit  |
| HTTP Requests | Requests   |
| Server        | Uvicorn    |

---

## 📂 Project Structure

```
sentiment-analyzer-mistral/
│
├── backend/
│   └── main.py
│
├── frontend/
│   └── app.py
│
├── requirements.txt
└── README.md
```

---

## ⚙️ Installation & Setup

### 1️⃣ Clone the Repository

```bash
git clone https://github.com/aqsa-hafeez/sentiment-analyzer-mistral.git
cd sentiment-analyzer-mistral
```

---

### 2️⃣ Create Virtual Environment

```bash
python -m venv venv
```

Activate:

**Windows**

```bash
venv\Scripts\activate
```

**Mac/Linux**

```bash
source venv/bin/activate
```

---

### 3️⃣ Install Dependencies

```bash
pip install -r requirements.txt
```

If needed:

```bash
pip install python-multipart
```

---

### 4️⃣ Install & Pull Mistral Model (Ollama)

Make sure Ollama is installed and running.

Pull the model:

```bash
ollama pull mistral
```

---

## ▶️ Running the Application

### Step 1: Start Backend

```bash
uvicorn backend.main:app --reload
```

Backend will run at:

```
http://127.0.0.1:8000
```

You can verify using:

```
http://127.0.0.1:8000/docs
```

---

### Step 2: Start Frontend

Open a new terminal (do not stop backend):

```bash
streamlit run frontend/app.py
```

The browser will open automatically.

---

## 🧪 Example Test Inputs

### Positive

```
I absolutely love this product!
```

### Negative

```
This is the worst experience ever.
```

### Neutral

```
The meeting is scheduled for tomorrow.
```

---

## 🔄 How It Works

1. User enters text in Streamlit UI
2. Frontend sends request to FastAPI backend
3. Backend sends prompt to Mistral model via Ollama
4. Model returns sentiment
5. Result is displayed in the UI

Architecture Flow:

```
Streamlit → FastAPI → Ollama → Mistral → Response → Streamlit
```

---
