# Audio Grammar Scoring 🗣️✍️

Automatically convert English audio clips (45–60 seconds) into text using OpenAI Whisper, extract grammar and readability features, and predict grammar scores (0–5) using XGBoost—all inside a single Jupyter Notebook.

---

## 📘 Overview

This project is a complete Grammar Scoring Engine for evaluating spoken English.  
It performs the following steps:

1. **Transcribe** audio to text using Whisper  
2. **Extract** grammar errors (via LanguageTool), readability scores (via Textstat), and text complexity features  
3. **Train** an XGBoost regression model on labeled audio-text data  
4. **Evaluate** model performance with MAE, RMSE, and R²  
5. **Predict** grammar scores for test audio clips  
6. **Generate** a `submission.csv` file for output

---

## 🗂️ Dataset Setup

Organize your dataset in the following structure under a folder called `dataset/`:

dataset/
├── audios_train/             # ≈444 .wav files for training
├── audios_test/              # ≈204 .wav files for testing
├── train.csv                 # Training metadata: filename, label
├── test.csv                  # Test metadata: filename, dummy_label
└── sample_output.csv    # Example format for submission

Output Format
audio_filename,grammar_score
file_1.wav,3.5
file_2.wav,4.2
file_3.wav,2.8
...


Project Structure

├── audio_grammar_scoring.ipynb   # All-in-one Jupyter notebook for the entire workflow
├── dataset/                      # Contains audio files and CSVs
│   ├── audios_train/             # ≈444 .wav files for training
│   ├── audios_test/              # ≈204 .wav files for testing
│   ├── train.csv                 # Training metadata: filename, label
│   ├── test.csv                  # Test metadata: filename, dummy_label
│   └── sample_output.csv         # Example format for submission
├── requirements.txt              # Python dependencies for the project
└── README.md                     # This file

