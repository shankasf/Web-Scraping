# Automated Web Scraper for Survey Files (.pdf & .txt)

> Automatically search, crawl, and download survey-related documents from the web.

---

## 📚 Project Description

This project implements a simple, yet effective, automated scraper designed to:

- Search Google (or any search engine supporting `/search?q=` pattern).
- Find up to **100 survey-related PDF and TXT** files.
- Download and store them locally.
- Avoid duplicate downloads and handle relative URLs.

It is mainly designed for collecting publicly available survey documents such as **election reports**, **public opinion surveys**, and **data sheets**.

---

## ✨ Features

- Dynamically performs Google search based on custom query.
- Extracts websites from search results.
- Crawls websites to find downloadable `.pdf` and `.txt` files.
- Downloads files automatically into a local `downloaded_files` directory.
- Handles relative links, duplicate URLs, and connection errors gracefully.

---

## 🧩 Components

- **search_websites()**: Searches Google and extracts result URLs.
- **process_website()**: Crawls a website and finds PDF/TXT files.
- **download_file()**: Downloads and saves the file.
- **main()**: Controls the scraping loop and limits to 100 downloads.

---

## 🛠️ Technologies Used

- Python
- BeautifulSoup (HTML parsing)
- Requests (HTTP client)
- urllib (URL resolution)
- Standard Python modules (`os`, `queue`, etc.)

---

## 🗃️ Directory Structure

```
survey_scraper/
├── main.py
├── downloaded_files/     # Folder where all downloaded PDFs/TXT will be saved
├── README.md
└── requirements.txt
```

---

## ⚙️ How It Works

1. Accepts a query (default: `USA election survey filetype:pdf OR filetype:txt`).
2. Searches Google for the query.
3. Visits each website from the search results.
4. Finds and downloads PDF/TXT files.
5. Stops once **100 files** are downloaded.

---

## 🟢 How to Run

1. Install requirements:
   ```bash
   pip install -r requirements.txt
   ```
2. Run the program:
   ```bash
   python main.py
   ```

---

## ✅ Notes

- The scraper respects a maximum of 100 files per session.
- Make sure you have a stable internet connection.
- User-Agent is set to mimic a real browser.
- Google may temporarily block you if too many requests are sent too quickly.

---

## ✨ Future Improvements

- Integrate Bing as an alternative search engine.
- Download meta-data (e.g., publication date, author).
- Store download logs.
- Multi-threaded downloading.
- Improve anti-blocking techniques (CAPTCHA handling, proxy rotation).

---

## ✨ Credits

Developed by Sagar Shankaran for research and data collection purposes.

