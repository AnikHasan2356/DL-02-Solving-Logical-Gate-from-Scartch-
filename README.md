# Perceptron from Scratch in Python

A beginner-friendly implementation of the **Perceptron Learning Algorithm** using only **NumPy**. This project demonstrates how a single-layer perceptron learns linearly separable problems and why it fails on non-linearly separable data such as the XOR gate.

---

## 📌 Overview

The Perceptron is one of the earliest supervised machine learning algorithms introduced by Frank Rosenblatt in 1958. It is a binary linear classifier that learns a decision boundary by iteratively updating its weights based on classification errors.

In this project, the Perceptron is implemented completely from scratch without using any machine learning libraries such as Scikit-learn.

---

## 🚀 Features

- Perceptron implementation from scratch using NumPy
- Random weight initialization
- Bias term implementation
- Step activation function
- Weight update using the Perceptron Learning Rule
- Training over multiple epochs
- Prediction on unseen samples
- Decision boundary visualization
- Demonstration of linear separability
- Comparison of AND, OR, and XOR logic gates

---

## 🛠 Technologies Used

- Python
- NumPy
- Pandas
- Matplotlib

---

## 📂 Project Structure

```
.
├── perceptron.py
├── AND.ipynb
├── OR.ipynb
├── XOR.ipynb
├── plots/
└── README.md
```

---

## Perceptron Architecture

```
          x1
           │
           │
          w1
           │
           ▼
                Σ ─────► Activation Function ─────► Output
           ▲
          w2
           │
           │
          x2

      Bias = -1
```

The weighted sum is computed as

\[
z = w_1x_1+w_2x_2+b
\]

The step activation function is

\[
y=
\begin{cases}
1,& z>0\\
0,& z\le0
\end{cases}
\]

---

# Datasets

Three logic gate datasets are used.

## AND Gate

| x1 | x2 | y |
|---|---|---|
|0|0|0|
|0|1|0|
|1|0|0|
|1|1|1|

---

## OR Gate

| x1 | x2 | y |
|---|---|---|
|0|0|0|
|0|1|1|
|1|0|1|
|1|1|1|

---

## XOR Gate

| x1 | x2 | y |
|---|---|---|
|0|0|0|
|0|1|1|
|1|0|1|
|1|1|0|

---

# Results

## AND Gate

The Perceptron successfully learns the AND gate because the data is **linearly separable**.

✔ Successfully classified all samples.

---

## OR Gate

The Perceptron also successfully learns the OR gate because a single straight line can separate the two classes.

✔ Successfully classified all samples.

---

## XOR Gate

The Perceptron fails to learn the XOR gate.

Even after many epochs, the weights cannot converge to a solution because XOR is **not linearly separable**.

---

# Why XOR Cannot Be Learned?

A single-layer Perceptron can only learn problems that are **linearly separable**.

For the XOR gate, no single straight line can separate the two classes.

Positive samples:

```
(0,1)
(1,0)
```

Negative samples:

```
(0,0)
(1,1)
```

These four points lie diagonally opposite each other, making it impossible to separate them with one decision boundary.

Your visualization clearly demonstrates this limitation.

> **Conclusion:** A single-layer Perceptron cannot solve XOR because XOR is not linearly separable.

This problem motivated the development of **Multi-Layer Perceptrons (MLPs)** with hidden layers.

---

# Training Procedure

1. Initialize random weights.
2. Add a bias term.
3. Compute the weighted sum.
4. Apply the activation function.
5. Compute prediction error.
6. Update weights using the Perceptron Learning Rule.
7. Repeat for the specified number of epochs.

Weight update equation:

\[
w=w+\eta X^Te
\]

where

- \(w\) = weights
- \(\eta\) = learning rate
- \(e\) = prediction error

---

# Decision Boundary

The project also visualizes the learned decision boundary for each logic gate.

- AND → Linear decision boundary ✔
- OR → Linear decision boundary ✔
- XOR → No linear decision boundary ✖

This clearly illustrates the concept of **linear separability**.

---

# Learning Outcomes

After completing this project, you will understand:

- What a Perceptron is
- How the Perceptron Learning Algorithm works
- Weight initialization
- Bias implementation
- Step activation function
- Training and prediction
- Decision boundary
- Linear separability
- Why XOR cannot be solved using a single-layer Perceptron
- Why hidden layers are required in neural networks

---

# Future Improvements

- Multi-Layer Perceptron (MLP)
- Sigmoid activation
- ReLU activation
- Backpropagation
- Gradient Descent
- TensorFlow implementation
- PyTorch implementation

---

# References

- Frank Rosenblatt, *The Perceptron: A Probabilistic Model for Information Storage and Organization in the Brain*, 1958.
- Christopher Bishop, *Pattern Recognition and Machine Learning*.
- Ian Goodfellow, Yoshua Bengio, Aaron Courville, *Deep Learning*.

---

## ⭐ If you found this project helpful, consider giving it a star!
