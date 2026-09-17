# SongsLikeIt

A Python project for analyzing and comparing songs by their audio characteristics, built around the [GTZAN Music Genre Dataset](http://marsyas.info/downloads/datasets.html) (10 genres: blues, classical, country, disco, hip-hop, jazz, metal, pop, reggae, rock).

## Project Status

This repository is in an early setup stage. At the moment it contains only project configuration (`.gitignore`) and a local, git-ignored `data/` folder with the raw dataset and a local `venv/` virtual environment — no application source code has been committed yet.

## Tech Stack

Based on the packages currently installed in the local virtual environment, this project is built with:

- **Python**
- **librosa** — audio loading and feature extraction (e.g. MFCCs, spectral features)
- **numpy** / **pandas** — numerical processing and tabular data handling
- **soundfile** — audio file I/O

## Data

The `data/` directory (not tracked in git — see `.gitignore`) is expected to contain:

- `features_30_sec.csv`, `features_3_sec.csv` — pre-extracted audio features
- `genres_original/` — raw audio clips organized by genre
- `images_original/` — spectrogram images organized by genre

Audio files (`*.wav`, `*.mp3`) and the entire `data/` folder are excluded from version control because of their size. If you want to reproduce the project, download the GTZAN dataset separately and place it under `data/` following the structure above.

## Getting Started

```bash
# Create and activate a virtual environment
python -m venv venv
venv\Scripts\activate      # Windows
# source venv/bin/activate # macOS/Linux

# Install dependencies (once a requirements file is added)
pip install librosa numpy pandas soundfile
```

## License

No license has been chosen yet for this project.

## Contributing

This project does not yet have contribution guidelines. If you'd like to contribute, please open an issue to discuss your proposed changes first.
