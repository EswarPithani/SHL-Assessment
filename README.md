🧠 Grammar Scoring Engine using Whisper + BERT

This project implements a Grammar Scoring Engine for spoken English audio using OpenAI Whisper for transcription and a fine-tuned BERT regressor for grammar quality prediction. The system evaluates spoken sentences and outputs a Mean Opinion Score (MOS) between 0 and 5, based on grammar correctness.

🚀 Model Pipeline Overview

ASR (Automatic Speech Recognition)

Uses OpenAI Whisper (various model sizes supported) to convert audio to text.

Text Embedding + Regression

Uses a BERT-based regression model fine-tuned on transcribed text to predict the grammar score.

Evaluation

Model is trained using K-Fold Cross Validation.

Evaluation metric: Pearson Correlation Coefficient.

🧪 Results Model: Whisper (small) + BERT Regressor

Training Epochs: 10

K-Fold Splits: 5

Best Pearson Score: 0.778

🧰 Requirements Python 3.10+

PyTorch

Transformers (HuggingFace)

OpenAI Whisper

Librosa

Scikit-learn

Pandas, Numpy, tqdm

🔁 Training Details 5-Fold Cross Validation using KFold

Fine-tuning bert-base-uncased on text transcripts

Loss Function: MSELoss

Optimizer: AdamW

Outputs clipped between [0, 5]

🙌 Acknowledgements

OpenAI Whisper

HuggingFace Transformers

Organizers of the Grammar Scoring Competition

