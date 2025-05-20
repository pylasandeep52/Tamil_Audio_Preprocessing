````markdown
# Tamil Audio Preprocessing

##Overview

This repository contains a complete audio preprocessing pipeline for Tamil audio files. It loads raw `.mp3` audio data, trims silence, normalizes the audio, and extracts key features including:

- Waveform visualization
- Mel Spectrograms
- MFCC (Mel Frequency Cepstral Coefficients)

The project uses Python libraries such as `librosa`, `matplotlib`, `numpy`, and `soundfile` for audio processing and visualization.

## Repository Structure

Tamil_Audio_Preprocessing/
├── Dataset/                    # Raw Tamil audio files (.mp3)
├── ProcessedAudio/             # Preprocessed audio files (.wav)
├── Features/
│   ├── MFCCs/                  # Extracted MFCC feature arrays (.npy)
│   └── MelSpectrograms/        # Extracted Mel-Spectrogram feature arrays (.npy)
├── MFCC_Images/                # Saved MFCC visualizations (.png)
├── MelSpec_Images/             # Saved Mel-Spectrogram visualizations (.png)
├── Audio_Preprocessing.ipynb   # Jupyter notebook with preprocessing pipeline
└── README.md                   # This documentation file
````

---

## Getting Started

### Prerequisites

Make sure you have Python 3.7+ installed. Recommended to use a virtual environment.

### Install Dependencies

```bash
pip install numpy librosa matplotlib soundfile pillow
```

---

## Usage

1. **Clone the repository**

```bash
git clone https://github.com/pylasandeep52/Tamil_Audio_Preprocessing.git
cd Tamil_Audio_Preprocessing
```

2. **Download and extract your Tamil audio dataset**

Place the raw Tamil `.mp3` audio files inside the `Dataset/` directory.

3. **Open and run the Jupyter notebook**

```bash
jupyter notebook Audio_Preprocessing.ipynb
```

4. **Run all cells in the notebook**

The notebook will:

* Load each audio file, resample, trim silence, normalize amplitude
* Save preprocessed `.wav` files in `ProcessedAudio/`
* Extract MFCCs and Mel-Spectrogram features and save as `.npy` files
* Generate and save MFCC and Mel-Spectrogram images for visualization

---

## Outputs

* **Preprocessed Audio**: Cleaned and normalized `.wav` files
* **Feature Arrays**: MFCC and Mel-Spectrogram feature matrices in `.npy` format
* **Feature Images**: Visualization images of MFCCs and Mel-Spectrograms in `.png`

---

## Notes

* Audio is processed at 22,050 Hz sample rate and converted to mono.
* Silence trimming uses `librosa.effects.trim` with default parameters.
* Features extracted:

  * 13 MFCC coefficients
  * 128 Mel bands for Mel-Spectrogram

---


