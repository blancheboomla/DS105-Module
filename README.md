# DS105-Module
Examples of summative work for DS105 module

## Notebooks Folder
**1. NB01 Data Collection - 28109**
- This notebook scrapes the LSE's IR dept webpage
- Output: Menu.json (A dictionary of the subheadings and their links)
- Output: Images folder (Data/Images) scraping all images and placing in respective folder from webpage

**2. NB01 Data Collection Notebook**
- This notebook first scrapes the Peaky Blinders Fandom Wiki, creating an output of Peaky_blinders_epsiodes.csv which contains the Season Number; Season Url; Episode number; Episode Name; Episode Url and Air date for all seasons
- Then it scrapes the synopsis for all episodes and collects all the hyperlinks per episode that are contained within the synopsis. Peaky_blinders_synopsis.csv contains the Season Number; Episode number; Paragraph Id; Hyperlink title; Link url for every hyperlink across all episodes, seasons 1-6.

**3. NB02 Data Analysis Notebook**
   -  This notebook creates two plots:
         1. Using ggplot: 'Top 20 most common first hyperlink in the synopsis across seasons'
         2. Using matplotlib: 'Most mentioned characters throughout the seasons'
    



# Traditional Social Values Analysis - World Values Survey

## Project Overview
This project explores how demographic factors (age, gender, education level and country) influence traditional social values related to family roles, gender roles, work priorities, and respect for authority. This uses data from the World Values Survey (Wave 7).

## Research Question
**"What demographic factors predict adherence to traditional social values about family roles, gender roles, work priorities, and respect for authority, based on responses to the World Values Survey?"**

## Data Overview
- **Dataset**: `WVS_random_subset2000.csv`
- **Codebook**: `codebook.pdf`
- **Survey**: World Values Survey Wave 7 (2017–2022)
- **Sample Size**: ~2000 respondents (random subset)
- **Countries**: Global, multiple countries represented

## Codebook/ Variable Dictionary

### Demographic (Independant) Variables Used

The following demographic factors are included in the models:

| Variable Code | Description |
|:--------------|:------------|
| Q260          | Gender (Male/Female) |
| Q262          | Age (continuous, in years) |
| Q275          | Education level (ordinal scale: primary, secondary, university) |
| B_COUNTRY     | Country code (to control for country-level effects) |

---

### Variables (Dependant) Used

| Code | Description |
|:-----|:------------|
| Q1   | Importance of Family |
| Q5   | Importance of Work |
| Q28  | Working mothers harm preschool children |
| Q29  | Men make better political leaders than women |
| Q32  | Being a housewife is as fulfilling as working |
| Q33  | Men should have more right to jobs when jobs are scarce |
| Q40  | Work is a duty toward society |
| Q41  | Work should always come first, even if it means less spare time |
| Q43  | Less importance placed on work |
| Q45  | Greater respect for authority (future change) |

---

### Data Scales (Coding System)
Across WVS questions, common coding for categorical variables includes:

| Value | Meaning |
|:-----:|:--------|
| 1     | Strongest positive (e.g., Very Important, Strongly Agree) |
| 2     | Positive (e.g., Important, Agree) |
| 3     | Negative (e.g., Not Important, Disagree) |
| 4     | Strongest negative (e.g., Not Important at All, Strongly Disagree) |
| -1    | Don't know |
| -2    | No answer |
| -4    | Not asked in this country |
| -5    | Missing / Not available |

Negative values (-1 to -5) indicate non-responses and should be treated as missing data during analysis.

---

### Descriptive Statistics (Top 5 Selected Variables)

| Variable | Mean | Std Dev | Min | Max | Most Frequent Value |
|:---------|:-----|:--------|:----|:----|:--------------------|
| Q1 (Importance of Family) | 1.23 | 0.62 | 1 | 4 | 1 (Very Important) |
| Q5 (Importance of Work)   | 1.87 | 0.76 | 1 | 4 | 2 (Rather Important) |
| Q29 (Men Better Leaders)  | 2.31 | 1.02 | 1 | 4 | 2 (Agree) |
| Q32 (Housewife Fulfilling) | 2.15 | 1.03 | 1 | 4 | 2 (Agree) |
| Q45 (Greater Respect for Authority) | 1.85 | 0.91 | 1 | 3 | 1 (Good thing) |

> *Note: Missing data (-1, -2, -4, -5) were excluded from these calculations.*

---

## Folder Structure
```plaintext
wvs_traditional_values_analysis/
│
├── README.md                   # Project documentation
│
├── data/                        # Data files organized by stage
│   ├── raw/                     # Raw original files (e.g., WVS_random_subset2000.csv, codebook.pdf)
│   ├── transformed/             # Intermediate cleaned files (e.g., missing values handled, recoded scales)
│   └── clean/                   # Final datasets ready for analysis (e.g., traditional values index computed)
│
├── notebooks/                   # Jupyter or R notebooks for exploration and final reports
│   └── traditional_values_analysis.ipynb
│
├── outputs/                     # Generated results
│   ├── figures/                 # Plots and graphs
│   └── tables/                  # Statistical tables, regression outputs
│
├── scripts/                     # Scripts for processing and analysis
│   ├── clean_data.py             # Script for cleaning and preparing the data
│   ├── transform_data.py         # Script for variable transformation and index building
│   └── run_models.py             # Script for running analysis models
│
└── requirements.txt             # Python dependencies list




## Requirements

**Python**
- Python 3.8 or higher
- Libraries:
  - `pandas`
  - `numpy`
  - `scipy`
  - `statsmodels`
  - `seaborn`
  - `matplotlib`
  - `scikit-learn`


## Licenses
- **Data**: World Values Survey data is publicly available under the [WVS Data Use Agreement](https://www.worldvaluessurvey.org/WVSDocumentationWV7.jsp).
- **Code**: This code is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.
- **Figures**: All figures are generated from the analysis and are free to use with attribution to the original data source (World Values Survey).
- **Notebooks**: Jupyter notebooks are licensed under the [CC BY-NC-SA 4.0](https://creativecommons.org/licenses/by-nc-sa/4.0/) license.
- **Scripts**: Python scripts are licensed under the MIT License. 



