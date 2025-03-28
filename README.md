# Timbre Transfer Project

## Overview
This project focuses on timbre transfer, a process of altering the timbre of a target audio signal to resemble the timbre of a source signal, while retaining the original pitch and rhythm of the target. The methodology relies on Nonnegative Matrix Factorization (NMF) to manipulate audio features in the frequency domain.

## Objectives
- Understand spectral content using Short-Time Fourier Transform (STFT).
- Utilize Nonnegative Matrix Factorization (NMF) to factorize and manipulate audio spectra.
- Implement audio re-synthesis using ISTFT and Griffin-Lim algorithms.
- Automate timbre transfer across multiple audio sources and targets.
- Analyze and evaluate timbre similarity using Mel-Frequency Cepstral Coefficients (MFCCs) and Dynamic Time Warping (DTW).

## Key Features
### Signal Processing
- **STFT Analysis:** Transform audio signals to time-frequency domain, essential for timbre analysis.
- **Magnitude Spectrum Extraction:** Focus on spectral energy distribution to isolate timbre-related features.

### Nonnegative Matrix Factorization (NMF)
- **Matrix Initialization:** Establishes spectral templates and activation matrices from source and target audio.
- **Frobenius Error Analysis:** Measures reconstruction accuracy of spectrograms.
- **Compression Techniques:** Applies power-law compression for improved visualization of matrices.

### Timbre Transfer Methods
- **ISTFT Reconstruction:** Quick audio synthesis using original source phase information.
- **Griffin-Lim Reconstruction:** Iterative method refining phase for high-quality audio synthesis.

### Automation and Scalability
- **General Function (`timbre_transfer`):** Encapsulates the entire process from STFT through audio reconstruction, providing flexibility and ease of use.
- **Batch Processing:** Automates the transfer process across combinations of multiple source and target audio files.

### Evaluation and Analysis
- **MFCCs and DTW:** Measures timbral similarity objectively by aligning and comparing spectral features.

## Usage
1. **Load Audio Files:** Standardize sampling rate (Fs = 22050 Hz).
2. **Perform NMF and Timbre Transfer:**
   - Use the provided Python function to execute the entire transfer process.
   - Adjust parameters (hop size, window length, fix_W, etc.) for optimal results.
3. **Evaluate:** Compute similarity scores using MFCCs and DTW.

## Requirements
- Python
- Librosa
- NumPy

## Potential Applications
- Sound design and audio effect generation.
- Musical instrument emulation.
- Audio style transfer.

## Contribution
Feel free to enhance or modify the code for different audio datasets or additional features.

