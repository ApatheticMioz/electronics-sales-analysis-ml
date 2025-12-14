# Electronics Sales Analysis ML

Customer segmentation and sales prediction analysis for electronics retail using machine learning.

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
![Status](https://img.shields.io/badge/Status-Archived%20%2F%20Refactored-blue)

## Description

This project analyzes electronics retail sales data to address declining sales and customer retention challenges. Using machine learning techniques, it provides actionable insights through:

- **Exploratory Data Analysis (EDA)**: Comprehensive univariate, bivariate, and temporal analysis
- **Predictive Modeling**: Linear Regression for spending prediction and Decision Tree Classification for purchase prediction (~93% accuracy)
- **Customer Segmentation**: K-Means clustering with PCA visualization for targeted marketing strategies

Originally developed as coursework for Introduction to Data Science (DS-2001) at FAST NUCES, Islamabad.

## Project Structure

```
electronics-sales-analysis-ml/
├── electronics_sales_analysis.ipynb  # Main analysis notebook
├── electronics.json                   # Customer transaction dataset
├── project_report.pdf                 # Detailed project report
├── requirements.txt                   # Python dependencies
├── LICENSE                            # MIT License
├── CONTRIBUTING.md                    # Contribution guidelines
├── CHANGELOG.md                       # Version history
└── README.md                          # This file
```

## Setup & Installation

### Prerequisites

- Python 3.8+
- pip package manager
- Jupyter Notebook

### Installation

1. Clone the repository:
   ```bash
   git clone https://github.com/ApatheticMioz/electronics-sales-analysis-ml.git
   cd electronics-sales-analysis-ml
   ```

2. Install dependencies:
   ```bash
   pip install -r requirements.txt
   ```

## Usage

Launch Jupyter Notebook and run the analysis:

```bash
jupyter notebook electronics_sales_analysis.ipynb
```

The notebook contains the complete analysis pipeline:
1. Data loading and preprocessing
2. Exploratory Data Analysis with visualizations
3. Linear Regression and Decision Tree models
4. K-Means clustering and customer segmentation
5. Actionable business recommendations

## Tech Stack

| Category | Technologies |
|----------|-------------|
| Language | Python 3 |
| Data Processing | Pandas, NumPy |
| Machine Learning | Scikit-learn |
| Visualization | Matplotlib, Seaborn |
| Statistics | Statsmodels, SciPy |

## Key Findings

- **Decision Tree Classifier** achieved ~93% accuracy in predicting next-month purchases
- **4 customer segments** identified through K-Means clustering
- Significant seasonal patterns with October showing peak spending
- Recommendations for targeted marketing based on customer demographics and behavior

## Status

**Archived / Refactored**

This repository has been standardized for public archival. See [CHANGELOG.md](CHANGELOG.md) for version history.

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## Contributing

Contributions are welcome! Please read [CONTRIBUTING.md](CONTRIBUTING.md) for guidelines.

## Authors

- Muddassir Asghar (i23-2577)
- M. Abdullah Ali (i23-2523)
