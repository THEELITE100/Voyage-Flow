# 🔍 AEO Diagnostic Engine (Full-Stack SaaS)

Answer Engine Optimization (AEO) is the evolution of traditional SEO. This decoupled full-stack application simulates how modern AI Search Engines (like ChatGPT, Perplexity, or Gemini) process user queries to determine if a specific brand is actively being recommended to users.

Built with a highly resilient backend architecture, this tool utilizes custom headless browser automation to securely extract real-time AI analytics and product imagery without relying on rate-limited, premium APIs.

## 🚀 Key Features

* **Resilient Data Extraction:** Utilizes `Selenium WebDriver` to navigate anti-bot systems and extract live AI responses and product imagery dynamically.
* **Keyless Architecture:** Operates entirely without traditional API keys by routing through public AI gateways, resulting in zero rate limits and zero operational costs.
* **Modern UI/UX:** Built with React, Tailwind CSS, and Framer Motion for a fluid, responsive, and highly polished user experience.
* **Interactive Data Parsing:** Automatically analyzes raw AI text to detect brand presence and extract competitor lists using dynamic Markdown rendering.
* **Fail-Proof Grace Degradation:** Implements strict error handling to ensure the UI remains intact even if network requests drop.

## 🛠️ Tech Stack

**Frontend:**
* React 18 (Vite)
* Tailwind CSS (Styling & Dark/Light Mode)
* Framer Motion (Complex SVG & Component Animations)
* Lucide React (Iconography)
* React-Markdown (Text parsing)

**Backend:**
* Python 3
* FastAPI & Uvicorn (High-performance API routing)
* Selenium (Headless browser automation)
* Webdriver-Manager (Automated browser binary management)

---

## 💻 Getting Started

To run this application locally, you will need **Node.js**, **Python 3.10+**, and **Google Chrome** installed on your machine.

### 1. Start the Backend (API & Scrapers)

Open a terminal and navigate to the backend directory:

```bash
cd backend
```bash

Create and activate a virtual environment:

```bash
# Windows
python -m venv venv
venv\Scripts\activate

```bash
# Mac/Linux
python3 -m venv venv
source venv/bin/activate

```bash
Install the required Python dependencies:

pip install -r requirements.txt

```bash
Start the FastAPI server:

uvicorn main:app --reload

The backend API will now be running on http://localhost:8000

2. Start the Frontend (UI)

Open a second, separate terminal and navigate to the frontend directory:

```bash
cd frontend

Install the required Node dependencies:

```bash
npm install

Start the Vite development server:

```bash
npm run dev

The frontend application will now be running on http://localhost:5173

🏗️ Architecture Overview
User Input: The React frontend captures the target query and brand.
Concurrent Scraping: FastAPI spins up headless Chrome instances.
Thread A requests visual data from image search engines.
Thread B interacts with a public AI gateway to simulate an Answer Engine response.
Data Structuring: The raw text is cleaned, parsed, and evaluated for brand presence.
Delivery: Structured JSON (including the image URL and Markdown text) is delivered to the frontend for final rendering.
📝 License

This project is built for portfolio and educational demonstration purposes. Data scraping logic is designed for personal use.
