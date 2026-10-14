# Mean Car Prices of Manufacturers

## The problem or research question
Which automobile manufacturers have the highest mean vehicle prices in the UCI automobiles sample, and how are prices distributed across the market?

## Dataset source and usage permissions
- File: `automobiles.csv`
- Source: UCI Automobile Data Set (public educational dataset used in CISC7204 Tutorial 09 / The Data Visualization Workshop).
- Usage: public, non-restricted teaching data. No personal data, passwords, or API keys are included.

## Methods and tools used
Python 3 (Anaconda), pandas group-by aggregation (`mean` of `price` by `make`), and matplotlib scatter / histogram plots. An interactive Bokeh version of the same analysis is in `notebooks/mean_car_prices.ipynb`.

## Key findings and one limitation
Jaguar, Mercedes-Benz, Porsche, and BMW sit at the high end of mean prices; mass-market makes cluster much lower. One limitation is the small, older UCI sample (missing values and a limited set of makes), so results do not represent today's global car market.

## Instructions for running the analysis
```bash
pip install -r requirements.txt
python -c "import pandas as pd; df=pd.read_csv('automobiles.csv'); print(df.groupby('make')['price'].mean().sort_values(ascending=False).head())"
jupyter notebook notebooks/mean_car_prices.ipynb
```
