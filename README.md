# Audio Feature Visualizer — Real STFT/MFCC Edition

An interactive web-based audio feature visualizer for exploring waveform, FFT, STFT, log spectrogram, MFCC, delta, and delta-delta features using both synthetic signals and uploaded audio.

## Overview

This project is an interactive educational web application designed to help users understand how audio signals are represented across different stages of signal processing.

Instead of showing static images or placeholder examples, the app computes real audio features directly from the current signal. Users can generate synthetic signals such as sine waves, chords, sweeps, AM signals, and FM signals, or upload their own audio files for live analysis.

The system is designed to support step-by-step learning through the following pipeline:

**Waveform → FFT → STFT / Spectrogram → MFCC → Δ / ΔΔ → Summary & Quiz**

## Features

- Interactive synthetic signal generation
  - Pure sine
  - Two-tone chord
  - Noisy sine
  - Linear sweep
  - AM signal
  - FM signal

- Uploaded audio analysis
  - Supports WAV / MP3 input
  - Real waveform visualization
  - Real FFT spectrum
  - Real STFT spectrogram
  - Real MFCC, delta, and delta-delta computation

- Learning-oriented visualization
  - Live cause-and-effect feedback when parameters change
  - Comparison between synthetic and real audio
  - Linear vs log energy views
  - MFCC / Δ / ΔΔ switching
  - Built-in summary and self-check quiz

## Representations Included

### 1. Waveform
Shows amplitude over time. Useful for understanding the raw signal shape, but frequency content is not directly visible.

### 2. FFT Spectrum
Shows the global frequency components present in the signal. Useful for identifying dominant frequencies and harmonics, but it does not show when they occur.

### 3. STFT / Spectrogram
Shows how frequency content changes over time. Useful for analyzing dynamic audio patterns such as sweeps, modulation, and transitions.

### 4. Log Spectrogram
Compresses dynamic range so that weaker frequency components become more visible compared to strong peaks.

### 5. MFCC
Provides a compact representation of the spectral envelope using Mel filter banks and DCT, making it more suitable for machine learning and speech/audio analysis tasks.

### 6. Delta and Delta-Delta
Capture temporal change and acceleration of MFCC features over time, helping represent motion and dynamics in audio.

## Technical Highlights

- Real FFT implementation
- Real STFT computation with Hann windowing
- Real Mel filter bank construction
- Real MFCC extraction using DCT
- Delta and delta-delta feature computation
- Dynamic normalization and heatmap rendering
- Interactive UI built for learning and experimentation

## How to Use

1. Open the application in your browser.
2. Start with a synthetic signal and adjust parameters such as:
   - base frequency
   - duration
   - signal type
   - modulation rate
   - modulation depth
   - noise amount
3. Move through the tabs:
   - Waveform
   - Spectrum / FFT
   - Spectrogram
   - MFCC + Δ
   - Summary & Quiz
4. Upload a WAV or MP3 file to compare real audio with synthetic examples.
5. Observe how parameter changes affect each representation.

## Learning Goals

This project is designed to help learners understand:

- the difference between time-domain and frequency-domain representations
- how FFT reveals global frequency content
- how STFT adds time-localized frequency analysis
- why log scaling helps reveal weak components
- how MFCC compresses spectral information
- why delta and delta-delta features are useful for capturing change over time

## Built With

- HTML
- CSS
- JavaScript
- Chart.js
- Web Audio API

## File Structure

```bash
index.html
