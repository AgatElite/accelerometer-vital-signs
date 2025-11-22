# Vital Sign Extraction from Smartphone Accelerometers

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/AgatElite/accelerometer-vital-signs/blob/main/HR_and_BR_Analysis.ipynb)

**Goal:** Extract Heart Rate (HR) and Respiration Rate (RR) from raw accelerometer data collected via a smartphone placed on the thorax.

###  How It Works
The algorithm processes raw X, Y, Z acceleration data using:
1.  **Preprocessing (PCA):** Combines 3 axes into the dominant direction of motion to handle phone orientation.
2.  **Zero-Phase Filtering:** Uses `filtfilt` (Butterworth) to remove noise without shifting peak timing.
3.  **Robust Estimation:** Compares **Time Domain** (Adaptive Thresholds) vs. **Frequency Domain** (Welch's Method) for validation.

### 📂 Structure
* `data/`: Contains raw accelerometer CSV files.
* `plots/`: Generated plots from the notebook, used for the presentation.
* `HR and BR Analysis.ipynb`: The Jupyter Notebook with code, visualizations, and results.
* `docs/`: Presentation slides and pdf.
