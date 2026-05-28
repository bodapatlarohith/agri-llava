# 🌿 Agri LLaVA — Leaf Disease Detection System

> A full stack AI-powered plant disease detection system that classifies leaf images as healthy or diseased using a custom CNN model with GradCAM visual explainability.

---

## 📄 Project Overview

**Objective:**
Build an end-to-end AI system where a user uploads a photo of a plant leaf and instantly receives a prediction on whether the leaf is healthy or diseased — with a heatmap showing exactly which region of the leaf influenced the decision.

---

## ✨ Key Features

- 🤖 Custom CNN model trained on a real leaf dataset (healthy / unhealthy classes)
- 🔥 GradCAM heatmap for visual explainability — see what the model focuses on
- 🖼️ Next-stage disease image generation using Diffusion Models
- 🔐 User authentication (login / signup) with JWT
- 📜 Prediction history tracking per user
- 📱 Clean and responsive React frontend
- 🔗 REST API for image upload and real-time prediction

---

## 🛠️ Technologies Used

| Layer | Technology |
|-------|-----------|
| **Frontend** | React.js, Vite |
| **Backend** | Python, Flask |
| **AI Model** | PyTorch (Custom CNN) |
| **Explainability** | GradCAM |
| **Image Generation** | Diffusers (Stable Diffusion) |
| **Database** | MongoDB |
| **Auth** | JWT, bcrypt |

---

## 🏛️ Architecture

```
User uploads leaf image
         │
         ▼
┌─────────────────────┐
│   React Frontend    │  → Image upload, prediction display, history
└────────┬────────────┘
         │ REST API
         ▼
┌─────────────────────┐
│   Flask Backend     │  → Auth, prediction route, GradCAM
└────────┬────────────┘
         │
    ┌────┴────┐
    ▼         ▼
 CNN Model  MongoDB
 (PyTorch)  (History)
```

---

## 💡 How It Works

1. **Upload** — User uploads a leaf image via the React frontend
2. **Predict** — Flask API passes the image through the trained CNN model
3. **GradCAM** — A heatmap is generated showing which region the model focused on
4. **Result** — Prediction (Healthy / Unhealthy) is displayed with the heatmap overlay
5. **History** — All predictions are saved to MongoDB and viewable per user
6. **Generate** — Users can generate next-stage disease visuals using a diffusion model

---

## 🚀 Getting Started

### Prerequisites
- Python 3.8+
- Node.js
- MongoDB

### Installation

**1. Clone the repository**
```bash
git clone https://github.com/bodapatlarohith/agri-llava.git
cd agri-llava
```

**2. Train the model (first time only)**
```bash
cd backend
python train_cnn_model.py
```

**3. Run the backend**
```bash
pip install -r requirements.txt
python app.py
```

**4. Run the frontend**
```bash
cd agri-llava-frontend
npm install
npm run dev
```

**5. Open in browser**
```
http://localhost:5173
```

---

## 📁 Project Structure

```
agri-llava/
├── backend/
│   ├── app.py                  # Flask API
│   ├── train_cnn_model.py      # CNN training script
│   ├── cnn_leaf_model.pth      # Trained model file
│   ├── leaf_dataset/
│   │   ├── healthy/            # Healthy leaf images
│   │   └── unhealthy/          # Diseased leaf images
│   ├── uploads/                # Uploaded images
│   ├── static/gradcam_results/ # GradCAM outputs
│   └── requirements.txt
├── agri-llava-frontend/
│   ├── src/
│   │   ├── components/         # React components
│   │   └── context/            # Auth context
│   └── package.json
└── README.md
```

---

## 🙋 Author

**Rohit**
📧 bodapatlarohithkumar7@gmail.com
📱 7981158530
🔗 GitHub: [bodapatlarohith](https://github.com/bodapatlarohith)
