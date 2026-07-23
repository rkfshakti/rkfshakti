<div align="center">

# Shakti Prasad Mohapatra

### *Intelligence is the new infrastructure. I'm the architect.*

**GenAI & Agentic AI Architect · Open Source Contributor · Data-Driven Builder**

10+ years in IT &nbsp;|&nbsp; MBA, Operations & Supply Chain, Liverpool Business School, UK &nbsp;|&nbsp; India

[![LinkedIn](https://img.shields.io/badge/LinkedIn-Connect-0A66C2?style=flat&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/oneshaktimohapatra)
[![Email](https://img.shields.io/badge/Email-Reach%20Out-D14836?style=flat&logo=gmail&logoColor=white)](mailto:rkfshakti@gmail.com)
[![GitHub Sponsors](https://img.shields.io/badge/Sponsor-Support%20My%20Work-EA4AAA?style=flat&logo=githubsponsors&logoColor=white)](https://github.com/sponsors/rkfshakti)

</div>

---

## Who I Am

I am an architect who lives and breathes data.

Not the kind who draws boxes on whiteboards. The kind who sits with the numbers, finds what they are actually saying, and builds systems that make organisations act on it. Autonomously. At scale. Reliably.

Over 10 years in IT, from business analyst to GenAI architect — always following the data. I've led cross-functional teams across the US and Middle East, engaged C-suite stakeholders on AI strategy, and driven real transformation in financial services (BFSI), consumer goods (CPG), energy (EPG), and healthcare (HLM).

MBA in Operations & Supply Chain at Liverpool Business School, UK — not to step away from technology, but to understand the business problems well enough to solve them with it.

What drives me: the 10-day process that becomes 2 hours. The 3% error rate that drops to under 0.5%. The alert noise cut by 30%. The best AI systems are the ones nobody notices, because they just work.

---

## What I Build

I operate where enterprise complexity meets agentic AI.

```
Multi-Agent Orchestration      LangGraph · LangChain · Temporal · MCP · A2A Protocol
Agentic RAG & Knowledge        Agentic RAG · Text2SQL · Document Intelligence DB
LLM Platform Architecture      AWS Bedrock · Azure OpenAI · Google Vertex AI
Vector Search Infrastructure   Pinecone · FAISS · ChromaDB · Azure AI Search
Real-Time ML Pipelines         Streaming intelligence at production scale
Enterprise AI Governance       Ethical AI · Model Risk Management · Audit Ready Systems
SLM Fine-Tuning               Task-specific small models for enterprise constraints
API-Driven AI Workflows       FastAPI · Microservices · CI/CD · Multi-cloud
Agent Frameworks              Hermes Agent · Pi Agent · CrewAI · AutoGen · Semantic Kernel
```

**Open to freelance, collaboration, and technical co-founder conversations.**

---

## Open Source Contributions

I fix real bugs in production-grade AI infrastructure — the kind that silently corrupt data, break under concurrency, or fail in edge cases that only surface at scale. Every single one is a genuine bug fix — not a typo, not a docs tweak.

| Repo | Stars | Impact |
|------|-------|--------|
| [langgenius/dify](https://github.com/langgenius/dify) | 149K+ | **2 PRs merged** — email validator fix, audio-to-text 400 error. Open: MCP timeout fix, Agent node completion params |
| [chroma-core/chroma](https://github.com/chroma-core/chroma) | 28.8K | 9 PRs — path normalization, fixture registration, NUL byte FTS5 corruption, include-list mutation, dependency cleanup, naming bugs |
| [openai/openai-python](https://github.com/openai/openai-python) | 31.1K | 4 PRs — null output guard, NO_PROXY sanitization, stream drain, list merge by logical index |
| [NousResearch/hermes-agent](https://github.com/NousResearch/hermes-agent) | 217K+ | 3 PRs — cwd-shaped path detection, Telegram caption retry, environment shutdown guard |
| [firecrawl/firecrawl](https://github.com/firecrawl/firecrawl) | 153K+ | 3 PRs — charset detection, ignoreRobotsTxt forwarding, community link fix |
| [mem0ai/mem0](https://github.com/mem0ai/mem0) | — | 2 PRs — ImportError pattern, embedding dim propagation |
| [topoteretes/cognee](https://github.com/topoteretes/cognee) | — | 2 PRs — ACL raw-download for read-grant users, Postgres import guard |
| [QwenLM/qwen-code](https://github.com/QwenLM/qwen-code) | — | 1 PR — npm path resolution with mise/asdf Node version managers |
| [huggingface/smolagents](https://github.com/huggingface/smolagents) | — | 2 PRs — managed-agent summary leak, big-integer timeout bypass |
| [crewAIInc/crewAI](https://github.com/crewAIInc/crewAI) | — | 1 PR — async tools in native tool loop |
| [pydantic/pydantic-ai](https://github.com/pydantic/pydantic-ai) | — | 1 PR — AG-UI round-trip metadata loss |
| [langchain-ai/langchain](https://github.com/langchain-ai/langchain) | 101K+ | 2 PRs — PydanticOutputParser type coercion, OpenAI phased response parsing (auto-closed, no assignment) |
| [agno-agi/agno](https://github.com/agno-agi/agno) | — | 2 PRs — mutable default arguments, team history subteam query (closed, no assignment) |
| [openai/openai-agents-python](https://github.com/openai/openai-agents-python) | — | 1 PR — incomplete tool call stream guard (closed, maintainer wanted repro) |
| [earendil-works/pi](https://github.com/earendil-works/pi) | — | 1 PR — wl-copy exit code + xclip fallback (closed) |

---

## Recent Impact

### ✅ Merged

**Dify — Email validator rejects trailing newlines** — `re.search` matched valid emails even with trailing newlines, causing silent validation bypass. Fix: `re.fullmatch`. → **Merged** ✅ [#39320](https://github.com/langgenius/dify/pull/39320)

**Dify — Audio-to-text returns 400 instead of 500** — Missing file field caused an unhandled server error. Fix: return proper 400 with clear message. → **Merged** ✅ [#39322](https://github.com/langgenius/dify/pull/39322)

### 🟡 Active

**Smolagents — `10 ** 10**8` freezes entire process** — CPython computes arbitrary-precision integers in C while holding the GIL. The thread-based `timeout()` decorator never fires because the worker never reaches a bytecode boundary. After timeout, the leaked thread still holds the GIL, blocking all subsequent executor submissions. Fix: pre-check bit-length before allowing exponentiation. → [#2564](https://github.com/huggingface/smolagents/pull/2564)

**CrewAI — `asyncio.run()` crash in async native tools** — When the async native tool path calls `tool.run()` → `asyncio.run()`, it crashes with `RuntimeError: asyncio.run() cannot be called from a running event loop`. Fix: add async variants that use `asyncio.gather` and `await tool.arun()`. → [#6622](https://github.com/crewAIInc/crewAI/pull/6622)

**Pydantic AI — Metadata loss across AG-UI round-trip** — Seven categories of part-level fields (`id`, `provider_name`, `provider_details`) were silently dropped when messages were round-tripped through `dump_messages()`/`load_messages()`. Fix: extend existing carrier mechanisms to preserve metadata. → [#6682](https://github.com/pydantic/pydantic-ai/pull/6682)

**OpenAI Python — Streamed output lost on null response.completed** — The streaming accumulator never updated the snapshot on done events, so a null `output` field caused silent data loss. Fix: handle all four done event types in `accumulate_event()`. → [#3517](https://github.com/openai/openai-python/pull/3517)

**Chroma — NUL bytes corrupt FTS5 index** — Embedded null bytes in documents bypassed validation and corrupted the SQLite FTS5 index. Fix: reject NUL bytes before storage. → [#7474](https://github.com/chroma-core/chroma/pull/7474)

**Hermes Agent — write_file creates doubled paths** — A cwd-shaped relative path like `home/user/dev/notes/x.md` produced `/home/user/dev/home/user/dev/notes/x.md`. Fix: structural detection in path resolver. → [#67426](https://github.com/NousResearch/hermes-agent/pull/67426)

**Firecrawl — Charset detection in fire-engine** — Responses without UTF-8 charset produced garbled text. Fix: detect charset from Content-Type and HTML meta tags. → [#4088](https://github.com/firecrawl/firecrawl/pull/4088)

**Cognee — ACL read-grant users blocked from downloading raw data** — The endpoint called `get_data(user.id, data_id)` which checks `data.owner_id == user_id`, blocking users with dataset-level read grants. Fix: use the already-verified membership result instead. → [#4200](https://github.com/topoteretes/cognee/pull/4200)

**Qwen Code — npm path resolution fails with mise/asdf** — Node version managers replace `bin/npm` with a bash shim. `fs.realpathSync` succeeds but spawning `node /path/to/bash-wrapper` fails with Syntax Error. Fix: validate resolved path ends with `.js`. → [#7591](https://github.com/QwenLM/qwen-code/pull/7591)

### 🔴 Closed — But the Work Was Real

**LangChain — PydanticOutputParser type coercion** — List-to-str and str-to-list field types in PydanticOutputParser failed silently. Fix: coerce types at parse boundary. → *Auto-closed (no issue assignment)* [#38996](https://github.com/langchain-ai/langchain/pull/38996)

**OpenAI Agents Python — Incomplete tool call stream guard** — Non-buffered Chat Completions stream could emit incomplete tool calls that crashed the parser. Fix: guard against partial tool call payloads. → *Closed (maintainer wanted real-provider repro)* [#3912](https://github.com/openai/openai-agents-python/pull/3912)

**Pi Agent — wl-copy exit code ignored** — The `/copy` command always set `copied=true` after spawning wl-copy without awaiting its exit code. When wl-copy failed, the xclip/OSC 52 fallbacks never ran. Fix: await exit code, fall through on failure. → *Closed (not merged)* [#7009](https://github.com/earendil-works/pi/pull/7009)

---

## GitHub Stats

<div align="center">

[![GitHub Streak](https://streak-stats.demolab.com?user=rkfshakti&hide_border=true&date_format=j%20M%5B%20Y%5D&background=00000000&stroke=6A0DAD&ring=6A0DAD&fire=FF6B35&currStreakLabel=6A0DAD)](https://git.io/streak-stats)

[![GitHub Activity Graph](https://github-readme-activity-graph.vercel.app/graph?username=rkfshakti&theme=minimal&hide_border=true&color=6A0DAD&line=6A0DAD&point=FF6B35&area=true)](https://github.com/ashutosh00710/github-readme-activity-graph)

</div>

---

## Let's Connect

I'm open to architecture challenges, enterprise AI strategy, freelance engagements, or startup ideas in the GenAI space.

If you're building something that matters, let's talk.

[![LinkedIn](https://img.shields.io/badge/LinkedIn-Connect-0A66C2?style=flat&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/oneshaktimohapatra)
[![Email](https://img.shields.io/badge/Email-Reach%20Out-D14836?style=flat&logo=gmail&logoColor=white)](mailto:rkfshakti@gmail.com)
[![GitHub Sponsors](https://img.shields.io/badge/Sponsor-Support%20My%20Work-EA4AAA?style=flat&logo=githubsponsors&logoColor=white)](https://github.com/sponsors/rkfshakti)

---

<div align="center">

*Data first. Always.*

</div>
