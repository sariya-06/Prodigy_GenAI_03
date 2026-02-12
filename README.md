# Task 3 – Text Generation using Markov Chains

## 📌 Project Overview
This project implements a simple text generation model using Markov Chains in Python.  
The objective is to understand how probabilistic models can generate text based on patterns learned from a dataset.

## 🎯 Objective
To build a statistical text generator that predicts the next word based on previous words using Markov Chains.

## 🛠 Technologies Used
- Python
- Google Colab
- Markovify Library

## 📂 Dataset
A custom text dataset related to Artificial Intelligence and the Software Industry was used to train the model.

## ⚙️ Implementation Steps
1. Installed the Markovify library.
2. Uploaded and read the text dataset.
3. Built a Markov model using `markovify.Text()`.
4. Generated new sentences using probability-based predictions.

## 💡 How It Works
Markov Chains work by calculating the probability of a word occurring after a given sequence of words.  
The model learns patterns from the dataset and generates new sentences that resemble the original text.

## ▶️ Sample Code

```python
import markovify

with open("task3_dataset.txt", "r", encoding="utf-8") as f:
    text = f.read()

text_model = markovify.Text(text, state_size=2)

for i in range(5):
    print(text_model.make_short_sentence(120))
