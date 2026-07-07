# 07 - System Prompts

> **Volume 01 – Java AI Foundations**

## Learning Objectives

- Understand System Prompts
- System Prompt vs User Prompt
- Prompt hierarchy
- Role-based prompting
- Spring AI usage

---

# What is a System Prompt?

A **System Prompt** is a high-priority instruction that defines how the AI should behave throughout a conversation.

Think of it as the AI's job description.

Example:

```text
You are an expert Java and Spring Boot mentor.
Always answer with production-ready examples.
```

---

# Prompt Hierarchy

```text
System Prompt
      ↓
User Prompt
      ↓
Model Response
```

The model first follows the System Prompt, then the User Prompt.

---

# System Prompt vs User Prompt

| System Prompt | User Prompt |
|---------------|-------------|
| Defines behavior | Asks a question |
| Usually set by developer | Provided by user |
| High priority | Lower priority |

---

# Real-world Examples

## Customer Support Bot

```text
You are a customer support assistant.
Be polite.
Never reveal internal information.
```

## Java Tutor

```text
You are a Java instructor.
Explain concepts step by step.
Use simple language.
```

## SQL Assistant

```text
Generate SQL only.
Do not explain.
```

---

# Why are System Prompts Important?

They help:

- Control AI behavior
- Maintain consistent responses
- Reduce hallucinations
- Enforce formatting
- Improve user experience

---

# Spring AI Example

```java
String system = "You are a Java expert.";

String response = chatClient.prompt()
    .system(system)
    .user("Explain Dependency Injection.")
    .call()
    .content();
```

---

# Best Practices

- Keep instructions clear.
- Define the AI's role.
- Specify output format when needed.
- Avoid conflicting instructions.
- Keep prompts concise.

---

# Common Mistakes

- Writing very long system prompts.
- Giving contradictory instructions.
- Assuming system prompts guarantee perfect security.

---

# Mini Project

Build a Java mentor chatbot.

System Prompt:

```text
You are a senior Java developer.
Answer only Java-related questions.
```

Test with Java and non-Java questions.

---

# Interview Questions

1. What is a System Prompt?
2. How is it different from a User Prompt?
3. Why is it useful?
4. How do you use it in Spring AI?
5. Can a System Prompt improve consistency?

---

# Exercises

1. Write a System Prompt for a travel assistant.
2. Write one for a coding assistant.
3. Compare responses with and without a System Prompt.

---

# Summary

You learned:

- System Prompt basics
- Prompt hierarchy
- Spring AI usage
- Best practices

## Next Chapter

**08-Prompt-Engineering.md**
