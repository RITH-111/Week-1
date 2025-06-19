# Week-1

# Water Pollutant Dataset Analysis and Preprocessing

This project performs **Exploratory Data Analysis (EDA)** and **preprocessing** on a historical dataset of various water pollutants collected from 2000 to 2021. The dataset is loaded from a semicolon-separated CSV file and undergoes data cleaning, outlier removal, feature engineering, and scaling.



 📁 Dataset

- **File**: `PB_All_2000_2021.csv`
- **Format**: Semicolon-separated (`sep=';'`)
- **Pollutants Analyzed**:
  - `O2` (Oxygen)
  - `NO3` (Nitrate)
  - `NO2` (Nitrite)
  - `SO4` (Sulfate)
  - `PO4` (Phosphate)
  - `CL`  (Chloride)

---

## 📊 Features & Columns

The dataset includes:
- `id`: Unique monitoring station identifier
- `date`: Date of sample collection (in `dd.mm.yyyy` format)
- Pollution concentration readings (`O2`, `NO3`, etc.)

---

## ✅ Steps Performed

### 1. **Loading and Initial Inspection**
- Loaded CSV using `pandas.read_csv()` with `sep=';'`
- Inspected shape, info, and null values

### 2. **Exploratory Data Analysis (EDA)**
- Generated a **correlation matrix heatmap**
- Plotted **distributions for each pollutant**

### 3. **Preprocessing**
- Removed duplicates
- Parsed `date` column to datetime format
- Extracted `year` and `month` from `date`
- Sorted data by `id` and `date`
- Removed outliers using **z-score filtering**
- Filled remaining null values with column means
- Converted `id` to categorical (dummy-encoded)
- Scaled numeric features using `StandardScaler`

---

## 🧪 Output

- Cleaned feature matrix `X_scaled`
- Multi-label target matrix `y` containing pollutant concentrations

---

## 🛠️ Libraries Used

- `pandas`
- `numpy`
- `matplotlib`
- `seaborn`
- `scikit-learn`

---

## 📌 How to Run

1. Place the dataset in the same directory or update the file path in the script.
2. Make sure required libraries are installed:
   ```bash
   pip install pandas numpy matplotlib seaborn scikit-learn
