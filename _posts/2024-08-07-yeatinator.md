---
layout: post
title: Yeatinator - Generate Lyrics in the Style of Your Favorite Artists
author: Fabio
tags:
date: 2024-09-27 13:56 +0800
last_modified_at: 2024-09-27 13:56 +0800
---
# Yeatinator: A Comparative Analysis of LSTM and GPT-2 for Rap Lyric Generation

![image](/yeat.jpg)
The **Yeatinator** project explores the effectiveness of different NLP architectures—specifically an LSTM-based model and a fine-tuned GPT-2 model—in generating lyrics inspired by the rapper *Yeat*. This project highlights the creative potential of AI for text generation tasks and provides insights into the differences between older, more traditional sequence models (LSTM) and newer transformer models like GPT-2.

## Project Overview

- **LSTM (Long Short-Term Memory)**: A recurrent neural network (RNN) architecture capable of handling long-range dependencies in sequences, frequently used in NLP tasks.
- **GPT-2 (Generative Pre-trained Transformer 2)**: A transformer-based model that excels at generating human-like text by leveraging a massive amount of pre-training data and a more sophisticated attention mechanism.

The project consisted of two major stages:

1. Training an LSTM model from scratch using the lyrics of *Yeat*.
2. Fine-tuning a pre-trained GPT-2 model on the same corpus to specialize it for lyric generation in *Yeat*'s style.

## Dataset

The dataset used in this project comprised a comprehensive collection of lyrics from *Yeat*'s songs. This data was preprocessed to ensure uniformity in text formatting, tokenization, and to reduce noise (e.g., removing punctuation and non-lyrical elements).

- **Size of the dataset**: ~300 yeat songs
- **Vocabulary size**: Around 8000 unique tokens

## Model Architecture

### LSTM Model

- **Embedding Layer**: Converts input tokens into dense vectors of fixed size.
- **LSTM Layers**: Two layers of LSTM cells, each with 128 hidden units, designed to capture sequential dependencies and relationships between words and phrases.
- **Dense Layer**: A final dense layer with a softmax activation to predict the next word in the sequence.

The LSTM was trained using:

- **Loss Function**: Categorical Cross-Entropy
- **Optimizer**: Adam
- **Training Time**: ~1 hour on my laptop

### GPT-2 Model

A pre-trained GPT-2 model was fine-tuned on the *Yeat* lyrics corpus, making use of transfer learning to adapt the general language capabilities of GPT-2 to the specific task of rap lyric generation.

- **Base Model**: GPT-2
- **Training Epochs**: 5 epochs
- **Training Time**: ~1 hour on a GPU

## Results

### LSTM

The LSTM model produced coherent lyrics that captured some of *Yeat*'s stylistic patterns and repetitive structures. However, due to the limited memory of RNNs, it struggled to maintain longer-term coherence across multiple lines. The model also had difficulty generating creative, novel phrases, often producing lyrics that were highly repetitive or simple.

#### Sample Output from LSTM:
```
i'm at the top
  got to me up, i got some bitch, and right go nobody, if all that sleep
  got to of bitch that am when baby, bitch, first, the oh yeah
  back it 'bout i'ma really wanna big feel at landin'?"
  i gon' all these ran you just from the i'm not this but i heard i end
  i flipping skin me
  ah, and they pushing
  i took gotta what's her her if yeah, when yeah, the need changin' like up
  i'm this inside you want the never feeling
  i be couldn't keller,
```

### GPT-2

The fine-tuned GPT-2 model outperformed the LSTM in nearly every aspect. It generated more diverse, coherent, and complex lyrics that better mimicked *Yeat*'s unique flow and wordplay. GPT-2’s ability to capture larger contexts resulted in more creative and less repetitive lyric generation.

#### Sample Output from GPT-2:
```
im at the top',
'I got a whole lot of fuckin' money,
I got a whole lot of fuckin' bullets',
"I got a whole lot of fuckin' bullets,
just sayin' out loud",
'I got all these racks,
yeah,
all they rackie',
"Yeah,
I got these bitches on me,
it's way too much food",
"I'm fuckin' my money up,
bitch,
I'm fuckin' my money down ",
"I might be the
```

## Conclusion

The results of the **Yeatinator** project demonstrated that while both LSTM and GPT-2 models can generate lyrics, **GPT-2 significantly outperformed the LSTM** in terms of grammar and maintaining *Yeat*'s style.  We can clairly see the difficulties in training models for text generation from scratch and the benefits of leveraging pre-trained models for specific tasks.
