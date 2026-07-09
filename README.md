# Next Word Prediction using LSTM (PyTorch)

A simple Next Word Prediction model built with **PyTorch**. The model learns from a collection of quotes and predicts the next word given a sequence of previous words.

---

## Features

- Text preprocessing
- Vocabulary creation
- Integer encoding
- Sequence generation
- Padding variable-length sequences
- Embedding Layer
- LSTM Network
- Fully Connected Classifier
- CrossEntropy Loss
- Adam Optimizer
- Training Accuracy Tracking
- Loss & Accuracy Visualization
- Model Summary using torchinfo

---

## Project Structure

```
.
├── qoute_dataset.csv
├── next_word_prediction.py
├── README.md
```

---

## Dataset

The dataset contains a column named:

```
quote
```

Example:

```
The future belongs to those who believe
Knowledge is power
Success comes from hard work
```

---

## Preprocessing

The preprocessing pipeline performs:

- Convert text to lowercase
- Remove punctuation
- Split into words (tokenization)

Example

Input

```
"Dream Big!"
```

Output

```
["dream", "big"]
```

---

## Vocabulary Creation

Each unique word is assigned a unique integer ID.

Example

```
{
"<pad>":0,
"life":1,
"is":2,
"beautiful":3
}
```

---

## Sequence Generation

Each sentence is converted into multiple training samples.

Example

Sentence

```
I love deep learning
```

Training pairs

| Input | Target |
|--------|---------|
| [] | I |
| I | love |
| I love | deep |
| I love deep | learning |

---

## Padding

Since every sequence has a different length, all sequences are padded using

```python
pad_sequence()
```

Padding Value

```
0
```

---

## Model Architecture

```
Input
      │
Embedding Layer
      │
LSTM
      │
Last Hidden State
      │
Linear
      │
ReLU
      │
Linear
      │
Vocabulary Size
```

---

## Model

Embedding Size

```
64
```

Hidden Size

```
32
```

Output

```
Vocabulary Size
```

---

## Loss Function

```
CrossEntropyLoss
```

---

## Optimizer

```
Adam
```

Learning Rate

```
0.001
```

Weight Decay

```
0.01
```

---

## Training

The model trains for

```
100 Epochs
```

During training, the following metrics are recorded:

- Loss
- Accuracy

---

## Visualization

After training, Matplotlib is used to plot

- Training Loss
- Training Accuracy

---

## Model Summary

The project uses

```
torchinfo.summary()
```

to display

- Number of Parameters
- Input Shape
- Output Shape
- Layer Information

---

## Requirements

Install dependencies

```bash
pip install torch pandas matplotlib torchinfo
```

---

## Run

```bash
python next_word_prediction.py
```

---

## Future Improvements

- Train/Test Split
- Validation Accuracy
- DataLoader
- Batch Training
- GPU Support
- Early Stopping
- Dropout
- Save & Load Model
- Beam Search
- Temperature Sampling
- Interactive Text Generation

---

## Learning Outcomes

This project demonstrates:

- NLP preprocessing
- Vocabulary building
- Integer encoding
- Sequence modeling
- Word embeddings
- LSTM networks
- Multi-class classification
- Training neural networks using PyTorch

---

## Author

**Debajyoti Hazra**

Built while learning **Natural Language Processing (NLP)** and **PyTorch**.# Next_Token_Predict_Using_RNN
