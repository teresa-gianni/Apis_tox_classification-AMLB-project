# Classification of pesticide toxicity to honey bees
This basic machine learning project involves training a model using a given set of data to enable it to predict the toxicity level of various pesticides to honey bees.
## Description of the dataset
**Overview:**

**Number of instances:** 1035  
**Number of attributes:** 11 features + 2 targets (one for binary classification and one for multiclass classification)  
**Associated task:** Multiclass classification (Outcome: 0 - non-toxic, 1 - moderately toxic, 2 - highly toxic)

**Variables Description:**

| Feature           | Type        | Description                                                                 |
|-------------------|-------------|-----------------------------------------------------------------------------|
| name              | Categorical | Chemical name, either according to IUPAC nomenclature or a commonly used trivial name. |
| CID               | Integer     | PubChem Compound ID number.                                                 |
| CAS               | Categorical | Chemical Abstracts Service registry number. A globally recognized identifier assigned by CAS, usually written in three blocks of numbers. |
| SMILES            | Categorical | Molecule structure in SMILES format (text-based representation of a molecule’s structure using specific rules). |
| source            | Categorical | Compound source: ECOTOX, PPDB or BPDB (databases from which the compound information was collected). |
| year              | Integer     | First publication year in literature according to PubChem.                  |
| toxicity_type     | Categorical | Strongest toxicity type: Contact, Oral or Other.                            |
| herbicide         | Binary      | Boolean (yes=1/no=0) feature indicating whether the chemical is used as a herbicide. |
| fungicide         | Binary      | Boolean (yes=1/no=0) feature indicating whether the chemical is used as a fungicide. |
| insecticide       | Binary      | Boolean (yes=1/no=0) feature indicating whether the chemical is used as an insecticide. |
| other_agrochemical| Binary      | Boolean (yes=1/no=0) feature indicating whether the chemical is used in other way as an agrochemical. |
| label             | Binary      | Binary toxicity label (0 = non-toxic, 1 = toxic).                           |
| ppdb_level        | Integer     | Ternary toxicity level (0 = non-toxic, 1 = moderately toxic, 2 = highly toxic). |

## Pipeline of the project
- Initial setup importing the required packages and libraries
- Download of the dataset
- Explorative data analysis (EDA)
- Split data in train and test set
- Data preprocessing
- Feature selection
- Model training
- Performance evaluation 

Tha same pipeline has been applied to solve firstly a multiclass classification problem using the output column 'ppdb_level' and secondly to a binary classification problem using the column 'label'. 

The entire workflow and code of this project can be found at  
