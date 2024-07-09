# Alzheimer's Disease in Mus Musculus - RNA-seq Analysis

## Project Overview
This project involves the analysis of RNA-seq data related to Alzheimer's disease in Mus Musculus (mice). The data has been sourced from Refine.Bio and will be used to investigate specific scientific questions related to gene expression differences in Alzheimer's disease.

## Dataset Information
The dataset includes RNA-seq data for Mus Musculus samples, focusing on Alzheimer's disease. The dataset contains at least 73 samples, ensuring robust analysis.

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

## Contents

This download includes gene expression matrices and experiment and sample metadata for the samples that you selected for download.

* The `aggregated_metadata.json` file contains information about the options you selected for download.
Specifically, the `aggregate_by` and `scale_by` fields note how the samples are grouped into gene expression matrices and how the gene expression data values were transformed, respectively.
The `quantile_normalized` fields note whether or not quantile normalization was performed.
Currently, we only support skipping quantile normalization for RNA-seq experiments when aggregating by experiment on the web interface.

* Individual gene expression matrices and their corresponding sample metadata files are in their directories.

* Gene expression matrices are the tab-separated value (TSV) files named by the experiment accession number (if aggregated by experiment) or species name (if aggregated by species).
Note that samples are _columns_ and rows are _genes_ or _features_.
This pattern is consistent with the input for many programs specifically designed for working with high-throughput gene expression data. Still, it may be transposed from what other machine learning libraries expect.

* Sample metadata (e.g. disease vs. control labels) are contained in TSV files with `metadata` in the filename and any JSON files.
We apply light harmonization to some sample metadata fields, which are denoted by `refinebio_` (`refinebio_annotations` is an exception).
The contents of a sample's `refinebio_annotations` field include the submitter-supplied sample metadata.

* Experiment metadata (e.g., experiment title and description) are contained in JSON files with `metadata` in the filename.

Please see [our documentation](https://refinebio-docs.readthedocs.io/) for more details.

## Usage

The gene expression matrix TSV and JSON files can be read in, manipulated, or parsed with standard functions or libraries in the language of your choice.
Below are some code snippets to help you import the data into R or Python and examine it.

### Reading TSV Files

Here's an example reading a gene expression TSV (`GSE11111.tsv`) into R as a data.frame with base R:

```
expression_df <- read.delim("GSE11111.tsv", header = TRUE,
							row.names = 1, stringsAsFactors = FALSE)
```

### Reading JSON Files

#### R

The `rjson` R package allows us to read a metadata JSON file (`aggregated_metadata.json`) into R as a list:

```
library(rjson)
metadata_list <- fromJSON(file = "aggregated_metadata.json")
```

#### Python

In Python, we can read in the metadata JSON like so:

```
import json
with open('aggregated_metadata.json', 'r') as jsonfile:
    data = json.load(jsonfile)
print(data)
```

For example R workflows, such as clustering of gene expression data, please see [our repository of example uses](https://github.com/AlexsLemonade/refinebio-examples).

## Contact

If you identify issues with this download, please [file an issue on GitHub](https://github.com/AlexsLemonade/refinebio/issues).
If you would prefer to report issues via e-mail, you can also email [requests@ccdatalab.org](mailto:requests@ccdatalab.org).

## Citing refine.bio

Please use the following:

Casey S. Greene, Dongbo Hu, Richard W. W. Jones, Stephanie Liu, David S. Mejia, Rob Patro, Stephen R. Piccolo, Ariel Rodriguez Romero, Hirak Sarkar, Candace L. Savonen, Jaclyn N. Taroni, William E. Vauclain, Deepashree Venkatesh Prasad, Kurt G. Wheeler. **refine.bio: a resource of uniformly processed publicly available gene expression datasets.** URL: https://www.refine.bio


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
