# ⚙️ How AI Works?

> **Phase 1 - AI Fundamentals**
>
> **File:** `03-How-AI-Works.md`

---

# 📚 Table of Contents

1. Introduction
2. How AI Learns?
3. AI Development Lifecycle
4. Dataset
5. Training
6. Model
7. Inference
8. Fine-Tuning
9. Parameters
10. AI Pipeline
11. AI vs Traditional Software
12. Java Perspective
13. Interview Questions
14. MCQs
15. Assignment
16. Summary

---

# 1. Introduction

Ab tak humne dekha:

- AI kya hai
- ML kya hai
- Deep Learning
- Generative AI

Ab question aata hai:

> **AI actually kaam kaise karta hai?**

Bahut log sochte hain ChatGPT ke andar har question ka answer already stored hota hai.

❌ Ye completely true nahi hai.

AI answers **memorize** nahi karta.

AI **patterns learn** karta hai.

Isi wajah se wo naye questions ka bhi answer generate kar sakta hai.

---

# 2. AI ka Working Process

Ek AI system normally ye steps follow karta hai.

```text
Collect Data
      │
      ▼
Clean Data
      │
      ▼
Train Model
      │
      ▼
Save Model
      │
      ▼
User Question
      │
      ▼
Prediction
      │
      ▼
Response
```

Example

```text
Thousands of Java Books

↓

Training

↓

AI Learns Java Concepts

↓

User:

Explain Polymorphism

↓

AI Generates Answer
```

---

# 3. AI Development Lifecycle

Complete lifecycle

```text
Problem

↓

Collect Data

↓

Prepare Data

↓

Train Model

↓

Evaluate Model

↓

Deploy Model

↓

User Uses Model

↓

Improve Model
```

Ye process baar baar repeat hota hai.

---

# 4. Dataset

Dataset matlab

> Data ka collection.

Example

Suppose tum Dog aur Cat identify karna chahte ho.

Dataset

```
5000 Dog Images

+

5000 Cat Images
```

AI isi data se seekhega.

---

## Dataset Types

### Text

- Books
- Articles
- Blogs
- Code

---

### Images

- Face Images
- Medical Images
- Cars

---

### Audio

- Songs
- Speech

---

### Video

- CCTV
- Movies

---

### Structured Data

- Excel
- CSV
- Database

---

# Example

ChatGPT ne training ke time bahut saara text dekha.

Examples

- Wikipedia
- Documentation
- Programming Books
- Public Code
- Articles
- Research Papers

Isi wajah se wo Java ke questions answer kar pata hai.

---

# 5. Data Cleaning

Raw data directly use nahi hota.

Usko clean karna padta hai.

Example

Raw Data

```
Hello!!!

hello

HELLO

hello...
```

Cleaning ke baad

```
hello
```

Benefits

- Better Accuracy
- Less Noise
- Faster Training

---

# 6. Training

Training matlab

AI ko data dekar sikhana.

Diagram

```text
Dataset

↓

Learning Algorithm

↓

Model
```

Training ke time AI baar baar data dekhta hai.

Mistakes karta hai.

Unhe improve karta hai.

Fir dheere dheere better ho jata hai.

---

Example

Student

↓

Reads Book

↓

Makes Mistakes

↓

Learns

↓

Passes Exam

Exactly waise hi AI bhi learn karta hai.

---

# 7. Model

Training ke baad jo result milta hai usko

**Model**

kehte hain.

Model hi actual brain hota hai.

Examples

- GPT-4
- Gemini
- Claude
- Llama

Spring AI directly model se communicate karta hai.

---

# 8. Inference

Training complete hone ke baad

User question puchta hai.

AI answer generate karta hai.

Is process ko

**Inference**

kehte hain.

Diagram

```text
User Prompt

↓

AI Model

↓

Generated Response
```

Example

Prompt

```
Write Java Bubble Sort.
```

↓

Inference

↓

Java Code

---

Important

Training expensive hoti hai.

Inference relatively cheap hota hai.

Isi wajah se companies model train nahi karti.

Wo existing models use karti hain.

Spring AI bhi inference ke liye APIs use karta hai.

---

# 9. Fine-Tuning

Kabhi kabhi existing model enough nahi hota.

Tab usko company apne data par dobara train karti hai.

Isko

**Fine-Tuning**

kehte hain.

Example

General GPT

↓

Hospital Data

↓

Medical AI

OR

General GPT

↓

Legal Documents

↓

Legal Assistant

---

Fine-Tuning kab use hoti hai?

- Medical
- Banking
- Law
- Enterprise

---

# 10. Parameters

AI Model ke andar millions ya billions parameters hote hain.

Ye parameters learning ko represent karte hain.

Simple Example

Student

Knowledge

↓

Experience

↓

Better Decision

AI

Parameters

↓

Knowledge

↓

Better Prediction

Example

- GPT-2 → 1.5 Billion Parameters
- Llama 3 → Billions of Parameters

Bigger model ≠ Always better

Quality bhi matter karti hai.

---

# 11. AI Pipeline

Complete AI Flow

```text
Data

↓

Cleaning

↓

Training

↓

Model

↓

Deployment

↓

Prompt

↓

Inference

↓

Response
```

Ye complete pipeline almost har AI application me hoti hai.

---

# 12. Real Life Example

Suppose

Amazon Product Recommendation

Process

```text
Customer Purchases

↓

Collect Data

↓

Train Recommendation Model

↓

Customer Opens App

↓

Inference

↓

Recommended Products
```

---

# ChatGPT Example

```text
User

↓

Prompt

↓

GPT Model

↓

Token Generation

↓

Response
```

Note:

ChatGPT internet search nahi karta (unless enabled).

Wo trained model se response generate karta hai.

---

# 13. Traditional Software vs AI

Traditional Software

```text
Rules

↓

Code

↓

Output
```

Example

```java
if(age>=18){
   System.out.println("Eligible");
}
```

Output fixed hoga.

---

AI Software

```text
Data

↓

Model

↓

Prediction

↓

Output
```

Output context ke according change ho sakta hai.

---

# 14. AI in Spring AI

Spring AI khud model train nahi karta.

Spring AI ka kaam hai

```text
Spring Boot App

↓

Spring AI

↓

LLM API

↓

Response

↓

User
```

Matlab

Spring AI ek bridge hai.

Ye AI model aur Java application ko connect karta hai.

Isi wajah se Java developers ko model training nahi aani chahiye.

Unhe inference use karna aana chahiye.

---

# 15. Key Terms

| Term | Meaning |
|-------|---------|
| Dataset | Collection of data |
| Training | Learning process |
| Model | Trained AI |
| Inference | Generating response |
| Fine-Tuning | Re-training on custom data |
| Parameters | Model knowledge |
| Prompt | User instruction |

---

# 16. Interview Questions

### Q1. AI training kya hoti hai?

### Q2. Dataset kya hota hai?

### Q3. Inference kya hota hai?

### Q4. Model aur Dataset me difference?

### Q5. Fine-Tuning kya hai?

### Q6. Parameters kya hote hain?

### Q7. Spring AI model train karta hai?

### Q8. AI Pipeline explain karo.

### Q9. Training aur Inference me difference?

### Q10. ChatGPT response kaise generate karta hai?

---

# 17. MCQs

### Q1

Training ke baad kya banta hai?

A. Dataset

B. Model

C. Prompt

D. Token

✅ Answer: **B**

---

### Q2

User question process karna kya kehlata hai?

A. Training

B. Cleaning

C. Inference

D. Dataset

✅ Answer: **C**

---

### Q3

Dataset kya hota hai?

A. Programming Language

B. Collection of Data

C. Database

D. Framework

✅ Answer: **B**

---

### Q4

Spring AI ka main role kya hai?

A. Model Train Karna

B. Neural Network Banana

C. Java Application ko AI Model se Connect Karna

D. GPU Banana

✅ Answer: **C**

---

### Q5

Fine-Tuning ka use kab hota hai?

A. Custom Domain Knowledge ke liye

B. UI Banane ke liye

C. CSS Improve Karne ke liye

D. SQL Optimize Karne ke liye

✅ Answer: **A**

---

# 18. Assignment

### Beginner

- Dataset aur Model ka difference likho.
- AI Pipeline ka diagram banao.

### Intermediate

Research karo:

- GPT
- Gemini
- Claude

Aur pata karo:

- Kaunsa model inference provide karta hai?

### Advanced

Find:

- OpenAI API
- Gemini API
- Ollama

Aur likho

- Training kaun karta hai?
- Inference kaun provide karta hai?

---

# 19. Summary

Aaj humne seekha:

- AI ka actual working process
- Dataset kya hota hai
- Training kaise hoti hai
- Model kya hota hai
- Inference kya hota hai
- Fine-Tuning
- Parameters
- AI Pipeline
- Spring AI ka role

> **Remember:** Spring AI ka main focus **Inference** hai, **Training** nahi. Java developers ko AI models banana nahi, balki unhe efficiently use karna seekhna hota hai.

---

# 🚀 Next Chapter

## `04-What-is-LLM.md`

Hum seekhenge:

- What is LLM?
- GPT ka full form
- Transformer Architecture (Easy Explanation)
- Tokens ka role
- Context Window
- Popular LLMs (GPT, Gemini, Claude, Llama, Mistral)
- Closed vs Open Source Models
- Spring AI me LLM ka use
- Interview Questions & MCQs
