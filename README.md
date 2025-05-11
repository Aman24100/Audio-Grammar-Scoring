# Audio Grammar Scoring 🗣️✍️

Automatically convert English audio clips (45–60 seconds) into text using OpenAI Whisper, extract grammar and readability features, and predict grammar scores (0-5) using XGBoost—all inside a single Jupyter Notebook.

---

## 📘 Overview

This project evaluates spoken English by:

1. **Transcribing** audio to text with Whisper  
2. **Extracting** grammar and readability features  
3. **Training** an XGBoost model on the data  
4. **Evaluating** the model's performance  
5. **Predicting** grammar scores for test data  
6. **Generating** a `submission.csv` file

---

## 🗂️ Dataset Setup

Organize your dataset as follows:
dataset/
├── audios_train/ # ≈444 .wav files for training
├── audios_test/ # ≈204 .wav files for testing
├── train.csv # Training metadata: filename, label
├── test.csv # Test metadata: filename, dummy_label
└── sample_output.csv # Example format for submission


---

## 📝 Output Format
audio_filename,grammar_score
file_1.wav,3.5
file_2.wav,4.2
file_3.wav,2.8
...


---

## 📁 Project Structure

├── audio_grammar_scoring.ipynb # Main notebook
├── dataset/
│ ├── audios_train/ # Training audio files
│ ├── audios_test/ # Test audio files
│ ├── train.csv # Training labels
│ ├── test.csv # Test filenames
│ └── sample_output.csv # Submission example
├── requirements.txt # Dependencies
└── README.md # Documentation


---

## ▶️ How to Run

1. Install dependencies:
   ```bash
   pip install -r requirements.txt
2. Open the notebook:
   jupyter notebook audio_grammar_scoring.ipynb
3. Run all cells to:
     Process audio files
     Train the model
     Generate predictions







