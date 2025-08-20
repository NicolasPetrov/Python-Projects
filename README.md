# Python-Projects
Welcome! This folder contains all my Python projects. Below are brief descriptions and links to the corresponding folders.

## 1) Task Manager - Personal Task Manager
<img width="1433" height="766" alt="task" src="https://github.com/user-attachments/assets/0365780d-d39f-4670-a84a-096a4f5edc36" />

A **personal task manager** with a Flask web UI and **EN/RU localization**. Demonstrates a production-style CRUD app: modular architecture, internationalization, error handling, and an easy deploy setup. Suitable as a starter for learning projects, pet tools, or small internal apps.

**Key Features**
- Tasks: create, edit, complete, delete
- Priorities: **High / Medium / Low**
- Statuses: **Pending / In Progress / Done**
- Due dates with overdue highlighting
- Modern, responsive UI (Bootstrap 5)
- Internationalization (EN/RU, EN by default)
- Storage: SQLite (single DB file) with a simple migration path

**Technical Details**: Python 3.7+, **Flask**, **SQLAlchemy**, **Flask-Babel**, Bootstrap 5, Jinja2  
**Structure (main)**: `app.py`, `run.py` (port 5001), `requirements.txt`, `templates/`, `translations/`

<a href="https://github.com/NicolasPetrov/Task-Manager"><kbd>Learn more →</kbd></a>

---

## 2) Housing Price Predictor
<img width="1429" height="756" alt="458637868-a3fec453-b305-4725-b909-b17fa7b4cb49" src="https://github.com/user-attachments/assets/208b95c9-d474-464f-85c5-917208679b92" />

A **production-ready ML application** for real estate price prediction using **XGBoost**, interpretability (SHAP/LIME), and a **Streamlit web interface**. The project demonstrates the full cycle: data generation/preparation, training with hyperparameter tuning (Optuna), artifact persistence, dashboards, error handling, and a modular architecture. Supports **EN/RU** interface switching.

**Key Features**
- XGBoost + Optuna (10k+ records, automated training)
- Streamlit UI: real-time predictions, data analysis, visualizations
- Interpretability: **SHAP** (feature importance), **LIME** (local behavior)
- Advanced preprocessing: features for location/infrastructure/environment, outlier handling (IQR)
- Metrics: R², RMSE, MAE, MAPE + plots
- Logging, robustness to missing values, structured persistence of models/configs

**Technologies**: Python 3.8+, `xgboost`, `streamlit`, `shap`, `optuna`, `plotly`

**Structure (main)**
- `app.py` — web interface (EN/RU)
- `train_model.py` — automated training & optimization
- `config/config.py` — data/model parameters
- `src/model.py` — XGBoost wrapper (fit/predict/eval)
- `src/data_processing.py` — preprocessing & feature engineering
- `src/visualization.py` — plots & dashboards
- `src/explainer.py` — SHAP/LIME

<a href="https://github.com/NicolasPetrov/Housing-Price-Predictor"><kbd>Learn more →</kbd></a>

---

## 3) GifAnimalBot
<img width="716" height="733" alt="416006986-841a89f5-cbcc-495f-a8d8-2b30b05a368c-2" src="https://github.com/user-attachments/assets/90650fc2-8721-41b7-bd08-fccb5480cac0" />

A Telegram bot built with **aiogram 3.x** that sends random animal GIFs from the **GIPHY API** (cats, dogs, capybaras, parrots, pandas, otters). It includes **usage statistics**, a **size filter (<5MB)** for Telegram compatibility, inline buttons, and resilient error/retry handling. A solid example of an asynchronous bot with a modular architecture.

**Key Features**
- Choose an animal → random GIF
- `/stats` — counter of received GIFs and favorite animals
- Size filtering (<5MB) based on GIPHY size metadata
- Inline buttons: “More”, “Another Animal”
- In-memory GIF caching; de-duplication via JSON persistence
- Network retries and logging

**Technical Details**: Python 3.13, `aiogram` (3.x), `aiohttp`

**Structure (main)**
- `config.py` — tokens (Telegram/GIPHY)
- `gif_manager.py` — fetching/caching/size filtering/persistence
- `keyboards.py` — inline keyboards
- `handlers.py` — commands & callbacks (`/start`, `/stats`)
- `bot.py` — entry point, polling with retries
- `used_gifs.json` — prevents duplicates

<a href="https://github.com/NicolasPetrov/GifAnimalBot"><kbd>Learn more →</kbd></a>



