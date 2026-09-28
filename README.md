******Evaluating Online Health-Seeking Behaviors as Digital Proxies for Emerging Infectious Disease Burden in Zambia (2019-2024)
******
**📌 Project Overview
**
This repository contains the data analysis pipeline and codebase for the research project: "Evaluating Online Health-Seeking Behaviors as Digital Proxies for Emerging Infectious Disease Burden in Zambia: A Google Trends Time-Series Analysis (2019-2024)."

Traditional public health surveillance methods, while essential, often suffer from delayed reporting. As internet penetration in Zambia grows, digital footprints such as search engine queries offer a real-time, complementary tool for monitoring public health. This project evaluates the correlation between Google Relative Search Volume (RSV) for Emerging Infectious Diseases (EIDs) and official case reporting data in Zambia.

**Author: Taonga Jere (Student I.D: 21166977)**

**Institution: Copperbelt University, Michael Chilufya Sata School of Medicine, Department of Public Health
**
**🎯 Objectives
**
Analyze Trends: Track EID-related Google search queries in Zambia from 2019 to 2024.

Examine Disease Burden: Assess trends in reported EID cases over the same period.

Contextual Evaluation: Determine the influence of internet penetration, population size, and major health events on search behavior.

Evaluate Surveillance Potential: Correlate Google RSV with EID burden to determine its viability as a supplementary public health surveillance tool.

**📊 Data Sources**

The analysis integrates multiple datasets to form a comprehensive ecological time-series study:

Google Trends (RSV): Extracted via Pytrends for Zambia (geo='ZM'). Includes primary EIDs (Cholera, Typhoid, Ebola) and secondary EIDs (Mpox, Measles).

Disease Burden Data: Official incidence and prevalence data sourced from Zambia's Health Management Information System (HMIS) and District Health Information System 2 (DHIS2).

Contextual Data:

Internet penetration statistics from the Zambia Information and Communications Technology Authority (ZICTA).

Population estimates from the Central Statistical Office (CSO).

Major health campaign data from the Ministry of Health (MOH).

**🛠️ Technologies & Libraries**

The entire analysis is conducted in Python. The following libraries are utilized:

pandas - For data cleaning, merging, and time-series manipulation.

matplotlib & seaborn - For descriptive trend visualizations and correlation heatmaps.

statsmodels & scipy - For statistical testing (Pearson/Spearman correlations, simple linear regression).

geopandas - For mapping regional and provincial data distributions across Zambia.

pytrends - For automated Google Trends RSV data extraction.

**🔬 Methodology & Analytical Pipeline**

Data Preparation:

Extract, clean, and handle missing values.

Aggregate both HMIS and Google Trends data into a uniform monthly time-series format (Jan 2019 – Dec 2024).

Calculate a Composite RSV Index for terms related to the same disease.

Descriptive & Temporal Trend Analysis: Visual inspection of peaks, fluctuations, and seasonal similarities between online searches and clinical cases.

Geographical Analysis: Provincial mapping of search behavior vs. reported cases using GeoPandas.

Correlational Analysis: Using Pearson's $r$ (for linear associations) and Spearman's $\rho$ (for ranked/normalized RSV data) to test the strength and direction of relationships.

Lagged Correlational Analysis: Shifting Google Trends data forward by 1-3 months to evaluate if search spikes act as early warning indicators for outbreaks.

Regression Modeling: Applying simple linear regression to assess if Google RSV can accurately predict reported EID cases.

**📂 Repository Structure (Proposed)**

├── data/
│   ├── raw/                 # Raw HMIS, ZICTA, and Google Trends extracts
│   ├── processed/           # Cleaned and merged time-series datasets
├── notebooks/
│   ├── 01_data_extraction_and_cleaning.ipynb
│   ├── 02_exploratory_data_analysis.ipynb
│   ├── 03_correlation_and_lagged_analysis.ipynb
│   ├── 04_regression_modeling.ipynb
│   └── 05_geospatial_mapping.ipynb
├── src/
│   ├── data_loader.py       # Scripts for API pulling (Pytrends)
│   ├── utils.py             # Helper functions for statistical testing
├── visuals/                 # Exported graphs, maps, and plots
├── requirements.txt         # Python dependencies
└── README.md                # Project documentation


**🚀 How to Run the Project**

Clone this repository:

git clone https://github.com/yourusername/zambia-eid-google-trends.git
cd zambia-eid-google-trends


Install the required dependencies:

pip install -r requirements.txt


Open the Jupyter Notebooks in the notebooks/ directory to follow the step-by-step analysis. (Note: Access to raw HMIS data requires ethical clearance and MOH approval, and thus may not be fully public in this repository).

****⚖️ Ethical Considerations**

This study utilizes secondary, aggregated data. All data is anonymized and conforms to the General Data Protection Regulation (GDPR) and the Data Protection Act of Zambia. Ethical clearance is processed through the CBU-BREC.**
>>>>>>> a5a05374cb189c3243965363ca848bdbb144cef4
