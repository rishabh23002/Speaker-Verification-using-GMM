
# 🎙️ Speaker Verification using Gaussian Mixture Models (GMM)

This repository implements a **Speaker Verification System** using **Gaussian Mixture Models (GMMs)** with **MFCC**, **Delta**, and **Double Delta** features. The system is trained and tested on a subset of a speaker recognition dataset containing 1-second WAV files per speaker.

---

## 📌 Project Overview

Speaker verification is an essential component in audio-based security and authentication systems. This project uses GMMs to learn speaker-specific acoustic patterns and verify the identity of a speaker based on short utterances.

### 🔍 Key Highlights

- 📂 Preprocessing includes noise addition, resampling, and pre-emphasis.
- 🎚️ Feature extraction based on MFCC, delta, and double-delta coefficients.
- 🎯 Model training using Gaussian Mixture Models with Expectation-Maximization.
- 📊 Equal Error Rate (EER) used for evaluation; best model achieves **EER = 0.177**.
- 👥 Includes speaker pair comparisons and real-world applicability demonstrations.

---

## 🛠️ Project Structure

```bash
.
├── Audio/                     # Contains 1-second audio files for each speaker
├── Noise/                     # Contains noise samples used for robustness
├── test_pairs.txt             # File containing speaker comparison test cases
├── ml-end.ipynb               # Main notebook for training, evaluation, and testing
├── README.md                  # You're reading it
```

---

## 🔄 Pipeline Summary

### 1. Preprocessing
- **Silence and Noise Removal**
- **Resampling to 16kHz**
- **Pre-Emphasis Filtering**

### 2. Feature Extraction
- **MFCC** (Mel-Frequency Cepstral Coefficients)
- **MFCC Delta**
- **MFCC Double Delta**

### 3. Model Training
- Trained a **GMM per speaker** using `sklearn.mixture.GaussianMixture`
- Parameters: `n_components=4`, `max_iter=160`

### 4. Evaluation
- **Log-likelihood comparison** for speaker prediction
- **Equal Error Rate (EER)** calculated for performance
- Also supports **speaker pair comparison**

---

## 📊 Results

| Model Version                  | EER   |
|-------------------------------|-------|
| MFCC + Delta + Double Delta   | 0.177 |
| MFCC only                     | Higher |

A lower EER indicates better performance (balance between false accept and false reject).

---

## 📚 References

Key papers referenced include:

- Reynolds & Rose (1995): Robust text-independent speaker identification using GMM
- Dehak et al. (2007): Modeling Prosodic Features with Joint Factor Analysis
- Jadhav et al. (2018): GMM + MFCC + EM-based speaker recognition

[See full reference list in the report](./Project_Final_Report.pdf)

---

## 📈 Future Work

- Train on larger datasets with more speakers
- Explore i-vector and x-vector embeddings
- Apply deep learning approaches (e.g., LSTM, CNN) for feature extraction
- Integrate with real-time APIs or voice assistants

---


