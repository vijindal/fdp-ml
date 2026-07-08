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
| 1 | 4 | *(coming soon -- Fe/BCC and Ti/HCP comparison)* | |
| 2 | | *(coming soon)* | |
| 3 | | *(coming soon)* | |
| 4 | | *(coming soon)* | |
| 5 | | *(coming soon)* | |

*(This table will be updated as each day's notebooks are finalized.)*

---

## Datasets

- **`day1_hallpetch.csv`** -- a small, clean 7-point grain-size/yield-stress example table.
- **`hallpetch_multimetal_data.csv`** -- 1,445 real grain-size/strength measurements across 20 pure metals, compiled from six decades of published literature. Sourced from:
  > Cordero, Z.C., Knight, B.E., & Schuh, C.A. (2016). *Six decades of the Hall-Petch effect -- a survey of grain-size strengthening studies on pure metals.* International Materials Reviews, 61(8), 495-512.

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
│   └── hallpetch_multimetal_data.csv
├── day2/                    # coming soon
├── day3/                    # coming soon
├── day4/                    # coming soon
└── day5/                    # coming soon
```

## Contact

Prof. Vikas Jindal, Dept. of Metallurgical Engineering, IIT (BHU) Varanasi
