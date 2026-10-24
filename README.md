# Predictive Analytics in Instagram Reels

A CRISP-DM analysis of which content characteristics are associated with high-performing DIY Instagram Reels, using Python and classification models.

## Business question

Reel performance varies widely, even within one creator's account. Can a Reel's content (craft category, hook, structure, and delivery choices) help identify which Reels will outperform a creator's baseline, so teams can plan content around repeatable patterns?

## Data

`Data/raw_data.csv` has one row per Reel (258 rows from 26 creators). Performance is labeled **creator-relative** (`high` or `baseline`), which reduces bias from differences in follower count. The content features are:

- `craft_category`, `hook_category`, `reel_structure`
- `pov_present`, `result_shown_first`, `voice_present`, `audio_not_required`

Views, likes, comments, and engagement rate describe the outcome, so they are **not** used as predictors.

## Approach

The project follows the six CRISP-DM phases across four notebooks:

| Notebook | CRISP-DM phase | What it does |
|---|---|---|
| `01_business_and_data_understanding` | Business Understanding, Data Understanding | Goals, success criteria, risks, data dictionary, data quality checks |
| `02_data_preparation` | Data Preparation | Cleaning, feature construction, exploration of the cleaned data, encoding |
| `03_modeling` | Modeling | Logistic regression, k-NN, and a classification tree, with and without interaction features |
| `04_evaluation_and_deployment` | Evaluation, Deployment | Results against the business goal, lessons learned, deployment plan |

**Tools:** Python, pandas, NumPy, matplotlib, seaborn, scikit-learn, Jupyter

## Key findings



## Data quality notes



## Limitations



## How to run

1. Place `raw_data.csv` in `Data/`.
2. Run the notebooks in order (01 to 04). Notebook 2 writes `Data/cleaned_data.csv`, and notebook 3 writes `Data/model_results.csv`.

## Project structure

```
├── Data/
│   ├── raw_data.csv
│   ├── cleaned_data.csv        (generated)
│   └── model_results.csv       (generated)
└── Notebooks/
    ├── 01_business_and_data_understanding.ipynb
    ├── 02_data_preparation.ipynb
    ├── 03_modeling.ipynb
    └── 04_evaluation_and_deployment.ipynb
```
