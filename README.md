# Hi, I'm Chandra Mohan Busam 👋

**Senior Software Engineer | AI Engineer**
St. Louis, MO &nbsp;|&nbsp; +1 636-233-2009 &nbsp;|&nbsp; chandramohan.net@gmail.com

[![LinkedIn](https://img.shields.io/badge/LinkedIn-chandramohanbusam-0077B5?style=flat&logo=linkedin)](https://www.linkedin.com/in/chandramohanbusam/)
[![Email](https://img.shields.io/badge/Email-chandramohan.net%40gmail.com-D14836?style=flat&logo=gmail)](mailto:chandramohan.net@gmail.com)
![Open to Work](https://img.shields.io/badge/Open%20to%20Work-AI%20Engineer%20Roles-16a34a?style=flat)

---

🕐 **Current time in St. Louis, MO:** Wednesday, April 29, 2026 at 07:00 PM CDT

---

## About Me

20+ years of production engineering experience in healthcare SaaS, now building AI agents and MCP servers in production. I bring deep backend and infrastructure experience (.NET/C#, Azure, distributed systems) combined with hands-on AI engineering: LangChain agents, MCP servers, GPT-4o integration, RAG pipelines, and Python automation.

I build AI systems that solve real operational problems, not demos. Every project here either runs in production or is directly derived from production work.

---

## Featured Projects

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

### MdTutor.ai (Dr. Olivia) -- TiberHealth Innovation
> AI-powered virtual tutor for PHSU medical students.

Built the data pipeline and RAG infrastructure for an AI medical tutor. Scraped and vectorized medical textbooks from ClinicalKey and LWW Health Library into Pinecone using Playwright. Vectorized Kaltura video SRT files for video content search. Frontend chat (text and audio) delivered via Tavus.io.

**Stack:** Python, Playwright, Pinecone, RAG pipeline, Tavus.io, Kaltura

---

### SaaS Central Analyzr -- TiberHealth Innovation
> Multi-partner SaaS analytics platform for medical schools.

Built the full analytics platform including USMLE gap analysis, PEV scores, pass prediction, and video engagement tracking. Implemented CQRS pattern for dashboard data reads, TExAS/TPV queue processing, and bell curve/gauge visualizations.

**Stack:** Blazor WASM, C# Web APIs, MySQL, Entity Framework, Redis, Azure Repos, Oracle Queue, Python, AnyChart

---

## Technical Skills

| Category | Skills |
|---|---|
| AI / ML | LangChain, LangGraph, FastMCP, GPT-4o, OpenAI API, Prompt Engineering, RAG Pipelines, Pinecone, AI Agents, LLM Integration |
| Languages | Python, C#, .NET Core, SQL |
| Infrastructure | Azure DevOps, Azure Blob Storage, SSH/Paramiko, Docker, CI/CD |
| Backend | FastAPI, REST APIs, CQRS, Entity Framework, Redis, MySQL |
| Automation | Python Automation, Playwright, Azure DevOps Pipelines |
| Protocols | MCP (Model Context Protocol), Slack Bolt, Microsoft Teams Webhooks |

---

## Currently

- Building AI agents and MCP integrations at TiberHealth Innovation
- Targeting **AI Engineer** and **Senior Software Engineer** roles
- Open to remote and hybrid opportunities

---

## Get in Touch

I am actively looking for AI Engineer roles where I can apply production AI engineering experience. If you are building something interesting with LLMs, agents, or AI automation, I would love to connect.

📧 chandramohan.net@gmail.com
📞 +1 636-233-2009
🔗 [linkedin.com/in/chandramohanbusam](https://www.linkedin.com/in/chandramohanbusam/)
