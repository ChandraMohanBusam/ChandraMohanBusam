# Hi, I'm Chandra Mohan Busam 👋

**Principal Full Stack Engineer | AI Engineer**

St. Louis, MO &nbsp;|&nbsp; +1 636-233-2009 &nbsp;|&nbsp; chandramohan.net@gmail.com

[![LinkedIn](https://img.shields.io/badge/LinkedIn-chandramohanbusam-0077B5?style=flat&logo=linkedin)](https://www.linkedin.com/in/chandramohanbusam/)
[![Email](https://img.shields.io/badge/Email-chandramohan.net%40gmail.com-D14836?style=flat&logo=gmail)](mailto:chandramohan.net@gmail.com)
![Open to Work](https://img.shields.io/badge/Open%20to%20Work-AI%20Engineer%20%7C%20Senior%2FLead%20Full%20Stack%20Engineer-16a34a?style=flat)

---

## About Me

I build production AI systems: LangChain agents, MCP servers, LangGraph orchestrators, RAG pipelines, and GPT-4o integrations that solve real operational problems. Every AI project here either runs in production or is directly derived from production work.

20+ years of backend and infrastructure depth in .NET/C#, Azure, AWS, distributed systems, and healthcare SaaS gives me the foundation to ship AI systems that are reliable, cost-aware, and maintainable, not just demos.

---

## 🛠️ Tech Stack

### AI and LLM
![LangChain](https://img.shields.io/badge/LangChain-1C3C3C?style=flat&logo=langchain&logoColor=white)
![LangGraph](https://img.shields.io/badge/LangGraph-1C3C3C?style=flat&logo=langchain&logoColor=white)
![FastMCP](https://img.shields.io/badge/FastMCP-5B2D8E?style=flat&logoColor=white)
![OpenAI](https://img.shields.io/badge/OpenAI-412991?style=flat&logo=openai&logoColor=white)
![GPT-4o](https://img.shields.io/badge/GPT--4o-412991?style=flat&logo=openai&logoColor=white)
![RAG](https://img.shields.io/badge/RAG-FF6B35?style=flat&logoColor=white)
![Pinecone](https://img.shields.io/badge/Pinecone-000000?style=flat&logoColor=white)
![Claude Desktop](https://img.shields.io/badge/Claude_Desktop-CC785C?style=flat&logoColor=white)

### Languages and Frameworks
![Python](https://img.shields.io/badge/Python-3776AB?style=flat&logo=python&logoColor=white)
![C#](https://img.shields.io/badge/C%23-239120?style=flat&logo=csharp&logoColor=white)
![.NET Core](https://img.shields.io/badge/.NET_Core-512BD4?style=flat&logo=dotnet&logoColor=white)
![Blazor](https://img.shields.io/badge/Blazor_WASM-512BD4?style=flat&logo=blazor&logoColor=white)
![React](https://img.shields.io/badge/React-61DAFB?style=flat&logo=react&logoColor=black)
![Angular](https://img.shields.io/badge/Angular-DD0031?style=flat&logo=angular&logoColor=white)

### Cloud and Infrastructure
![Azure](https://img.shields.io/badge/Azure-0078D4?style=flat&logo=microsoftazure&logoColor=white)
![AWS](https://img.shields.io/badge/AWS-232F3E?style=flat&logo=amazonwebservices&logoColor=white)
![Docker](https://img.shields.io/badge/Docker-2496ED?style=flat&logo=docker&logoColor=white)
![Redis](https://img.shields.io/badge/Redis-DC382D?style=flat&logo=redis&logoColor=white)
![MySQL](https://img.shields.io/badge/MySQL-4479A1?style=flat&logo=mysql&logoColor=white)
![SQL Server](https://img.shields.io/badge/SQL_Server-CC2927?style=flat&logo=microsoftsqlserver&logoColor=white)

### DevOps and Tools
![Azure DevOps](https://img.shields.io/badge/Azure_DevOps-0078D4?style=flat&logo=azuredevops&logoColor=white)
![Paramiko](https://img.shields.io/badge/Paramiko-3776AB?style=flat&logo=python&logoColor=white)
![Playwright](https://img.shields.io/badge/Playwright-2EAD33?style=flat&logo=playwright&logoColor=white)
![GitHub](https://img.shields.io/badge/GitHub-181717?style=flat&logo=github&logoColor=white)

---

## 🚀 AI Project Portfolio

---

### 🔗 [mcp-composition-demo](https://github.com/ChandraMohanBusam/mcp-composition-demo)
> Four specialized MCP servers composed into one deployment pipeline using LangGraph orchestration.

FastMCP mount pattern with config-driven notification routing, Redis session memory, health checks, auto-rollback, structured JSON logging, Bearer token auth, Docker, and pytest test suite. Includes ADAPTING.md for swapping simulations with real infrastructure and full distributed port mode for production scaling.

**Key design decisions:**
- LangGraph enforces guaranteed node execution order: config, deploy, health check, audit, notify
- Redis session_id as coordination key across all four servers and all log files
- Conditional edges route to rollback node automatically on health check failure
- Single config file controls notification routing per outcome with zero code changes

**Stack:** FastMCP | LangGraph | Redis | Python | Docker | pytest

[![View Repo](https://img.shields.io/badge/View-Repository-1a2744?style=flat&logo=github)](https://github.com/ChandraMohanBusam/mcp-composition-demo)

---

### 🔗 [langchain-debug-demo](https://github.com/ChandraMohanBusam/langchain-debug-demo)
> Debug and log LangChain ReAct agents and LangGraph state machines without paid observability tools.

Three debugging levels for LangChain (verbose, FileCallbackHandler, custom callback stack with loop detection and Slack alerts), four LangGraph tools (stream_mode, get_state, Time Travel, LangGraph Studio), and config-driven alerting.

**Key design decisions:**
- LoopDetectionHandler fires on the third identical tool call, not after max_iterations exhausts
- on_llm_error vs on_chain_error: individual failure vs full chain failure, not the same alert
- LangGraph Time Travel: replay from any checkpoint without restarting from scratch

**Stack:** LangChain | LangGraph | BaseCallbackHandler | Python | LangGraph Studio

[![View Repo](https://img.shields.io/badge/View-Repository-1a2744?style=flat&logo=github)](https://github.com/ChandraMohanBusam/langchain-debug-demo)

---

### 🔗 [ai-deployment-agent](https://github.com/ChandraMohanBusam/ai-deployment-agent)
> Reduced a 14-step manual deployment process from 20-30 minutes to a single natural language command completing in under 2 minutes.

A production-grade AI deployment agent accepting natural language commands from both a Slack slash command and a Claude MCP interface. Both interfaces share the same LangChain ReAct agent orchestrating deployment across multiple Linux servers via SSH.

**Key design decisions:**
- 3-layer version resolution: Python regex (free), GPT-4o NLP (1-2 cents), LangChain execution (3-8 cents)
- Dual interface: Slack for team use, Claude MCP for conversational deployment
- Config-driven human-in-the-loop: confirmation gates controlled by agent_config.json, not hardcoded
- Azure DevOps REST API integration for natural language build resolution

**Stack:** LangChain | FastMCP | GPT-4o | Paramiko | Azure DevOps | Slack | Python

[![View Repo](https://img.shields.io/badge/View-Repository-1a2744?style=flat&logo=github)](https://github.com/ChandraMohanBusam/ai-deployment-agent)

---

### 🔗 [mcp-notification-server](https://github.com/ChandraMohanBusam/mcp-notification-server)
> Shared MCP notification service consumed by multiple LangChain and LangGraph agents.

HTTP/SSE transport for real-time event streaming. Designed as a shared service in an MCP composition architecture where multiple agents consume one notification server.

**Stack:** FastMCP | HTTP/SSE | LangChain | LangGraph | Slack | Teams | Python

[![View Repo](https://img.shields.io/badge/View-Repository-1a2744?style=flat&logo=github)](https://github.com/ChandraMohanBusam/mcp-notification-server)

---

### 🔗 [mcp-queue-monitor](https://github.com/ChandraMohanBusam/mcp-queue-monitor)
> 9 tools, 9 prompts, zero SQL. Workflow queue monitoring via plain English from Claude Desktop.

A local stdio MCP server connecting directly to Claude Desktop, giving conversational access to MySQL job queue data without writing a single query. Replaced 10 to 15 minutes of daily manual SQL queries with a single prompt click.

**Key design decisions:**
- 9 MCP tools covering queue depth, job status, error rates, and retry counts
- 9 prompt templates for common workflows including morning queue briefing and error triage
- stdio transport for zero-config local Claude Desktop integration
- MCP Prompts as a first-class primitive alongside Tools, not just Tools alone

**Stack:** FastMCP | stdio | MySQL | Claude Desktop | Python

[![View Repo](https://img.shields.io/badge/View-Repository-1a2744?style=flat&logo=github)](https://github.com/ChandraMohanBusam/mcp-queue-monitor)

---

## 🎓 EdTech Projects

### MdTutor.ai RAG Pipeline
> AI-powered virtual tutor for medical school students built for a healthcare education platform.

Built the data pipeline and RAG infrastructure. Scraped and vectorized medical textbooks from ClinicalKey and LWW Health Library into Pinecone using Playwright. Chunked content with careful attention to context boundaries, generated OpenAI embeddings, and stored vectors in Pinecone for semantic retrieval. Vectorized Kaltura video SRT files for video content search.

**Stack:** Python | Playwright | Pinecone | OpenAI Embeddings | RAG | Tavus.io | Kaltura

---

### SaaS Central Analyzr
> Multi-partner SaaS analytics platform serving medical school programs across multiple institutions.

Built the full analytics platform including USMLE gap analysis, PEV scores, pass prediction, and video engagement tracking. Implemented CQRS pattern for dashboard data reads, workflow queue processing, and bell curve visualizations.

**Stack:** Blazor WASM | C# | .NET Web APIs | Entity Framework | MySQL | Redis | Azure | Oracle Queue | Python | AnyChart

---

## 📝 Writing About What I Build

I document real problems I solve, not tutorials. Recent LinkedIn posts:

- **MCP Composition Pattern** - Four servers, one LangGraph orchestrator, Redis coordination
- **LangChain vs LangGraph** - Practical comparison from someone who has used both in production
- **Debugging LangChain Agents** - Three levels: verbose, FileCallbackHandler, custom callbacks
- **MCP Queue Monitor** - How I stopped opening a database client every morning
- **AI Deployment Agent** - Replacing a 14-step deployment with a single natural language command

[Follow on LinkedIn](https://linkedin.com/in/chandramohanbusam) for new posts as projects ship.

---

## 💼 Background

- **20+ years** in .NET/C# and healthcare domain software
- **Recent focus:** AI Engineering, MCP servers, LangChain/LangGraph, production observability
- **Certifications:** SAFe 4 Agilist | Microsoft Certified Professional Web Apps C# .NET
- **Education:** M.Sc Information Systems (Sri Krishnadevaraya University) | Bachelor of Computer Applications (BCA) (S.V. University)

---

## Currently

- Expanding RAG pipeline expertise: chunking strategies, OpenAI embeddings, Pinecone, retrieval optimization
- Exploring Agent-to-Agent (A2A) protocol for multi-agent coordination
- Targeting **AI Engineer**, **Senior Software Engineer**, and **Lead Software Engineer** roles
- Open to remote and hybrid opportunities
- H-1B transfer required

---

## 📬 Get in Touch

I am actively looking for AI Engineer and Senior/Lead Software Engineer roles where I can apply production AI engineering experience. If you are building something interesting with LLMs, agents, or AI automation, I would love to connect.

[![LinkedIn](https://img.shields.io/badge/LinkedIn-0A66C2?style=flat&logo=linkedin&logoColor=white)](https://linkedin.com/in/chandramohanbusam)
[![Email](https://img.shields.io/badge/Email-EA4335?style=flat&logo=gmail&logoColor=white)](mailto:chandramohan.net@gmail.com)

📞 +1 636-233-2009

> **Visa:** H-1B active. Requires employer-sponsored H-1B transfer. Not available for C2C or independent contracting.
