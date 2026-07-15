# 🛒 E-Commerce Sales Analysis & Dashboard

An end-to-end e-commerce data analysis project featuring exploratory data analysis (EDA) in Jupyter Notebook and an interactive Streamlit dashboard for visualizing revenue, products, customers, and sales trends.

---

## 📁 Project Structure

```
ecomerc_analysis/
│
├── data.csv                        # Raw e-commerce dataset (~45 MB)
├── cleaned_ecommerce_data.csv      # Cleaned/preprocessed dataset (~69 MB)
│
├── Ecommerce_Analysis.ipynb        # Jupyter Notebook — full EDA & analysis
├── Ecommerce_dashboard.py          # Streamlit interactive dashboard
│
├── requirements.txt                # Python dependencies
│
├── customer_summary.csv            # Exported customer-level summary data
├── country_revenue.csv             # Exported country-wise revenue data
│
├── correlation_heatmap.png         # Heatmap of feature correlations
├── order_value_distribution.png    # Distribution of order values
├── revenue_by_country.png          # Bar chart — revenue by country
├── sales_by_dayofweek.png          # Bar chart — sales by day of week
├── sales_by_hour.png               # Line chart — sales by hour of day
├── top_customers.png               # Bar chart — top customers by spend
├── top_products_quantity.png       # Bar chart — top products by quantity
├── top_products_revenue.png        # Bar chart — top products by revenue
│
└── README.md                       # Project documentation (this file)
```

---

## 🔍 Analysis Overview

### Data Cleaning & Preprocessing
- Removed rows with missing `Description` values
- Filtered out cancelled orders (invoices starting with `"C"`)
- Excluded records with non-positive `Quantity` or `UnitPrice`
- Derived new features: `TotalPrice`, `Year`, `Month`, `Hour`, `DayOfWeek`, `YearMonth`

### Key Analyses Performed
| Analysis | Description |
|---|---|
| **Monthly Revenue Trend** | Line chart showing revenue over time by year-month |
| **Top Countries by Revenue** | Horizontal bar chart of the top 10 revenue-generating countries |
| **Top Products by Revenue** | Highest revenue-earning products |
| **Top Products by Quantity** | Most frequently purchased products |
| **Order Value Distribution** | Histogram + KDE of order totals |
| **Sales by Day of Week** | Revenue breakdown across weekdays |
| **Sales by Hour** | Hourly revenue patterns throughout the day |
| **Top Customers** | Customer-level aggregation — total spend, order count, average order value |
| **Correlation Heatmap** | Feature correlation matrix for numerical columns |

---

## 📊 Dashboard Features

The **Streamlit dashboard** (`Ecommerce_dashboard.py`) provides:

- **Sidebar Filters** — Filter by country and date range
- **KPI Cards** — Total Revenue, Total Orders, Total Customers, Avg Order Value
- **6 Interactive Charts** — Monthly trend, country revenue, top products, order distribution, day-of-week & hourly revenue
- **Top Customers Table** — Sortable table of highest-spending customers
- **Raw Data Viewer** — Expandable section to inspect filtered data

---

## 🛠️ Tech Stack

| Tool | Purpose |
|---|---|
| **Python** | Core programming language |
| **Pandas / NumPy** | Data manipulation & numerical operations |
| **Matplotlib / Seaborn** | Static visualizations & charts |
| **Plotly** | Interactive visualizations |
| **Scikit-learn** | Machine learning utilities |
| **Streamlit** | Interactive web dashboard |
| **Jupyter Notebook** | Exploratory data analysis |

---

## 🚀 Getting Started

### Prerequisites
- Python 3.8 or higher
- pip (Python package manager)

### Installation

1. **Clone the repository**
   ```bash
   git clone <repository-url>
   cd ecomerc_analysis
   ```

2. **Install dependencies**
   ```bash
   pip install -r requirements.txt
   ```

### Running the Dashboard

```bash
streamlit run Ecommerce_dashboard.py
```

The dashboard will open in your browser at `http://localhost:8501`.

### Running the Notebook

```bash
jupyter notebook Ecommerce_Analysis.ipynb
```

---

## 📈 Sample Visualizations

| Visualization | File |
|---|---|
| Correlation Heatmap | `correlation_heatmap.png` |
| Order Value Distribution | `order_value_distribution.png` |
| Revenue by Country | `revenue_by_country.png` |
| Sales by Day of Week | `sales_by_dayofweek.png` |
| Sales by Hour | `sales_by_hour.png` |
| Top Customers | `top_customers.png` |
| Top Products (Quantity) | `top_products_quantity.png` |
| Top Products (Revenue) | `top_products_revenue.png` |

---

## 📄 Dataset Info

The dataset contains transactional records from a UK-based online retail store. Each row represents a single product line item within an invoice.

| Column | Description |
|---|---|
| `InvoiceNo` | Unique invoice identifier |
| `StockCode` | Product code |
| `Description` | Product description |
| `Quantity` | Number of units purchased |
| `InvoiceDate` | Date and time of the transaction |
| `UnitPrice` | Price per unit (£) |
| `CustomerID` | Unique customer identifier |
| `Country` | Customer's country |

---

## 📝 License

This project is for educational and analytical purposes.
