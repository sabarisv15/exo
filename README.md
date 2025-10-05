# 🪐 EXORC – Exoplanet Classifier (AI Model)

> **An AI-powered Exoplanet Classification System using NASA Kepler Dataset + Random Forest + Pyodide Frontend**

[![Python](https://img.shields.io/badge/Python-3.11-blue?logo=python&logoColor=white)](https://www.python.org/)
[![Pyodide](https://img.shields.io/badge/Pyodide-0.24.1-008080?logo=python&logoColor=white)](https://pyodide.org/en/stable/)
[![VSCode Live Server](https://img.shields.io/badge/Live%20Server%20Extension-VSCode-0078D7?logo=visualstudiocode&logoColor=white)](https://marketplace.visualstudio.com/items?itemName=ritwickdey.LiveServer)
[![Ngrok](https://img.shields.io/badge/Ngrok-Tunnel%20Service-FF69B4?logo=ngrok&logoColor=white)](https://ngrok.com/)

---

## 🔭 Overview

**EXORC (Exoplanet Orbit Recognition Classifier)** is a machine learning model that identifies whether a celestial candidate is:
- 🟢 **CONFIRMED**
- 🟡 **CANDIDATE**
- 🔴 **FALSE POSITIVE**

Built on NASA’s **Kepler cumulative exoplanet dataset**, this project combines:
- A **Random Forest Classifier** (600 estimators)
- A **Pyodide + HTML frontend** to execute AI in the browser
- **Ngrok tunneling** for global access to your local app

---

## 🌌 Features

✅ Cleans and preprocesses NASA’s dataset (`cumulativefiltered.csv`)  
✅ Handles missing values automatically  
✅ Encodes categorical target (`koi_disposition`)  
✅ Trains a **RandomForestClassifier** and saves it as `exo_planet.pkl`  
✅ Predicts exoplanet type from custom KOI inputs  
✅ Runs fully in-browser (via Pyodide, no backend needed)  
✅ Accessible globally using **Ngrok**

---

## 🧠 Model Pipeline

| Step | Process | Library |
|------|----------|----------|
| 1️⃣ | Load and clean data | `pandas` |
| 2️⃣ | Encode labels | `LabelEncoder` |
| 3️⃣ | Split dataset (80/20) | `train_test_split` |
| 4️⃣ | Train Random Forest (600 trees) | `scikit-learn` |
| 5️⃣ | Evaluate model (Accuracy ≈ 76%) | `accuracy_score` |
| 6️⃣ | Save trained model | `pickle` |
| 7️⃣ | Predict based on frontend input | `Pyodide + JS` |

---

## 🧩 Repository Structure

```
📁 EXORC-Exoplanet-Classifier/
│
├── EXO Project.ipynb          # Jupyter notebook for model training
├── cumulativefiltered.csv     # NASA exoplanet dataset
├── exo_planet.pkl             # Trained RandomForest model
├── index.html                 # Web interface (Pyodide-based)
├── style.css                  # Custom dark theme styling
└── README.md                  # You’re reading it!
```

---

## ⚙️ Installation & 🧬 To Run the Model (Notebook)

1. Clone this repo:
   ```bash
   git clone https://github.com/sabarisv15/exo.git
   cd exo
   ```
2. Open `index.html` and run all cells.  
   
---

## 🌐 Web App with Pyodide + Ngrok

### Step 1: Start Local Server
Install Live server extension in VSCode:


### Step 2: Expose It Using Ngrok
Right click index.html file and click on Open with live server option.

### Step 3: Expose It Using Ngrok
```
ngrog http 5500
```

Ngrok will provide a **public URL** (for example):
```
https://abcd1234.ngrok.io
```

### Step 4: Access the Web App
Open the generated URL — you’ll see:

> 🔭 **Exoplanet Classifier – Run EXORC**  
> Enter KOI parameters → click 🚀 *Execute* → get instant prediction.

---

## 🧪 Sample Input Parameters

| Parameter | Example |
|------------|----------|
| koi_period | 9.48 |
| koi_time0bk | 170.53 |
| koi_duration | 2.95 |
| koi_depth | 616.0 |
| koi_prad | 2.26 |
| koi_snr | 35.8 |
| koi_steff | 5455 |
| koi_srad | 0.927 |
| koi_smass | 0.919 |
| koi_kepmag | 15.347 |

---

## 📊 Example Output

```
RandomForestClassifier Accuracy: 0.7616
Predicted class: CONFIRMED
```

---

## 🌍 Live Demo (via Ngrok)

When Ngrok is running, share your public link:

```
🌐 https://your-ngrok-url.ngrok.io
```

Anyone with the link can run the classifier live — no setup required!

---

## 🧩 Tech Stack

| Component | Technology |
|------------|-------------|
| ML Backend | Python, scikit-learn |
| Dataset | NASA Kepler Archive |
| Frontend | HTML, JS, Pyodide |
| Deployment | Ngrok |
| Visualization | Pandas, Seaborn |

---



## 👨‍🚀 Team

**Developed by:**  
> ******
> ******

**Powered by:**  
🌌 NASA Exoplanet Archive  
🧠 Pyodide  
🌍 Ngrok  

---

## 🪐 License
This project is released under the [MIT License](LICENSE).
