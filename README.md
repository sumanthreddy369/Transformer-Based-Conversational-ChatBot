Transformer-Based Ubuntu Technical Support Chatbot
Overview

This project implements a Transformer-based encoder–decoder conversational AI model trained on the Ubuntu Dialogue Corpus for multi-turn technical support conversations.

The system includes large-scale data preprocessing, subword tokenization, and a custom Transformer architecture implemented using PyTorch.

Dataset

Ubuntu Dialogue Corpus

~165 million cleaned messages

1.8+ million multi-turn dialogues

Technical support domain conversations

Project Structure
ubuntu-dialogue-transformer-chatbot-part-1.ipynb   # Data preprocessing
ubuntu-dialogue-transformer-chatbot-part-2.ipynb   # Model training and inference
README.md
Part 1 – Data Preprocessing

Merged multiple dialogue datasets

Removed duplicate and null text records

Filtered incomplete and one-sided dialogues

Cleaned and normalized text (URL removal, lowercase, whitespace normalization)

Token length analysis

Aggregated chronological multi-turn dialogues

Generated structured dataset for training

Part 2 – Modeling and Training

Subword tokenization using SentencePiece (vocab size: 10,000)

Transformer encoder–decoder implementation (PyTorch)

Embedding dimension: 256

Attention heads: 8

Encoder/decoder layers: 3

Feedforward dimension: 1024

Dropout: 0.1

Cross-entropy loss with padding mask

Adam optimizer with warm-up learning rate schedule

Greedy decoding for inference

Results

Final Training Loss: 4.236

Validation Loss: 4.027

BLEU Score: 1.034

Technologies Used

Python
PyTorch
NumPy
Pandas
Matplotlib
SentencePiece
CUDA (GPU acceleration)
