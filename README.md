🧠 Transformer-Based Ubuntu Technical Support Chatbot
-------------------------------------------------------------------------------------------------------------------------------------------------------------------


📌 Overview

This project implements a Transformer-based encoder–decoder conversational AI model trained on the Ubuntu Dialogue Corpus for multi-turn technical support conversations.

The system includes large-scale dialogue preprocessing, subword tokenization, and a custom Transformer architecture implemented using PyTorch.
--------------------------------------------------------------------------------------------------------------------------------------------------------------
📂 Dataset

. Ubuntu Dialogue Corpus

. 165M+ cleaned messages

. 1.8M+ multi-turn dialogues

. Technical support domain
------------------------------------------------------------------------------------------------------------------------------------------------------------------
🏗 Project Architecture

- Data Pipeline (Part 1)

. Merged multiple dialogue datasets

. Removed duplicates and null entries

. Filtered incomplete and one-sided conversations

. Cleaned and normalized text

. Token length analysis

. Aggregated chronological multi-turn dialogues
---------------------------------------------------------
- Modeling Pipeline (Part 2)

. Tokenization

. SentencePiece subword tokenizer

. Vocabulary size: 10,000

. Special tokens: <BOS>, <EOS>, <PAD>
-------------------------------------------------------------------------------------------------------------------------------------------------------------------
- Transformer Architecture

. Encoder–Decoder structure

. Embedding dimension: 256

. Attention heads: 8

. Encoder/Decoder layers: 3

. Feedforward dimension: 1024

. Dropout: 0.1

. Sinusoidal positional encoding
----------------------------------------------------------------------------------------------------------------------------------------------------------------

- Training Setup

. Adam optimizer

. Learning rate warm-up (4,000 steps)

. Cross-entropy loss (padding masked)

. ~200,000 training batches

. GPU acceleration (CUDA)
--------------------------------------------------------------------------------------------------------------------------------------------------------------
📊 Results

| Metric                | Value |
| --------------------- | ----- |
| Initial Training Loss | 4.707 |
| Final Training Loss   | 4.236 |
| Validation Loss       | 4.027 |
| BLEU Score            | 1.034 |
---------------------------------------------------------------------------------------------------------------------------------------------------------------
🛠 Tech Stack

. Python

. PyTorch

. NumPy

. Pandas

. Matplotlib

. SentencePiece

. CUDA
