# 🎯 Phase-04 Prompt Engineering

> **Spring AI Mastery**
>
> **File:** `Phase-04-Prompt-Engineering.md`

---

# 📖 Table of Contents

1. What is Prompt Engineering?
2. Prompt Components
3. Types of Prompts
4. Prompting Techniques
5. Prompt Templates
6. Output Formatting
7. Prompt Chaining
8. Guardrails
9. Common Mistakes
10. Best Practices
11. Spring AI PromptTemplate
12. Interview Questions
13. MCQs
14. Assignment
15. Summary

---

# 1. What is Prompt Engineering?

Prompt Engineering ka matlab hai AI ko is tarike se instruction dena ki wo accurate, useful aur predictable response de.

Simple Formula

```
Better Prompt
        ↓
Better Response
```

Prompt = AI ke liye instruction.

Example

Bad Prompt

```
Explain Java.
```

Good Prompt

```
Explain Java OOP concepts in Hinglish with real-world examples in table format for interview preparation.
```

---

# 2. Prompt Components

Ek effective prompt me generally ye components hote hain.

### Role

```
You are a Senior Java Developer.
```

### Task

```
Explain Spring Boot Dependency Injection.
```

### Context

```
Audience is Java Freshers.
```

### Constraints

```
Use Hinglish.

Maximum 500 words.
```

### Output Format

```
Return Markdown Table.
```

Complete Example

```
You are a Senior Java Trainer.

Explain Spring Boot Dependency Injection.

Language: Hinglish

Length: 500 words

Output: Markdown Table
```

---

# 3. Types of Prompts

## System Prompt

Model ka behavior define karta hai.

Example

```
You are an AI Interviewer.
```

---

## User Prompt

User ka actual question.

```
Explain Spring Boot.
```

---

## Assistant Prompt

Previous AI response.

Conversation maintain karne ke liye use hota hai.

---

# 4. Prompting Techniques

## Zero-Shot Prompting

Koi example nahi.

```
Explain Java Collections.
```

---

## One-Shot Prompting

Ek example diya jata hai.

```
Example

Java = Programming Language

Now Explain Spring Boot.
```

---

## Few-Shot Prompting

2–5 examples diye jate hain.

AI pattern samajh leta hai.

---

## Role Prompting

```
You are an HR Interviewer.

Take my interview.
```

---

## Step-by-Step Prompting

```
Explain one step at a time.
```

Useful for learning.

---

## Chain of Thought (CoT)

Complex problem ko reasoning ke sath solve karna.

Example

```
Solve the problem step by step.
```

Use Cases

- Math
- Logic
- Algorithms
- Debugging

---

## ReAct Prompting

Reason + Act

```
Think

↓

Choose Tool

↓

Observe

↓

Answer
```

Mostly AI Agents me use hota hai.

---

# 5. Prompt Templates

Dynamic prompts banane ke liye.

Template

```
Hello {name}

Welcome to {course}
```

Input

```
Sachin

Spring AI
```

Output

```
Hello Sachin

Welcome to Spring AI
```

Spring AI me PromptTemplate isi concept par based hai.

---

# 6. Output Formatting

AI ko clearly batao output kis format me chahiye.

Examples

### Bullet List

```
Return bullet points.
```

---

### Table

```
Return Markdown table.
```

---

### JSON

```
Return JSON only.
```

Output

```json
{
  "name":"Sachin",
  "skill":"Spring AI"
}
```

---

### Java Object

```
Return Java Record.
```

---

# 7. Prompt Chaining

Ek prompt ka output next prompt ka input ban jata hai.

Flow

```
Prompt 1

↓

Summary

↓

Prompt 2

↓

Questions

↓

Prompt 3

↓

Final Notes
```

Use Cases

- PDF Summarization
- Resume Analysis
- Code Review

---

# 8. Guardrails

Guardrails AI ko safe aur controlled response dene me help karte hain.

Examples

- Don't generate harmful content.
- Don't expose API Keys.
- Don't answer outside given context.
- Return only JSON.

---

# 9. Common Prompt Mistakes

❌ Very long prompts

❌ Multiple questions ek sath

❌ No context

❌ No output format

❌ Ambiguous instructions

❌ Missing examples

---

# 10. Prompt Engineering Best Practices

✅ Clear Objective

✅ Proper Context

✅ Mention Role

✅ Mention Output Format

✅ Keep Prompt Short

✅ Use Examples

✅ Reuse Templates

✅ Test Multiple Prompts

---

# 11. Prompt Engineering in Spring AI

Spring AI provides:

- Prompt
- PromptTemplate
- SystemMessage
- UserMessage
- AssistantMessage

Example Flow

```
User

↓

PromptTemplate

↓

ChatClient

↓

LLM

↓

Response
```

Example

```java
PromptTemplate template =
    new PromptTemplate("Hello {name}");

template.create(Map.of("name","Sachin"));
```

Benefits

- Reusable
- Dynamic
- Clean Code
- Easy Maintenance

---

# 12. Interview Questions

### Beginner

1. What is Prompt Engineering?
2. What is a Prompt?
3. System Prompt vs User Prompt?
4. Zero-Shot Prompting kya hai?
5. Few-Shot Prompting kya hai?

### Intermediate

6. Chain of Thought kya hai?
7. PromptTemplate kya hota hai?
8. Prompt Chaining explain karo.
9. Guardrails kya hote hain?
10. Spring AI PromptTemplate ka use?

### Advanced

11. Enterprise Prompt Design kaise karte hain?
12. Prompt Optimization techniques?
13. ReAct Prompting explain karo.
14. AI Agent Prompting kaise work karti hai?

---

# 13. MCQs

Q1. Prompt Engineering ka goal?

A. Database banana

B. Better AI Response ✅

C. CSS likhna

D. Docker banana

---

Q2. Example-based prompting?

A. Zero-Shot

B. Few-Shot ✅

C. HTML

D. JDBC

---

Q3. Dynamic Prompt kis class se banta hai?

A. PromptTemplate ✅

B. JdbcTemplate

C. RestTemplate

D. BeanFactory

---

Q4. ReAct ka matlab?

A. Read and Act

B. Reason and Act ✅

C. Retry and Act

D. Response Action

---

# 14. Assignment

## Beginner

- 10 bad prompts ko improve karo.
- 5 Zero-Shot prompts likho.

## Intermediate

- PromptTemplate use karke dynamic prompts banao.
- Same task ke liye 3 different prompts compare karo.

## Advanced

- AI Resume Reviewer ka prompt design karo.
- AI Code Reviewer ke liye system prompt likho.

---

# 15. Summary

Is phase me humne seekha:

- Prompt Engineering
- Prompt Components
- System/User Prompts
- Zero, One & Few-Shot
- Chain of Thought
- ReAct
- PromptTemplate
- Output Formatting
- Prompt Chaining
- Guardrails
- Spring AI PromptTemplate

---

# 🎯 Key Takeaways

- Better Prompt = Better Response
- Context bahut important hai.
- PromptTemplate reusable prompts banata hai.
- Chain of Thought reasoning improve karta hai.
- ReAct AI Agents ka base hai.
- Spring AI PromptTemplate dynamic prompts create karta hai.

---

# 🚀 Next Phase

## **Phase-05-ChatClient.md**

Topics:

- ChatClient Deep Dive
- ChatModel
- Request Lifecycle
- Streaming
- Advisors
- Error Handling
- Best Practices
- Production Ready Chat Applications
