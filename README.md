# 🧠 EMG Multi-Segment Analysis with NeuroKit2

This repository contains a Jupyter Notebook (`EMG_Analyze_Multi_Segment.ipynb`) for analyzing EMG (electromyography) signals, especially from mouse experiments. It enables flexible, segment-wise analysis of EMG amplitude and frequency characteristics, leveraging the power of [**NeuroKit2**](https://neuropsychology.github.io/NeuroKit/).

---

## 📌 Features

- **Flexible Multi-Segment Analysis**  
  Define custom time segments (e.g., Phase 1: 0–10s) for isolated statistical comparison.

- **EMG Signal Preprocessing**  
  - Optional bandpass filtering (default: 10–400 Hz)
  - Adjustable sampling rate

- **Robust Feature Extraction**  
  - **Time-Domain Metrics**:
    - Mean, Median, Variance, Standard Deviation
    - RMS (Root Mean Square)
  - **Frequency-Domain Metrics** (via Welch’s method):
    - Mean frequency
    - Median frequency
    - Variance and standard deviation of power spectral distribution

- **Excel Export**  
  Automatically saves results for each segment into an `.xlsx` file, facilitating downstream statistical analysis or visualization.

---

## 🧪 Dependencies

The notebook relies on the following Python packages:

```bash
pip install neurokit2 scipy numpy pandas openpyxl
```

- `neurokit2`: Core EMG processing and signal feature extraction
- `scipy`: Welch PSD estimation, filtering utilities
- `numpy`: Statistical and numerical analysis
- `pandas`: File handling and Excel export
- `openpyxl`: Excel I/O backend

---

## 🛠 Example Configuration

```python
sampling_rate = 400  # Hz

emg_segments = [
    ("Phase 1", 0, 10),
    ("Phase 2", 10, 20),
    ("Phase 3", 20, 30)
]

apply_filter = True
lowcut = 10
highcut = 400
```

---

## 📂 File Description

- `EMG_Analyze_Multi_Segment.ipynb`:  
  The main notebook performing segmented EMG analysis with NeuroKit2.

---

## 🧬 Applications

- Behavioral neuroscience EMG recordings
- Muscle activation profiling
- Preclinical neurophysiological studies
- Signal quality or treatment effect comparisons across conditions

---

## 📄 License

This project is released under the MIT License.
