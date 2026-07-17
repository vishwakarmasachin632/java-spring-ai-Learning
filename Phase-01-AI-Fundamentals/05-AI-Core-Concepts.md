# 🧠 AI Core Concepts

> **Phase 1 - AI Fundamentals**
>
> **File:** `05-AI-Core-Concepts.md`

---

# 📖 Table of Contents

1. What are Tokens?
2. Tokenization
3. Types of Tokens
4. Token Limits
5. Token Pricing
6. Context Window
7. Prompt Engineering
8. Types of Prompting
9. Prompt Engineering Best Practices
10. Temperature & Top-P
11. Embeddings
12. Embedding Models
13. Embeddings in Spring AI
14. Interview Questions
15. MCQs
16. Assignment
17. Summary

---

# 1. What are Tokens?

Jab bhi hum ChatGPT, Gemini ya kisi bhi Large Language Model (LLM) ko koi prompt bhejte hain, to model **words ko directly process nahi karta**.

Wo sabse pehle text ko **small pieces** me divide karta hai.

In small pieces ko **Tokens** kehte hain.

Simple language me:

> **Token = Text ka smallest meaningful unit jo AI process karta hai.**

Example:

```
I love Java Programming
```

Approx Tokens:

```
I

love

Java

Programming
```

Lekin reality me har model ka tokenizer alag hota hai.

Example

```
SpringBoot
```

Ye tokenize ho sakta hai:

```
Spring

Boot
```

ya

```
SpringBoot
```

Ye model par depend karta hai.

---

# Why Tokens Important?

LLM kabhi bhi words count nahi karta.

Wo sirf tokens count karta hai.

Har AI model ke liye important cheeze:

✅ Input Tokens

✅ Output Tokens

✅ Context Window

✅ API Cost

Sab kuch tokens par depend karta hai.

---

# 2. Tokenization

Text ko tokens me convert karne ki process ko

**Tokenization**

kehte hain.

Flow

```
User Prompt

↓

Tokenizer

↓

Tokens

↓

LLM

↓

Response Tokens

↓

Final Response
```

Example

Input

```
Explain Spring Boot.
```

Possible Tokens

```
Explain

Spring

Boot

.
```

AI inhi tokens ko samajhta hai.

---

# Types of Tokens

Generally tokens ho sakte hain

### Word Tokens

```
Java

Spring

Boot
```

---

### Subword Tokens

```
Program

ming
```

---

### Character Tokens

```
J

a

v

a
```

Modern LLMs mostly **Subword Tokenization** use karte hain.

Kyuki ye zyada efficient hoti hai.

---

# Input Tokens

User jo prompt bhejta hai.

Example

```
Explain OOP in Java.
```

Ye Input Tokens hain.

---

# Output Tokens

AI jo answer generate karta hai.

Wo Output Tokens hote hain.

Example

```
Object-Oriented Programming is...
```

Ye output tokens hain.

---

# Total Tokens

```
Total Tokens

=

Input Tokens

+

Output Tokens
```

API billing bhi isi par hoti hai.

---

# 3. Token Limits

Har model ki ek maximum token capacity hoti hai.

Usko

**Context Window**

bolte hain.

Example

```
Prompt

+

Chat History

+

System Prompt

+

Response

=

Context Window
```

Agar ye limit exceed ho jaye

To model purani conversation bhool sakta hai.

---

# Example

Suppose

Model Limit

```
8000 Tokens
```

Already use ho chuke

```
7600
```

Remaining

```
400 Tokens
```

Agar tum 1000 token ka prompt bhejoge

To problem hogi.

---

# Best Practices

✅ Short Prompt

✅ Relevant Context

✅ Remove Unnecessary Chat History

✅ Summarize Old Messages

---

# 4. Token Pricing

Almost sabhi AI providers

(OpenAI, Gemini, Anthropic)

Token ke according charge karte hain.

Formula

```
Input Tokens

×

Input Price

+

Output Tokens

×

Output Price
```

Example

Input

```
500 Tokens
```

Output

```
700 Tokens
```

Total

```
1200 Tokens
```

Isliye enterprise applications me

Token optimization bahut important hota hai.

---

# 5. Context Window

Context Window matlab

AI ek request me kitni information yaad rakh sakta hai.

Simple Example

Suppose tum friend se baat kar rahe ho.

Tumne pehle bola

```
My Name is Sachin.
```

5 minute baad tum puchte ho

```
What's my name?
```

Friend ko yaad rahega.

Kyuki uske paas context hai.

LLM bhi isi tarah kaam karta hai.

---

# Context Window Flow

```
System Prompt

+

Conversation History

+

Current Prompt

↓

Context Window

↓

LLM

↓

Answer
```

---

# Why Context Matters?

Without Context

```
Who is he?
```

AI confuse ho jayega.

With Context

```
Sachin is learning Spring AI.

Who is he?
```

Answer

```
He is Sachin.
```

---

# Context Overflow

Agar context bahut bada ho jaye

Example

```
100 Pages PDF

+

Long Chat History

+

Large Prompt
```

To model kuch purani information ignore kar sakta hai.

Isi wajah se

RAG

Chunking

Summarization

use kiye jate hain.

---

# 6. Prompt Engineering

Prompt Engineering ka matlab hai

AI ko is tarah instruction dena ki wo best response de.

Simple Definition

> **Better Prompt = Better Output**

---

# Bad Prompt

```
Explain Java.
```

Bahut generic hai.

---

# Better Prompt

```
Explain Java OOP concepts in Hinglish with real-world examples for a fresher interview.
```

Ab AI ko clear instruction mil gaya.

---

# Good Prompt Formula

```
Role

+

Task

+

Context

+

Constraints

+

Expected Output
```

Example

```
You are a Senior Java Trainer.

Explain Spring Boot Dependency Injection.

Language: Hinglish

Length: 500 words

Include Interview Questions.
```

Is tarah ke prompts enterprise projects me use hote hain.

---

# Types of Prompting

## Zero Shot

Sirf question.

```
Explain Spring Boot.
```

---

## One Shot

Ek example ke sath.

```
Example:

Java → Programming Language

Now Explain Spring Boot.
```

---

## Few Shot

2–5 examples diye jate hain.

AI pattern samajh leta hai.

---

## Role Prompting

```
You are an Interviewer.

Take my Java interview.
```

Ye bahut powerful technique hai.

---

## Output Formatting

```
Return answer in Markdown Table.

OR

Return JSON.

OR

Return Bullet Points.
```

Enterprise APIs me bahut use hota hai.

---

# Prompt Engineering Best Practices

✅ Clear Objective

✅ Short Instructions

✅ Mention Output Format

✅ Give Examples

✅ Mention Language

✅ Avoid Ambiguous Questions

❌ Don't write very long unnecessary prompts.

❌ Don't ask multiple unrelated questions in one prompt.

---

# 7. Temperature

Temperature creativity control karta hai.

```
0.0

↓

Less Creative

↓

More Accurate
```

```
1.0

↓

More Creative

↓

Less Predictable
```

## Recommended Values

| Task | Temperature |
|------|-------------|
| Coding | 0.1 – 0.3 |
| Interview Answers | 0.2 – 0.4 |
| Documentation | 0.3 – 0.5 |
| Blogging | 0.7 |
| Story Writing | 0.9 – 1.0 |

---

# 8. Top-P

Top-P bhi randomness control karta hai.

Difference

Temperature

↓

Randomness

Top-P

↓

Vocabulary Selection

Generally

Default value enough hoti hai.

Coding applications me

Temperature low rakhna best practice hai.

---

# 9. Embeddings (Introduction)

Embeddings AI ka sabse important concept hai.

Simple Definition

> Embedding kisi bhi text ko numbers (vectors) me convert karta hai taaki AI uska meaning compare kar sake.

Example

```
Java is a Programming Language.
```

↓

Embedding Model

↓

```
[0.21, -0.45, 0.89, ...]
```

Ye vector human ke liye useful nahi hota, lekin AI ke liye bahut valuable hota hai.

---

# Why Embeddings?

LLM words compare nahi karta.

Wo vectors compare karta hai.

Example

```
Car
```

Aur

```
Automobile
```

Words different hain.

Meaning same hai.

Embedding vectors bhi almost similar honge.

Isi wajah se Semantic Search possible hoti hai.

---

# Common Use Cases

- Semantic Search
- RAG (Retrieval-Augmented Generation)
- Recommendation Systems
- Duplicate Detection
- Similar Document Search
- AI Chatbots
- Knowledge Base Search

---

# Spring AI Perspective

Spring AI me Embeddings generate karne ke liye mainly use hote hain:

- `EmbeddingModel`
- `VectorStore`

Flow:

```
Document
      ↓
EmbeddingModel
      ↓
Vector
      ↓
Vector Database
      ↓
Similarity Search
      ↓
LLM
      ↓
Final Answer
```

---

# Interview Questions

### Q1. What is a Token?

### Q2. What is Tokenization?

### Q3. Difference between Input and Output Tokens?

### Q4. What is Context Window?

### Q5. What happens when Context Window is full?

### Q6. What is Prompt Engineering?

### Q7. Difference between Zero Shot and Few Shot Prompting?

### Q8. What is Temperature?

### Q9. What is Top-P?

### Q10. What are Embeddings?

### Q11. Why are Embeddings used in RAG?

### Q12. Which Spring AI classes are used for Embeddings?

---

# MCQs

### Q1

LLM kis unit me text process karta hai?

A. Words

B. Characters

C. Tokens

D. Sentences

✅ Answer: **C**

---

### Q2

Prompt ko tokens me convert karne ki process ko kya kehte hain?

A. Encoding

B. Tokenization

C. Parsing

D. Translation

✅ Answer: **B**

---

### Q3

Coding tasks ke liye best Temperature kya hota hai?

A. 0.2

B. 0.9

C. 1.5

D. 2.0

✅ Answer: **A**

---

### Q4

Embeddings mainly kis kaam aate hain?

A. CSS Styling

B. Semantic Search

C. JDBC Connection

D. Docker Deployment

✅ Answer: **B**

---

# Assignment

## Beginner

- Explain Tokens in your own words.
- Write 5 good prompts and improve them.

## Intermediate

- Compare Temperature and Top-P.
- Research OpenAI Token Pricing.

## Advanced

Research:

- Embedding Models
- Cosine Similarity
- Semantic Search
- Vector Search

Aur note karo ki Spring AI me Embeddings ka use RAG ke saath kaise hota hai.

---

# Summary

Is chapter me humne seekha:

- Tokens kya hote hain
- Tokenization kaise hoti hai
- Context Window kya hota hai
- Prompt Engineering aur uske types
- Temperature aur Top-P
- Embeddings kya hote hain
- Spring AI me Embeddings ka role

Ye concepts Spring AI ki backbone hain. Agar tumhe ye clear ho gaye, to RAG, Vector Database aur AI Agents samajhna bahut easy ho jayega.

---

## 🎯 Next Chapter

**06-Advanced-AI-Concepts.md**

Hum seekhenge:

- Vector Databases
- RAG (Retrieval-Augmented Generation)
- Hallucination
- Function Calling
- AI Agents
- MCP (Model Context Protocol)
- Spring AI Integration
