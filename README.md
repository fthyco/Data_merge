#Data Merge Helper

A Streamlit app for merging two data files interactively — no coding required.

---

## Features

- Upload two files (CSV or Excel)
- Drop unwanted columns before merging
- Auto-detect common columns with similarity scoring (Jaccard)
- Smart visualizations for numeric and categorical columns
- Outlier detection via Z-score
- Choose join type: `inner`, `left`, `right`, `outer`
- Download the merged result as CSV

---

## Requirements

```
streamlit
pandas
matplotlib
openpyxl
```

Install with:

```bash
pip install streamlit pandas matplotlib openpyxl
```

---

## Usage

```bash
streamlit run app.py
```

Then open your browser at `http://localhost:8501`.

---

## How It Works

1. Upload two files side by side
2. Optionally drop columns you don't need
3. The app detects shared columns and scores their similarity
4. Set a similarity threshold to filter suggested merge keys
5. Pick your join type and click **Merge tables**
6. Preview the result and download it

---

## Notes

- Column names are auto-normalized (stripped and lowercased)
- Composite key similarity is shown when merging on multiple columns
- Categorical columns with more than 20 unique values are skipped in charts
