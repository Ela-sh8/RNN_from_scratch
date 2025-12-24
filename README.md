# Recurrent Neural Network from Scratch

This repository presents a **minimal yet conceptually important implementation of a vanilla Recurrent Neural Network (RNN)**, developed to study the fundamental behavior of recurrent sequence models and **Backpropagation Through Time (BPTT)**.

Rather than aiming for performance or production use, this project focuses on **exposing the internal dynamics of recurrent learning**, including hidden-state evolution and gradient flow across time steps.

---

## Motivation

Modern deep learning frameworks hide most recurrent computations behind high-level abstractions.  
This project was designed as a **controlled experimental setup** to:

- Analyze how hidden states propagate information over time
- Understand how sequence length affects learning behavior
- Study the mechanics and limitations of vanilla RNNs
- Build intuition for why architectures such as LSTM and GRU were introduced

---

## Core Characteristics

- Explicit recurrent computation (no `nn.RNN`, `nn.LSTM`, or `nn.GRU`)
- Character-level sequence modeling
- Manual temporal unfolding with shared parameters
- Training via Backpropagation Through Time
- Lightweight and interpretable implementation

---

## Method Overview

At each time step, the model:
- Combines the current input with the previous hidden state
- Updates the hidden representation using shared weights
- Produces an output distribution used for final classification

Only the final time step is used for supervision, emphasizing sequence-level learning.

---

## Experimental Insights

- The model successfully captures short-range character dependencies
- Training loss converges steadily under controlled settings
- Performance degrades with longer sequences, highlighting vanishing gradient effects

These observations align with known theoretical limitations of vanilla RNNs.

---

## Scope and Limitations

This project is **not intended as a benchmark or production model**.  
Its purpose is analytical: to clarify the strengths and weaknesses of basic recurrent architectures.

---

## Possible Extensions

- Gradient clipping and stability analysis
- Extension to LSTM / GRU for comparative study
- Quantitative comparison with framework-based RNN modules
- Application to simple time-series datasets

---

## Disclaimer

This repository is intended for educational and exploratory research purposes only.

