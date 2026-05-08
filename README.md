# ESLpred: SVM-based Method for Subcellular Localization of Eukaryotic Proteins

Welcome to the official documentation for **ESLpred**, a computational tool developed to predict the subcellular localization of eukaryotic proteins using Support Vector Machines (SVM). Accurate functional annotation of genomes relies heavily on knowing where a protein resides within a cell. ESLpred utilizes diverse protein features, including amino acid composition, dipeptide composition, and physico-chemical properties, to provide high-accuracy predictions.

**Web Server:** [http://www.imtech.res.in/raghava/eslpred/](http://www.imtech.res.in/raghava/eslpred/)(https://webs.iiitd.edu.in/raghava/haptendb)

---

## Citation

Bhasin, M., & Raghava, G. P. S. (2004). 
**ESLpred: SVM-based method for subcellular localization of eukaryotic proteins using dipeptide composition and PSI-BLAST.** *Nucleic Acids Research*, 32(Web Server issue), W414-W419. 
[https://doi.org/10.1093/nar/gkh350](https://doi.org/10.1093/nar/gkh350)

---

## About the Platform

ESLpred was designed to improve upon existing subcellular localization methods that were limited to either simple amino acid composition or N-terminal characteristics. By implementing SVM and integrating multiple features into a hybrid module, ESLpred achieves superior performance in classifying proteins into four major subcellular locations:
* **Cytoplasmic**
* **Nuclear**
* **Mitochondrial**
* **Extracellular**

### Key Features
* **SVM-Light Implementation**: Utilizes the SVM-light package with a radial basis function (RBF) kernel for robust classification.
* **PSI-BLAST Integration**: Incorporates similarity searches against a database of experimentally annotated proteins to refine predictions.
* **Hybrid Approach**: Combines dipeptide composition, amino acid composition, and physico-chemical properties for maximum accuracy.

---

## Technical Overview

The method was developed and validated using a non-redundant dataset of 2,183 eukaryotic proteins (1,192 cytoplasmic, 464 nuclear, 391 extracellular, and 136 mitochondrial).

| Feature / Module | Accuracy (%) |
| :--- | :--- |
| **Amino Acid Composition** | 71.3% |
| **Dipeptide Composition** | 71.5% |
| **Physico-chemical Properties** | 65.4% |
| **PSI-BLAST** | 71.1% |
| **Hybrid (SVM + PSI-BLAST)** | 88.0% |

---

## Model Features

* **Dipeptide Composition**: Captures local order information by representing a protein as a 400-dimensional vector.
* **Physico-chemical Properties**: Includes features such as hydrophobicity, hydrophilicity, and polarity.
* **Similarity Search**: Queries are searched against a curated dataset; if a significant hit is found, the localization of the hit is assigned to the query.

---

## Applications

* **Genome Annotation**: Automatically predicting the localization of newly sequenced eukaryotic proteins.
* **Drug Target Discovery**: Identifying extracellular or nuclear proteins that may serve as potential therapeutic targets.
* **Proteomics**: Assisting in the analysis of experimental data by providing cellular context.

---

## Contact & Authors

**G. P. S. Raghava** Bioinformatics Centre, Institute of Microbial Technology, Sector 39A, Chandigarh, India.  
**Email**: raghava@imtech.res.in

---

## License

This project is open-access and distributed under standard academic terms, permitting free use for research purposes provided the original work is properly cited.
