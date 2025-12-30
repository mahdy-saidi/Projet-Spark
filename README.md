# ⛽ French gas prices analysis & forecasting project

## Description

This project analyzes French gas price data using Apache Spark (PySpark).  
It covers the full data pipeline, from data collection and preparation to visualization and
machine learning modeling.

The objective is twofold:
- Analyze spatial and temporal dynamics of gas prices in France
- Forecast the next-day fuel price at a station using Spark ML

All steps are implemented in a single notebook.

---

## Data Sources

The datasets are downloaded from prepared CSV files hosted on GitHub, originating from the
official French gas price open data portal.

Data includes:
- Daily gas prices by station and fuel type
- Gas station metadata
- Services metadata

---

## Setup

### Creating a virtual environment

Create a virtual environment in the project root:

```bash
python -m venv venv

Activate it:

* Linux / macOS
```bash
source venv/bin/activate
```
* Windows
```bash
venv\Scripts\activate
```
### Install all required dependencies:
```bash
pip install -r requirements.txt
```
### Create a Jupyter Kernel
After activating the virtual environment, create a new Jupyter kernel so the notebook can use the correct environment:
```bash
python -m ipykernel install --user --name=french-gas-env --display-name "Python (French Gas)"
```
Here, `french-gas-env` is the internal kernel name, and `Python (French Gas)` is the display name in Jupyter.

### Configuration File

The project is fully parameterized using a YAML configuration file.
Default `config.yaml`:
```bash
download_directory: "data"
start_year: 2022
end_year: 2024
github_base_url: "https://raw.githubusercontent.com/etalab/prix-carburants/master/archives"
```
You can modify this file to:
* Include more data
* Change the download directory

### Running the Project

Start Jupyter Notebook:
```bash
jupyter notebook
```
Then select the kernel "Python (French Gas)" and open:
```bash
notebook.ipynb
```