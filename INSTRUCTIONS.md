# Modeling Human Activity States Using Hidden Markov Models

## Background

In real-world systems—from wearable health monitors to smart home sensors—continuous data streams such as accelerometer and gyroscope signals reveal valuable information about human activity. However, the true activity state (e.g., walking or standing) is often hidden behind noisy measurements.

This project challenges you to collect, analyze, and model your own motion data using the Sensor Logger app (or a similar tool) and then build a Hidden Markov Model (HMM) to infer human activity states from the recorded sensor signals.

## Project Tasks

### 1. Data Collection

Use your smartphone and a motion logging app to collect real sequential data.

**Recommended Apps**

- Sensor Logger (iOS/Android)
- Physics Toolbox Accelerometer (Android)
- Or any alternative motion data logging app

**Sensors to Record**

- Accelerometer (x, y, z)
- Gyroscope (x, y, z)

**Activities to Record**

Perform and record the following four activities:

| Activity | Duration | Notes |
| --- | --- | --- |
| Standing | 5–10 seconds | Keep your phone steady at waist level. |
| Walking | 5–10 seconds | Maintain a consistent pace. |
| Jumping | 5–10 seconds | Record continuous jumps. |
| Still (no movement) | 5–10 seconds | Place your phone on a flat surface. |

- You should collect approximately 20 samples across each activity combined.
- If you record across more than one phone or session, harmonize the sampling rates used for data collection. Make sure you state the sampling rate for each device/session in the report.
- Save recordings as `.csv` or `.txt` files and include a timestamp column.

### 2. Feature Extraction

From each time window of your collected data, compute both time-domain and frequency-domain features.

**Example features**

- **Time-domain:** mean, variance, standard deviation, signal magnitude area (SMA), correlation between axes
- **Frequency-domain:** dominant frequency, spectral energy, FFT components

These features will form your observation sequence for the HMM.

### 3. Define Model Components

Define your HMM structure based on your data.

| Element | Description |
| --- | --- |
| Hidden States (Z) | The underlying activities (e.g., standing, walking, jumping, still). |
| Observations (X) | Feature vectors derived from accelerometer and gyroscope signals. |
| Transition Probabilities (A) | Probability of moving from one activity to another over time. |
| Emission Probabilities (B) | Probability of observing a specific feature pattern given a hidden activity. |
| Initial State Probabilities (π) | Likelihood of starting in a specific activity. |

### 4. Model Implementation

Use Python to implement your Hidden Markov Model.

**Options**

- Implement from scratch using `numpy`
- Use the `hmmlearn` library for model creation and fitting

**Algorithm Requirements**

- Implement the Viterbi algorithm to decode the most likely sequence of activities
- Apply the Baum–Welch algorithm to train and optimize model parameters

**Visualization**

- Display your transition matrix as a heatmap
- Plot decoded sequences showing predicted activity transitions

### 5. Model Evaluation with Unseen Data

Test your trained model on unseen data (new recordings not used in training).

In your report, describe:

- How you obtained the unseen data (e.g., new session, different participant, different environment)
- Whether the model generalizes well to this new data

Complete the following table based on your evaluation results:

| State (Activity) | Number of Samples | Sensitivity | Specificity | Overall Accuracy |
| --- | --- | --- | --- | --- |
| Activity 1 | | | | |
| Activity 2 | | | | |
| Activity 3 | | | | |
| Activity 4 | | | | |

### 6. Analysis and Reflection

In your analysis section, discuss:

- Which activities were easiest or hardest to distinguish
- How transition probabilities reflect realistic behavior patterns
- How sensor noise or sampling rate affected the model
- What improvements could be made (e.g., more data, new features, additional sensors)

## Submission

A GitHub repository containing:

- Make a copy, fill, and export the provided document as PDF and add it to your repo
- Directory (folder) of well-labelled CSV dataset files (`.csv`)
- Python notebook (`.ipynb`) implementing your HMM
- Short report (4–5 pages) containing:
  - **Background and motivation** (1 paragraph) — state your unique use case, connecting it to why human activity recognition is needed.
  - **Data collection and preprocessing steps**
  - **HMM setup and implementation details**
  - **Results and interpretation** (including visualizations and metrics)
  - **Discussion and conclusion**
