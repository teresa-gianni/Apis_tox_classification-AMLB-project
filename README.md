# Classification of Pesticide Toxicity to Honey Bees

This project focuses on the application of **machine learning methods** to predict the toxicity level of pesticides to honey bees.  
The study relies on a curated dataset that includes chemical descriptors and toxicological information.

## Dataset Description

### **Overview**

- **Number of instances:** 1035  
- **Number of attributes:** 11 features + 2 targets  

### **Tasks:**  
  - **Binary classification** (Target: `label`)  
  - **Multiclass classification** (Target: `ppdb_level`)  

### Variables

| Feature             | Type        | Description                                                                 |
|---------------------|-------------|-----------------------------------------------------------------------------|
| `name`              | Categorical | Chemical name (IUPAC nomenclature or commonly used trivial name).           |
| `CID`               | Integer     | PubChem Compound ID.                                                        |
| `CAS`               | Categorical | CAS Registry Number (globally recognized identifier, format: XXX-XX-X).     |
| `SMILES`            | Categorical | Molecule structure in SMILES format (text-based structural representation). |
| `source`            | Categorical | Data source: ECOTOX, PPDB or BPDB.                                          |
| `year`              | Integer     | First publication year in literature (PubChem).                             |
| `toxicity_type`     | Categorical | Strongest toxicity type: Contact, Oral, or Other.                           |
| `herbicide`         | Binary      | 1 if used as herbicide, 0 otherwise.                                        |
| `fungicide`         | Binary      | 1 if used as fungicide, 0 otherwise.                                        |
| `insecticide`       | Binary      | 1 if used as insecticide, 0 otherwise.                                      |
| `other_agrochemical`| Binary      | 1 if used for other agrochemical purposes, 0 otherwise.                     |
| `label`             | Binary      | Binary toxicity label: 0 = non-toxic, 1 = toxic.                            |
| `ppdb_level`        | Integer     | Ternary toxicity level: 0 = non-toxic, 1 = moderately toxic, 2 = highly toxic. |

## Project Pipeline

1. **Setup** – Import of the required libraries and packages  
2. **Data acquisition** – Loading of the dataset  
3. **Exploratory Data Analysis (EDA)**  
4. **Data splitting** – Train/test partition  
5. **Preprocessing** – Data cleaning, encoding, and normalization  
6. **Feature selection**  - With SelectKBest and Recursive Feature Elimination (RFE)
7. **Model training**  - Among different models 
8. **Performance evaluation** - On the best performing model resulted from the comparison

The pipeline was applied twice:  
- Multiclass classification using `ppdb_level` as target  
- Binary classification using `label` as target  

The complete workflow and source code are available at:  
[Project Notebook](https://github.com/teresa-gianni/Machine-Learning-project/blob/main/AMLB_project_Teresa_Gianni.ipynb)


## Author

**Teresa Gianni**  
Alma Mater Studiorum – University of Bologna (Italy)  
Email: [teresa.gianni@studio.unibo.it](mailto:teresa.gianni@studio.unibo.it)
