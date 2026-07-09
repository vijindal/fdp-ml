# Machine Learning for Materials and Metallurgical Engineering

Faculty Development Programme (FDP) under the UGC – Malaviya Mission Teacher Training
Programme (MM-TTP), organized by the Centre for Faculty Development & Educational
Technology (CFDET), Indian Institute of Technology (BHU) Varanasi.

**Dates:** 13–18 July 2026 | **Mode:** Fully Online | **Coordinator:** Prof. Vikas Jindal,
Dept. of Metallurgical Engineering, IIT (BHU) Varanasi

---

## How to use these notebooks

Each practical session has a notebook in `notebooks/` and, where needed, a dataset in
`data/`. You do **not** need to install anything locally -- everything runs in Google Colab.

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

| Day | Session | Practical | Open in Colab |
|---|---|---|---|
| 1 | 3 | Hall-Petch relation -- linear regression & linearization (7-point example dataset) | [Open](https://colab.research.google.com/github/vijindal/fdp-ml/blob/main/day1/day1_hallpetch_practical.ipynb) |
| 1 | 3 | Hall-Petch across a real literature dataset (Copper, 198 points) -- data-fetching techniques, quizzes, nanocrystalline breakdown | [Open](https://colab.research.google.com/github/vijindal/fdp-ml/blob/main/day1/day1_session3_cu_practical.ipynb) |
| 1 | 4 | Gradient descent -- cost function derivation, worked convergence, convexity, hyperparameters, feature scaling | [Open](https://colab.research.google.com/github/vijindal/fdp-ml/blob/main/day1/day1_session4_gradient_descent.ipynb) |
| 2 | -- | Feature engineering & descriptors -- predicting alloy phase from composition (MPEA dataset, ~1,545 alloys); Magpie-style descriptors by hand and automated, feature selection | [Open](https://colab.research.google.com/github/vijindal/fdp-ml/blob/main/day2/FeatureEngineering_Descriptors.ipynb) |
| 3 | 3 | Clustering practical on real nanoindentation data -- elbow/silhouette method, comparing baseline vs. engineered vs. combined feature sets | [Open](https://colab.research.google.com/github/vijindal/fdp-ml/blob/main/day3/Clustering_Session3_Nanoindentation_Practical.ipynb) |
| 3 | 4 | Dimensionality reduction (PCA) & spatial mapping -- component selection, re-clustering in reduced space, predicting a real spatial microstructure map | [Open](https://colab.research.google.com/github/vijindal/fdp-ml/blob/main/day3/Clustering_Session4_PCA_SpatialMap.ipynb) |
| 4 | | *(guest sessions -- Deep Learning/CNN; no notebook planned from coordinator side, TBD for bridge practical)* | |
| 5 | | *(guest sessions -- LLMs/GenAI and a second guest topic; no notebook planned from coordinator side, TBD for bridge practical)* | |

*(This table will be updated as each day's notebooks are finalized.)*

---

## Datasets

- **`day1_hallpetch.csv`** -- a small, clean 7-point grain-size/yield-stress example table.
- **`hallpetch_multimetal_data.csv`** -- 1,445 real grain-size/strength measurements across 20 pure metals, compiled from six decades of published literature. Sourced from:
  > Cordero, Z.C., Knight, B.E., & Schuh, C.A. (2016). *Six decades of the Hall-Petch effect -- a survey of grain-size strengthening studies on pure metals.* International Materials Reviews, 61(8), 495-512.
- **`day2/MPEA_dataset.csv`** -- ~1,545 multi-principal-element alloy compositions with phase labels, used for the Day 2 feature-engineering practical.
- **`day3/Training_set.csv`, `Test_set.csv`, `Validation_set.csv`** -- 2,621 nanoindentation measurements (S390 Microclean steel), 5 phase labels, used for the clustering practical. Sourced from:
  > Trost, C. et al. (2025). *Materials & Design*, 253:113897.
- **`day3/HSS_BW_3mN_map01 LC.txt`** -- raw spatial nanoindentation map (load-displacement curves), used for the predicted-only spatial microstructure visualization in Day 3 Session 4. No ground-truth phase labels exist for this specific map.

---

## Repo structure

```
fdp-ml/
├── README.md
├── requirements.txt        # for local/offline use only -- Colab needs none of this
├── day1/
│   ├── day1_hallpetch_practical.ipynb
│   ├── day1_hallpetch.csv
│   ├── day1_session3_cu_practical.ipynb
│   ├── hallpetch_multimetal_data.csv
│   └── day1_session4_gradient_descent.ipynb
├── day2/
│   ├── FeatureEngineering_Descriptors.ipynb
│   └── MPEA_dataset.csv
├── day3/
│   ├── Clustering_Session3_Nanoindentation_Practical.ipynb
│   ├── Clustering_Session4_PCA_SpatialMap.ipynb
│   ├── Training_set.csv
│   ├── Test_set.csv
│   ├── Validation_set.csv
│   └── HSS_BW_3mN_map01 LC.txt
├── day4/                    # coming soon -- guest sessions (Deep Learning/CNN)
└── day5/                    # coming soon -- guest sessions (LLMs/GenAI + TBD)
```

## Contact

Prof. Vikas Jindal, Dept. of Metallurgical Engineering, IIT (BHU) Varanasi
