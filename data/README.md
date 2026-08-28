# Data

Source: [Maven Analytics — Mexico Toy Sales](https://mavenanalytics.io/data-playground/mexico-toy-sales)  
Dataset license: Public Domain

## Raw tables

- `sales.csv` — 829,262 daily sales transactions from 2017-01-01 to 2018-09-30.
- `products.csv` — 35 products with category, cost, and retail price.
- `stores.csv` — 50 stores in Mexico with city, location type, and opening date.
- `inventory.csv` — 1,593 store-product inventory records.

The corresponding field definitions are stored in `data_dictionary/`.

The file in `support/` is a supporting exchange-rate table preserved from the original academic project. It is not part of the official Maven Analytics dataset.

All source tables were checked for missing values and duplicate sale identifiers. No missing values or duplicate `Sale_ID` records were found.
