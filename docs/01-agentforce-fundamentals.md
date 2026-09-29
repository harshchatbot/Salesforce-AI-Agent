# Agentforce Fundamentals

This document contains concepts learned while building the HealthAssist
Healthcare AI Agent using Salesforce Agentforce.

---

## Agentic Reasoning vs Deterministic Execution

Large Language Models (LLMs) are probabilistic, while many enterprise
business operations must behave deterministically.

In HealthAssist:

- Agentforce understands the user's intent and conversation.
- The agent reasons about which capability/action should be used.
- Flow or Apex performs deterministic business operations.
- Salesforce security controls what data and operations are accessible.
- External integrations are exposed through controlled actions.

A useful mental model is:

User Request
    ↓
Agent understands intent
    ↓
Agent selects appropriate action
    ↓
Flow / Apex executes business logic
    ↓
Salesforce / External System
    ↓
Result returned to Agent
    ↓
Agent formulates response

### Key Principle

> Let the agent reason about **what needs to happen**.
> Let deterministic application logic control **how critical operations happen**.

---

## AI Governance

AI governance is broader than simply securing the LLM.

A production AI agent should consider:

- Identity
- Authentication
- Authorization
- Least-privilege access
- Data privacy
- PII/PHI protection
- Prompt injection
- Grounding
- Hallucination management
- Permitted actions
- External API security
- Auditability
- Monitoring
- Human escalation

These concerns will be implemented and tested throughout the HealthAssist project.