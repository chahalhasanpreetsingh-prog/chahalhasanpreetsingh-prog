## Hasanpreet Singh Chahal

I build and run production systems end to end, Linux and Docker infrastructure, Python/FastAPI
backends, AI and MCP integrations, and shipped mobile apps. Most of what's here is
infrastructure I actually operate, not demos.

**AI agents in production**: custom MCP servers, and scheduled LLM automation that runs
unattended against real infrastructure. Scoped tool allow-lists instead of disabled permission
checks, cooldowns and locks so a failure cannot loop, and verification outside the agent so
"it said it fixed it" is never the success condition. RAG over large document sets with pgvector
and Qdrant.

**Infrastructure**: 22 production services across multiple hosts with no inbound ports open (Tailscale +
Cloudflare Tunnel). Migrated the lot to a new host with zero downtime and no data loss, including
recovering corrupted Postgres and Redis state. Traced a process leak that took host load from 6.4
to 0.67.

**Backend**: Python, FastAPI, PostgreSQL (incl. pgvector), Redis, Celery. I care about the boring
parts: per-user data isolation, signed expiring URLs, constant-time secret checks, race conditions
on quota limits, migrations that don't lose data.

**Mobile**: Flutter app shipped solo to TestFlight and Android, with a FastAPI backend and
in-app subscriptions.

**Debugging is what I'm best at.** A production TLS failure that turned out to be a socket-level
clash with Cloudflare; network-wide DNS outages caused by a service quietly filling the router's
NAT table. If it works locally but not in production, that's the work I want.

---

### Selected work

| | |
|---|---|
| **[dump-case-study](https://github.com/chahalhasanpreetsingh-prog/dump-case-study)** | Flutter + FastAPI knowledge app: share anything in, get a structured, searchable note back |
| **[nexus-ui](https://github.com/chahalhasanpreetsingh-prog/nexus-ui)** | Next.js operations dashboard for a multi-host platform, with a browser terminal |
| **[semantic-search](https://github.com/chahalhasanpreetsingh-prog/semantic-search)** | Spotlight-style semantic search across disks, documents and media |
| **[linkedin-operator](https://github.com/chahalhasanpreetsingh-prog/linkedin-operator)** | Scheduled AI posting driven through an MCP server |
| **[self-healing-watchdogs](https://github.com/chahalhasanpreetsingh-prog/self-healing-watchdogs)** | Check → fix → escalate to an AI agent with a fixed tool allow-list |
| **[ai-agent-ops](https://github.com/chahalhasanpreetsingh-prog/ai-agent-ops)** | How I let agents touch production: allow-lists, cooldowns, cost control, verification |
| **[windows-node-agent](https://github.com/chahalhasanpreetsingh-prog/windows-node-agent)** | Token-authenticated agent making a headless Windows box controllable from Linux |
| **[self-hosted-platform](https://github.com/chahalhasanpreetsingh-prog/self-hosted-platform)** | The platform behind most of the above, and the incidents that shaped it |

Open-source contribution: `create_post` / `like_post` write tools for
[linkedin-mcp-server](https://github.com/stickerdaniel/linkedin-mcp-server).

Available for freelance work, 
[Upwork](https://www.upwork.com/freelancers/~0186e73905e9132382)
