# Vibration Signal Analysis for Fault Detection

## 1. Time-Domain Features
Time-domain features are directly extracted from the raw vibration signal. These features are effective for detecting trends, changes in amplitude, and irregularities in the vibration pattern.

- **Root Mean Square (RMS)**: Measures the overall energy of the vibration signal. Typically, an increase in RMS signals faults.
  
- **Peak Value**: The maximum amplitude of the signal. Sudden peaks could indicate abnormal impacts or vibrations.

- **Crest Factor**: Ratio of peak value to RMS. Higher crest factors often signal rough surfaces or sudden impacts, like bearing damage.

- **Skewness**: Indicates the asymmetry of the signal's distribution. Changes can signal evolving faults.

- **Kurtosis**: Measures "tailedness" in the probability distribution. High kurtosis is often linked to impulsive events, such as bearing failures.

- **Zero-Crossing Rate**: Tracks how often the signal crosses the zero axis. Sudden changes could signal an anomaly.

- **Variance**: Measures the spread or dispersion of the signal values around the mean, indicating inconsistencies or variability.

- **Signal Envelope**: Captures modulation patterns, particularly useful for detecting fault frequencies in rolling element bearings.

---

## 2. Frequency-Domain Features (via FFT)
Frequency-domain features provide insights into the dominant frequencies of a vibration signal, which can be linked to specific mechanical faults.

- **Frequency Spectrum (FFT)**: Fast Fourier Transform identifies dominant frequencies linked to issues like misalignment or imbalance.
  
- **Power Spectral Density (PSD)**: Shows how the signal’s power is distributed across different frequencies, highlighting severity and fault type.

- **Harmonics and Subharmonics**: Harmonics of the fundamental frequency often indicate imbalance, while subharmonics are linked to gear or bearing faults.

- **Resonance Frequencies**: Energy spikes at specific resonance frequencies can indicate rotor imbalances or defective bearings.

- **Sidebands**: Frequencies near the fundamental frequency, typically caused by modulations from mechanical faults like bearing or gear wear.

---

## 3. Time-Frequency Domain Features (Wavelet Transform)
Time-frequency analysis is used to study non-stationary signals where faults occur at specific times, not throughout the entire signal.

- **Wavelet Energy**: Shows energy levels across different frequencies over time, helping to pinpoint faults.

- **Wavelet Entropy**: Measures disorder across frequency bands, indicating signal complexity and potential faults.

- **Short-Time Fourier Transform (STFT)**: Similar to FFT, but provides localized time-frequency information, useful for transient faults.

---

## 4. Statistical Features
Statistical descriptors can be highly valuable for identifying anomalies or patterns in vibration data.

- **Mean**: Average value of the signal over time. A shift in the mean could indicate a drift in the system’s behavior.

- **Standard Deviation**: Measures variability. Increasing variability usually points to a developing fault.

- **Autocorrelation**: Detects repeating patterns and can identify periodic faults.

---

## 5. Fault-Specific Features
Certain features are unique to specific types of machinery faults:

- **Bearing Fault Frequencies**: For rotating machinery, these include:
  - **Ball Pass Frequency of Outer Race (BPFO)**
  - **Ball Pass Frequency of Inner Race (BPFI)**
  - **Fundamental Train Frequency (FTF)**
  - **Ball Spin Frequency (BSF)**

- **Gear Mesh Frequency (GMF)**: Faults like gear wear or pitting are often detected via sidebands around the GMF.

- **Imbalance Frequency**: Occurs at the fundamental rotational frequency, indicating rotor imbalance.

---

## 6. Domain Knowledge-Driven Features
Incorporating domain knowledge about the system improves fault detection accuracy.

- **Operating Speed (RPM)**: Plays a key role in determining normal and abnormal vibrations.

- **Temperature**: Vibration levels can change with temperature, so monitoring this relationship helps detect faults.

- **Lubrication Conditions**: Poor lubrication in bearings and gears often results in high-frequency noise, which can be detected through vibration signals.

---

## Summary of Key Features

- **Time-Domain**: RMS, Peak Value, Crest Factor, Kurtosis, Skewness, Variance
- **Frequency-Domain**: Dominant Frequencies, Harmonics, Sidebands, PSD
- **Time-Frequency**: Wavelet Transform Features (Wavelet Energy, Entropy)
- **Statistical**: Mean, Standard Deviation, Autocorrelation
- **Fault-Specific**: Bearing Fault Frequencies, Gear Mesh Frequencies

---