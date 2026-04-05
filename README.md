# Pitch Detection using YIN and pYIN Algorithms

##  Overview

This project implements and compares two pitch detection algorithms:

* **YIN Algorithm**
* **pYIN (Probabilistic YIN) Algorithm**

The goal is to evaluate how both methods perform under different noise conditions and demonstrate that **pYIN is more robust than YIN**, especially in noisy environments.

---

##  Objectives

* Implement YIN and pYIN algorithms from scratch
* Analyze pitch detection accuracy under noise
* Compare performance using graphical results
* Understand probabilistic modeling in signal processing

---

##  Methodology

###  YIN Algorithm

The YIN algorithm estimates pitch using:

1. Difference function
2. Cumulative Mean Normalized Difference (CMND)
3. Threshold-based peak detection
4. Parabolic interpolation for refinement

---

###  pYIN Algorithm

pYIN improves YIN by:

1. Using **multiple thresholds** instead of a fixed one
2. Assigning **probabilities to pitch candidates**
3. Applying a **Hidden Markov Model (HMM)**
4. Using **Viterbi decoding** to find the best pitch sequence

---

##  Technologies Used

* Python
* NumPy
* Librosa
* Matplotlib
* SciPy

---

##  How to Run

### 1. Install dependencies

```bash
pip install numpy matplotlib librosa scipy
```

### 2. Run the code

```bash
python main.py
```

---

##  Results

The algorithms were tested across multiple noise levels.

### Key Observations:

* YIN performs well in clean signals
* pYIN performs better in **moderate noise conditions**
* At very high noise levels, both algorithms degrade

Example conclusion:

> pYIN consistently achieves higher accuracy than YIN due to probabilistic thresholding and temporal smoothing.

---

##  Output

The program generates:

* Accuracy vs Noise Level graph
* Pitch tracking comparison plot

---

##  Limitations

* Computationally intensive (not suitable for microcontrollers like STM32)
* Performance drops in extreme noise
* Designed for monophonic signals only

---

##  References

* Mauch, M., & Dixon, S. (2014).
  *pYIN: A Fundamental Frequency Estimator using Probabilistic Threshold Distributions*


---

##  Status

✔ Completed and tested successfully
✔ Results match expected research outcomes

---
