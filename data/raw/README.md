# Raw Data Sources

## Lightcast Job Postings Data

- **File**: `lightcast_job_postings.csv`
- **Source**: Lightcast Platform
- **Date Downloaded**: 2025-10-04
- **Time Period**: January - September 2024
- **Description**: Job posting data including location, industry, skills, and remote work status
- **Size**: 684 MB (12,955,715 rows)
- **Downloaded by**: Thomas Primero

## Data Dictionary

### Key Variables

| Variable | Type | Description |
|----------|------|-------------|
| `job_id` | string | Unique job posting identifier |
| `title` | string | Job title |
| `location` | string | Geographic location (city, state) |
| `state` | string | US state abbreviation |
| `industry` | string | Industry classification |
| `remote` | string | Remote work status (yes/no/hybrid) |
| `ai_related` | boolean | Whether job is AI-related |
| `posted_date` | date | Date job was posted |
| `salary_min` | numeric | Minimum salary (USD) |
| `salary_max` | numeric | Maximum salary (USD) |

## Important Notes

- **DO NOT EDIT FILES IN THIS FOLDER**
- Raw data should remain unchanged for reproducibility
- All cleaning/processing should happen in scripts
- If you need to re-download data, document it here

## Access

- Data source URL: https://drive.google.com/uc?id=1V2GCHGt2dkFGqVBeoUFckU4IhUgk4ocQ
- Contact for data access: [email]