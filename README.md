# Healthcare Cost Driver Analysis (Synthetic Claims Data)

Portfolio project analyzing healthcare cost drivers using **CMS DE-SynPUF** synthetic Medicare claims-style data.  
The goal is to replicate a real payer/provider analytics workflow: **ingestion → cleaning → feature engineering → cost & utilization metrics → cost driver insights → recommendations**.

## What’s Included
- **Notebook:** `notebooks/claims_cost_driver_analysis.ipynb`
- **Analysis topics:**
  - Total cost and utilization trends
  - PMPM proxy (cost per active member per month)
  - High-cost cohorts (Top 1% and Top 5%)
  - Inpatient vs outpatient spend mix
  - Interpretable driver signals (correlations / grouped means)

## Key Outputs (at a glance)
- Spend concentration (Pareto / high-cost cohort share of total spend)
- Monthly cost and utilization trends (2008–2010)
- Inpatient vs outpatient cost split
- Member-level summary metrics and driver indicators

## Data Setup (Synthetic)
This project uses **synthetic public use files** from CMS (DE-SynPUF).  
Raw data is intentionally **not committed** to GitHub.

### Expected Files (place in `data/raw/`)
- `DE1_0_2008_Beneficiary_Summary_File_Sample_1.csv`
- `DE1_0_2008_to_2010_Inpatient_Claims_Sample_1.csv`
- `DE1_0_2008_to_2010_Outpatient_Claims_Sample_1.csv`

Download from CMS DE-SynPUF Sample 1.

## How to Run
1. Create an environment (optional) and install dependencies:
   ```bash
   pip install pandas numpy matplotlib jupyter
