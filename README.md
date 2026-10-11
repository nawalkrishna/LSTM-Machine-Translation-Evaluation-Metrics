Machine Translation and Evaluation Metrics

## Overview

This lab implements Machine Translation (MT) using an Encoder–Decoder LSTM model with Attention. The model translates Hindi sentences into English and evaluates the generated translations using BLEU, ROUGE, BERTScore, and MoverScore.

## Objectives

- Implement Machine Translation using an LSTM-based sequence-to-sequence architecture.
- Understand tokenization, padding, and teacher forcing.
- Generate translations using the trained model.
- Evaluate translation quality using multiple evaluation metrics.
- Compare lexical-overlap metrics with semantic similarity metrics.

## Technologies Used

- Python
- TensorFlow / Keras
- NumPy and Pandas
- NLTK
- ROUGE Score
- BERTScore
- MoverScore
- Google Colab

## Implementation

### 1. Dataset Preparation
A small, manually created Hindi–English parallel dataset is used for demonstration. Separate tokenizers are created for the source and target languages, and the sequences are padded to uniform lengths.

### 2. LSTM-Based Machine Translation
An Encoder–Decoder architecture is implemented using LSTM layers and an attention mechanism. The encoder processes the input sentence, while the decoder generates the translated sentence token by token.

### 3. Translation Generation
The trained model generates English translations for Hindi input sentences using autoregressive decoding.

### 4. Evaluation Metrics

- **BLEU:** Measures n-gram precision between generated translations and reference translations.
- **ROUGE:** Measures lexical overlap using ROUGE-1, ROUGE-2, and ROUGE-L.
- **BERTScore:** Evaluates semantic similarity using contextual embeddings from a pretrained language model.
- **MoverScore:** Evaluates semantic similarity using contextual embeddings and an Earth Mover's Distance-based approach.

## How to Run

1. Download or clone this repository.
2. Open `Lab10_LSTM_MT_Evaluation_Metrics.ipynb` in Google Colab or Jupyter Notebook.
3. Install the required dependencies using the installation cells.
4. Execute the notebook cells sequentially.
5. Observe the generated translations and evaluation scores.

## Expected Output

- Trained Encoder–Decoder LSTM model.
- Predicted English translations for Hindi input sentences.
- Corpus BLEU score.
- Average ROUGE-1, ROUGE-2, and ROUGE-L F1 scores.
- BERTScore Precision, Recall, and F1 scores.
- MoverScore, if the required dependencies are compatible with the runtime.

## Limitations

The experiment uses a small, manually created dataset and evaluates the model on the same examples used for training. Therefore, the resulting scores are intended for demonstration purposes and do not represent general translation performance. A larger parallel corpus and a separate test dataset are required for reliable evaluation.

## Conclusion

This lab demonstrates an end-to-end machine translation pipeline using an LSTM-based sequence-to-sequence model with attention and evaluates translation quality using BLEU, ROUGE, BERTScore, and MoverScore.
