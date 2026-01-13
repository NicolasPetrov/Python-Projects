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

## 2) GifAnimalBot
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



