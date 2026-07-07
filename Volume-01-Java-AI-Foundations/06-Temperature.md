# 06 - Temperature

> **Volume 01 – Java AI Foundations**

## Learning Objectives

After this chapter you will understand:

- What Temperature is
- Why it matters
- Low vs High Temperature
- Real-world use cases
- Temperature in Spring AI

---

# What is Temperature?

Temperature is a model setting that controls **how random or creative** the AI's responses are.

It does **not** change the model's knowledge. It changes **how the model chooses the next token**.

---

# Temperature Range

Typical values:

| Temperature | Behavior |
|-------------|----------|
| 0.0 | Very deterministic |
| 0.2 | Accurate & consistent |
| 0.5 | Balanced |
| 0.7 | Creative |
| 1.0+ | Highly creative, less predictable |

---

# Low Temperature (0.0 - 0.2)

Use when you need:

- Code generation
- SQL generation
- API documentation
- Technical explanations

Example Prompt:

```
Write a Java method to reverse a string.
```

The response is usually consistent every time.

---

# Medium Temperature (0.5 - 0.7)

Use for:

- General chat
- Customer support
- Educational assistants
- Email drafting

Produces balanced responses.

---

# High Temperature (0.8 - 1.2)

Use for:

- Story writing
- Brainstorming
- Marketing ideas
- Creative content

The same prompt may produce different answers each time.

---

# Visual Idea

```text
Low Temperature
      ↓
More Predictable

Medium
      ↓
Balanced

High
      ↓
More Creative
```

---

# Real-world Examples

| Application | Recommended Temperature |
|-------------|------------------------:|
| Coding Assistant | 0.1 - 0.2 |
| SQL Generator | 0.0 |
| Resume Analyzer | 0.2 |
| Chatbot | 0.5 |
| Email Writer | 0.6 |
| Story Generator | 0.9 |

---

# Temperature in Spring AI

Example configuration:

```yaml
spring:
  ai:
    ollama:
      chat:
        options:
          model: llama3
          temperature: 0.2
```

You can also configure temperature programmatically depending on the provider and API.

---

# Best Practices

- Use low temperature for deterministic business tasks.
- Increase temperature only when creativity is valuable.
- Test different values for your use case.
- Keep production settings consistent.

---

# Common Mistakes

- Using high temperature for SQL generation.
- Assuming higher temperature means smarter AI.
- Using one value for every application.

---

# Mini Project

Create two chatbot endpoints:

- `/creative` → higher temperature
- `/technical` → lower temperature

Compare the responses.

---

# Interview Questions

1. What is Temperature?
2. Does Temperature change model knowledge?
3. Which temperature is suitable for code generation?
4. Which temperature is suitable for creative writing?
5. Why is temperature important?

---

# Exercises

1. Test the same prompt with 0.1, 0.5 and 0.9.
2. Compare the outputs.
3. Decide the best value for a customer support bot.

---

# Summary

You learned:

- What Temperature is
- Low vs High Temperature
- Production use cases
- Spring AI configuration
- Best practices

## Next Chapter

**07-System-Prompts.md**
