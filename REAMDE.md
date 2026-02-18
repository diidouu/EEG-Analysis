# EEG Analysis: Auditory Lateralization & Time-Frequency Dynamics

![Python](https://img.shields.io/badge/Python-3.8%2B-blue)
![MNE](https://img.shields.io/badge/MNE--Python-v1.0%2B-red)
![Status](https://img.shields.io/badge/Status-Completed-success)

## 🧠 Project Overview

This project implements a complete EEG processing pipeline using **MNE-Python** to analyze brain responses to auditory stimuli. The goal is to investigate **hemispheric lateralization** (contralateral processing) and **time-frequency dynamics** of the auditory cortex.

Using the MNE Sample Dataset (multimodal MEG/EEG), this analysis simulates a standard clinical EEG setup by isolating specific channels and applying rigorous signal processing techniques to validate neurophysiological hypotheses.

## 🎯 Key Objectives

1.  **Preprocessing:** Clean raw EEG data using digital filtering and Independent Component Analysis (ICA) to remove ocular artifacts (EOG).
2.  **Time-Frequency Analysis:** Quantify induced and evoked oscillatory power (1–50 Hz) using Morlet Wavelets.
3.  **ERP Estimation:** Extract Event-Related Potentials (N100/P200 components) via averaging.
4.  **Lateralization Study:** Statistically and visually demonstrate that left-ear sounds activate the right brain hemisphere and vice-versa.

## 🛠️ Methodology & Pipeline

The notebook follows a strict scientific structure:

*   **Data Loading:** MNE Sample Dataset (Audio/Visual task).
*   **Preprocessing:**
    *   High-pass (0.1 Hz) & Low-pass (100 Hz) filtering.
    *   Artifact correction using **ICA (Picard algorithm)** on a high-pass filtered copy.
    *   Re-referencing to **Average Reference**.
*   **Epoching:** Segmentation (-0.5s to +1.0s) with baseline correction.
*   **Spectral Analysis:** Time-Frequency representation using **Morlet Wavelets** with adaptive cycles.
*   **Statistical Analysis:** Comparison of Region of Interest (ROI) and Topographical mapping (Topomaps).

## 📊 Key Results

*   **Artifact Removal:** Successfully identified and removed blink artifacts using EOG-correlated ICA components.
*   **Spectral Signature:** Observed strong low-frequency synchronization (Delta/Theta) post-stimulus.
*   **N100 Component:** Detected a clear N100 peak at ~100ms.
*   **Contralaterality:** Confirmed that **Left Ear stimulation** results in significantly higher amplitude in the **Right Temporal Lobe**, validating the cross-wiring of the auditory pathways.

## 🚀 How to Run

1.  **Clone the repository:**
    ```bash
    git clone https://github.com/YOUR_USERNAME/eeg-auditory-analysis.git
    cd eeg-auditory-analysis
    ```

2.  **Install dependencies:**
    ```bash
    pip install mne numpy matplotlib jupyter
    ```

3.  **Launch the Notebook:**
    ```bash
    jupyter notebook EEG_Analysis_Pipeline.ipynb
    ```

## 📂 File Structure

*   `EEG_Analysis_Pipeline.ipynb`: The main Jupyter Notebook containing the full analysis and code.
*   `README.md`: Project documentation.

## 📚 Tools Used

*   **[MNE-Python](https://mne.tools/):** The core library for neurophysiological data analysis.
*   **NumPy:** Numerical computing.
*   **Matplotlib:** Data visualization.

---
*Author: [Your Name]*