# 🚀 Phase-02 Spring AI Basics

> Learn Spring AI from scratch in simple Hinglish.

---

# 📖 Table of Contents

1. Spring AI Introduction
2. Why Spring AI?
3. Architecture
4. Features
5. Requirements
6. Project Setup
7. AI Providers
8. ChatModel
9. ChatClient
10. Prompt
11. PromptTemplate
12. Advisors
13. Memory
14. Streaming
15. Structured Output
16. Best Practices
17. Interview Questions
18. MCQs
19. Assignment

---

# 1. What is Spring AI?

Spring AI ek Spring ecosystem project hai jo Java developers ko AI applications banane me help karta hai.

Ye different AI providers ko ek common API ke through access karne deta hai.

Supported Providers

- OpenAI
- Gemini
- Ollama
- Azure OpenAI
- Anthropic Claude
- AWS Bedrock
- Mistral

Simple Flow

```
User

↓

Spring Boot

↓

Spring AI

↓

LLM

↓

Response
```

---

# 2. Why Spring AI?

Problems Without Spring AI

- Har AI Provider ki API alag
- Different Authentication
- Different Request Format
- Different Response Format

Spring AI

↓

Ek Common Interface

↓

Provider Change karo

↓

Business Code Same

---

Benefits

- Less Boilerplate
- Provider Independent
- Easy Integration
- Spring Boot Friendly
- Production Ready

---

# 3. Spring AI Architecture

```
Client

↓

Controller

↓

Service

↓

ChatClient

↓

ChatModel

↓

AI Provider

↓

LLM

↓

Response
```

---

# 4. Core Modules

Spring AI mainly ye modules provide karta hai.

### ChatClient

AI ko request bhejne ke liye.

### ChatModel

LLM ke sath communication.

### EmbeddingModel

Embeddings generate karta hai.

### VectorStore

Embeddings store karta hai.

### PromptTemplate

Dynamic Prompt banata hai.

### Advisors

Memory aur Logging add karta hai.

### Tool Calling

Java Methods ko AI ke liye expose karta hai.

---

# 5. Requirements

- Java 21+
- Spring Boot 3.5+
- Maven
- IntelliJ IDEA
- Git
- API Key (OpenAI/Gemini)
- Ollama (Optional)

---

# 6. Project Setup

## Dependencies

```
Spring Web

Spring AI

Lombok
```

For OpenAI

```
spring-ai-starter-model-openai
```

For Gemini

```
spring-ai-starter-model-vertex-ai-gemini
```

For Ollama

```
spring-ai-starter-model-ollama
```

---

application.yml

```yaml
spring:
  ai:
    openai:
      api-key: YOUR_API_KEY
```

---

# 7. AI Providers

## OpenAI

Best for production.

## Gemini

Google LLM.

## Ollama

Run LLM locally.

## Claude

Strong reasoning.

## Azure OpenAI

Enterprise Cloud.

## AWS Bedrock

Multiple AI Models.

---

# 8. ChatModel

ChatModel actual AI model represent karta hai.

Example

```
OpenAiChatModel

GeminiChatModel

OllamaChatModel
```

Ye provider ke according implementation change karta hai.

Business Logic same rehta hai.

---

# 9. ChatClient

Spring AI ka sabse important component.

Example

```java
String response = chatClient
        .prompt("Explain Spring Boot")
        .call()
        .content();
```

Flow

```
Prompt

↓

ChatClient

↓

ChatModel

↓

LLM

↓

Response
```

---

Methods

```
prompt()

call()

stream()

content()
```

---

# 10. Prompt

Prompt matlab AI ko diya gaya instruction.

Bad Prompt

```
Explain Java.
```

Good Prompt

```
Explain Java OOP in Hinglish with interview examples.
```

Prompt Types

- System Prompt
- User Prompt
- Assistant Prompt

---

# 11. PromptTemplate

Dynamic Prompt banane ke liye use hota hai.

Example

```
Hello {name}
```

Input

```
Sachin
```

Output

```
Hello Sachin
```

Benefits

- Reusable
- Dynamic
- Clean Code

---

# 12. Advisors

Advisors request aur response ke beech extra processing karte hain.

Use Cases

- Logging
- Memory
- Security
- Monitoring

Flow

```
Request

↓

Advisor

↓

LLM

↓

Advisor

↓

Response
```

---

# 13. Chat Memory

Memory previous conversation ko remember karti hai.

Without Memory

```
Hi

↓

What's my name?

↓

AI doesn't know.
```

With Memory

```
My name is Sachin.

↓

What's my name?

↓

Sachin
```

Types

- InMemory
- Window Memory
- Persistent Memory

Benefits

- Better Conversations
- Better Context
- Personalized Chat

---

# 14. Streaming

Normally

```
Wait

↓

Complete Response
```

Streaming

```
H

He

Hel

Hello
```

Benefits

- Faster UX
- Real-Time Response
- Better User Experience

Methods

```
stream()

Flux<String>
```
