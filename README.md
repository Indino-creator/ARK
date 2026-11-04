# ARK
### Personal Agentic AI Assistant — Project Blueprint

> ARK is a long-term personal AI engineering project intended to combine agentic AI, large language models, machine learning, memory, voice interaction, task automation, and smart-home orchestration.

**Project name:** ARK  
**Full form:** To be finalized  
**Status:** Planning / pre-coding  
**Version:** 0.1 — Documentation baseline

## Vision

ARK aims to become a modular personal assistant that can understand natural-language requests, retrieve relevant context, plan multi-step tasks, use approved tools, verify outcomes, and communicate what it did.

The goal is not merely to build a chatbot. ARK is envisioned as a system that combines reasoning, integrations, memory, and carefully permissioned task execution.

## Planned capabilities

- Natural-language text and voice interaction
- Context and user-approved memory
- Task planning and tool calling
- Task scheduling and background processing
- Smart-home orchestration through a platform such as Home Assistant
- Document search and Retrieval-Augmented Generation (RAG)
- Machine-learning predictions and analysis
- Activity history, verification, and user notifications
- Secure access from authorized devices

These are planned capabilities, not claims that they are already implemented.

## Proposed architecture

```text
Phone / Laptop / Voice
          |
   Secure Interface
          |
    FastAPI Backend
          |
  Agent Orchestrator
   |      |       |
  LLM   Memory  Planner
          |
 Permission & Safety Checks
          |
   Task Execution Engine
      |      |      |
 Smart Home  APIs   ML Services
          |
 Result Verification
          |
 Activity Logs / User Response
```

See [`docs/architecture.md`](docs/architecture.md) for the detailed proposed design.

## Planned technology stack

| Area | Candidate technologies |
|---|---|
| Language | Python |
| Backend | FastAPI, Pydantic |
| Database | PostgreSQL, SQLAlchemy |
| AI agents | LLM APIs, structured tool calling, LangGraph or custom orchestration |
| RAG / embeddings | pgvector or FAISS, embedding models |
| Data science | NumPy, Pandas, Matplotlib |
| Machine learning | Scikit-learn, PyTorch |
| Smart home | Home Assistant, MQTT |
| Voice | Whisper or equivalent STT; Piper or equivalent TTS |
| Frontend | React |
| Deployment | Docker, Docker Compose, Linux later |
| Secure remote access | VPN-based solution such as Tailscale |

Choices may change based on implementation needs and learning.

## Documentation

- [`docs/project-vision.md`](docs/project-vision.md) — project purpose, scope, principles
- [`docs/architecture.md`](docs/architecture.md) — proposed system design
- [`docs/requirements.md`](docs/requirements.md) — functional and non-functional requirements
- [`docs/roadmap.md`](docs/roadmap.md) — staged learning and development roadmap
- [`docs/phase-1-checklist.md`](docs/phase-1-checklist.md) — Phase 1 task tracker

## Development roadmap at a glance

| Phase | Focus |
|---|---|
| 0 | Planning and foundations |
| 1 | Backend and database |
| 2 | Smart-home simulation |
| 3 | Agentic AI brain |
| 4 | Memory and RAG |
| 5 | Smart-home integration |
| 6 | Voice interface |
| 7 | Task scheduler and background execution |
| 8 | Server deployment |
| 9 | Machine learning and deep learning |
| 10 | Evaluation, hardening, and portfolio |

See [`docs/roadmap.md`](docs/roadmap.md) for details. Timeline is flexible; academic priorities come first.

## Safety and security

ARK should operate with bounded permissions and clear user control.

- Enforce permissions in application code, not solely through an LLM prompt.
- Require human approval for consequential operations.
- Begin smart-home work with a simulation and low-risk actions.
- Avoid unrestricted control of locks, security systems, or hazardous appliances.
- Validate inputs and protect credentials.
- Keep useful audit logs while minimizing sensitive data collection.
- Verify action outcomes and fail safely when outcomes are uncertain.

## Current status

**Planning and documentation only.** Implementation has not started. The architecture and requirements are preliminary and will be revised as the project develops.

## Long-term goal

Build a reliable, extensible personal AI assistant that brings together agentic workflows, ML capabilities, contextual memory, voice, and approved smart-home automation.

**ARK — A personal AI system built step by step.**
