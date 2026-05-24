# Asteroid Data Exploratory Analysis

## Project Summary

This project performs Exploratory Data Analysis (EDA) on a large asteroid dataset to understand the physical, orbital, and risk-related characteristics of asteroids in our solar system.

The notebook covers data acquisition, cleaning, preprocessing, statistical analysis, visualization, correlation analysis, and outlier detection. Special attention is given to Near-Earth Objects (NEOs) and Potentially Hazardous Asteroids (PHAs), helping identify patterns that may be relevant for astronomical research and planetary defense studies.

The objective is to transform raw asteroid data into meaningful insights through systematic data analysis and visualization.

---

## Features

* Automated dataset download from Kaggle
* Data inspection and quality assessment
* Missing value identification and treatment
* Data cleaning and preprocessing
* Handling categorical and numerical missing values
* Statistical summary generation
* Distribution analysis of asteroid properties
* Correlation analysis between orbital and physical features
* Outlier detection through visual exploration
* Near-Earth Object (NEO) analysis
* Potentially Hazardous Asteroid (PHA) analysis
* Asteroid class distribution analysis
* Multiple visualizations using Matplotlib and Seaborn

---

## Tech Stack

### Programming Language

* Python

### Libraries

* Pandas
* NumPy
* Matplotlib
* Seaborn
* KaggleHub

### Development Environment

* Google Colab
* Jupyter Notebook

### Data Visualization

* Matplotlib
* Seaborn

### Data Source

* Kaggle Asteroid Dataset

---

## Dataset Information

### Source

Dataset downloaded directly from Kaggle using KaggleHub:

```python
path = kagglehub.dataset_download("sakhawat18/asteroid-dataset")
```

### Dataset Description

The dataset contains detailed information about asteroids, including:

* Physical properties
* Orbital parameters
* Classification labels
* Near-Earth Object indicators
* Hazard assessment indicators

### Important Features

| Column     | Description                         |
| ---------- | ----------------------------------- |
| id         | Asteroid identifier                 |
| full_name  | Asteroid name                       |
| neo        | Near-Earth Object flag              |
| pha        | Potentially Hazardous Asteroid flag |
| H          | Absolute magnitude                  |
| diameter   | Estimated diameter                  |
| albedo     | Surface reflectivity                |
| moid       | Minimum Orbit Intersection Distance |
| e          | Orbital eccentricity                |
| a          | Semi-major axis                     |
| q          | Perihelion distance                 |
| i          | Orbital inclination                 |
| per        | Orbital period                      |
| class_name | Asteroid classification             |

### Data Characteristics

* Large-scale asteroid catalog
* Contains both numerical and categorical features
* Includes orbital mechanics measurements
* Contains hazard-related classifications
* Features missing values requiring preprocessing

---

## Methodology / Workflow

### 1. Data Collection

* Download asteroid dataset from Kaggle using KaggleHub.
* Load data into a Pandas DataFrame.

### 2. Data Understanding

* Examine dataset structure.
* Review column data types.
* Analyze dataset dimensions and feature availability.

### 3. Data Cleaning

* Detect missing values.
* Fill missing binary fields such as:

  * `neo`
  * `pha`
* Remove records with missing critical orbital parameters:

  * `ma`
  * `ad`
  * `per`
  * `per_y`
  * `rms`
* Verify data quality after cleaning.

### 4. Statistical Analysis

* Generate descriptive statistics for numerical variables.
* Analyze categorical feature distributions.
* Examine asteroid classifications.

### 5. Distribution Analysis

Visualize distributions for:

* Absolute magnitude (`H`)
* Diameter
* Albedo
* MOID
* Eccentricity (`e`)
* Semi-major axis (`a`)
* Perihelion distance (`q`)
* Inclination (`i`)
* Orbital period (`per`)

### 6. Correlation Analysis

* Compute correlation matrix.
* Visualize feature relationships using heatmaps.
* Identify highly correlated asteroid properties.

### 7. Outlier Detection

Analyze potential outliers through scatter plots involving:

* Magnitude vs Diameter
* Diameter vs Albedo
* Eccentricity vs Semi-major Axis
* Orbital Period vs Magnitude
* Additional orbital parameter combinations

### 8. Class Distribution Analysis

* Visualize asteroid class frequencies.
* Explore class imbalance and category representation.

---

## Key Insights

* The dataset contains a diverse range of asteroid classes and orbital characteristics.
* Near-Earth Objects (NEOs) and Potentially Hazardous Asteroids (PHAs) are explicitly identified.
* Several numerical variables exhibit skewed distributions.
* Strong relationships exist among orbital parameters such as eccentricity, perihelion distance, and semi-major axis.
* Outlier analysis reveals extreme asteroid characteristics that may warrant further investigation.
* Asteroid classes are unevenly distributed, indicating class imbalance within the dataset.

---

## Recommendations

* Perform focused analysis on NEO and PHA populations.
* Apply anomaly detection algorithms to investigate extreme asteroids.
* Build predictive models for asteroid classification.
* Develop hazard prediction systems using orbital parameters.
* Explore clustering techniques to identify asteroid groups.
* Create interactive dashboards for astronomical data exploration.
* Incorporate temporal observations if longitudinal data becomes available.

---

## Installation

### Clone Repository

```bash
git clone https://github.com/Divyam-Deep/Asteroid-EDA.git
cd Asteroid-EDA
```

### Install Dependencies

```bash
pip install pandas numpy matplotlib seaborn kagglehub
```

---

## Usage

### Run the Notebook

```bash
jupyter notebook Asteroid.ipynb
```

or open the notebook in Google Colab.

### Execute Analysis

1. Download dataset automatically from Kaggle.
2. Run data cleaning cells.
3. Perform statistical exploration.
4. Generate visualizations.
5. Analyze correlations and outliers.
6. Review insights and findings.

---

## Project Structure

```text
Asteroid-EDA/
│
├── Asteroid.ipynb
├── README.md
│
├── visualizations/
│   ├── distributions.png
│   ├── correlation_heatmap.png
│   ├── outlier_analysis.png
│   └── class_distribution.png
│
└── requirements.txt
```

---

## Future Improvements

* Machine learning-based asteroid classification
* Hazard prediction modeling for PHAs
* Interactive dashboards using Plotly or Streamlit
* Advanced anomaly detection techniques
* Automated reporting pipeline
* Dimensionality reduction and clustering analysis
* Integration with NASA asteroid APIs
* Deployment as a web-based analytics platform

---

## Author

**Divyam Deep**

Data Analyst | Python Developer | Exploratory Data Analysis Enthusiast

This project demonstrates practical data cleaning, visualization, statistical analysis, and exploratory data analysis techniques applied to a real-world asteroid dataset, with emphasis on asteroid characteristics, orbital properties, and hazard assessment.
