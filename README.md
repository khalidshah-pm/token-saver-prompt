# 🪨 Token Saver Prompt — Caveman Language for AI

> Cut enterprise AI token usage by up to 70% with a single 12-word prompt.

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
[![Works With](https://img.shields.io/badge/Works%20With-Claude%20%7C%20GPT--4%20%7C%20Gemini-blue)]()

---

## The Prompt

```
Respond in caveman language. Only necessary words. No filler. Just the answer.
```

Paste at the start of any conversation — or add to your system prompt for always-on savings.

---

## The Problem

LLMs are trained to sound helpful and polite. That costs tokens.

**Every response starts with something like:**
> *"Great question! I'd be happy to help you understand how this works. Let me break it down for you..."*

That's ~25 tokens. Zero value. Multiply by millions of API calls and it becomes a serious budget line.

---

## Real Dollar Impact

Based on average 200-token output per call, published API pricing, and 70% token reduction:

| Model | 1M calls/month (before) | 1M calls/month (after) | Monthly Saving | Annual Saving |
|---|---|---|---|---|
| **GPT-4o** | ~$2,000 | ~$600 | **$1,400** | **$16,800** |
| **Claude Sonnet** | ~$3,000 | ~$900 | **$2,100** | **$25,200** |
| **Azure OpenAI** | ~$2,200 | ~$660 | **$1,540** | **$18,500** |

> Scale to 10M calls/month? Add a zero.

---

## Before vs After

**Default AI:**
```
User: What is RAG?

AI: Great question! RAG, which stands for Retrieval-Augmented Generation, is a 
technique used in modern AI systems that combines the power of large language 
models with external knowledge retrieval. Essentially, instead of relying solely 
on what the model learned during training, RAG allows the system to...
[~120 tokens]
```

**Caveman Mode:**
```
User: What is RAG?

AI: RAG = Retrieval-Augmented Generation. AI fetches external docs, adds to 
prompt, answers with real data. Beats hallucination.
[~35 tokens]
```

**Same answer. 70% fewer tokens.**

---

## Where It Works Best

| Use Case | Why It Helps |
|---|---|
| Internal AI assistants & copilots | High call volume, repetitive queries |
| Document processing pipelines | Automated — no human reading the fluff anyway |
| Customer-facing chatbots | Faster response + lower cost |
| Dev tools & code assistants | Devs want answers, not essays |
| RAG pipelines | Reduces noise in retrieved + generated content |

---

## Compatibility

| Model | Tested | Notes |
|---|---|---|
| Claude Sonnet / Opus | ✅ | Works excellently |
| GPT-4o | ✅ | Strong compliance |
| GPT-3.5 Turbo | ✅ | Good, occasional verbosity |
| Gemini Pro | ✅ | Works well |
| Llama 3 | ⚠️ | Partial — fine-tuned models vary |

---

## How to Use

**Single conversation:**
Paste the prompt at the start of your chat.

**System prompt (recommended for production):**
```python
system_prompt = """
Respond in caveman language. Only necessary words. No filler. Just the answer.
"""
```

**LangChain / LlamaIndex:**
```python
from langchain.prompts import SystemMessagePromptTemplate

system = SystemMessagePromptTemplate.from_template(
    "Respond in caveman language. Only necessary words. No filler. Just the answer."
)
```

---

## Limitations

- Not suitable for customer-facing responses requiring empathy or tone (support, HR)
- Responses may feel abrupt for non-technical end users
- Creative writing tasks should skip this prompt

---

## Contributing

Found a better formulation? Tested on a new model? Open a PR or raise an issue.

---

## License

MIT — free to use, modify, and deploy.

---

*Built by a PM who got tired of paying for AI small talk.*

**If this saved you money, star the repo ⭐**
