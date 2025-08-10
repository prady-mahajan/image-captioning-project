# Image Captioning Project

This repository contains an **Image Captioning** pipeline implemented in Python using PyTorch and Transformers.  
It supports two main approaches:  
- **Custom CNN–LSTM model** (with attention mechanism)  
- **BLIP Visual Language Model (VLM)** (Hugging Face) for performance comparison  


## Features
- **Text Preprocessing**  
  - Caption cleaning, tokenization, and vocabulary creation  
- **Image Feature Extraction**  
  - Pretrained **ResNet50** for global image embeddings  
  - Spatial features support for attention-based decoding  
- **Caption Generation**  
  - LSTM decoder with **Bahdanau Attention** for improved context awareness  
  - Supports **Greedy Search** and **Beam Search** decoding strategies  

## Usage

- Text Preprocessing: notebooks\1_preprocessing_text.ipynb

- CNN Encoder for Feature Extraction: notebooks\2_feature_extraction_cnn_encoder.ipynb

- LSTM Decoder and Caption Generation: notebooks\3_LSTM_Decoder.ipynb

- CNN-LSTM Model with Bahdanau Attention: notebooks\4_With_Attention.ipynb

- BLIP Captioning Reference: notebooks\5_BLIP_Captioning.ipynb


## Evaluation

The model performances are evaluated using:
- **BLEU** (Bilingual Evaluation Understudy)
- **METEOR** (Metric for Evaluation of Translation with Explicit ORdering)

| Model                       | BLEU    | METEOR  |
|-----------------------------|---------|---------|
| CNN–LSTM (With Attention)   | 0.3716  | 0.3795  |
| BLIP (zero-shot reference)  | 0.4282  | 0.4137  |