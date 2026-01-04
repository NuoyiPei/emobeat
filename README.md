# EmoBeat  
EEG-Based Emotion Recognition and Music Recommendation System

EmoBeat is a digital health project that integrates EEG-based emotion recognition, machine learning, and music recommendation to support emotion regulation in a non-invasive and data-driven way. The system detects users’ emotional states from EEG signals and recommends or generates music to help stabilize mood and alleviate negative emotions.

## Motivation

Depression is a major global mental health challenge, and non-pharmacological interventions such as music therapy have shown strong potential for emotional regulation. Inspired by evidence demonstrating the positive impact of music on mental health and help-seeking behavior, EmoBeat aims to bridge brain signals and music interaction using EEG and machine learning.

## System Overview

EmoBeat follows a real-time processing pipeline:

1. EEG signal acquisition  
2. EEG preprocessing and feature extraction  
3. Emotion classification (positive, neutral, negative)  
4. Music recommendation or audio style transfer  
5. Low-latency playback (less than 2 seconds)

## Datasets

### SEED Dataset (EEG Emotion Recognition)
- 15 participants (ages 20–30)  
- 32 EEG channels using the international 10–20 system  
- Emotion labels: positive, neutral, negative  
- Emotion elicitation via curated movie clips  

### DEAM Dataset (Music Emotion Analysis)
- Over 1,800 royalty-free music tracks  
- 45-second annotated clips  
- Continuous and categorical valence–arousal annotations  
- Audio features extracted using openSMILE  

## Models and Methods

### EEG Emotion Classification

The following machine learning models were evaluated:

| Model | Accuracy |
|------|----------|
| Support Vector Machine (SVM) | 93% |
| Convolutional Neural Network (CNN) | 96% |
| Long Short-Term Memory (LSTM) | 97% |
| Decision Tree | 76% |

The LSTM model achieved the best performance due to its ability to capture temporal patterns in EEG signals. Regularization techniques including dropout, batch normalization, and early stopping were applied to reduce overfitting.

### Music Recommendation and Generation

- Emotion-aware music recommendation based on EEG classification results  
- GAN-based audio style transfer for generating emotion-aligned music  
- Audio representations include Mel-spectrograms and MFCCs  

GAN architecture:
- Generator: emotion-conditioned Mel-spectrogram synthesis  
- Discriminator: validation of emotion-specific audio styles  

## Performance

- Emotion classification accuracy: 97%  
- Macro F1-score: 97%  
- End-to-end latency: approximately 1.5 seconds  
- Supports real-time EEG-to-music interaction  

## Technology Stack

- Python  
- NumPy, SciPy  
- MNE (EEG processing)  
- PyTorch or TensorFlow  
- Librosa (audio processing)  
- Machine learning and deep learning models  

## Features

- Real-time EEG-based emotion recognition  
- Emotion-aware music recommendation  
- GAN-based music style transfer  
- Low-latency system design  
- Non-invasive digital mental health support  

## Future Work

- Expansion to more fine-grained emotional categories  
- Improved audio diversity and realism using advanced generative models  
- Further latency optimization for real-time deployment  
- Integration with edge devices and IoT systems  
- Extended evaluation through user studies  

## Disclaimer

This project is intended for research and educational purposes only and does not provide medical diagnosis or treatment.
