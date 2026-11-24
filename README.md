# Proxy Scraper & Parser

A lightweight Python tool that fetches live public proxy lists from the Geonode API, processes the raw payload, and structures the proxy metadata.

---

## 📌 Features

- **Automated Fetching**: Retrieves real-time proxy data from Geonode's public proxy list API.
- **Data Parsing & Cleaning**: Slices and formats raw response data into structured text entries.
- **Simple Execution**: Modular pipeline orchestrating scraping, processing, and organizing in a single run.

---

## 📁 Project Structure

```text
├── main.py            # Entry point that executes the full pipeline
├── web.py             # Fetches proxy data from the Geonode API and saves to data.txt
├── manage.py          # Cleans and formats the raw text/JSON data
├── organize.py        # Organizes and aligns proxy fields
├── requirements.txt   # Project dependencies
└── data.txt           # Output text file storing the processed proxy data
```

---

## 🚀 Getting Started

### 1. Prerequisites

Make sure you have Python 3.8+ installed on your system.

### 2. Clone the Repository

```bash
git clone https://github.com/MCnima/web.git
cd web
```

### 3. Set Up Virtual Environment (Recommended)

Create and activate a virtual environment to manage dependencies cleanly:

- **Linux / macOS:**
  ```bash
  python3 -m venv venv
  source venv/bin/activate
  ```

- **Windows (Command Prompt):**
  ```cmd
  python -m venv venv
  venv\Scripts\activate.bat
  ```

- **Windows (PowerShell):**
  ```powershell
  python -m venv venv
  venv\Scripts\Activate.ps1
  ```

### 4. Install Dependencies

Once your virtual environment is activated, install the required packages:

```bash
pip install -r requirements.txt
```

---

## 🛠 Usage

Run the `main.py` script to fetch, parse, and organize the proxy list:

```bash
python main.py
```

### Execution Flow:
1. **`web.web_scraping()`**: Queries `https://proxylist.geonode.com/api/proxy-list` and saves raw data into `data.txt`.
2. **`manage.condition()` & `manage.proses_data()`**: Strips header/footer padding and normalizes delimiters.
3. **`organize.organize()`**: Iterates through proxy attributes and prints the organized proxy list.

---

## ⚠️ Notes & Troubleshooting

- **Network Access**: Ensure you have an active internet connection. If the request fails, check if the Geonode API endpoint is accessible or if VPN/firewall settings are blocking outbound requests.
- **Output File**: `data.txt` is overwritten during execution to store the latest processed output.

---

## 📄 License

MIT licence