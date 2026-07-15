# Machine Learning for Materials and Metallurgical Engineering

Faculty Development Programme (FDP) under the UGC – Malaviya Mission Teacher Training
Programme (MM-TTP), organized by the Centre for Faculty Development & Educational
Technology (CFDET), Indian Institute of Technology (BHU) Varanasi.

**Dates:** 13–18 July 2026 | **Mode:** Fully Online | **Coordinator:** Prof. Vikas Jindal,
Dept. of Metallurgical Engineering, IIT (BHU) Varanasi

---

## How to use these notebooks

Each practical session has a notebook in `notebooks/`, along with the datasets it needs
(also in `notebooks/`). You do **not** need to install anything locally -- everything runs
in Google Colab.

**Steps for every practical:**
1. Click the "Open in Colab" link for that day (see table below).
2. As your very first action, go to **File -> Save a copy in Drive**. This creates your
   own editable copy -- you'll be working in that copy, not the shared original.
3. Run cells top to bottom (Shift+Enter). Data loads automatically from this repo; no
   file upload required.
4. If a notebook needs extra libraries (matminer, pymatgen, BoTorch, etc.), the first
   code cell will install them with `!pip install` -- just run it and wait a few seconds.
5. Save your completed notebook back to your Drive (auto-saves) and submit as instructed
   by the coordinator (required for certification -- see programme guidelines).

---

## Notebooks

| Day | Practical | Open in Colab |
|---|---|---|
| 1 | Hall-Petch relation -- linear regression & linearization | [Open](https://colab.research.google.com/github/vijindal/fdp-ml/blob/main/notebooks/day1_session3_cu_practical.ipynb) |
| 1 | Feature Engineering & Descriptors for Materials | [Open](https://colab.research.google.com/github/vijindal/fdp-ml/blob/main/notebooks/day1_session4_FeatureEngineering_Descriptors.ipynb) |
| 2 | Gradient descent -- cost function derivation, worked convergence, convexity, hyperparameters, feature scaling | [Open](https://colab.research.google.com/github/vijindal/fdp-ml/blob/main/notebooks/day2_session2_gradient_descent.ipynb) |
| 2 | Logistic regression -- classifying alloy phase (FCC vs. not-FCC) on the MPEA dataset; sigmoid, decision boundary, confusion matrix, precision/recall, ROC vs. PR curves, and L2 regularization | [Open](https://colab.research.google.com/github/vijindal/fdp-ml/blob/main/notebooks/day2_session2_LogisticRegression_Classification.ipynb) |
| 3 | Random Forest & ensemble methods -- decision trees, bagging, feature importance on steel strength prediction | [Open](https://colab.research.google.com/github/vijindal/fdp-ml/blob/main/notebooks/Day3_Session2_RandomForest_Practical.ipynb) |
| 3 | Clustering & dimensionality reduction -- K-means, hierarchical clustering, PCA, and spatial mapping of nanoindentation data | [Open](https://colab.research.google.com/github/vijindal/fdp-ml/blob/main/notebooks/Day3_Session4_Clustering_Practical.ipynb) |
| Capstone | Fully worked capstone example -- Random Forest regression on the steel strength dataset, start to finish | [Open](https://colab.research.google.com/github/vijindal/fdp-ml/blob/main/notebooks/Capstone_Template_Notebook.ipynb) |

*(This table will be updated as each day's notebooks are finalized.)*

---

## Repo structure

```
fdp-ml/
├── README.md
├── requirements.txt        # for local/offline use only -- Colab needs none of this
└── notebooks/               # all notebooks and their datasets, loaded directly via raw GitHub URL
    ├── day1_session3_cu_practical.ipynb
    ├── hallpetch_multimetal_data.csv
    ├── day1_session4_FeatureEngineering_Descriptors.ipynb
    ├── SupplementaryMaterial1_GrainSizeStrengtheningData.txt
    ├── SupplementaryMaterial2_ExperimentalInfo.pdf
    ├── day2_session2_gradient_descent.ipynb
    ├── day2_session2_LogisticRegression_Classification.ipynb
    ├── MPEA_dataset.csv
    ├── MPEA_featurized.csv
    ├── Day3_Session2_RandomForest_Practical.ipynb
    ├── steel_strength.csv
    ├── Day3_Session4_Clustering_Practical.ipynb
    ├── Training_set.csv
    ├── Test_set.csv
    ├── Validation_set.csv
    ├── HSS_BW_3mN_map01 LC.txt
    └── BayesianOptimisation_AlloyHardness_Practical.ipynb
```

## Contact

Prof. Vikas Jindal, Dept. of Metallurgical Engineering, IIT (BHU) Varanasi
