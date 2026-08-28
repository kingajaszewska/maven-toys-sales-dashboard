# Maven Toys Sales Dashboard

**Author:** Kinga Jaszewska  
**Tools:** Power BI, Power Query, DAX, data modeling  
**Project type:** Academic sales and profitability analysis

This Power BI project analyzes sales, products, stores, and inventory for Maven Toys, a fictitious chain of toy stores in Mexico. The original dashboard was created as a university project and is preserved in this repository as part of my data analytics portfolio.

## Business objective

The project explores two main questions:

1. How does revenue change over time?
2. Which product categories generate the highest profit?

The source tables also provide a foundation for deeper store and inventory analysis.

## Dataset

The analysis uses the **Mexico Toy Sales** dataset from the [Maven Analytics Data Playground](https://mavenanalytics.io/data-playground/mexico-toy-sales). It contains sales and inventory data for a fictitious retail chain and is published under a Public Domain license.

| Table | Description | Records |
|---|---|---:|
| `sales` | Daily product-level sales transactions | 829,262 |
| `products` | Product names, categories, costs, and prices | 35 |
| `stores` | Store locations and opening dates | 50 |
| `inventory` | Stock on hand by store and product | 1,593 |

The transactions cover the period from **2017-01-01 to 2018-09-30**.

## Key results

The figures below were validated directly against the source CSV files.

| KPI | Result |
|---|---:|
| Units sold | 1,090,565 |
| Revenue | $14,444,572.35 |
| Gross profit | $4,014,029.00 |
| Gross margin | 27.8% |
| Inventory units on hand | 29,742 |
| Inventory value at cost | $300,209.58 |
| Store-product combinations with zero stock | 77 |

### Profit by category

| Category | Gross profit |
|---|---:|
| Toys | $1,079,527 |
| Electronics | $1,001,437 |
| Art & Crafts | $753,354 |
| Games | $673,993 |
| Sports & Outdoors | $505,718 |

Additional observations:

- **Colorbuds** generated the highest product-level profit: $834,944.
- **March 2018** was the highest-revenue month: $883,515.64.
- Toys delivered the most total profit, while Electronics reached a similar result with substantially fewer units sold.

## Power BI report

The current report contains:

- a revenue overview with a date hierarchy;
- profit cards for individual product categories;
- category-level profit comparison visuals;
- DAX measures used to calculate revenue and profit.

GitHub does not display `.pbix` files directly. Download [`Maven_Toys_Sales_Dashboard.pbix`](powerbi/Maven_Toys_Sales_Dashboard.pbix) and open it in Power BI Desktop to view the interactive report. The imported data is stored in the file. To refresh it, update the source paths to the files in `data/raw` and `data/support`.

## Repository structure

```text
maven-toys-sales-dashboard/
├── data/
│   ├── raw/                 # Source sales, product, store, and inventory tables
│   ├── data_dictionary/     # Field definitions
│   └── support/             # Supporting exchange-rate file from the original project
├── powerbi/
│   └── Maven_Toys_Sales_Dashboard.pbix
├── LICENSE
└── README.md
```

## Calculations

The validated summary metrics use the following definitions:

```text
Revenue = Units × Product Price
Gross Profit = Units × (Product Price − Product Cost)
Gross Margin = Gross Profit ÷ Revenue
```

## License

The Maven Analytics dataset is Public Domain. The project documentation and report are available under the MIT License.
