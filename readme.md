
## 📝 Final Report: Producer vs Consumer Price Analysis (Austria)

### 📌 Objective:

To explore the **relationship between producer prices (PPI)** and **consumer prices (CPI)** in Austria over time, and analyze how the pricing gap evolved from 1991 to 2024.

---

### 🧮 Datasets Used:

1. **Producer Price Data (PPI)**: Monthly product-level prices from 1991–2024.
2. **Consumer Price Index (CPI)**: Monthly index data for consumer food prices (base year = 2015).

---

### 🛠️ Key Steps:

1. **Data Cleaning**:

   * Dropped non-numeric rows and headers.
   * Removed irrelevant categories like "General Indices" from CPI.
   * Standardized formats and handled duplicates.

2. **Normalization**:

   * Both datasets were normalized using:

     $$
     \text{Normalized} = \frac{x - \min(x)}{\max(x) - \min(x)}
     $$
   * This allowed us to compare trends on the same scale.

3. **Monthly to Yearly Aggregation**:

   * Aggregated both CPI and PPI data by year using the mean.
   * This was done to simplify comparison and smooth short-term fluctuations.

4. **Gap Calculation**:

   * Calculated yearly gap as:

     $$
     \text{Gap} = \text{CPI}_{\text{norm}} - \text{PPI}_{\text{norm}}
     $$

---

### 📊 Key Findings:

* **1990s**: CPI and PPI were relatively close; some years showed PPI slightly higher.
* **2000–2010**: The gap steadily widened, with CPI outpacing PPI.
* **Post-2010**: Sharp increase in consumer prices, while producer prices remained relatively flat.
* **2023–2024**: The gap reached its **highest point**.

---

### 🤔 Limitations:

* **No item-level match**: CPI data was general, while PPI had specific products.
* **Monthly CPI reset issue**: CPI data was oddly structured with repeating years (due to how months were ordered).
* **Normalization skews scale**: While good for trend, it hides absolute values.
* **External factors not included**: E.g., inflation policy, subsidies, transport costs, etc.

---

### 🧠 Reflection:

This project gave insight into:

* How price pressure shifts between producers and consumers.
* Real-world complexity when working with national statistics.
* The need to **understand structure** before diving into plots.

---

### 📁 Artifacts:

* `../visuals/price_gap_trend.png` (Gap chart)
* `../visuals/ppi_vs_cpi.png` (Trend comparison)
