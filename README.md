# Airbnb Host Analysis – Bangkok

Exploratory data analysis of Airbnb listings in Bangkok, aimed at helping prospective hosts decide **where** and **what type** of listing to start with.

> Capstone Project 2 – Data Science Bootcamp, Purwadhika
> Author: Vito Muhammad

---

## 1. Background

Airbnb lets travelers rent a room or an entire home from a local host instead of staying in a hotel. Bangkok is one of the most visited cities in the world, so its short-term rental market is large and competitive. This project looks at current listing data to understand how the market is structured and where a new host might find an opportunity.

## 2. Problem Statements

1. Which areas of Bangkok are best for a new Airbnb listing?
2. Which room type offers the best opportunity for a new host?
3. What words appear most often in successful listing titles?

## 3. Data

| Item | Detail |
|---|---|
| File | `data/airbnb_listings_bangkok.csv` |
| Data dictionary | `docs/airbnb_listings_bangkok_data_dictionary.pdf` |
| Source | [isi sumber asli dataset, mis. Inside Airbnb / Kaggle + link] |
| Rows / columns | [isi jumlah baris] / [isi jumlah kolom] |

## 4. Method

1. Data cleaning (missing values, duplicates, outliers) – [jelaskan singkat apa yang kamu lakukan]
2. Descriptive statistics and visualization by area and room type
3. Statistical test to check price differences between room types – [sebutkan uji yang dipakai, mis. Kruskal-Wallis, dan nilai p-nya]
4. Text analysis of listing titles (word frequency)

## 5. Key Findings

| # | Finding |
|---|---|
| 1 | Listings are open for booking a median of **308 days per year**; the remaining days are booked or blocked by the host. |
| 2 | The areas with the most listings are **Vadhana, Khlong Toei, Ratchathewi, Huai Khwang, and Bang Rak**. |
| 3 | **Entire home/apt** is the most common room type [isi persentase, mis. XX%]. |
| 4 | Typical minimum stay is **2 nights** for entire home/apt and **1 night** for other room types. |
| 5 | Price differs significantly between room types ([uji, p = ...]). **Hotel rooms** are the most expensive on average. |
| 6 | The most frequent title words are **bts, room, near, bangkok, sukhumvit, cozy, mrt**. |
| 7 | By number of reviews, **entire home/apt** is the most booked type (assuming review count approximates bookings). |

<!-- Tambahkan 1–2 grafik utama di sini, contoh:
![Listings per area](images/listings_per_area.png)
-->

## 6. Recommendations

1. **Location:** Vadhana and Khlong Toei (both along Sukhumvit) have the highest listing counts, which signals strong demand. Ratchathewi and Huai Khwang are the next options.
2. **Room type:** Focus on entire home/apt, which dominates the market. For a budget listing, the Phra Nakhon (Banglamphu) area is worth exploring.
3. **Titles:** Use frequent search terms such as *BTS, MRT, near, room, view, city* where they honestly describe the property.

> Location notes (tourist attractions, transport access, etc.) are general context rather than outputs of this dataset.

## 7. Limitations

- **Listing count is not profit.** A high number of listings shows demand but also competition. This analysis does not calculate occupancy rate, revenue, or ROI.
- **Review count is only a proxy for bookings**; not every guest leaves a review.
- The data is a **single snapshot**, so seasonality is not captured.
- Availability (308 days) does not show how many days are actually booked.

## 8. Next Steps

- Add price-per-area analysis and an estimated revenue / occupancy model.
- Compare with neighboring cities or hotel prices.
- Build a simple dashboard (Tableau / Streamlit).

## 9. Repository Structure

```
AirBnb-Host-Analysis-Bangkok/
├── data/
│   └── airbnb_listings_bangkok.csv
├── docs/
│   ├── airbnb_listings_bangkok_data_dictionary.pdf
│   └── capstone2_presentation.pdf
├── notebooks/
│   └── bangkok_airbnb_analysis.ipynb
├── images/
├── requirements.txt
├── .gitignore
└── README.md
```

## 10. How to Run

```bash
git clone https://github.com/rgt88/AirBnb-Host-Analysis-Bangkok.git
cd AirBnb-Host-Analysis-Bangkok
pip install -r requirements.txt
jupyter notebook notebooks/bangkok_airbnb_analysis.ipynb
```

## 11. Links

- [Presentation (PDF)](docs/capstone2_presentation.pdf)
- [Notebook](notebooks/bangkok_airbnb_analysis.ipynb)

> **Note:** the notebook uses NLTK stopwords. On first run it downloads them automatically (internet required).
> Tested with Python 3.14 and the library versions in `requirements.txt`.
