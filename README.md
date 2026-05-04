# Hi, I'm Chandra Mohan Busam 👋

**AI Engineer | Full Stack Engineer**
St. Louis, MO &nbsp;|&nbsp; +1 636-233-2009 &nbsp;|&nbsp; chandramohan.net@gmail.com

[![LinkedIn](https://img.shields.io/badge/LinkedIn-chandramohanbusam-0077B5?style=flat&logo=linkedin)](https://www.linkedin.com/in/chandramohanbusam/)
[![Email](https://img.shields.io/badge/Email-chandramohan.net%40gmail.com-D14836?style=flat&logo=gmail)](mailto:chandramohan.net@gmail.com)
![Open to Work](https://img.shields.io/badge/Open%20to%20Work-AI%20Engineer%20%7C%20Senior%20Software%20Engineer-16a34a?style=flat)

---

## About Me

I build production AI systems: LangChain agents, MCP servers, RAG pipelines, and GPT-4o integrations that solve real operational problems. Currently at Tiber Health Innovation, where every AI project here either runs in production or is directly derived from production work.

20+ years of backend and infrastructure depth (.NET/C#, AWS, distributed systems, healthcare SaaS) gives me the foundation to ship AI systems that are reliable, cost-aware, and maintainable, not just demos.

---

## Featured AI Projects

### AI Deployment Agent
> Reduced a 14-step manual deployment process from 20-30 minutes to a single natural language command completing in under 2 minutes.

A production-grade AI deployment agent with a 3-layer hybrid architecture. Accepts natural language deploy commands from both a Slack slash command and a Claude MCP interface. Both interfaces share the same underlying LangChain ReAct agent that orchestrates deployment across multiple Linux servers via SSH.

**Stack:** LangChain, FastMCP, GPT-4o, FastAPI, Slack Bolt, Paramiko, Azure DevOps, Azure Blob Storage, Python

**Key design decisions:**
- 3-layer version resolution: Python regex (free), GPT-4o NLP (1-2 cents), LangChain execution (3-8 cents)
- Dual interface: Slack for team use, Claude MCP for personal conversational deployment
- Config-driven human-in-the-loop: confirmation gates controlled by JSON policy, not hardcoded
- 6 MCP tools: resolve version, deploy, check status, deployment history, email notification

[![View Repo](https://img.shields.io/badge/View-Repository-1a2744?style=flat&logo=github)](https://github.com/ChandraMohanBusam/ai-deployment-agent)

---

### MCP Queue Monitor
> 9 tools, 9 prompts, zero SQL. Job queue ops via plain English from Claude Desktop.

A local MCP server that connects directly to Claude Desktop over stdio transport, giving the entire team conversational access to MySQL job queue data without writing a single query. Built because the team was context-switching constantly just to check queue statuses.

**Stack:** FastMCP, stdio transport, MySQL, Claude Desktop, Python

**Key design decisions:**
- 9 MCP tools covering queue depth, job status, error rates, and retry counts
- 9 prompt templates for common workflows including morning queue briefing and error triage
- stdio transport for zero-config local Claude Desktop integration
- Prompt layer designed so non-technical teammates get useful answers instantly

[![View Repo](https://img.shields.io/badge/View-Repository-1a2744?style=flat&logo=github)](https://github.com/ChandraMohanBusam/mcp-queue-monitor)

---

### MCP Notification Server
> Event-driven notification dispatch via HTTP/SSE transport with LangGraph orchestration.

An MCP notification server that uses HTTP/SSE transport for real-time event streaming. LangGraph manages the notification workflow as a stateful graph, enabling reliable multi-step dispatch with state inspection and replay via get_state_history().

**Stack:** FastMCP, HTTP/SSE, LangChain, LangGraph, Python

[![View Repo](https://img.shields.io/badge/View-Repository-1a2744?style=flat&logo=github)](https://github.com/ChandraMohanBusam/mcp-notification-server)

---

### MdTutor.ai (Dr. Olivia) -- Tiber Health Innovation
> AI-powered virtual tutor for PHSU medical students.

Built the data pipeline and RAG infrastructure for an AI medical tutor. Scraped and vectorized medical textbooks from ClinicalKey and LWW Health Library into Pinecone using Playwright. Chunked content with careful attention to context boundaries, generated OpenAI embeddings, and stored vectors in Pinecone for semantic retrieval. Vectorized Kaltura video SRT files for video content search. Frontend chat (text and audio) delivered via Tavus.io.

**Stack:** Python, Playwright, Pinecone, OpenAI Embeddings, RAG pipeline, Tavus.io, Kaltura

---

### SaaS Central Analyzr -- Tiber Health Innovation
> Multi-partner SaaS analytics platform for medical schools.

Built the full analytics platform including USMLE gap analysis, PEV scores, pass prediction, and video engagement tracking. Implemented CQRS pattern for dashboard data reads, TExAS/TPV queue processing, and bell curve/gauge visualizations.

**Stack:** Blazor WASM, C# Web APIs, MySQL, Entity Framework, Redis, Azure Repos, Oracle Queue, Python, AnyChart

---

## Technical Skills

| Category | Skills |
|---|---|
| AI / ML | LangChain, LangGraph, FastMCP, GPT-4o, OpenAI API, Prompt Engineering, RAG Pipelines, Pinecone, AI Agents, LLM Integration |
| Languages | Python, C#, .NET Core, JavaScript, Node.js, SQL |
| Frontend | React, Angular, Blazor WASM |
| Infrastructure | Azure DevOps, Azure Blob Storage, AWS (Lambda, S3), SSH/Paramiko, Docker, CI/CD |
| Backend | FastAPI, REST APIs, Node.js APIs, CQRS, Entity Framework, Redis, MySQL, SQL Server |
| Automation | Python Automation, Playwright, Azure DevOps Pipelines |
| Protocols | MCP (Model Context Protocol), HTTP/SSE, stdio transport, Slack Bolt, Microsoft Teams Webhooks |

---

## Currently

- Building AI agents and MCP integrations at Tiber Health Innovation
- Expanding RAG pipeline expertise: chunking strategies, OpenAI embeddings, Pinecone vector search, and retrieval optimization
- Exploring Agent-to-Agent (A2A) protocol for multi-agent coordination
- Targeting **AI Engineer** and **Senior Software Engineer** roles
- Open to remote and hybrid opportunities, H-1B transfer supported

---

## Get in Touch

I am actively looking for AI Engineer and Senior Software Engineer roles where I can apply production AI engineering experience. If you are building something interesting with LLMs, agents, or AI automation, I would love to connect.

📧 chandramohan.net@gmail.com
📞 +1 636-233-2009
🔗 [linkedin.com/in/chandramohanbusam](https://www.linkedin.com/in/chandramohanbusam/)
