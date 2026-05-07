# UK Sanctions Data Exploration

This workspace contains a Jupyter notebook that cleans and analyzes the UK Sanctions List CSV, then exports summary tables and interactive Plotly visualizations.

## Files

- `main.ipynb` - notebook with the data cleaning, analysis, and export steps
- `UK-Sanctions-List.csv` - source dataset
- `choropleth_country.html` - generated country-level choropleth map
- `treemap_country_sanction.html` - generated country-to-sanction treemap

## What the notebook does

The notebook performs the following work:

- loads the sanctions CSV into pandas
- explores missing values, unique values, and duplicates
- standardizes text fields such as names, gender, and ship type
- combines name columns into `name_combined`
- cleans phone numbers and identifier values
- parses dates such as date of birth, last updated, and date designated
- extracts sanctions, passport, and subsidiary details into structured columns
- creates summary charts and exports cleaned datasets

## Requirements

Use Python 3 with the following packages:

- pandas
- numpy
- matplotlib
- seaborn
- networkx
- plotly

If you are running the notebook in a fresh environment, install the packages first:

```bash
pip install pandas numpy matplotlib seaborn networkx plotly
```

## How to run

1. Open `main.ipynb` in Jupyter Notebook, JupyterLab, or VS Code.
2. Run the notebook cells from top to bottom.
3. Make sure `UK-Sanctions-List.csv` stays in the same folder as the notebook, or update the file path in the loading cell.

## Outputs

The notebook writes cleaned and consolidated results to an output folder defined in the notebook. It also generates these HTML visualizations in the workspace:

- `choropleth_country.html`
- `treemap_country_sanction.html`

Depending on which export cells you run, the notebook will also create cleaned CSV files such as:

- `cleaned_data.csv`
- `unique_sanctions.csv`
- `consolidated_data.csv`

## Notes

Some notebook cells assume that specific columns exist in the CSV. If the source file changes, a few cells may need small updates to column names or output paths.
