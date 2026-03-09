# Exploring Airbnb Market Trends — New York City

> A DataCamp Data Science bonus project exploring NYC Airbnb listings using multi-format data ingestion and analysis.

![NYC Airbnb](https://github.com/user-attachments/assets/4dd3aa17-9be6-4d93-b8cb-212c24eeb362)

---

## 1. Project Overview

New York City is one of the most-visited cities in the world, and its Airbnb market reflects that — with thousands of listings ranging from short overnight stays to multi-month lodging. This project takes a closer look at the NYC Airbnb landscape by combining data from **three different file formats**: `.csv`, `.tsv`, and `.xlsx`.

The goal is to merge and analyse these datasets to surface key trends around pricing, room types, and listing activity across NYC's boroughs and neighbourhoods.

---

## 2. Dataset

All data covers **2019 Airbnb listings** in New York City, split across three source files:

| File | Format | Description |
|------|--------|-------------|
| `data/airbnb_price.csv` | CSV | Listing prices and locations |
| `data/airbnb_room_type.xlsx` | Excel | Room types and listing descriptions |
| `data/airbnb_last_review.tsv` | TSV | Host names and last review dates |

### 2.1 Column Reference

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

## 3. Data Processing Steps

1. Loaded CSV, Excel, and TSV files using `pandas` with appropriate parameters
2. Merged all three datasets using `listing_id` as the common key
3. Converted `last_review` from plain text to Python `datetime` format
4. Standardised `room_type` values to lowercase for consistent filtering
5. Stripped the word `dollars` from price values and converted to `float`
6. Calculated summary statistics: date range, private room count, and average price

---

## 4. Skills Demonstrated

- **Multi-format data ingestion** — Reading `.csv`, `.xlsx`, and `.tsv` files with `pandas`
- **Data merging** — Joining multiple DataFrames on a common key (`listing_id`)
- **Data cleaning** — Handling inconsistent text casing, date parsing, and type conversion
- **Exploratory Data Analysis (EDA)** — Summarising price distributions, room type breakdowns, and review activity
- **Filtering & aggregation** — Borough-level and neighbourhood-level comparisons

---

## 5. Project Structure

```
├── data/
│   ├── airbnb_price.csv
│   ├── airbnb_room_type.xlsx
│   └── airbnb_last_review.tsv
├── notebook.ipynb
└── README.md
```

---

##  6. Key Findings

| Metric | Value |
|--------|-------|
| 📅 First listing reviewed | 1 January 2019 |
| 📅 Last listing reviewed | 9 July 2019 |
| 🏠 Number of private rooms | 11,356 |
| 💰 Average nightly price | USD 141.78 |

### 6.1 Review Activity

The dataset covers listings reviewed between **January and July 2019** — a 6-month window capturing the busy first half of the year, likely including peak spring travel season.

### 6.2 Room Types

**Private rooms are the most common** room type on NYC Airbnb, with 11,356 listings in 2019. This reflects the nature of New York's housing market, where many residents rent out a spare room while still living in the property.

### 6.3 Pricing

The **average nightly price was USD 141.78** across all listings and boroughs. Prices were originally stored as text strings with the word `dollars` appended, which required cleaning before any calculation could be done.

---

## 7. Output

```
  first_reviewed last_reviewed  nb_private_rooms  avg_price
0     2019-01-01    2019-07-09             11356     141.78
```

## 8. Course

This project was completed as part of the **DataCamp Associate Data Scientist in Python** career track.


