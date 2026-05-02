# 🛒 Retail Product Scrapers (Modern Trade Analysis)

A Python-based scraping toolkit to extract and analyze product data across major modern retail chains in India.

This project is designed for **SKU benchmarking, private label tracking, and category-level analysis** using direct API scraping and intelligent filtering logic.

---

## Supported Platforms

* JioMart (Single + Multi-brand scraping)
* Nature’s Basket
* DMart
* Le Marche

---

## 🚀 Key Features

### Smart Product Filtering

* Multi-word relevance scoring
* Synonym-based matching (Indian + English)
* Dynamic threshold filtering:

  * 1–2 words → 100% match required
  * 3 words → 67%
  * 4+ words → 50%

### Advanced Logic

* Multipack filtering (removes combos/bundles)
* Category validation (ensures product type relevance)
* Private label detection (e.g., Reliance brands)
* Exact brand matching (for multi-brand scraping)

### Output Formats

* Structured Excel reports
* Console output (for quick debugging)
* Multi-sheet outputs:

  * Products Found
  * Removed Items
  * Summary

---

## Installation

Clone the repository:

```bash
git clone https://github.com/Gods-Hell/retail-product-scrapers.git
cd retail-product-scrapers
```

Install dependencies:

```bash
pip install -r requirements.txt
```

---

##  Requirements

Create a `requirements.txt` file with:

```
requests
openpyxl
```

---

##  Usage

Run individual scrapers:

```bash
python dmart_api.py
python natures_api.py
python jiomart_api.py
python jiomart_multibrand.py
python le_marche_api.py
```

---

## Important Notes

### API Tokens (JioMart)

Some scripts require fresh authentication tokens.

* Update:

  * `BEARER_TOKEN`
  * `COOKIE`
  * `x-fp-signature`

These expire frequently and must be refreshed from browser network calls.

---

### Location-Based Results

* APIs use location headers (latitude, pincode)
* Product availability may vary by region

---

### Rate Limiting

* Scripts include delays to avoid blocking
* Avoid aggressive parallel execution

---

## Example Use Cases

* SKU benchmarking across retail chains
* Private label identification
* Category gap analysis
* Pricing intelligence
* Competitive product mapping

---

## Project Structure (Recommended)

```
retail-product-scrapers/
│
├── scrapers/
│   ├── dmart_api.py
│   ├── natures_api.py
│   ├── jiomart_api.py
│   ├── jiomart_multibrand.py
│   ├── le_marche_api.py
│
├── output/
│
├── requirements.txt
├── README.md
```

---

##  Author

Developed as part of a **Modern Trade Retail Analysis Project**, focused on SKU intelligence and institutional sales insights.

---

## Future Improvements

* CLI interface (single command execution)
* Config file for tokens and settings
* Logging system (instead of print)
* Docker support for deployment

---
