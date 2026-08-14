# NusaGlow Supply Chain Analysis

This repository contains the NusaGlow data-analysis work for SCMission 2026 Round 3. The analysis is developed in a Jupyter notebook and covers the supplied customer, facility, product, demand, inventory-transfer, and transportation-cost datasets.

## Repository contents

- `Nusaglow.ipynb` — data loading, exploration, visualization, and analysis
- `requirements.txt` — required Python libraries
- `Nusaglow document.docx` — supporting project document
- `Bekasi - Indonesia Image.jpg` — supporting image

The competition datasets are kept outside this repository because they may be large or subject to sharing restrictions. In particular, `DailyDemand.csv` is approximately 1 GB and is intentionally excluded by `.gitignore`.

## Setup

Python 3.11 or newer is recommended.

```powershell
git clone https://github.com/phucvoftu2/nusaglow.git
cd nusaglow
python -m venv .venv
.\.venv\Scripts\Activate.ps1
python -m pip install --upgrade pip
python -m pip install -r requirements.txt
jupyter lab
```

Open `Nusaglow.ipynb` in JupyterLab and run the cells in order.

## Data location

The notebook currently reads the source files from:

```text
D:\LSCM - Self Study\Case\scmission\2026\[ROUND 3] CASE\SCMission2026_Round3_Data\SCMission2026_Round3_Data
```

If the project is used on another computer, update `DATA_DIR` in the notebook to the local dataset folder.

## Large-file handling

Most tables are loaded directly with pandas. `DailyDemand.csv` is read as a 100,000-row sample for exploration and exposed as a chunked reader for full-data processing. This prevents the notebook from exhausting system memory.

## Contributing

Create a branch for each piece of work, commit the changes, and open a pull request into `main`.

```powershell
git switch -c feature/analysis-name
git add .
git commit -m "Describe the analysis change"
git push -u origin feature/analysis-name
```
