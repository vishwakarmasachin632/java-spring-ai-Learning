---

# 15. Structured Output

Normally AI String return karta hai.

```
"What is Java?"
        ↓
Long Text
```

Lekin enterprise applications me hume JSON ya Java Object chahiye.

Spring AI Structured Output support karta hai.

Example

```
User

↓

LLM

↓

JSON

↓

Java Object
```

Benefits

- Easy Parsing
- Type Safety
- Clean Code
- API Friendly

---

# 16. EmbeddingModel

EmbeddingModel text ko vectors me convert karta hai.

Flow

```
Document

↓

EmbeddingModel

↓

Vector

↓

VectorStore
```

Use Cases

- Semantic Search
- RAG
- Recommendation
- Similarity Search

---

# 17. VectorStore

Embeddings ko store karne ke liye use hota hai.

Supported Stores

- PGVector
- Chroma
- Pinecone
- Milvus
- Redis
- Elasticsearch

Flow

```
Text

↓

Embedding

↓

VectorStore

↓

Similarity Search
```

---

# 18. Tool Calling

Spring AI Java methods ko AI ke tools bana sakta hai.

Flow

```
User

↓

LLM

↓

Tool

↓

Java Method

↓

Result
```

Example Use Cases

- Weather API
- Payment API
- Email Service
- Database Query
- Calculator
- Flight Booking

Benefits

- AI real-world actions perform kar sakta hai.
- External APIs integrate kar sakte hain.

---

# 19. Error Handling

Common Errors

### Invalid API Key

```
401 Unauthorized
```

Solution

- Check API Key
- Verify Provider

---

### Rate Limit

```
429 Too Many Requests
```

Solution

- Retry
- Backoff Strategy

---

### Timeout

```
Request Timeout
```

Solution

- Increase Timeout
- Retry

---

### Model Not Found

```
404 Model Not Found
```

Solution

- Check Model Name
- Check Provider

---

# 20. Best Practices

## Project

- Layered Architecture
- Service Layer
- Configuration Class
- Environment Variables

---

## Prompt

- Small Prompt
- Clear Context
- Expected Output
- Proper Formatting

---

## Security

- Never hardcode API Keys
- Use Environment Variables
- Validate User Input

---

## Performance

- Cache Responses
- Use Streaming
- Reduce Token Usage
- Optimize Prompt Size

---

## Production

- Logging
- Monitoring
- Retry
- Exception Handling
- Rate Limiting

---

# 21. Mini Project

## AI Chat Application

Features

- Chat Interface
- Multiple Providers
- Conversation Memory
- Streaming Response
- Markdown Support

Architecture

```
User

↓

Controller

↓

Service

↓

ChatClient

↓

ChatModel

↓

LLM

↓

Response
```

Future Enhancements

- PDF Chat
- Image Generation
- Voice Chat
- RAG
- Tool Calling

---

# 22. Common Mistakes

❌ Hardcoding API Keys

❌ Long Prompts

❌ Ignoring Token Usage

❌ No Exception Handling

❌ No Logging

❌ Using High Temperature for Coding

❌ No Input Validation

---

# 23. Interview Questions

## Beginner

1. What is Spring AI?
2. Why Spring AI?
3. ChatClient kya hai?
4. ChatModel kya hai?
5. Prompt kya hota hai?
6. PromptTemplate kya hai?
7. Memory kya hoti hai?
8. Streaming kya hai?

---

## Intermediate

9. ChatClient vs ChatModel
10. EmbeddingModel kya karta hai?
11. VectorStore kya hai?
12. Tool Calling explain karo.
13. Structured Output kya hai?
14. Advisors kya hote hain?

---

## Advanced

15. Spring AI Architecture explain karo.
16. Multiple AI Providers kaise switch karte hain?
17. Production Best Practices?
18. Streaming kaise implement hoti hai?
19. Chat Memory kaise work karti hai?
20. Enterprise AI Architecture explain karo.

---

# 24. MCQs

### Q1

Spring AI kis framework ka part hai?

A. Django

B. Spring Ecosystem

C. Laravel

D. Express

✅ Answer: **B**

---

### Q2

AI ko request bhejne ke liye kaunsa component use hota hai?

A. ChatClient

B. EntityManager

C. JdbcTemplate

D. DispatcherServlet

✅ Answer: **A**

---

### Q3

Dynamic Prompt banane ke liye?

A. PromptTemplate

B. BeanFactory

C. RestTemplate

D. JdbcTemplate

✅ Answer: **A**

---

### Q4

Conversation History kis component se manage hoti hai?

A. Chat Memory

B. Controller

C. Repository

D. Maven

✅ Answer: **A**

---

### Q5

Embeddings kahan store hote hain?

A. MySQL Table

B. VectorStore

C. HTML

D. Browser

✅ Answer: **B**

---

### Q6

Real-time response ke liye kya use hota hai?

A. Streaming

B. Thread.sleep()

C. JSP

D. JDBC

✅ Answer: **A**

---

# 25. Assignment

## Beginner

- Spring AI project create karo.
- OpenAI ya Gemini integrate karo.
- First AI response print karo.

---

## Intermediate

Build

- AI Chat Application
- PromptTemplate use karo.
- Chat Memory add karo.

---

## Advanced

Build

- Streaming Chatbot
- Multi Provider Support
- Structured Output
- Tool Calling
- Logging

---

# 26. Summary

Is phase me humne seekha:

- Spring AI Introduction
- Spring AI Architecture
- Project Setup
- ChatClient
- ChatModel
- Prompt
- PromptTemplate
- Advisors
- Chat Memory
- Streaming
- Structured Output
- EmbeddingModel
- VectorStore
- Tool Calling
- Error Handling
- Best Practices

---

# 🎯 Key Takeaways

✅ Spring AI Java developers ke liye AI development ko easy banata hai.

✅ ChatClient sabse commonly use hone wala component hai.

✅ ChatModel provider-specific implementation deta hai.

✅ Prompt Engineering response quality improve karti hai.

✅ PromptTemplate reusable prompts banata hai.

✅ Memory better conversations provide karti hai.

✅ Streaming real-time user experience improve karti hai.

✅ Embeddings + VectorStore RAG ki foundation hain.

✅ Tool Calling AI ko external APIs aur Java methods execute karne deta hai.

---

# 🚀 Next Phase

## **Phase-03-LLM-Providers.md**

Hum detail me seekhenge:

- OpenAI
- Gemini
- Ollama
- Claude
- Azure OpenAI
- AWS Bedrock
- DeepSeek
- Mistral
- Provider Selection
- Cost Comparison
- Performance Comparison
- Spring AI Configuration

🎉 **Congratulations!** Ab tum Spring AI ke core concepts samajh chuke ho aur actual enterprise AI applications banana start kar sakte ho.
