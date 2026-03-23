# Deep Search Crawler for Kazakh E-Government Data

This repository contains the implementation and dataset for the paper:

**"Building a Deep Search Crawler for the Kazakh Language: A Reproducible Web-Scale Pipeline"**

---

## 📌 Overview

This project provides a reproducible pipeline for collecting, parsing, and structuring data from the Kazakhstan e-government portal (https://egov.kz).

The system combines:
- Static HTML parsing (requests + BeautifulSoup)
- Optional headless rendering (Selenium / Playwright)
- Automatic extraction of structured fields
- JSON-based data storage

The resulting dataset is designed for **Kazakh-language NLP tasks**, including:
- Text classification
- Named Entity Recognition (NER)
- Information extraction
- LLM fine-tuning

---

## 📂 Repository Structure
├── crawler.py # Main Python scraping script
├── dataset/
│ └── data.json # Collected dataset (sample or full)
├── templates/ # HTML interface (Django)
├── README.md


---

## ⚙️ Requirements

- Python 3.8+
- requests
- beautifulsoup4
- Django (optional for web interface)

Install dependencies:

```bash
pip install requests beautifulsoup4 django
🚀 How to Run
1. Run crawler (basic usage)
python crawler.py

Or using Django interface:

Run server
Open web form
Enter egov.kz URL
🔍 Data Extraction

The crawler extracts the following fields:

url – page URL
category – extracted from breadcrumb navigation
Title – page headings (<h1>)
descriptions – cleaned textual content

Example:

{
  "url": "https://egov.kz/...",
  "category": "Real Estate",
  "Title": ["Service name"],
  "descriptions": ["Text content..."]
}
📊 Dataset Description
Source: egov.kz (public pages)
Total corpus: 915 services across 12 categories
Evaluation subset: 213 pages (stratified sampling)

The dataset represents official-administrative language and is suitable for domain-specific NLP.

♻️ Reproducibility

To ensure reproducibility, the repository includes:

Source code
Data extraction pipeline
JSON output format
Example dataset

The crawling process follows:

Breadth-first traversal
UTF-8 normalization
Structured extraction rules
⚖️ Ethics and Data Usage
Only publicly available data is collected
No authentication required
No personal data is processed
Intended for research purposes only
📎 Notes
Some dynamic content may require headless rendering
Website structure may change over time (DOM updates)
📬 Contact

Author: Assel Ospan
Affiliation: Al-Farabi Kazakh National University
Email: (add your email)

📄 License

This project is released for academic and research purposes.
