# Data Directory

**Project**: Geographic & Remote Work Analysis - AI vs. Non-AI Careers  
**Team**: Group 09  
**Last Updated**: [today's date]

---

## 📁 Directory Structure
data/
├── raw/              # Original data files (NEVER EDIT)
├── processed/        # Cleaned, analysis-ready datasets
├── scripts/          # Data cleaning and processing code
└── README.md         # This file

---

## 📖 Folder Descriptions

### `raw/`
**Purpose**: Store original, unmodified data files  
**Rules**:
- ⚠️ **NEVER edit files in this folder**
- These are your backup/source of truth
- If you need to modify data, create a script and save output to `processed/`
- Document all raw data sources in `raw/README.md`

### `processed/`
**Purpose**: Store cleaned, analysis-ready datasets  
**Rules**:
- These files should be created by scripts in `scripts/`
- All team members should use these files for analysis
- Use descriptive filenames (e.g., `jobs_cleaned.csv`, not `data.csv`)
- Document any transformations made from raw data

### `scripts/`
**Purpose**: Store data cleaning and processing code  
**Rules**:
- Number scripts in order (e.g., `01_clean_data.R`, `02_aggregate.R`)
- Include comments explaining what each script does
- Scripts should be reproducible (anyone can run them and get same results)

---

## 🗂️ Key Data Files

### Processed Data (Ready for Analysis)

| File | Description | Created By | Last Updated |
|------|-------------|------------|--------------|
| `jobs_cleaned.csv` | Main cleaned dataset - use this for all analyses | [Name] | [Date] |
| `geographic_summary.csv` | State-level job counts and metrics | [Name] | [Date] |
| `remote_trends.csv` | Remote work trends over time | [Name] | [Date] |
| `tech_hubs.csv` | Jobs in major tech hubs vs. other locations | [Name] | [Date] |
| `urban_rural.csv` | Urban vs. rural job market comparison | [Name] | [Date] |

### Data Dictionary (Main Variables)

**File**: `jobs_cleaned.csv`

| Variable | Type | Description | Example |
|----------|------|-------------|---------|
| `job_id` | string | Unique identifier for each job posting | "ABC123" |
| `title` | string | Job title | "Data Scientist" |
| `city` | string | City where job is located | "Austin" |
| `state` | string | State abbreviation | "TX" |
| `metro_area` | string | Metropolitan statistical area | "Austin-Round Rock" |
| `region` | string | US region | "South" |
| `industry` | string | Industry classification | "Technology" |
| `remote_status` | string | Remote work availability | "Remote", "Hybrid", "On-site" |
| `ai_related` | boolean | Whether job involves AI/ML | TRUE/FALSE |
| `posted_date` | date | Date job was posted | "2024-03-15" |
| `salary_min` | numeric | Minimum salary (annual, USD) | 80000 |
| `salary_max` | numeric | Maximum salary (annual, USD) | 120000 |
| `urban_rural` | string | Urban or rural classification | "Urban", "Rural" |
| `tech_hub` | boolean | Whether location is a major tech hub | TRUE/FALSE |

---

## 🔄 Data Workflow

### Step 1: Obtain Raw Data
1. Download Lightcast job postings data
2. Save to `data/raw/` with descriptive filename
3. **DO NOT modify the file**
4. Document in `data/raw/README.md`

### Step 2: Clean Data
1. Create cleaning script in `data/scripts/`
2. Script reads from `data/raw/`
3. Script performs cleaning/transformations
4. Script saves cleaned data to `data/processed/`

### Step 3: Use in Analysis
1. All `.qmd` analysis files load data from `data/processed/`
2. Use relative paths: `read_csv("data/processed/jobs_cleaned.csv")`
3. Never load from `raw/` in analysis files

---

## 📊 Data Sources

### Primary Source: Lightcast Job Postings

- **Platform**: Lightcast (formerly Burning Glass)
- **Data Type**: Job posting microdata
- **Coverage**: United States
- **Time Period**: [January 2024 - September 2024]
- **Downloaded**: [DATE]
- **Downloaded By**: [Team member name]
- **File Size**: [XX MB, XXX,XXX rows]
- **Access**: [Describe how to access - course portal, direct download, etc.]

### Secondary Sources (if applicable)

- **Bureau of Labor Statistics**: Occupational classifications
- **US Census Bureau**: Urban/rural classifications
- **[Other sources]**: [Description]

---

## 👥 Team Responsibilities

| Team Member | Responsibility | Files |
|-------------|----------------|-------|
| [Name 1] | Data cleaning & main dataset | `jobs_cleaned.csv` |
| [Name 2] | Geographic aggregation | `geographic_summary.csv`, `geographic_trends.qmd` |
| [Name 3] | Remote work analysis | `remote_trends.csv`, `remote_work_trends.qmd` |
| [Name 4] | Tech hub analysis | `tech_hubs.csv`, `tech_hubs_analysis.qmd` |
| [Name 5] | Urban/rural comparison | `urban_rural.csv`, `urban_rural_comparison.qmd` |

---

## 💻 How to Use This Data

### In R
```r
# Load packages
library(tidyverse)

# Load main cleaned dataset
jobs <- read_csv("data/processed/jobs_cleaned.csv")

# Load specific analysis datasets
geo_data <- read_csv("data/processed/geographic_summary.csv")
remote_data <- read_csv("data/processed/remote_trends.csv")


### Analysis Approach
- **Descriptive Statistics**: Job counts, growth rates, salary distributions
- **Geographic Analysis**: State and metro-level comparisons
- **Trend Analysis**: Time-series analysis of remote work patterns
- **Comparative Analysis**: AI vs. non-AI, urban vs. rural, tech hubs vs. other locations

### Tools & Technologies
- **R / Python**: Data cleaning and analysis
- **Quarto**: Website creation and reproducible reports
- **ggplot2 / matplotlib**: Data visualization
- **Git/GitHub**: Version control and collaboration
- **GitHub Pages**: Website hosting
