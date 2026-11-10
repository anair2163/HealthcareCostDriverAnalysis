# Payment Concentration in Synthetic Medicare Claims

Which member cohorts accounted for the most inpatient and outpatient payments in CMS's synthetic Sample 1, and how did their utilization differ?

[Open the analysis notebook](notebooks/claims_cost_driver_analysis.ipynb) · [Download CMS DE-SynPUF Sample 1](https://www.cms.gov/data-research/statistics-trends-and-reports/medicare-claims-synthetic-public-use-files/cms-2008-2010-data-entrepreneurs-synthetic-public-use-file-de-synpuf/de10-sample-1)

## Findings

The saved analysis retained **846,310 claim rows** across **86,705 members with claims** and summed **$848.7 million** in synthetic payments.

| Member cohort | Share of payments | Claim rows per member | Members with an inpatient claim |
| --- | ---: | ---: | ---: |
| Top 1% by payment | 10.7% | 27.5 | 100.0% |
| Top 5% by payment | 33.8% | 21.2 | 98.7% |
| Bottom 95% | 66.2% | 9.2 | 40.7% |

The top 1% is included in the top 5%. The payment measure sums `CLM_PMT_AMT` across inpatient and outpatient claim rows, including adjustments. The monthly ratio uses members with a claim that month. Enrollment-based per-member-per-month spending would use covered member-months, including months with zero claims.

The analysis demonstrates a payer workflow. The synthetic payments and utilization figures describe this sample, and the cohort comparisons do not identify avoidable spending or causal drivers.

## Reproduce

Extract these files from CMS Sample 1 into `data/raw/`:

- `DE1_0_2008_Beneficiary_Summary_File_Sample_1.csv`
- `DE1_0_2008_to_2010_Inpatient_Claims_Sample_1.csv`
- `DE1_0_2008_to_2010_Outpatient_Claims_Sample_1.csv`

```bash
python -m pip install pandas numpy matplotlib jupyter
jupyter notebook
```

Open `notebooks/claims_cost_driver_analysis.ipynb` and run all cells.
