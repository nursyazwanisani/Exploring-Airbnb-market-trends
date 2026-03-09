# NYC Airbnb Market Trends — Analysis Summary

> DataCamp Data Science Project | 2019 Dataset

---

## 1. Project Overview

This project analyses the New York City Airbnb market using 2019 listing data sourced from three different file formats. The goal was to combine these datasets, clean the data, and extract key insights about pricing, room types, and listing activity across the city.

---

## 2. Data Sources

Three files were loaded and merged on a common `listing_id`:

| File | Format | Contents |
|------|--------|----------|
| `data/airbnb_price.csv` | CSV | Nightly prices and neighbourhood locations |
| `data/airbnb_room_type.xlsx` | Excel | Room type classifications and listing descriptions |
| `data/airbnb_last_review.tsv` | TSV | Host names and most recent review dates |

---

## 3. Key Findings

| Metric | Value |
|--------|-------|
| 📅 First listing reviewed | 1 January 2019 |
| 📅 Last listing reviewed | 9 July 2019 |
| 🏠 Number of private rooms | 11,356 |
| 💰 Average nightly price | USD 141.78 |

### 3.1 Review Activity

The dataset covers listings reviewed between **January and July 2019** — a 6-month window capturing the busy first half of the year, likely including peak spring travel season.

### 3.2 Room Types

**Private rooms are the most common** room type on NYC Airbnb, with 11,356 listings in 2019. This reflects the nature of New York's housing market, where many residents rent out a spare room while still living in the property.

### 3.3 Pricing

The **average nightly price was USD 141.78** across all listings and boroughs. Prices were originally stored as text strings with the word `dollars` appended, which required cleaning before any calculation could be done.

---

## 4. Data Processing Steps

1. Loaded CSV, Excel, and TSV files using `pandas` with appropriate parameters
2. Merged all three datasets using `listing_id` as the common key
3. Converted `last_review` from plain text to Python `datetime` format
4. Standardised `room_type` values to lowercase for consistent filtering
5. Stripped the word `dollars` from price values and converted to `float`
6. Calculated summary statistics: date range, private room count, and average price

---

## 5. Output

```
  first_reviewed last_reviewed  nb_private_rooms  avg_price
0     2019-01-01    2019-07-09             11356     141.78
```

---

## 6. Skills Demonstrated

- Multi-format data ingestion with `pandas` (`.csv`, `.xlsx`, `.tsv`)
- DataFrame merging on shared keys
- Data type conversion and string cleaning
- Date parsing and min/max aggregation
- Boolean filtering to count specific categories
- Summarising results into a clean output DataFrame

---

*Completed as part of the [DataCamp Associate Data Scientist in Python Career Track](https://www.datacamp.com)*
