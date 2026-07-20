<div align="center">

# Shakti Prasad Mohapatra

### *Intelligence is the new infrastructure. I'm the architect.*

**GenAI & Agentic AI Architect · Strategic AI Leader · Data-Driven Builder**

10+ years in IT &nbsp;|&nbsp; MBA, Operations & Supply Chain, Liverpool Business School, UK &nbsp;|&nbsp; India

[![LinkedIn](https://img.shields.io/badge/LinkedIn-Connect-0A66C2?style=flat&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/oneshaktimohapatra)
[![Email](https://img.shields.io/badge/Email-Reach%20Out-D14836?style=flat&logo=gmail&logoColor=white)](mailto:rkfshakti@gmail.com)

</div>

---

## Who I Am

I am an architect who lives and breathes data.

Not the kind who draws boxes on whiteboards and calls it a day. The kind who sits with the numbers, finds what they are actually saying, and builds systems that make organisations act on it. Autonomously. At scale. Reliably.

Over 10 years in IT, I have moved from business analyst to GenAI architect, always following the data. I have led cross-functional teams, managed delivery across geographies including the United States and Middle East, engaged C-suite stakeholders on AI strategy, and driven real transformation in financial services (BFSI), consumer goods (CPG), energy (EPG), and healthcare (HLM).

I did my MBA in Operations & Supply Chain at Liverpool Business School, UK. Not to step away from technology, but to understand the business problems well enough to solve them with it.

What drives me is not the hype around AI. It is the measurable outcome. The 10 day process that becomes 2 hours. The 3% error rate that drops to under 0.5%. The alert noise that gets cut by 30%. Those numbers are what make this work real.

I believe the best AI systems are the ones nobody notices, because they just work.

---

## What I Build

I operate where enterprise complexity meets agentic AI, designing systems that reason, plan, and act without hand holding.

```
Multi-Agent Orchestration      LangGraph · LangChain · Temporal · MCP · A2A Protocol
Agentic RAG & Knowledge        Agentic RAG · Text2SQL · Document Intelligence DB
LLM Platform Architecture      AWS Bedrock · Azure OpenAI · Google Vertex AI
Vector Search Infrastructure    Pinecone · FAISS · ChromaDB · Azure AI Search · Anova DB
Real-Time ML Pipelines          Streaming intelligence at production scale
Enterprise AI Governance        Ethical AI · Model Risk Management · Audit Ready Systems
SLM Fine-Tuning                 Task specific small models for enterprise constraints
API-Driven AI Workflows         FastAPI · Microservices · CI/CD · Multi-cloud
Agent Frameworks                Hermes Agent · Pi Agent · CrewAI · AutoGen · Semantic Kernel
Embedding & Retrieval           Gemini Embedding 001 · Text Embedding 002 · Page Index
Notification & Queue            AWS SES · Celery · Redis Queue · Kafka
```

**I take on freelance and collaborative projects.**

If you are a company looking to implement GenAI seriously, not a pilot but production, or a founder with a product idea that needs AI architecture, or an investor looking for a technical co builder in the AI space, I am open to the conversation.

---

## Open Source Contributions

I actively contribute to the GenAI and Agentic AI open source ecosystem. My focus is on fixing real bugs in production grade AI infrastructure — the kind that silently corrupt data, break under concurrency, or fail in edge cases that only surface at scale.

| Repo | Stars | What I Fixed |
|------|-------|-------------|
| [chroma-core/chroma](https://github.com/chroma-core/chroma) | 28.8K | PersistentClient path normalization, conftest fixture registration, unused dependency removal, example fixes |
| [NousResearch/hermes-agent](https://github.com/NousResearch/hermes-agent) | 217K+ | write_file path validation for cwd shaped relative paths, Telegram send_document basename fix |
| [langchain-ai/langchain](https://github.com/langchain-ai/langchain) | 142K+ | CancelledError guard, TracerCore copy fix, default_tools mutation, LogStream send return |
| [langgenius/dify](https://github.com/langgenius/dify) | 149K+ | OAuth trigger credentials optional for polling, workflow parallel trace misattribution fix |
| [openai/openai-python](https://github.com/openai/openai-python) | 31.1K | None response.output guard in parse_response, NO_PROXY newline sanitization |
| [firecrawl/firecrawl](https://github.com/firecrawl/firecrawl) | 153K+ | README community link fix, ignoreRobotsTxt forwarding in crawl payload |

---

## Recent Impact

Here is what I have been working on recently — bugs that were subtle, silent, and took real digging to find.

**Workflow trace misattribution in parallel branches** — When a Dify workflow node executed multiple times in parallel branches, the `node_started` and `agent_log` handlers matched trace entries by `node_id` (the definition identifier) instead of the unique execution `id`. Started and finished events for the same execution silently landed on different trace entries. The fix: match by execution id first, fall back to `node_id` only for backward compatibility. Added regression tests that fail on the old code. → [dify #39313](https://github.com/langgenius/dify/pull/39313)

**Streamed output lost when response.completed has null output** — The OpenAI Python SDK silently dropped streamed content when the final `response.completed` event carried a null `output` field. The snapshot never reflected the accumulated stream data. The fix: guard the null-output fallback in the streaming accumulator so the snapshot serializes the real accumulated output. → [openai-python #3517](https://github.com/openai/openai-python/pull/3517)

**Newlines in NO_PROXY env var breaking httpx client init** — The `NO_PROXY` environment variable with newline-separated entries caused httpx to fail during client initialization. The fix: sanitize newlines before passing to httpx. → [openai-python #3519](https://github.com/openai/openai-python/pull/3519)

**TracerCore copy returning self instead of a real copy** — LangChain's `_TracerCore.__copy__` returned `self`, so concurrent chain runs corrupted each other's trace data. The fix: allocate fresh internal dicts on copy. → [langchain #38964](https://github.com/langchain-ai/langchain/pull/38964)

**Telegram send_document silent delivery failure** — Hermes Agent's Telegram integration failed silently when sending documents because the basename was not explicitly passed. The fix: pass explicit basename to the send_document API. → [hermes-agent #68107](https://github.com/NousResearch/hermes-agent/pull/68107)

**ignoreRobotsTxt not forwarded in crawl payload** — Firecrawl's JavaScript SDK ignored the `ignoreRobotsTxt` option when constructing crawl payloads, causing crawls to always respect robots.txt regardless of the setting. → [firecrawl #4087](https://github.com/firecrawl/firecrawl/pull/4087)

---

## How I Approach a Bug Fix

Every bug I fix follows the same discipline:

1. **Understand the full call chain** — not just where the error surfaces, but where the root cause originates. I read at least 50 lines above and below the change site.
2. **Check for similar patterns** — grep the codebase for the same bug pattern elsewhere. If it happened once, it probably happened twice.
3. **Fix the root cause, not the symptom** — adding a null check without understanding *why* the value is null is not a fix.
4. **Add a regression test** — the test must fail on the old code and pass with the fix. This prevents the bug from recurring silently.
5. **Keep the change minimal** — no refactoring, no style changes, no unrelated improvements. The diff should show exactly what needed to change.
6. **Write the PR description like a human** — explain the problem, the root cause, and the fix in natural language. No bullet-point vomit, no robotic phrases.

This is not the fastest way to fix a bug. But it is the only way I trust.

---

## Tech Stack

### AI / GenAI & Orchestration
![LangChain](https://img.shields.io/badge/LangChain-1C3C3C?style=flat&logo=langchain&logoColor=white)
![LangGraph](https://img.shields.io/badge/LangGraph-1C3C3C?style=flat&logo=langchain&logoColor=white)
![LangSmith](https://img.shields.io/badge/LangSmith-1C3C3C?style=flat&logoColor=white)
![CrewAI](https://img.shields.io/badge/CrewAI-FF0000?style=flat&logoColor=white)
![AutoGen](https://img.shields.io/badge/AutoGen-0078D4?style=flat&logo=microsoft&logoColor=white)
![Semantic Kernel](https://img.shields.io/badge/Semantic%20Kernel-5C2D91?style=flat&logo=microsoft&logoColor=white)
![MCP](https://img.shields.io/badge/MCP%20Protocol-6A0DAD?style=flat&logoColor=white)
![A2A](https://img.shields.io/badge/A2A%20Protocol-4285F4?style=flat&logo=google&logoColor=white)
![Temporal](https://img.shields.io/badge/Temporal-000000?style=flat&logoColor=white)
![Hermes Agent](https://img.shields.io/badge/Hermes%20Agent-217K★-6A0DAD?style=flat&logoColor=white)

### LLMs & Model Platforms
![Claude](https://img.shields.io/badge/Claude%20(Anthropic)-D97757?style=flat&logoColor=white)
![OpenAI](https://img.shields.io/badge/OpenAI-412991?style=flat&logo=openai&logoColor=white)
![Gemini](https://img.shields.io/badge/Gemini-8E44AD?style=flat&logo=google&logoColor=white)
![Llama](https://img.shields.io/badge/Llama%203-0467DF?style=flat&logo=meta&logoColor=white)
![Mistral](https://img.shields.io/badge/Mistral%20AI-FF7000?style=flat&logoColor=white)
![Groq](https://img.shields.io/badge/Groq-F54703?style=flat&logoColor=white)
![HuggingFace](https://img.shields.io/badge/HuggingFace-FFD21E?style=flat&logo=huggingface&logoColor=black)
![AWS Bedrock](https://img.shields.io/badge/AWS%20Bedrock-FF9900?style=flat&logo=amazonaws&logoColor=white)
![Azure OpenAI](https://img.shields.io/badge/Azure%20OpenAI-0078D4?style=flat&logo=microsoftazure&logoColor=white)
![Google Vertex AI](https://img.shields.io/badge/Vertex%20AI-4285F4?style=flat&logo=googlecloud&logoColor=white)

### RAG & Knowledge Infrastructure
![LlamaIndex](https://img.shields.io/badge/LlamaIndex-8A2BE2?style=flat&logoColor=white)
![Pinecone](https://img.shields.io/badge/Pinecone-000000?style=flat&logo=pinecone&logoColor=white)
![Weaviate](https://img.shields.io/badge/Weaviate-22B573?style=flat&logoColor=white)
![Qdrant](https://img.shields.io/badge/Qdrant-DC244C?style=flat&logoColor=white)
![FAISS](https://img.shields.io/badge/FAISS-3670A0?style=flat&logo=meta&logoColor=white)
![ChromaDB](https://img.shields.io/badge/ChromaDB-FF6B35?style=flat&logoColor=white)
![Azure AI Search](https://img.shields.io/badge/Azure%20AI%20Search-0078D4?style=flat&logo=microsoftazure&logoColor=white)
![pgvector](https://img.shields.io/badge/pgvector-4169E1?style=flat&logo=postgresql&logoColor=white)

### Embeddings & Retrieval
![Gemini Embedding](https://img.shields.io/badge/Gemini%20Embedding%20001-8E44AD?style=flat&logo=google&logoColor=white)
![Text Embedding 002](https://img.shields.io/badge/Text%20Embedding%20002-4285F4?style=flat&logo=google&logoColor=white)
![Page Index](https://img.shields.io/badge/Page%20Index-FF6B35?style=flat&logoColor=white)
![Document Intelligence DB](https://img.shields.io/badge/Document%20Intelligence%20DB-6A0DAD?style=flat&logoColor=white)

### Notification & Queue Infrastructure
![AWS SES](https://img.shields.io/badge/AWS%20SES-FF9900?style=flat&logo=amazonaws&logoColor=white)
![Redis](https://img.shields.io/badge/Redis-DC382D?style=flat&logo=redis&logoColor=white)
![Kafka](https://img.shields.io/badge/Kafka-231F20?style=flat&logo=apachekafka&logoColor=white)
![Celery](https://img.shields.io/badge/Celery-37814A?style=flat&logo=celery&logoColor=white)

### Languages & Frameworks
![Python](https://img.shields.io/badge/Python-3776AB?style=flat&logo=python&logoColor=white)
![FastAPI](https://img.shields.io/badge/FastAPI-005571?style=flat&logo=fastapi&logoColor=white)
![SQL](https://img.shields.io/badge/SQL-4479A1?style=flat&logo=postgresql&logoColor=white)
![REST APIs](https://img.shields.io/badge/REST%20APIs-FF6C37?style=flat&logo=postman&logoColor=white)

### Cloud & Infrastructure
![AWS](https://img.shields.io/badge/AWS-FF9900?style=flat&logo=amazonaws&logoColor=white)
![Azure](https://img.shields.io/badge/Azure-0078D4?style=flat&logo=microsoftazure&logoColor=white)
![GCP](https://img.shields.io/badge/GCP-4285F4?style=flat&logo=googlecloud&logoColor=white)
![Docker](https://img.shields.io/badge/Docker-2496ED?style=flat&logo=docker&logoColor=white)
![Kubernetes](https://img.shields.io/badge/Kubernetes-326CE5?style=flat&logo=kubernetes&logoColor=white)

### AI Dev Tools & Observability
![Cursor](https://img.shields.io/badge/Cursor-000000?style=flat&logoColor=white)
![GitHub Copilot](https://img.shields.io/badge/GitHub%20Copilot-000000?style=flat&logo=github&logoColor=white)
![Weights & Biases](https://img.shields.io/badge/W%26B-FFBE00?style=flat&logo=weightsandbiases&logoColor=black)
![MLflow](https://img.shields.io/badge/MLflow-0194E2?style=flat&logo=mlflow&logoColor=white)

### Analytics & Delivery
![Power BI](https://img.shields.io/badge/Power%20BI-F2C811?style=flat&logo=powerbi&logoColor=black)
![Advanced Excel](https://img.shields.io/badge/Advanced%20Excel-217346?style=flat&logo=microsoftexcel&logoColor=white)
![Git](https://img.shields.io/badge/Git-F05032?style=flat&logo=git&logoColor=white)
![JIRA](https://img.shields.io/badge/JIRA-0052CC?style=flat&logo=jira&logoColor=white)
![Confluence](https://img.shields.io/badge/Confluence-172B4D?style=flat&logo=confluence&logoColor=white)

---

## GitHub Stats

<div align="center">

![GitHub Streak](https://streak-stats.demolab.com?user=rkfshakti&hide_border=true&date_format=j%20M%5B%20Y%5D&background=00000000&stroke=6A0DAD&ring=6A0DAD&fire=FF6B35&currStreakLabel=6A0DAD)

![GitHub Activity Graph](https://github-readme-activity-graph.vercel.app/graph?username=rkfshakti&theme=minimal&hide_border=true&color=6A0DAD&line=6A0DAD&point=FF6B35&area=true)

</div>

---

## Let's Connect

I am open to talking about **architecture challenges, enterprise AI strategy, freelance engagements, or startup ideas** in the GenAI space.

If you are building something that matters, let's talk.

[![LinkedIn](https://img.shields.io/badge/LinkedIn-Shakti%20Prasad%20Mohapatra-0A66C2?style=flat&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/oneshaktimohapatra)
[![Email](https://img.shields.io/badge/Email-Get%20in%20touch-D14836?style=flat&logo=gmail&logoColor=white)](mailto:rkfshakti@gmail.com)

---

<div align="center">
<sub>Data first. Always.</sub>
</div>
