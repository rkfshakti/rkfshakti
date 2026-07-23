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

Over 10 years in IT, from business analyst to GenAI architect — always following the data. I have led cross-functional teams across the US and Middle East, engaged C-suite stakeholders on AI strategy, and driven real transformation in financial services (BFSI), consumer goods (CPG), energy (EPG), and healthcare (HLM).

MBA in Operations & Supply Chain at Liverpool Business School, UK — not to step away from technology, but to understand the business problems well enough to solve them with it.

What drives me: the 10-day process that becomes 2 hours. The 3% error rate that drops to under 0.5%. The alert noise cut by 30%. The best AI systems are the ones nobody notices, because they just work.

---

## What I Build

I operate where enterprise complexity meets agentic AI.



**Open to freelance, collaboration, and technical co-founder conversations.**

---

## Open Source Contributions

I fix real bugs in production-grade AI infrastructure — the kind that silently corrupt data, break under concurrency, or fail in edge cases that only surface at scale.

| Repo | Stars | Impact |
|------|-------|--------|
| [langgenius/dify](https://github.com/langgenius/dify) | 149K+ | **2 PRs merged** — email validator fix, audio-to-text 400 error. Open: MCP timeout fix, Agent node completion params |
| [chroma-core/chroma](https://github.com/chroma-core/chroma) | 28.8K | 8 PRs — path normalization, fixture registration, NUL byte validation, dependency cleanup |
| [openai/openai-python](https://github.com/openai/openai-python) | 31.1K | 4 PRs — null output guard, NO_PROXY sanitization, stream drain, list merge fix |
| [NousResearch/hermes-agent](https://github.com/NousResearch/hermes-agent) | 217K+ | 3 PRs — cwd-shaped path detection, Telegram send_document, environment shutdown guard |
| [firecrawl/firecrawl](https://github.com/firecrawl/firecrawl) | 153K+ | 3 PRs — charset detection, ignoreRobotsTxt forwarding, community link fix |
| [mem0ai/mem0](https://github.com/mem0ai/mem0) | — | 2 PRs — ImportError pattern, embedding dim propagation |

---

## Recent Impact

**Dify — Email validator rejects trailing newlines** — `re.search` matched valid emails even with trailing newlines. Fix: `re.fullmatch`. → **Merged** ✅ [#39320](https://github.com/langgenius/dify/pull/39320)

**Dify — Audio-to-text returns 400 instead of 500** — Missing file field caused unhandled server error. Fix: return proper 400. → **Merged** ✅ [#39322](https://github.com/langgenius/dify/pull/39322)

**OpenAI Python — Streamed output lost on null response.completed** — Snapshot never updated on done events. Fix: handle all four done event types in accumulator. → [#3517](https://github.com/openai/openai-python/pull/3517)

**Chroma — NUL bytes corrupt FTS5 index** — Embedded null bytes bypassed validation. Fix: reject NUL bytes before storage. → [#7474](https://github.com/chroma-core/chroma/pull/7474)

**Hermes Agent — write_file creates doubled paths** — Cwd-shaped relative path produced doubled path. Fix: structural detection in path resolver. → [#67426](https://github.com/NousResearch/hermes-agent/pull/67426)

**Firecrawl — Charset detection in fire-engine** — Non-UTF-8 responses produced garbled text. Fix: detect charset from Content-Type and HTML meta tags. → [#4088](https://github.com/firecrawl/firecrawl/pull/4088)

---

## Let's Connect

I am open to architecture challenges, enterprise AI strategy, freelance engagements, or startup ideas in the GenAI space.

If you are building something that matters, let us talk.

[![LinkedIn](https://img.shields.io/badge/LinkedIn-Connect-0A66C2?style=flat&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/oneshaktimohapatra)
[![Email](https://img.shields.io/badge/Email-Reach%20Out-D14836?style=flat&logo=gmail&logoColor=white)](mailto:rkfshakti@gmail.com)
[![GitHub Sponsors](https://img.shields.io/badge/Sponsor-Support%20My%20Work-EA4AAA?style=flat&logo=githubsponsors&logoColor=white)](https://github.com/sponsors/rkfshakti)

---

<div align="center">

*Data first. Always.*

</div>
