# 🐼 Pandas — Basic to Advanced Level Data Analysis

A comprehensive **hands-on Pandas tutorial** covering everything from basic data exploration to advanced data transformation, grouping, querying, and business insights — all performed on the **Global Superstore** dataset (51,290 orders).

---

## 🎯 Objective

To master **Pandas** — Python's most powerful data analysis library — through a structured, progressive notebook that takes you from basic operations (reading data, inspecting columns) all the way to advanced techniques (lambda functions, binning, currency conversion, and business analytics).

---

## 📁 Dataset

**Source:** [Tableau Global Superstore](https://www.tableau.com/sites/default/files/training/global_superstore.zip)

| Detail | Value |
|--------|-------|
| **Rows** | 51,290 orders |
| **Columns** | 24 features |
| **Time Span** | Jan 2011 — Dec 2014 |
| **Markets** | 7 (US, APAC, EU, Africa, EMEA, LATAM, Canada) |
| **Categories** | 3 (Technology, Furniture, Office Supplies) |
| **Sub-Categories** | 17 |

---

## 📚 Topics Covered (140 Cells — Fully Commented)

### 1️⃣ Setup & Data Loading
- Importing Pandas and installing dependencies (`xlrd`)
- Loading Excel files with `pd.read_excel()` with sheet selection

### 2️⃣ Data Exploration
- `head()`, `tail()`, `shape`, `columns`, `dtypes`
- Accessing individual columns — `df["Profit"]`, `df["Ship Mode"]`
- `describe()` for both numeric and non-numeric columns (`include="all"`)

### 3️⃣ Basic Statistical Analysis
- `mean()`, `median()`, `mode()` on numeric columns (Sales, Profit, Discount, Shipping Cost)
- Understanding the difference between `.mean` (Series) vs `.mean()` (value)
- Handling non-numeric columns with statistical functions

### 4️⃣ Filtering & Querying Data
- Boolean filtering — `df[df["Profit"] > 1000]`
- Multi-condition filtering with `&` operator
- Filtering on categorical columns (Segment, City, State, Category)
- Column selection after filtering — `df[condition][["col1", "col2"]]`
- Advanced querying with `df.query()` — string-based conditions
- Complex queries with multiple conditions and `in` operator

### 5️⃣ Adding & Modifying Columns
- Creating new columns — `df["My_column"] = 0`
- `loc[]` and `iloc[]` for precise row-column access
- Modifying individual cell values
- Creating sub-DataFrames with selected columns

### 6️⃣ Applying Functions on Columns
- `apply()` with `lambda` functions for row-wise operations
- Creating computed columns:
  - `Actual Cost` = Sales + Shipping Cost
  - `Actual Cost 1` = Sales - Shipping Cost + (Sales × Discount)
- String concatenation across columns
- Looping through DataFrame rows with `loc[]`

### 7️⃣ GroupBy & Aggregation
- `groupby().min()`, `groupby().max()`, `groupby().sum()`
- Grouping by City, State, Segment, Region, Market, Country
- Multi-level grouping — `groupby(['Category', 'Sub-Category'])`
- Finding `idxmin()` and `idxmax()` for business insights

### 8️⃣ Data Transformation (Binning)
- `pd.cut()` for creating categorical bins from numerical data
- Sales Group — Low / Medium / High
- Profit Group — Low / Medium / High
- Discount Group — Low / Medium / High
- Exploring unique categories with `.unique()`

### 9️⃣ Missing Data Analysis
- `isnull().sum()` for identifying missing values per column
- Handling missing Postal Code data (41,296 nulls)

### 🔟 Business Insights (20+ Analytical Questions Answered)
- City with minimum profit
- State with maximum profit
- Segment with maximum sales
- Most repetitive customer
- Country with minimum shipping cost
- Region with highest shipment cost
- Market with maximum/minimum sales
- Category & Sub-Category with maximum discount
- Category closest to overall mean profit
- Total distinct categories, sub-categories, markets, regions, customers

### 1️⃣1️⃣ Currency Conversion
- Converting Sales, Profit, and Shipping Cost to multiple currencies:
  - Indian Rupees (₹)
  - Japanese Yen (¥)
  - British Pounds (£)

---

## 🛠️ Tech Stack

| Tool | Purpose |
|------|---------|
| **Python 3** | Programming language |
| **Pandas** | Data manipulation & analysis |
| **xlrd** | Reading `.xls` Excel files |
| **Jupyter Notebook** | Interactive development environment |

---

## 🚀 Getting Started

```bash
# Clone the repository
git clone https://github.com/Shaiksameenasulthana/Pandas.git
cd Pandas

# Install dependencies
pip install pandas xlrd jupyter

# Launch Jupyter Notebook
jupyter notebook Basic_to_advancelevel_pandas.ipynb
```

---

## 📂 Project Structure

```
Pandas/
│
├── Basic_to_advancelevel_pandas.ipynb   # Main notebook (140 cells, fully commented)
├── Global Superstore.xls                # Dataset (51,290 orders)
└── README.md                            # Project documentation
```

---

## 💡 Key Learnings

1. **`.mean` vs `.mean()`** — The first returns a method reference, the second actually computes the value
2. **Boolean Indexing** — Combine conditions with `&` and `|`, always wrap each condition in parentheses
3. **`query()` vs Boolean Filtering** — `query()` provides cleaner syntax for complex multi-condition filters
4. **`pd.cut()` for Binning** — Converts continuous numerical data into categorical groups for analysis
5. **`apply()` with `lambda`** — Powerful row-wise operations without explicit loops
6. **`groupby().idxmax()`** — Quickly find which group has the highest/lowest value

---

## 👤 Author

**Shaik Sameena Sulthana**  
GitHub: [@Shaiksameenasulthana](https://github.com/Shaiksameenasulthana)

---

> ⭐ If you found this helpful, please give it a star!
