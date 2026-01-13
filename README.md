# ArcGIS Online Feature Layer QA Automation

A Python-based quality assurance (QA) tool for validating the integrity of hosted feature layer data in **ArcGIS Online (AGOL)**.

## 📌 Overview

This tool automates common data QA tasks such as identifying null attributes, detecting duplicate values, validating coded-value domains, and checking for missing geometries.

A final CSV report is generated summarizing all issues found.

---

## 🗂 Project Structure
```
hosted-feature-layer-QA/
│
├── notebooks/                       # Jupyter notebooks
│   └── hosted_feature_layer_QA.ipynb # Notebook version of main QA workflow
│
├── output/                         # Script outputs
│   └── <layer_name>_QA_<date>.csv   # Generated QA report(s)
│
├── src/                            # Python modules / scripts
│   └── hosted_feature_layer_QA.py  # Main QA script
│
├── .gitignore                     # Ignored files for Git
├── README.md                      # Project overview and instructions
├── LICENSE                        # License
└── requirements.txt               # Python dependencies
```

## 🚀 Features

This script performs the following QA checks:

### ✔ Null Value Check  
Identifies features with missing required attribute values.

### ✔ Duplicate Value Check  
Detects duplicate records across selected fields (with exclusions for fields where duplicates are expected).

### ✔ Coded-Value Domain Validation  
Ensures that attributes with coded-value domains contain only valid, predefined codes.

### ✔ Geometry Integrity Check  
Finds records that have missing or null geometries.

### ✔ CSV QA Report  
Outputs a timestamped CSV summarizing discovered issues, including:
- Issue type  
- Field name  
- ObjectID  
- Invalid value  
- Additional notes  

---

## 🧩 Requirements

This tool requires:

- ArcGIS API for Python (`arcgis`)
- pandas
- Python 3.7+

Install dependencies using:

```bash
pip install arcgis pandas
