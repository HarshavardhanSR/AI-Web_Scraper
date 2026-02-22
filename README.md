## 📂 Repository Structure

This project is organized into modular components for scraping, AI parsing, and UI interaction.

### 🧠 Core Application Files

- **main.py**  
  Streamlit-based user interface that controls the full workflow.  
  Handles URL input, triggers scraping, manages session state, and displays AI-parsed results.

- **scrape.py**  
  Responsible for web scraping operations using Selenium and BeautifulSoup.  
  Includes logic for:
  - Loading dynamic websites  
  - Extracting body content  
  - Cleaning HTML  
  - Splitting DOM into chunks  

- **parse.py**  
  Implements the AI extraction pipeline using LangChain and Ollama.  
  Processes DOM chunks and extracts user-requested information using natural language prompts.

---

### ⚙️ Configuration & Dependencies

- **requirements.txt**  
  Contains all Python dependencies required to run the project.

- **sample.env**  
  Example environment configuration file for Bright Data Scraping Browser connection.  
  Users should copy this to `.env` and add their credentials.

- **README.md**  
  Project documentation with setup and usage instructions.

---

### 🌐 WebDriver Files

- **chromedriver.exe**  
  Chrome WebDriver executable used by Selenium to automate the browser.

- **chromedriver-win64/**  
  Contains platform-specific ChromeDriver binaries.

- **chromedriver**  
  Additional WebDriver binary (platform dependent).

> ⚠️ Note: Ensure ChromeDriver version matches your installed Chrome browser version.

---

### 🧹 Auto-Generated Files

- **__pycache__/**  
  Python bytecode cache directory automatically created during execution.  
  Not required for source control.

---

## ▶️ How the Project Works

1. User enters a website URL in the Streamlit UI  
2. Selenium loads and scrapes the webpage  
3. HTML content is cleaned and chunked  
4. User describes what data to extract  
5. Ollama LLM processes the content  
6. Extracted information is displayed in the UI

---

## 🔧 Setup Instructions

1. Install dependencies:

```bash
pip install -r requirements.txt
```

2. Create a .env file from sample.env and add your Bright Data credentials.

```bash
SBR_WEBDRIVER="your_brightdata_webdriver_url"
```

3. Run the application:

```bash
streamlit run main.py
```
