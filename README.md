# Single-Head vs Multi-Head Attention

## Overview
This repository contains implementations of **Single-Head** and **Multi-Head Attention**, key components in Transformer architectures used in NLP and deep learning models.

## 🔹 Single-Head Attention
### 📌 Description
Single-head attention computes attention using a single Query, Key, and Value matrix. It captures only one type of relationship within the input sequence.

### 🏗️ Implementation Steps
1. Compute **Query (Q), Key (K), and Value (V)** matrices.
2. Compute the **scaled dot-product attention**:
   - \( \text{scores} = QK^T / \sqrt{d_k} \)
   - Apply **softmax** to get attention weights.
   - Compute weighted sum with **V**.
3. Return the final attention output.

### ⚡ Pros & Cons
✅ Simple and computationally efficient.
❌ Limited ability to capture diverse relationships in input sequences.

---

## 🔹 Multi-Head Attention
### 📌 Description
Multi-head attention extends single-head attention by using multiple sets of **Q, K, V** matrices. Each head captures different types of relationships, leading to a richer representation.

### 🏗️ Implementation Steps
1. Compute **Q, K, V** matrices.
2. Split Q, K, and V into **multiple heads**.
3. Compute **scaled dot-product attention** separately for each head.
4. Concatenate all head outputs.
5. Transform the concatenated output back to the original dimension.

### ⚡ Pros & Cons
✅ Captures multiple perspectives in the input.
✅ Enhances model expressiveness.
❌ More computationally expensive than single-head attention.

---



## 🚀 Conclusion
- **Single-Head Attention**: Good for simple relationships, computationally light.
- **Multi-Head Attention**: More powerful, captures complex patterns, widely used in Transformers.

For further details, refer to the implementation files in this repository. 🚀

