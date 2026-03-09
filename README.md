# 🗽 Exploring Airbnb Market Trends — New York City

> A DataCamp Data Science bonus project exploring NYC Airbnb listings using multi-format data ingestion and analysis.

![NYC Airbnb](https://github.com/user-attachments/assets/4dd3aa17-9be6-4d93-b8cb-212c24eeb362)

---

## 📌 Project Overview

New York City is one of the most-visited cities in the world, and its Airbnb market reflects that — with thousands of listings ranging from short overnight stays to multi-month lodging. This project takes a closer look at the NYC Airbnb landscape by combining data from **three different file formats**: `.csv`, `.tsv`, and `.xlsx`.

The goal is to merge and analyse these datasets to surface key trends around pricing, room types, and listing activity across NYC's boroughs and neighbourhoods.

---

## 🗂️ Dataset

All data covers **2019 Airbnb listings** in New York City, split across three source files:

| File | Format | Description |
|------|--------|-------------|
| `data/airbnb_price.csv` | CSV | Listing prices and locations |
| `data/airbnb_room_type.xlsx` | Excel | Room types and listing descriptions |
| `data/airbnb_last_review.tsv` | TSV | Host names and last review dates |

### Column Reference

**`airbnb_price.csv`**
- `listing_id` — Unique identifier of listing
- `price` — Nightly listing price in USD
- `nbhood_full` — Borough and neighbourhood name

**`airbnb_room_type.xlsx`**
- `listing_id` — Unique identifier of listing
- `description` — Listing description
- `room_type` — One of: `Shared room`, `Private room`, `Entire home/apt`

**`airbnb_last_review.tsv`**
- `listing_id` — Unique identifier of listing
- `host_name` — Name of the listing host
- `last_review` — Date of the most recent review

---

## 🛠️ Skills Demonstrated

- **Multi-format data ingestion** — Reading `.csv`, `.xlsx`, and `.tsv` files with `pandas`
- **Data merging** — Joining multiple DataFrames on a common key (`listing_id`)
- **Data cleaning** — Handling inconsistent text casing, date parsing, and type conversion
- **Exploratory Data Analysis (EDA)** — Summarising price distributions, room type breakdowns, and review activity
- **Filtering & aggregation** — Borough-level and neighbourhood-level comparisons

---

## 🚀 Getting Started

### Prerequisites

```bash
pip install pandas openpyxl
```

### Run the Notebook

```bash
jupyter notebook airbnb_market_trends.ipynb
```

---

## 📊 Key Questions Explored

- What is the average nightly price across NYC boroughs?
- How are room types distributed across listings?
- Which listings have the most recent reviews?
- What are the most active neighbourhoods on Airbnb?

---

## 📁 Project Structure

```
├── data/
│   ├── airbnb_price.csv
│   ├── airbnb_room_type.xlsx
│   └── airbnb_last_review.tsv
├── airbnb_market_trends.ipynb
└── README.md
```

---

## 🎓 Course

This project was completed as part of the **DataCamp Associate Data Scientist in Python** career track.

---
