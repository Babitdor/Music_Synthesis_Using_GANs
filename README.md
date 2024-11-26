# Music Synthesis Using Conditional-GAN

This project aims to synthesize music using a Conditional Generative Adversarial Network (Conditional-GAN). The model generates music by learning from various audio features, including **MFCC**, **delta**, **delta_2**, **chroma**, **centroid**, **rolloff**, **contrast**, **zero-crossing rate (ZC)**, and **root mean square error (RMSE)**. These features are extracted from audio clips and used as input conditions for the generator network to create realistic music sequences.

## Project Overview

The key objective is to train a Conditional GAN to generate musical samples that follow a distribution learned from real audio data. The generator is conditioned on audio features, and the discriminator evaluates whether the generated samples are realistic or not. The model architecture includes:

- **Generator**: Takes audio feature representations (MFCC, delta, chroma, etc.) as input and generates new audio samples.
- **Discriminator**: Evaluates real vs. fake music based on feature representations.

### Features

- **MFCC (Mel-Frequency Cepstral Coefficients)**: Represent the short-term power spectrum of sound, widely used for audio processing.
- **Delta & Delta_2**: Capture the change in MFCCs over time (first and second derivatives), providing dynamic temporal features.
- **Chroma**: Encodes harmonic and melodic content, representing the twelve different pitch classes.
- **Centroid**: Measures the "center of mass" of the spectrum, indicating timbral texture.
- **Rolloff**: Describes the frequency below which a specified percentage of the total spectral energy lies.
- **Contrast**: Measures spectral contrast, indicating the difference in amplitude between peaks and valleys in the spectrum.
- **Zero-Crossing Rate (ZC)**: Indicates the rate at which the audio signal changes sign, often used in percussive sound detection.
- **Root Mean Square Error (RMSE)**: Measures the magnitude of audio signal variations.

## Requirements

- Python 3.7+
- TensorFlow / Keras
- Librosa (for audio feature extraction)
- NumPy
- Matplotlib (for visualization)
- Soundfile (for saving audio files)

## Installation

Clone the repository:

```bash
git clone https://github.com/your-username/music-synthesis-cgan.git
cd music-synthesis-cgan
