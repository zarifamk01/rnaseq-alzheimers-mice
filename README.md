# Alzheimer's Disease in Mus Musculus - RNA-seq Analysis

## Project Overview
This project involves the analysis of RNA-seq data related to Alzheimer's disease in Mus Musculus (mice). The data has been sourced from Refine.Bio and will be used to investigate specific scientific questions related to gene expression differences in Alzheimer's disease.

## Dataset Information
The dataset includes RNA-seq data for Mus Musculus samples, focusing on Alzheimer's disease. The dataset contains at least 50 samples, ensuring robust analysis.

### Data Source
- **Source:** [Refine.Bio](https://www.refine.bio/)
- **Dataset Title:** TREM2 Acts Downstream of CD33 in Modulating Microglial Pathology in Alzheimer's Disease
- **Accession Number:** [SRP201011](https://www.refine.bio/experiments/SRP201011)
- **Description:** This dataset explores the role of TREM2 and CD33 in modulating microglial pathology in Alzheimer's disease using RNA-seq technology in Mus Musculus models.
- **Instructions to Download:**
  1. Go to [Refine.Bio](https://www.refine.bio/).
  2. Search for "TREM2 Acts Downstream of CD33 in Modulating Microglial Pathology in Alzheimer's Disease".
  3. Select the dataset with accession number SRP201011.
  4. Download the dataset.

## Scientific Question
The main objective of this project is to investigate gene expression differences between Alzheimer's disease samples and healthy control samples in Mus Musculus. Specific questions include:
- What are the key gene expression differences between Alzheimer's disease and healthy samples?
- Can we identify specific biomarkers associated with Alzheimer's disease in mice?

## Project Structure
- `data/`: Directory containing the RNA-seq data files.
- `notebooks/`: Jupyter notebooks for data analysis.
- `results/`: Directory for storing analysis results and figures.
- `src/`: Source code for data processing and analysis scripts.
- `README.md`: Project overview and information.

/alzheimers-mice-rnaseq-analysis
│
├── data/ # Directory for data files
│ ├── README.md # Instructions on how to download the data
│ └── sample_data.csv # (Optional) Sample data for demonstration
│
├── notebooks/ # Jupyter Notebooks
│ └── analysis.ipynb # Main analysis notebook
│
├── .gitignore # Git ignore file
├── README.md # Project README
└── requirements.txt # Python dependencies

## Instructions for Use
1. Clone the repository:
   ```bash
   git clone https://github.com/zarifamk01/rnaseq-alzheimers-mice.git
