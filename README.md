# Jakarta House Price Analysis

An exploratory analysis of about 10,000 house listings in Jakarta to understand what drives prices, where houses are most and least expensive per m², and where first-time buyers can find the most space for their budget.

![Dashboard](images/dashboard_jakarta_house.png)

## Key Findings

- **Building area (r ≈ 0.70) and land area (r ≈ 0.69)** show the strongest relationship with price, well above the number of bedrooms (r ≈ 0.20).
- **Median price per m² varies about 7.4x** across districts: Mega Kuningan is the highest (about Rp78.8 million/m²) and Legenda Wisata the lowest (about Rp10.7 million/m²).
- **Best value districts** by median price per m² include Legenda Wisata, Pulogebang, Klender, and Cibubur, mostly in eastern Jakarta.
- **Jakarta Timur is dominated by budget listings** (about 50%), while Jakarta Pusat (22.6%) and Jakarta Selatan (21.1%) have the largest luxury share.
- **1,095 houses** are priced below the median (Rp4.4 billion) yet have above-median room counts. Jagakarsa, Rawamangun, and Kelapa Gading have the most.

## Dataset

[Jakarta House Price Dataset](https://www.kaggle.com/datasets/abiyyurasyiq/jakarta-house-price-dataset) from Kaggle: 10,000 listings with price, district, city, bedrooms, bathrooms, carport, land area, and building area.

The notebook downloads the data automatically with `kagglehub`, so no manual download is needed.

## Methodology

1. **Data understanding:** structure and descriptive statistics
2. **Cleaning:** removed missing values, investigated outliers (IQR and manual inspection), and filtered unrealistic listings (9,992 to 9,605 rows)
3. **Feature engineering:** price per m², price category (by quartile), total rooms, building ratio, carport category
4. **EDA:**
   - Median price per m² by district (minimum 10 listings)
   - Effect of bedrooms and carports on price
   - Price segment mix per city
   - Correlation analysis
   - Value-for-money districts and a first-time-buyer "sweet spot"
5. **Dashboard:** six summary charts
6. **Conclusion:** findings, recommendations, and limitations

## Limitations

- Data likely reflects asking prices, not final transaction prices.
- Some categories (e.g., houses with very many bedrooms) have small samples, and a few extreme values remain.
- The analysis is descriptive: correlation does not imply causation, and no prediction model is included yet.

## Tech Stack

Python, Pandas, Matplotlib, Seaborn, kagglehub

## How to Run

Open `Analisis_Harga_Rumah_Jakarta.ipynb` in Google Colab or Jupyter and run all cells.

```bash
pip install pandas matplotlib seaborn kagglehub[pandas-datasets]
```

Kaggle version: [Kaggle](https://www.kaggle.com/code/salsabilaarfanaulia/analisis-harga-rumah-jakarta)

## Author

Salsabila Arfan Aulia | Software Engineering Technology, IPB University
[LinkedIn](https://linkedin.com/in/salsabila-arfan-aulia-909637342)
