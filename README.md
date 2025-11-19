# 📘 TMDB Discover – QA Automation Assignment  
**Production-Ready Selenium + PyTest Automation Framework**

This repository contains a complete, production-grade UI test automation framework built for validating the **TMDB Discover Web Application**.  
The solution is implemented using **Python, Selenium WebDriver, PyTest**, and includes robust reporting, screenshots, utilities, modular page objects, and full negative/edge-case validation.

---

## 🚀 1. Overview  
This project automates end-to-end functional testing of key modules of the TMDB Discover website:

- Navigation tabs (Popular, Trend, Newest, Top Rated)  
- Search functionality (positive + negative scenarios)  
- Discover Options:  
  - Type (Movie / TV Shows)  
  - Genre dropdown (full selection validation)  
  - Year range  
  - Ratings filter  
- Scrolling, pagination, dynamic loading  
- Broken image validation (API HEAD requests)  

Every interaction (click/scroll/type) is made reliable using a custom **Safe Actions Utility**, ensuring stable executions without flakiness.

---

## 🧱 2. Project Structure

```
rr-qa-automation-assignment/
│
├── pages/
│   ├── base_page.py
│   ├── discover_page.py
│   └── discover_page_extended.py
│
├── tests/
│   ├── api/
│   │   └── test_api.py
│   └── ui/
│       ├── test_discover_full.py
│       ├── test_discover_navigation.py
│       ├── test_search_and_title.py
│       ├── test_pagination_and_boundaries.py
│       └── test_negative_and_searches.py
│
├── utils/
│   ├── safe_actions.py
│   └── logger.py
│
├── reports/
├── conftest.py
├── pytest.ini
├── requirements.txt
├── run_tests.sh
└── README.md
```

---

## 🔍 3. Testing Strategy

### **1. Functional Validation**
- Tab navigation  
- Search (valid/invalid)  
- Genre & Type dropdown interactions  
- Ratings selector  
- Year range boundaries  
- Poster card loading  

### **2. API-Based Validation**
- Broken poster detection  
- Response code validation  
- Basic feed validation  

### **3. Negative Testing**
- Non-existing movie names  
- Invalid input  
- Long input strings  
- Special characters  

### **4. Boundary Testing**
- Year (1900 – 2024)  
- Ratings min–max  
- Search string boundary  

### **5. Robustness Testing**
- Scroll-to-view  
- Lazy load handling  
- Retry logic  
- JS click fallback  

---

## 🧪 4. Test Design Techniques Used
- **Equivalence Partitioning**  
- **Boundary Value Analysis**  
- **State Transition Testing**  
- **Error Guessing**  
- **Exploratory Testing**  
- **Page Object Model**  

---

## 🧰 5. How to Run the Tests

### Install Dependencies
```bash
python -m venv .venv
source .venv/bin/activate
pip install -r requirements.txt
```

### Run All Tests
```bash
pytest -q --html=reports/all_report.html --self-contained-html
```

### Run UI Tests Only
```bash
pytest tests/ui -q
```

### Headless Mode
```bash
HEADLESS=1 pytest -q
```

---

## 📄 6. Future Enhancements
- GitHub Actions CI  
- PyTest parallel execution  
- Docker support  
- API mock layer  

---

## 👤 Author
**Dinesh**  
QA Automation Engineer  
