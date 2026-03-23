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
