---
type: "week"
week: 46
phase: "Phase 6 — Reliability, Agents, Scale Simulation & Your Specialization"
status: "not-started"
start: 
end: 
objective: "MCP: building & operating servers — transports, OAuth 2.1, discovery, progressive tool discovery."
concepts: ["[[MCP]]"]
project: ["[[Level 7 — Production-grade AI platform]]"]
deliverable: 
tags: ["week", "phase/6"]
---

# Week 46 — MCP — building & operating servers

**Phase:** [[Phase 6 — Reliability, Agents, Scale Simulation & Your Specialization]]  
**Objective:** MCP: building & operating servers — transports, OAuth 2.1, discovery, progressive tool discovery.  
**Concepts:** [[MCP]]
**Project:** [[Level 7 — Production-grade AI platform]]

> [!info] How to use this week
> Timebox the four blocks (~60 min/day total). **Learn** builds the model, **Read** grounds it in reality, **Build** makes it real, **Reflect** locks it in. The **Step-by-step** expands the Build; the **Done when** list is your exit criteria.

## Learn (20m)
MCP spec + 2026 roadmap; the official SDK docs.

## Read (15m)
An MCP security writeup (known design pitfalls, the OWASP-LLM-adjacent risks).

## Build (20m)
Build and deploy an MCP server (wrap an internal API/tool); connect it to a client; add auth.

## Step-by-step
1. Read the MCP spec + the official SDK docs.
2. Build an MCP server that wraps one internal API/tool; expose a couple of tools/resources.
3. Connect a client (e.g. Claude or an SDK client) and call the tools.
4. Add OAuth 2.1 auth and test progressive/scoped tool discovery.
5. Threat-model the server: injection via tool results, over-broad scopes, context bloat.

## Reflect (5m)
> What are the security and context-bloat risks of exposing tools via MCP, and how does progressive discovery help?

## Done when
- [ ] A working, authenticated MCP server connected to a client.
- [ ] Progressive tool discovery demonstrated.
- [ ] A short threat model of your server.

## Common pitfalls
- Tool results flow into the model's context — a compromised tool is a prompt-injection vector.
- Dumping every tool into context bloats it and degrades the model; scope discovery.

## Resources
- [[MCP Specification & 2026 Roadmap]]
- [[modelcontextprotocol]]
- [[OWASP LLM Top 10]]

## Go deeper
- MCP spec + 2026 roadmap; the official SDK docs.
- An MCP security writeup (OWASP-LLM-adjacent risks).

## Tasks
- [ ] Study/open [[MCP Specification & 2026 Roadmap]]
- [ ] Study/open [[modelcontextprotocol]]
- [ ] Study/open [[OWASP LLM Top 10]]
- [ ] **Build:** Build and deploy an MCP server (wrap an internal API/tool); connect it to a client; add auth.
- [ ] A working, authenticated MCP server connected to a client.
- [ ] Progressive tool discovery demonstrated.
- [ ] A short threat model of your server.
- [ ] **Reflect:** answer the week's question in the learning log

## Notes
