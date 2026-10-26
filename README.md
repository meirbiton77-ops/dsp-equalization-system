# DSP-Based Digital Equalization System (ZF/MMSE)

## The Problem
Thermodynamic sensors naturally suffer from physical thermal lag and inertia, meaning they cannot respond instantly to rapid temperature changes. From a signal processing perspective, the sensor acts as a physical Low-Pass Filter (LPF) that attenuates high frequencies and smears the incoming signal over time. This distortion, combined with environmental AWGN (Additive White Gaussian Noise), leads to inaccurate real-time measurements and degrades overall system reliability.

## The Solution & Architecture
Developed a complete digital signal processing pipeline to mathematically invert the sensor's physical delay and reconstruct the original input signal. The project evaluates and implements two core equalization strategies:

*   **System Modeling:** Characterizing the sensor's impulse response and frequency domain behavior.
*   **Zero-Forcing (ZF) Equalizer:** Implemented an inverse filter to completely eliminate the thermal lag. While effective at canceling signal distortion, this approach demonstrated the classic DSP trade-off: severe noise amplification at frequencies where the sensor's original response was weak.
*   **MMSE Equalizer (Minimum Mean Square Error):** Designed an advanced optimal filter that minimizes the overall error by balancing between distortion cancellation and noise suppression. This resulted in a vastly superior Signal-to-Noise Ratio (SNR) and robust signal recovery even in highly noisy environments.

## Key Capabilities Demonstrated
*   **Signal Reconstruction:** Successful recovery of attenuated high-frequency signal components.
*   **Algorithm Evaluation:** Direct mathematical and visual comparison between ZF and MMSE performances under varying noise variances.
*   **From-Scratch Implementation:** The entire DSP pipeline was built in Python using core mathematical libraries, demonstrating deep algorithm understanding without relying on "black-box" proprietary toolboxes.

## Tech Stack
*   **Language:** Python
*   **Libraries:** NumPy, SciPy, Matplotlib
*   **Core Concepts:** Digital Signal Processing (DSP), Optimal Filtering, Estimation Theory, LTI Systems

## Visual Results
*(הוסף כאן את התמונה של הגרף שלך)*
