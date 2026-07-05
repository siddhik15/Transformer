# Transformer Self-Attention from Scratch using NumPy

This project demonstrates **how self-attention works inside a Transformer** using a simple **manual implementation in Python with NumPy**.

Instead of using deep learning libraries like TensorFlow or PyTorch, this script explains **each mathematical step of self-attention clearly** with a small example so that beginners can understand the internal calculations.

---

## 📌 Project Objective

The goal of this project is to manually compute **self-attention** for a small sentence:

**"I love AI"**

The script shows how input word embeddings are transformed into:

* **Query (Q)**
* **Key (K)**
* **Value (V)**

and then how these are used to calculate:

* **Attention Scores**
* **Scaled Scores**
* **Softmax Attention Weights**
* **Final Context-Aware Output**

---

## 🧠 Concepts Covered

This project helps in understanding the following Transformer concepts:

* Word embeddings
* Query, Key, and Value matrices
* Dot-product attention
* Scaling by √dk
* Softmax function
* Weighted sum of values
* Context-aware word representation

---

## ⚙️ Technologies Used

* **Python**
* **NumPy**

---

## 📝 How the Script Works

The script performs self-attention in **7 detailed steps**.

### **Step 1: Input Embeddings**

A small sentence is represented using numerical vectors:

* **I** → `[1, 0]`
* **love** → `[0, 1]`
* **AI** → `[1, 1]`

These vectors are stored in matrix **X**.

---

### **Step 2: Define Weight Matrices**

Three weight matrices are defined:

* **Wq** → Query weight matrix
* **Wk** → Key weight matrix
* **Wv** → Value weight matrix

These convert input embeddings into **Q, K, and V vectors**.

---

### **Step 3: Calculate Query, Key, and Value**

Using matrix multiplication:

* **Q = X × Wq**
* **K = X × Wk**
* **V = X × Wv**

This gives the query, key, and value representation for each word.

---

### **Step 4: Compute Attention Scores**

Attention scores are calculated using:

**Scores = Q × Kᵀ**

This tells us how strongly one word relates to another word.

---

### **Step 5: Scale the Scores**

The attention scores are scaled by:

**Scaled Scores = Scores / √dk**

where **dk** is the dimension of the key vector.

Scaling prevents very large values from affecting softmax too strongly.

---

### **Step 6: Apply Softmax**

Softmax is applied row-wise to convert scaled scores into probabilities.

These probabilities are called **attention weights**.

Each row shows **how much attention one word gives to every other word**.

---

### **Step 7: Compute Final Self-Attention Output**

The final output is calculated as:

**Output = Attention Weights × V**

This produces a new contextual representation for every word.

After attention, each word is no longer independent — it now contains information from other words in the sentence.

---

## ▶️ Example Output Flow

The program prints:

* Input embeddings
* Weight matrices
* Q, K, V matrices
* Attention score matrix
* Scaled score matrix
* Attention weights
* Final contextual output vectors
* Manual calculations for better understanding

This makes the script useful for **learning, teaching, interviews, and academic demonstrations**.

---

## 📊 Learning Outcome

By going through this project, you will understand:

* how self-attention is computed mathematically
* why Q, K, and V are used
* how softmax converts scores into attention probabilities
* how Transformers make words context-aware
* how attention combines information from all words in a sentence

---

## 🎯 Who Can Use This Project?

This project is useful for:

* **Students** learning Transformers and NLP
* **Beginners** who want self-attention explained step by step
* **Interview preparation** for AI/ML/NLP roles
* **Academic mini-projects / presentations**
* Anyone who wants to understand the internal working of Transformer attention without using large frameworks

---

## 📌 Conclusion

This project is a **beginner-friendly manual implementation of Transformer self-attention** using NumPy.
It breaks down the entire process into small understandable steps and shows how words become **context-aware** through attention.

It is a good educational project for understanding one of the most important ideas behind modern NLP models such as **Transformers, BERT, and GPT**.
