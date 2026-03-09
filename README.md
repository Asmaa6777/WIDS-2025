# WIDS-2025

Collaborative workspace for experiments on the **WiDS 2025** challenge, focused on predicting:
- `ADHD_Outcome`
- `Sex_F`

The repo currently centers on notebook-driven experimentation (EDA, feature engineering, model training, and submission generation).

## Repository Structure

```text
.
|-- notebooks/
|   |-- UnifiedStarterNotebook.ipynb
|   |-- Separated-models.ipynb
|   |-- Separated-models(updated).ipynb
|   |-- EDA_2.ipynb
|   |-- bagging.ipynb
|   |-- starter_v_2.ipynb
|   |-- Dictionary.ipynb
|   |-- nb*.ipynb
|   `-- todo.md
|-- submissions/
|   `-- *.csv
|-- requirements.txt
|-- todolist.md
`-- README.md
```

## Environment Setup

1. Create and activate a virtual environment:
   - Windows PowerShell:
     ```powershell
     python -m venv .venv
     .\.venv\Scripts\Activate.ps1
     ```
2. Install dependencies:
   ```powershell
   pip install -r requirements.txt
   ```

Current dependencies:
- `pandas`
- `numpy`
- `scikit-learn`
- `lightgbm`

## Data

Competition data files are **not included** in this repository.

Most notebooks assume local file paths and manual loading (Excel/CSV inputs for train/test splits and sample submission templates).  
Before running notebooks, update data paths in the first cells to your local dataset location.

## Workflow

Typical workflow in this repo:

1. Run EDA / preprocessing notebooks.
2. Try feature engineering ideas (including sex-specific ADHD signals and model chaining ideas).
3. Train and validate models (single-target or multi-output).
4. Export submission CSVs.
5. Track experiment ideas and follow-ups in:
   - `todolist.md`
   - `notebooks/Maab's/Notebooks/todo.md`

## Outputs

- Generated submissions are stored under:
  - `submissions/`
  - `notebooks/` (some direct `submission*.csv` files)

## Notes

- This is an active experimentation repo; notebooks may contain hardcoded paths and incremental trial code.
- Prefer adding new experiments as separate notebooks (or clearly versioned copies) to keep comparison easy.
