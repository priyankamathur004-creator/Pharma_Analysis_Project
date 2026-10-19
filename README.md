#  Pharma Product Analytics & Market Intelligence

##  Project Overview

**Pharma Product Analytics & Market Intelligence** is a data analytics project focused on analyzing pharmaceutical product data to understand **drug composition, pricing, therapeutic categories, dosage forms, packaging, and manufacturers**.

The project uses **Python/Pandas for data cleaning and analysis** and **Power BI for interactive visualization and business insights**.

The main goal is to convert raw pharmaceutical data into meaningful insights that can support **pricing decisions, product portfolio analysis, and market understanding**.

---

##  Project Objectives

- Analyze the pharmaceutical product portfolio.
- Identify the distribution of products across **therapeutic classes**.
- Analyze **drug composition** and active ingredients.
- Compare **single-ingredient and combination drugs**.
- Understand pharmaceutical **pricing patterns**.
- Analyze products by **dosage form and packaging**.
- Identify manufacturers with larger product portfolios.
- Create meaningful **price and product segments**.
- Build an interactive **Power BI dashboard**.
- Generate business insights from the analyzed data.

---

##  Tools & Technologies

- **Python**
- **Pandas**
- **NumPy**
- **Jupyter Notebook**
- **Power BI**
- **Power Query**
- **DAX**
- **Microsoft Excel / CSV**

---

## 🔄 Project Workflow

```text
Raw Pharmaceutical Data
        ↓
Data Exploration
        ↓
Data Cleaning using Python
        ↓
Data Transformation
        ↓
Exploratory Data Analysis
        ↓
Segmentation & Analysis
        ↓
Power BI Dashboard
        ↓
Business Insights
```

---

##  Python Data Cleaning & Analysis

Python and Pandas were used to prepare the dataset for analysis.

### Main steps performed:

1. Loaded the pharmaceutical dataset using Pandas.
2. Checked the dataset structure using:
   - `head()`
   - `info()`
   - `describe()`
   - `shape`
3. Checked missing values.
4. Removed rows containing missing values where required.
5. Standardized dosage-form values.
6. Standardized strength values such as `mg`.
7. Extracted packaging information.
8. Parsed the `active_ingredients` column.
9. Created an ingredient-name field for further analysis.
10. Analyzed therapeutic classes, manufacturers, pricing, dosage forms, and drug composition.

### Example: Finding Duplicate Product IDs

```python
df[df['product_id'].duplicated()]
```

This identifies duplicate values in the `product_id` column.

To identify all rows belonging to duplicate Product IDs:

```python
df[df['product_id'].duplicated(keep=False)]
---

---

##  Drug Composition Analysis

The project analyzes pharmaceutical products based on the number of active ingredients.

Products can be categorized into:

- **Single Ingredient**
- **Double Ingredient**
- **Multi Ingredient**

This helps understand the prevalence of combination medicines in the dataset.

The analysis also looks at:

- Frequently used active ingredients
- Common ingredient combinations
- Strength variations


## Therapeutic Class Analysis

Products are analyzed according to their **therapeutic class**.

The analysis helps identify:

- Product count by therapeutic class
- Top therapeutic categories
- Product diversity within each class

Example Python analysis:

```python
Top_therapeutic_categories = (
    Pharma_Df.groupby('therapeutic_class')['product_id']
    .count()
    .sort_values(ascending=False)
    .head(5)
    .reset_index()
)
```



##  Pricing Analysis

Pricing was analyzed across different product characteristics, including:

- Therapeutic class
- Pack size
- Number of active ingredients
- Dosage form
- Manufacturer

The project also looks for **pricing outliers** and differences in pricing among products with similar compositions.

### Price Segmentation

Products were categorized into:

| Price Segment | Range |
|---|---:|
| Low | ₹0–₹100 |
| Medium | ₹100–₹500 |
| Premium | Above ₹500 |

---

##  Manufacturer Analysis

The project analyzes manufacturers based on their product portfolios.

Key areas include:

- Number of products by manufacturer
- Manufacturer pricing comparison
- Manufacturer focus across therapeutic classes

This helps identify manufacturers with larger or more specialized portfolios.

---

##  Power BI Dashboard

The cleaned dataset was imported into Power BI to create an interactive dashboard.

### Dashboard focuses on:

- Product distribution by therapeutic class
- Pricing analysis
- Manufacturer comparison
- Dosage-form distribution
- Drug composition
- Active ingredients
- Product segmentation

The dashboard allows users to interact with the data using filters and visualizations.

<img width="1099" height="596" alt="image" src="https://github.com/user-attachments/assets/3cfaa3e2-6e30-4e23-b0cb-41f6b0f52b60" />

The project is designed to support **pricing optimization, portfolio planning, and identification of market opportunities**.


## 🚀 Conclusion

This project demonstrates how **Python and Power BI** can be combined to transform raw pharmaceutical product data into useful business information.

Python was mainly used for **data cleaning, transformation, and analysis**, while Power BI was used to create an **interactive dashboard and communicate insights visually**.

The overall objective is to help understand **pharmaceutical products, pricing, therapeutic segmentation, drug composition, and manufacturer portfolios**.

---

## 👩‍💻 Skills Demonstrated

**Python | Pandas | Data Cleaning | Data Analysis | Power BI | Power Query | DAX | Data Visualization | Business Intelligence**
