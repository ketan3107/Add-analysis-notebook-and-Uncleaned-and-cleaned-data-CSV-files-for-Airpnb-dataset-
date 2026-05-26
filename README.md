# 🏠 Airbnb NYC 2019 — AI & Data Analysis

> **AI Applications Course Project (M504D)**
> GISMA University of Applied Sciences | Student: Ketan Sharma (GH1044613)

---

## 📌 Project Overview

This project performs a comprehensive **Exploratory Data Analysis (EDA)** and **AI-driven insights** on the publicly available **New York City Airbnb 2019 dataset** — 48,895 listings across all five boroughs.

The goal is to uncover pricing patterns, neighbourhood trends, room-type popularity, and host behaviour insights that help hosts optimise listings and guests make informed booking decisions.

---

## 🗂️ Repository Contents

| File | Description |
|------|-------------|
| AI_APPLICATIONS_(M504D).ipynb | Full analysis notebook — EDA, cleaning, visualisation |
| AB_NYC_2019.csv (uncleaned) | Original raw Airbnb NYC 2019 dataset (48,895 listings) |
| cleaned_AB_data.csv | Cleaned dataset after preprocessing and outlier removal |

---

## 📋 Dataset Overview

- **Source:** NYC Airbnb Open Data 2019
- **Records:** 48,895 listings
- **Features:** 16 columns including neighbourhood, room type, price, availability, reviews

Key columns:
- neighbourhood_group (Bronx, Brooklyn, Manhattan, Queens, Staten Island)
- room_type (Entire home/apt, Private room, Shared room)
- price (nightly rate in USD)
- minimum_nights, number_of_reviews, reviews_per_month
- availability_365, calculated_host_listings_count

---

## 🔄 Workflow

### 1. Data Understanding
- Explored shape (48,895 x 16), dtypes, null counts, duplicates, and unique values
- Identified missing values in: name, host_name, reviews_per_month, last_review

### 2. Data Cleaning
- Dropped rows with null name and host_name fields
- Filled reviews_per_month NaN with 0 (no reviews = no monthly frequency)
- Filled last_review NaN with 'Never_Reviewed'
- Removed outliers: price > threshold, number_of_reviews > 400, availability_365 extremes
- Exported cleaned dataset to cleaned_AB_data.csv

### 3. Exploratory Data Analysis & Business Insights

Answered 5 core business questions through visualisation:

**Q1: Which neighborhoods have the highest average prices?**
- Manhattan: ~$179/night (most expensive)
- Brooklyn: ~$118/night
- Queens & Bronx: ~$85/night (most affordable)

**Q2: What room type is most popular or profitable by area?**
- Entire home/apt dominates Manhattan — guests prefer privacy
- Private rooms are popular in Brooklyn and Queens
- Shared rooms are rare across all boroughs

**Q3: How does host listing count affect review frequency?**
- Multi-listing hosts (2–7 properties) receive more reviews/month than single-listing hosts
- Hosts with 7+ properties see declining review rates (less personal engagement)

**Q4: Which neighbourhood has the best availability?**
- Bronx: 165 days/year average (high availability = lower demand)
- Brooklyn: 100 days/year (most competitive)
- Manhattan: 111 days/year

**Q5: How does minimum nights requirement affect reviews?**
- Listings requiring 1 night minimum get ~1.6 reviews/month
- Listings requiring 7+ nights get under 0.4 reviews/month
- Shorter stays drive significantly more booking frequency

### 4. Correlation Analysis
- Feature correlation heatmap across price, minimum_nights, number_of_reviews, reviews_per_month, availability_365, calculated_host_listings_count
- Price shows weak correlation with review count (-0.057) — expensive listings get fewer reviews

---

## 💡 Key Business Insights

- **Manhattan premium is real:** Entire home/apt listings in Manhattan can command 2x the price of Bronx equivalents.
- **Short stays = more reviews = better visibility:** Hosts should consider flexible minimum night policies to maximise review accumulation and search ranking.
- **Bronx is undervalued:** High availability + low prices signals opportunity for new hosts entering a less competitive market.
- **Multi-listing hosts outperform** in review frequency up to ~7 listings, after which management overhead reduces engagement quality.
- **Price and reviews are weakly linked** — expensive listings don't automatically get more reviews; quality and location matter more.

---

## 🛠️ Tech Stack

- Python, Pandas, NumPy — Data loading and manipulation
- Matplotlib, Seaborn — Visualisation (bar, line, box, heatmap charts)
- Jupyter Notebook — Interactive analysis environment

---

## ▶️ How to Run

```bash
# 1. Clone the repository
git clone https://github.com/ketan3107/Add-analysis-notebook-and-Uncleaned-and-cleaned-data-CSV-files-for-Airpnb-dataset-.git

# 2. Install dependencies
pip install pandas numpy matplotlib seaborn jupyter

# 3. Open the notebook
jupyter notebook "AI_APPLICATIONS_(M504D).ipynb"
```

The cleaned CSV is already provided — no re-cleaning needed.

---

## 👤 Author

**Ketan Sharma** | Roll No: GH1044613
MSc Data Science, AI & Digital Business — GISMA University of Applied Sciences
[LinkedIn](https://www.linkedin.com/in/ketan-sharma-993a0a1b6) | [GitHub](https://github.com/ketan3107)
