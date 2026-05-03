# 🔍 AEO Diagnostic Engine

Answer Engine Optimization (AEO) is a web application which simulates how modern AI Search Engines process user queries and checks if your specific brand is being recommended. 

Built with a highly resilient architecture, this tool utilizes custom headless browser automation to securely extract real time AI analytics and product imagery without relying on rate limited, premium APIs.

## Features
* **Custom Headless Scraping:** Utilizes a custom Selenium WebDriver algorithm to bypass anti bot walls and extract live data securely.
* **Keyless AI Integration:** Operates entirely without traditional API keys by routing through public AI gateways, resulting in zero rate limits and zero operational costs.
* **Live Visual Extraction:** Dynamically scrapes real time, product imagery from the web based on the user's specific brand and query.
* **Automated Diagnostics:** Analyzes the generated answer to determine if your brand is visible, and identifies exactly which competitors are currently winning the AI recommendation space.
* **Modern UI/UX:** Built with React, Tailwind CSS, and Framer Motion for a fluid, responsive, and highly polished user experience.

## Installation

### Prerequisites
* Node.js installed
* Python 3.10+ installed
* Google Chrome installed (required for the Selenium WebDriver)

1. Clone or download this repository.

### Backend Setup
2. Navigate to the backend directory:
   `cd backend`
3. Create a virtual environment:
   `python -m venv venv`
4. Activate the environment:
   * Mac/Linux: `source venv/bin/activate`
   * Windows: `venv\Scripts\activate`
5. Install dependencies:
   `pip install -r requirements.txt`

### Frontend Setup
6. Open a new terminal window and navigate to the frontend directory:
   `cd frontend`
7. Install dependencies:
   `npm install`


## Usage

To run the application, you need to start both the backend server and the frontend client simultaneously in two separate terminal windows.

**1. Start the Backend API**
In your backend terminal (with the virtual environment activated), run:
`uvicorn main:app --reload`
*(The backend will run on http://localhost:8000)*

**2. Start the Frontend UI**
In your frontend terminal, run:
`npm run dev`
*(The frontend will run on http://localhost:5173)*

Open your browser to `http://localhost:5173`, enter a customer search query (e.g., "Best noise canceling headphones") and your target brand (E.g., "Sony"), and run your global AEO Audit!
