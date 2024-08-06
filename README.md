# English-to-Italian Translation Transformer

Implement the [Attention is All You Need](https://arxiv.org/abs/1706.03762) paper from scratch using PyTorch, focusing on building a sequence-to-sequence transformer architecture for translating text from English to Italian.

## Overview

The transformer architecture, introduced in the paper [Attention is All You Need](https://arxiv.org/abs/1706.03762), revolutionized sequence-to-sequence tasks with its attention-based mechanism, eliminating the need for recurrent networks. This project leverages this architecture to translate English sentences into Italian.

## Data

The model was trained and evaluated on the [g8a9 / europarl_en-it](https://huggingface.co/datasets/g8a9/europarl_en-it) dataset, the dataset consists of English and Italian sentence pairs used for training and validation.

The intention was to train the model on the entire dataset (the entire dataset consist of 1.9M sentence pairs)  but because of the limited hardware capabilities I just used 100K for training, and 20K for evaluating.

Tokenizers from Hugging Face were employed solely for preprocessing the data, other components of the model were implemented from scratch.

## Results

| Epochs | Loss(train) | Loss(validation) | F1(train) | F1(validation) | Time(minutes) | Device     |
|--------|-------------|------------------|-----------|----------------|---------------|------------|
| 5      | 0.116378    | 0.091345         | 0.262342  | 0.273207       | 170           | 1 x T4 GPU |

## Acknowledgements

This project follows the architecture and configurations from the [Attention is All You Need](https://arxiv.org/abs/1706.03762) paper. The implementation is guided by the principles and methods outlined in the paper.

