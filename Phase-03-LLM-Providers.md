# 🚀 Phase-03 LLM Providers

> Spring AI Mastery

## Contents
1. What is an LLM Provider?
2. OpenAI
3. Gemini
4. Ollama
5. Claude
6. Azure OpenAI
7. AWS Bedrock
8. Mistral & DeepSeek
9. Provider Comparison
10. Spring AI Configuration
11. Best Practices
12. Interview Questions
13. MCQs
14. Summary

---

# 1. LLM Provider

LLM Provider wo company hoti hai jo AI models API ke through provide karti hai.

Flow

User → Spring AI → Provider → LLM → Response

---

# 2. OpenAI

Models: GPT family

Pros
- High quality
- Tool Calling
- Structured Output
- Strong coding

Cons
- Paid API
- Internet required

Use Cases
- Chatbots
- Code Assistant
- RAG
- Enterprise Apps

---

# 3. Gemini

Google ka LLM.

Pros
- Multimodal
- Strong reasoning
- Google ecosystem

Cons
- Rate limits (plan dependent)

Use Cases
- Vision
- Chat
- Search

---

# 4. Ollama

Local LLM runner.

Pros
- Free
- Offline
- Privacy

Cons
- High RAM
- Slower than cloud on low-end systems

Popular Models
- Llama
- Mistral
- Gemma
- DeepSeek

Install

```bash
ollama run llama3
```

---

# 5. Claude

Anthropic ka model.

Pros
- Long context
- Great writing
- Good reasoning

Use Cases
- Documentation
- Analysis

---

# 6. Azure OpenAI

Enterprise OpenAI.

Pros
- Azure Security
- Compliance
- Enterprise Ready

---

# 7. AWS Bedrock

Ek API se multiple foundation models access.

Supports:
- Claude
- Llama
- Mistral
- Amazon Nova (availability depends)

Best for AWS ecosystem.

---

# 8. Mistral & DeepSeek

## Mistral
- Fast
- Efficient
- Open models

## DeepSeek
- Strong coding
- Cost effective
- Good reasoning

---

# 9. Provider Comparison

| Provider | Best For |
|-----------|----------|
| OpenAI | Coding, General AI |
| Gemini | Multimodal |
| Ollama | Local Development |
| Claude | Writing & Analysis |
| Azure OpenAI | Enterprise |
| Bedrock | AWS Apps |
| Mistral | Open Source |
| DeepSeek | Coding |

---

# 10. Spring AI Configuration

Dependency

```xml
spring-ai-starter-model-openai
```

application.yml

```yaml
spring:
  ai:
    openai:
      api-key: YOUR_KEY
```

Provider change karne ke liye dependency aur config update karo.

---

# 11. Best Practices

- API keys env variables me rakho.
- Dev ke liye Ollama use karo.
- Production me monitoring enable karo.
- Retry & timeout configure karo.
- Cost optimize karo.

---

# 12. Interview Questions

1. LLM Provider kya hai?
2. OpenAI vs Gemini?
3. Ollama kab use karoge?
4. Azure OpenAI kyu?
5. Bedrock kya hai?
6. Claude kis liye famous hai?
7. Local vs Cloud models?
8. Spring AI provider kaise switch karta hai?

---

# 13. MCQs

Q1. Local AI ke liye best?

A OpenAI
B Ollama ✅
C Azure
D Bedrock

Q2. Enterprise Microsoft option?

A Gemini
B Azure OpenAI ✅
C Ollama
D Mistral

Q3. Google Provider?

A Claude
B Gemini ✅
C Llama
D Nova

---

# 14. Summary

- Provider = AI service company
- OpenAI = General purpose
- Gemini = Google multimodal
- Ollama = Local AI
- Claude = Writing & reasoning
- Azure = Enterprise
- Bedrock = AWS ecosystem
- Spring AI provider-independent abstraction deta hai.

Next: Phase-04-Prompt-Engineering.md
