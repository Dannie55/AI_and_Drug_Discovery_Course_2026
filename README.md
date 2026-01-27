# AI_and_Drug_Discovery_Course_2026

**Assignment 2: QSAR Data Curation Using ChEMBL**
---

**Selected Target Name : Cellular Tumor Antigen P53**

---
**Number of bioactivity records: 30**


**Short description of the data curation workflow**

## 📌 Project Overview
This project focuses on **QSAR Data Curation using chEMBL**  The workflow covers data collection, curation, descriptor calculation, model development, and model evaluation.

---

## 🗂️ Part 1: Data Collection & Curation

Google Colab is connected to Google Drive to enable seamless access to project files and datasets. This allows curated data to be saved, reloaded across sessions, and organized efficiently for reproducible analysis.

### 🔗 Mount Google Drive in Colab
```python
from google.colab import drive
drive.mount('/content/gdrive')

### 🛠️ Install and Import Required Libraries

To retrieve bioactivity data from ChEMBL and process it for QSAR modeling, we first need to install the ChEMBL web service package and import all necessary Python libraries.

### 🛠️ Import Required Libraries
We import the libraries required for data handling and accessing ChEMBL bioactivity data:
pandas – for loading, manipulating, and saving datasets and new_client from chembl_webresource_client – to query the ChEMBL database

### Search for Target Protein (P53)
We start by identifying the target protein P53 in ChEMBL and selecting the most relevant entry for bioactivity data retrieval.
Retrieve P53 Bioactivity Data (IC₅₀ in nM)
Finally Save the resulting bioactivity data to a CSV file bioactivity_raw_data.csv.
Now copy "bioactivity_raw_data.csv" file to Google Drive, in foler "data"
Inspect Missing Values
Filter Rows with Valid Bioactivity Values
Assign Bioactivity Classes Define active, intermediate, and inactive classes based on IC50 values.
Extract Relevant Columns
Create Preprocessed bioactivity Dataset
Remove Compounds without Valid SMILES. Drop rows with NaN, empty or None SMILES values.
Save Preprocessed Bioactivity Data. Save the cleaned dataset to CSV and copy to Google Drive.

