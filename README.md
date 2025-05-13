# Text Summarization Model

This project implements an abstractive text summarization model using a sequence-to-sequence architecture with an LSTM-based encoder and decoder. The model is trained on a subset of the CNN/DailyMail dataset, and it incorporates pretrained GloVe embeddings to enhance the quality of the summaries.

## Model Architecture

- **Encoder**: A 256-unit LSTM that processes the input sequence and encodes the context into a fixed-length vector.
- **Decoder**: A 256-unit LSTM that decodes the context into the summary, predicting the next word based on the previous words and encoded context.
- **GloVe Embeddings**: Pretrained GloVe 6B 100-dimensional embeddings are used to represent words in a dense vector space, improving the model's understanding of semantic relationships.
- **Embedding Matrix**: The GloVe embeddings are loaded into an embedding matrix using `word2idx` to map words to their corresponding 100-dimensional vectors.

## Dataset

- **Dataset**: A subset of the CNN/DailyMail dataset is used for training and testing the model.

## Key Features

- **Word2Vec Encoding**: GloVe 6B 100-dimensional embeddings are converted into a word-to-index mapping for efficient processing during training.
- **Sequence-to-Sequence Model**: The encoder-decoder architecture allows the model to generate human-like summaries for long text passages.

## Training

- **LSTM Units**: The model uses 256 LSTM units for both the encoder and decoder.
- **Test Accuracy**: Achieved 70% accuracy on the test set.
- **Performance**: Ongoing work to improve the performance and generalization of the model.

## Installation

1. Clone this repository.
2. Install required dependencies:
    ```bash
    pip install -r requirements.txt
    ```

## Usage

To train the model:
```bash
python train.py
