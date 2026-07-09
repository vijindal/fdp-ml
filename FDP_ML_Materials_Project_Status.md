# FDP: Machine Learning for Materials and Metallurgical Engineering
**Project Background & Status Tracker**

Last updated: 9 July 2026

---

## 0. Source Documents (Project Files)

- `260707selection_confirmation.pdf` — Selection confirmation email from CFDET TL Cell (7 Jul 2026), confirms online mode, timing, Google Meet link, e-certificate attendance requirement (24/24 sessions)
- `260707_invitation.pdf` — Google Calendar invite (Mon 13 Jul 09:45 – Sat 18 Jul 18:15 IST), same Meet link
- `Leaflet_FDP_1318_July_2026.pdf` — Official CFDET leaflet: lists "Hybrid Mode" (superseded — see Section 1), registration steps via mmc.ugc.ac.in
- `Participants_5.xlsx` — Registered participant list (n = 52)
- `syllabus.pdf` — Separate, related 9-credit institute elective ("Materials Informatics for Metallurgy," Dr. Vikas Jindal convener) — same topic arc, semester-length academic sibling of this FDP
- `slides-ch11-ML.pdf` — Prof. Jindal's prepared lecture deck, based on Google's ML Crash Course (Linear Regression + Logistic Regression + Classification modules); source material for Day 1
- `notes-ch10-curvefit-regression.docx` — Numerical-methods chapter; source of the Hall-Petch and lattice-parameter/XRD case studies (Section 3)
- `ML-3.pdf` — Prof. Jindal's prepared unsupervised-learning deck (K-means algorithm, cost function, elbow method) + two real case studies (Converter Energy Diagnostics, LF Refining Slag Prediction); source material for the Clustering topic (Section 4)

---

## 1. Background

**Programme:** FDP on *Machine Learning for Materials and Metallurgical Engineering*, under UGC–Malaviya Mission Teacher Training Programme (MM-TTP).
**Host:** CFDET, IIT (BHU) Varanasi. **Coordinator:** Prof. Vikas Jindal, Dept. of Metallurgical Engineering.
**Dates:** 13–18 July 2026, 10:00 AM–5:00 PM daily. **Credits:** 3 MM-TTP (36 hrs, 24 sessions).
**Mode:** **Fully Online — finalized**, per the 7 Jul confirmation email (overrides leaflet's "Hybrid").
**Google Meet:** `meet.google.com/bty-gdhq-vyu`

---

## 2. Participant Profile (n = 52)

33M/19F · 27 General/15 OBC/10 SC · mostly Assistant Professors · 0–20 yrs experience · concentrated in Gujarat (Parul University) and Tamil Nadu (Sathyabama Institute) · **disciplines wider than core metallurgy** (wireless comms, VLSI, archaeology, finance, aerospace, polymer chemistry, etc.) · coding/ML background largely undisclosed, assumed minimal for many.

---

## 3. Course Design — Standing Decisions

- **Structure:** 6 days, 4 sessions/day (2 "lecture," 2 "practical" — labels are loose; see Section 6 on actual delivery mode). Day 6 = capstone presentations only.
- **Capstone:** introduced in Day 1's first session; mid-course check-in for title/details; no dedicated daily slot — woven into lectures instead.
- **Pedagogy:** Core-track only (scaffolded notebooks, everyone completes). Stretch/advanced content is informal, facilitator-discretion, **not documented or evaluated**.
- **Assessment (completion-based):** in-session MCQs (formative) + certificate requires full theory attendance + complete practical submissions. Any gap disqualifies. *(Open reconciliation item: a national MM-TTP marks-based scheme — 2 MCQ tests + assignments + response, /100, <50 disqualifies — may apply on top of this; not yet confirmed with CFDET.)*
- **AI/LLM use policy:** explicitly allowed and expected, including in the capstone. Bar for assessment = can the participant explain/defend their results, not whether they wrote every line themselves.
- **Depth-first philosophy (superseding the original 10-practical/5-day breadth plan):** we build content topic-by-topic — case study → theory → operational parts → practical — and let actual content weight tell us where day boundaries fall, rather than pre-assigning days. **Day 1 (Linear Regression) is fully built and consumed all 4 sessions.** The "Clustering" topic (originally slated as part of Day 3) is currently mid-build and has already outgrown a single session — see Section 5.
- **Original 6-topic/10-practical skeleton** (kept for reference, no longer the operative plan): Day1 Linear Regression → Day2 Classification/Feature Engineering → Day3 Model Evaluation/Unsupervised → Day4 Neural Networks/CNN → Day5 GenAI *or* Bayesian Optimisation (fork never resolved) → Day6 Capstone.

---

## 4. Datasets — Sourced, Verified, In Use

| Dataset | Topic | Status |
|---|---|---|
| **Hall-Petch 7-point table** (from notes-ch10) | Day 1, linear regression | ✅ Built, verified, live on GitHub |
| **Cordero, Knight & Schuh (2016)** — 1,445 grain-size/strength measurements, 20 pure metals, *Int. Mater. Rev.* | Day 1, Cu case study | ✅ Built, verified, live on GitHub |
| **Trost et al. (2025)** — S390 Microclean nanoindentation, 2,621 rows (train/val/test), 5 phase labels, *Materials & Design* 253:113897 | Clustering topic | ✅ Fully verified — reproduced published F1 scores almost exactly (A: 0.686 vs 0.689; B: 0.763 vs 0.761; C: 0.760 vs 0.760). **Not yet uploaded to GitHub** or built into a course notebook. |
| — Raw P-d curves (400 files, Testing_Map) | Clustering — spatial map / raw-signal illustration | ✅ Obtained. No ground-truth labels exist for this map (confirmed by checking the raw data drop) — spatial visualization can only be **predicted-only**, Feature-Set-A (Er, H), not predicted-vs-actual. |
| — Full raw dataset (all 4 variants: BV/SV/LCV/SAV) | Clustering (potential future use) | ✅ Obtained (large zip), not yet used beyond confirming Testing_Map contents |

**GitHub repo:** `github.com/vijindal/fdp-ml` (public). Current contents: `day1/` only (Hall-Petch notebook + CSV, Cu-practical notebook, multimetal CSV, gradient-descent notebook). **No `day2/`–`day5/` folders exist yet** — the Clustering-topic materials built so far are local files only, not yet pushed.

---

## 5. Current Build Status by Topic

### Day 1 — Linear Regression: ✅ COMPLETE (4 sessions)
- Session 1: Opening Presentation (13 slides) + Case Study Trailer (7 slides) + ML Overview (23 slides)
- Session 2: Hall-Petch Theory (8 slides) + Lattice Parameter/XRD Theory (8 slides) + Python-for-Hall-Petch (17 slides)
- Session 3: Combined notebook — Part 0 (linear regression fundamentals, slides 24–33) + Part 1 (Cu practical: data-fetching techniques, loss/parameters exploration, fit, nanocrystalline breakdown) — 55 cells
- Session 4: Gradient descent notebook — cost function derivation, worked convergence, convexity, hyperparameters (learning rate divergence demo), feature scaling — 28 cells
- All notebooks verified end-to-end against live GitHub-hosted data.

### Clustering (topic originally slated for part of Day 3) — 🔶 IN PROGRESS, has outgrown one session
- **Session 1 (K-means theory): 37 slides built.** Covers: ML-systems recap, unsupervised motivation, K-means algorithm (formal steps), manual similarity measures (RMSE, Jaccard), a fully-verified worked numeric example on real Er/H nanoindentation values, non-separated-clusters caveat, optimization objective, random init, local optima, elbow method, silhouette score, cluster cardinality/magnitude, anomaly spotting, reassessing similarity measures, troubleshooting checklist, advantages/disadvantages (incl. "always converges," "warm-starting"), **curse of dimensionality** (sets up PCA justification for later). 7 quizzes, all verified in sequence.
  - ⚠️ **At ~37 slides this is almost certainly 2 sessions' worth of content, not 1** — this was flagged to the user and is an open decision (see Section 7).
- **Session 2, Part 1 (concepts/workflow): 12 slides built.** Covers Google's "What is clustering," "Clustering algorithms" (4 families: centroid/density/distribution/hierarchical), "Clustering workflow," "Data preparation" (scaling, transforms, missing data). 2 quizzes.
- **Session 2, Part 2 (case studies): NOT YET BUILT as a standalone deck.** Source material exists (ML-3.pdf slides 16–21: Converter Energy Diagnostics, LF Refining Slag Prediction) but hasn't been converted/rebuilt.
- **Session 3 (nanoindentation practical): NOT YET BUILT.** Data fully ready (see Section 4).
- **Session 4 (PCA + spatial map): NOT YET BUILT.** Data ready for PCA; spatial map limited to Feature-Set-A, predicted-only (no ground truth for that specific map).

### Day 2 (Classification/Feature Engineering), Day 4 (Neural Nets/CNN), Day 5 (GenAI/Bayesian Opt — fork unresolved): **not started.**

---

## 6. STYLE GUIDE — for continuity in a new chat

### PPTX conventions (all built via `pptxgenjs`, Node.js)
- **Layout:** `LAYOUT_WIDE` (13.3×7.5"). **Author:** "Prof. Vikas Jindal".
- **Colors:** Navy `1F3864` (titles, emphasis), Black `262626` (body), Grey `595959` (secondary/footer), White `FFFFFF` (background). No other colors, no icons, no decorative graphics — **plain, text-first style matching the user's own ch11 deck** (explicitly requested: "keep presentation simple as my style").
- **Standard slide anatomy:** Title (Calibri 30pt bold navy, top-left) → thin grey horizontal line divider → bullet body (Calibri 20pt, `•` top-level / `▪` sub-level via `bullet.code`) → small grey footer with deck name + session label.
- **Quiz slides:** headed "Quick Check N" (grey, 20pt), question in navy bold, lettered options (i)/(ii)/(iii), **answer placed in speaker notes only** (`slide.addNotes(...)`) — never shown on-slide, so it can be posed live and revealed verbally.
- **Title slides:** kicker line (grey) → big navy title → thin divider → grey subtitle/context lines.
- **Reusable helper functions per script:** `bulletSlide(title, bullets, opts)`, `quizSlide(qLabel, question, options, answerNote)`, `titleSlide(...)`, `footer(slide)` — copy these from any existing build script rather than rewriting.
- **Build pipeline (always, every deck):** write `.pptx` via pptxgenjs → `python3 /mnt/skills/public/pptx/scripts/rezip.py <file>` → `extract-text` for placeholder/content QA → convert to PDF + render JPEGs for visual spot-check.
- **⚠️ CRITICAL RECURRING BUG:** repeatedly (5+ times across this project) mistakenly used broken unicode superscript sequences (e.g., `\u2074\u2071\u2075\u2074` attempting "^(i)", or `\u141F` — a Canadian Aboriginal syllabics character — attempting a slash) instead of proper notation. **ALWAYS run this scan before building any deck with math/exponents:**
  ```python
  import re
  content = open('build_script.js', encoding='utf-8').read()
  escapes = re.findall(r'\\u([0-9A-Fa-f]{4})', content)
  safe_blocks = [(0x0020,0x007E),(0x00A0,0x024F),(0x0370,0x03FF),(0x2000,0x209F),(0x1D00,0x1D7F)]
  flagged = set(int(e,16) for e in escapes if not any(lo<=int(e,16)<=hi for lo,hi in safe_blocks))
  print([hex(c) for c in flagged])
  ```
  Then manually verify any flagged codepoint is legitimate (√ U+221A, − U+2212, → U+2192 are fine; anything else, check carefully). **Prefer plain notation** (`x^(i)`, `d^(-1/2)`) over unicode superscripts entirely — safer and it's what we've converged on.
- **Copyright practice:** Google Crash Course / Clustering course content is paraphrased in our own words throughout, never copied verbatim — consistent with copyright policy even though the material is being used for legitimate teaching purposes.

### Jupyter notebook conventions (`.ipynb`, built via Python `json` — not `nbformat`)
- Built with a helper script pattern: `md(src)` and `code(src)` functions appending to a `cells` list, then dumped as nbformat-4 JSON with `"colab": {"provenance": []}` in metadata.
- **Structure:** Title markdown cell (with dataset citation if real published data) → Setup/imports cell (once, at the top — not repeated) → numbered/lettered sections (`## Step 1 —`, `## Part A —`) mixing markdown explanation with code → embedded quizzes as a markdown "Quick Check N" question cell immediately followed by a separate "**Answer:** ..." markdown cell (same reveal-below pattern as PPTs) → Wrap-up markdown cell at the end, previewing what's next.
- **Data loading:** always via a `DATA_URL` variable pointing to `raw.githubusercontent.com/vijindal/fdp-ml/main/<day>/<file>.csv` — never local upload, per the "no local install, one-click Colab" design decision.
- **Verification practice (non-negotiable, done for every notebook before delivery):** extract all code cells into a `.py` file, run with `python3 -W error` (or at least `matplotlib.use('Agg')` for headless plotting) to confirm zero errors/warnings, confirm printed numbers match hand-verified expectations. For anything already pushed to GitHub, additionally re-run against the **live** raw URL (not just local files) to confirm end-to-end.
- **Repo file-naming pattern:** `day1/day1_<topic>_practical.ipynb`, `day1/<dataset_name>.csv` — mirror this for future days (`day2/...`, etc.) once day boundaries are settled.

### General working pattern with this user
- User prefers **discussion/confirmation before large builds**, especially when a design choice has trade-offs (e.g., session splits, dataset choices, which technique gets which day) — surface options, give an honest recommendation, but let them decide.
- User has repeatedly asked to **verify real data/numbers before building** (dataset structure, published-paper reproduction) rather than assume — this has caught real issues every time it's been done (e.g., the gradient-descent table discrepancy in the user's own deck, the O(n) vs O(nk) complexity error).
- When something doesn't fit as planned (e.g., missing dataset, factual error, scope creep), **flag it plainly and propose 2–3 concrete options** rather than silently picking one.
- Files are always copied to `/mnt/user-data/outputs/` and delivered via `present_files` — never assume the user can see `/home/claude/` working files.

---

## 7. Open Items / Pending Decisions

- [ ] **Clustering Session 1 (37 slides) almost certainly needs to split into two sessions** — not yet decided how (e.g., split at "worked example," or at "choosing K," or reallocate some content into Session 2). Flagged to user, awaiting direction.
- [ ] Build Clustering Session 2 Part 2 (case studies — Converter Energy, LF Refining) as a standalone deck.
- [ ] Build Clustering Session 3 (nanoindentation practical notebook) — data fully ready.
- [ ] Build Clustering Session 4 (PCA + spatial map notebook) — data ready, spatial map will be predicted-only (no ground truth available for that map).
- [ ] Push all Clustering-topic files to GitHub (`day2/` or `day3/` folder — naming TBD until day-split is settled).
- [ ] Reconcile completion-based certification with the possible national MM-TTP marks-based scheme (Section 3).
- [ ] Day 5 fork (Generative AI *vs.* Bayesian Optimisation) never resolved — leaned toward Bayesian Optimisation earlier (maps to real alloy-design workflow) but not confirmed.
- [ ] Day 2 (Classification/Feature Engineering) and Day 4 (Neural Nets/CNN) not yet checked against relevant Google Crash Course modules the way Day 1 and Clustering were — that check has caught real gaps/errors every time it's been done, worth doing before building either.
- [ ] Fully-online delivery/logistics plan (platform mechanics, attendance tracking) — flagged very early, never built.
- [ ] Google Classroom vs. plain Drive-folder submission tracking — discussed, leaning toward Drive folder, not finalized.

---

## 8. Immediate Next Step

Resolve the Clustering Session 1 length/split question, then continue building Session 2's case studies and Sessions 3–4's practical notebooks in the same verified, style-consistent manner described in Section 6.
