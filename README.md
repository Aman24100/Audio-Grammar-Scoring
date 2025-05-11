# Audio Grammar Scoring 🗣️✍️

Automatically evaluate spoken English by converting audio to text, extracting features, and predicting grammar scores (0-5) using OpenAI Whisper and XGBoost.

---

## 📘 Overview  
This project evaluates spoken English by:  
1. **Transcribing** audio to text with Whisper  
2. **Extracting grammar and readability features**  
3. **Training an XGBoost model** on the data  
4. **Evaluating the model’s performance**  
5. **Predicting grammar scores** for test data  
6. **Generating** a `submission.csv` file  

---

## 🗂️ Dataset Setup  
Download the dataset:

🔗 https://drive.google.com/drive/folders/1GPryhwimhwVIvO3BOa52aMyhcEUJluCM?usp=share_link

Organize your dataset as follows:  
dataset/  
├── audios_train                     # ~444 .wav files for training  
├── audios_test           # ~204 .wav files for testing  
├── train.csv              # Training metadata: filename, label  
├── test.csv               # Test metadata: filename, dummy_label  
└── sample_output.csv      # Example submission format 

---

## 📝 Output Format  
Generate a `submission.csv` with:  
```csv  
audio_filename,grammar_score  
file_1.wav,3.5  
file_2.wav,4.2  
file_3.wav,2.8  
...  

```
## 📁 Project Structure 
 
├── audio_grammar_scoring.ipynb    # Main Jupyter notebook  
├── dataset/  
│   ├── audios_train/             # Training audio files  
│   ├── audios_test/              # Test audio files  
│   ├── train.csv                 # Filename + ground truth labels  
│   ├── test.csv                  # Filename + dummy labels  
│   └── sample_output.csv         # Submission template  
├── requirements.txt              # Python dependencies  
└── README.md                     # This documentation  

## ▶️ How to Run

1. **Install dependencies**:
   ```bash
   pip install -r requirements.txt
2. Launch the Jupyter Notebook:
3. Run all cells to: Transcribe audio files using Whisper, extract grammar/readability features, train/evaluate the XGBoost model, and generate predictions in submission.csv.











