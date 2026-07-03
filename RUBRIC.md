# Formative 2 — Hidden Markov Models — Rubric

**Total Points: 60**

---

## 1. Data Collection & Quality — 10 pts
*Quality and completeness of activity recordings*

| Rating | Pts | Description |
| --- | --- | --- |
| **Excellent** | 10 | 16 well-labelled and cleaned files of 5–10s each are present (approximately 4 per activity). A minimum of four activities recorded, each captured in 5–10s clips. Windowing is based on the sampling rate, and you explain the logic of why you selected the window size based on the sampling rate. You explain how you dealt with different sampling rates (across devices or sessions). Includes visualization plots of sample data in the report generated from the notebook. |
| **Good** | 7 | Minor inconsistencies, uneven sampling, or slightly fewer than 16 files (e.g., 12–15). Most clips fall within 5–10s, but some are slightly shorter or longer. Sampling rate explanation is present but lacks depth or doesn't fully explain the differences between rates. Visualizations are included but might be basic or lack clarity. |
| **Fair** | 5 | Missing one activity or timestamp errors in several files. Significant number of files below the 16-file target (e.g., 8–11). Clip durations frequently fall outside the 5–10s range. Sampling rate justification is brief or missing. Minimal or no visualizations of the raw or sampled data. |
| **Needs Improvement** | 3 | Unusable data. Fewer than 8 files are usable, or data is missing one or more entire activity categories. Widespread timestamp errors or large gaps. No explanation or justification for the data collection, cleaning, or sampling rate. |

---

## 2. Feature Extraction (Time & Frequency Domain) — 10 pts
*Feature engineering and extraction quality*

| Rating | Pts | Description |
| --- | --- | --- |
| **Excellent** | 10 | >3 highly relevant features extracted, specifically including >2 time-domain features (e.g., RMS, variance) and >1 frequency-domain feature derived from the FFT. Every feature is fully justified with a clear explanation of why it helps distinguish the activities. All features correctly normalized using a well-suited method (e.g., Z-score), and the justification for the normalization method is provided. |
| **Good** | 7 | >3 features extracted, including at least one frequency feature, but the FFT-derived feature is either basic (e.g., only total power) or lacks strong justification. Features are computed, but normalization is entirely missing, incomplete, or incorrectly applied. Feature extraction process is correct but lacks depth in the explanation of relevance. |
| **Fair** | 5 | Few or unclear features extracted (e.g., only 1–2 basic features). If a frequency-domain feature is present, it is not clearly derived from the FFT or is incorrect. The selection lacks features from one of the required domains (time or frequency). Normalization is entirely missing, and there is only a brief or vague attempt at justifying the feature choices. |
| **Needs Improvement** | 3 | Missing or meaningless features. Fewer than 2 features extracted, or frequency-domain features are entirely absent. No attempt to justify or explain the chosen features. The feature extraction code contains major errors. |

---

## 3. Implementation (Viterbi / Baum–Welch) — 15 pts
*Code correctness and completeness*

| Rating | Pts | Description |
| --- | --- | --- |
| **Excellent** | 15 | Fully functional HMM with robust, error-free Viterbi decoding. Baum–Welch is fully implemented, uses a robust convergence check (e.g., log-likelihood < epsilon) as a stopping criterion, and converges effectively. Code is highly modular, well-documented, and seamlessly integrated. |
| **Good** | 11 | HMM structure is mostly sound, and Viterbi is functional. Baum–Welch is present but may be incomplete, struggles with convergence, or uses a fixed, arbitrary iteration limit instead of a proper convergence check. Code lacks modularity or comprehensive documentation. |
| **Fair** | 8 | Code runs but is poorly structured. Significant logical errors in either algorithm. Training is present but clearly flawed, does not converge correctly, or does not include any convergence check, yielding suboptimal and unstable results. |
| **Needs Improvement** | 5 | Non-functional or clearly copied code. Fundamental errors in the algorithms. No attempt at a correct implementation. |

---

## 4. Evaluation on Unseen Data — 10 pts
*Model testing and performance reporting*

| Rating | Pts | Description |
| --- | --- | --- |
| **Excellent** | 10 | Tested on unseen data (2 test files). Sensitivity, specificity, and accuracy are reported, and results discussion is personalized and detailed, showing deep reflection and discussion. Visualizations of Transition Probabilities and Emission Probabilities are present. Confusion Matrix is generated from the test data. |
| **Good** | 7 | Metrics computed, weak discussion or lack of personalized reflection. Only >1 test file used. Transition/Emission Probability visualizations are present, but Confusion Matrix is missing. |
| **Fair** | 5 | Partial evaluation (e.g., only one basic metric reported, such as accuracy). No visualization of probabilities or confusion matrix. Testing is done on limited or partially seen data. |
| **Needs Improvement** | 3 | No evaluation or reused data. The model is not tested on a separate, unseen test set. Metrics are entirely missing or clearly incorrect. |

---

## 5. GitHub Contribution & Workflow — 10 pts
*Table showing task allocation and GitHub contribution*

| Rating | Pts | Description |
| --- | --- | --- |
| **Excellent** | 10 | Consistent, incremental commit history that traces the development of the project. Clear task/milestone table shows what was done and when, and aligns with the GitHub history. Commits are meaningful and well-described. |
| **Good** | 7 | Reasonable commit history showing progress, but commits are uneven or bunched together. Task/milestone table is present but may be vague or lack detail. |
| **Fair** | 5 | Sparse commit history (e.g., most work landed in one or two large commits). Task/milestone table is missing or does not reflect the GitHub history. |
| **Needs Improvement** | 3 | No traceable workflow on GitHub. A single commit dump, or the commit history is minimal and uninformative. |

---

## 6. Report Presentation and Structure — 5 pts
*Report structure, clarity, and professionalism*

| Rating | Pts | Description |
| --- | --- | --- |
| **Excellent** | 5 | 4–5 pages in length. Strict adherence to structure. Follows strict section headings and indications in the instructions. Content is clear, justified, and professionally formatted (e.g., proper captions, clear figures, no major typos). |
| **Good** | 4 | Slightly over limit (e.g., 6–7 pages) or missing a minor section. Generally well-structured, but the writing may lack clarity in a few areas. Minor formatting issues. |
| **Fair** | 3 | Dense text, unreadable figures, no captions. Significant deviation from the required structure or length (e.g., < 3 pages). Writing is difficult to follow. |
| **Needs Improvement** | 2 | Missing structure or incomplete report. The submission is a raw notebook or a highly fragmented document that fails to meet the basic professional standards of a report. |

---

### Points Summary

| Criterion | Max Pts |
| --- | --- |
| Data Collection & Quality | 10 |
| Feature Extraction (Time & Frequency Domain) | 10 |
| Implementation (Viterbi / Baum–Welch) | 15 |
| Evaluation on Unseen Data | 10 |
| GitHub Contribution & Workflow | 10 |
| Report Presentation and Structure | 5 |
| **Total** | **60** |
