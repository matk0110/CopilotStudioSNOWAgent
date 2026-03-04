
# ServiceNow Conversational Agent Demo

## Purpose

This repository demonstrates how to build a **value‑driven conversational ServiceNow agent** using **Copilot Studio**.  

The agent design helps to demo responses to common questions like:
- Can it connect to real external systems?
- How hard is it to build and maintain?
- Is general knowledge actually viable and safe?
- Are the connectors production‑ready?

The agent focuses on **helping users**, not forcing them to navigate knowledge bases or ticketing systems


## 🎯 When to Use This Demo
- IT Service Desk modernization conversations
- Copilot Studio + ServiceNow integration discussions
- Deflection, AHT, or ticket quality improvement use cases

- 
## 📽️ Demo Walkthrough

A short video walkthrough explains the agent behavior and design decisions.

- **Video**: *(internal Copilot Studio + ServiceNow agent demo)*

The walkthrough shows how a small set of well‑chosen capabilities can address **~80% of common IT service desk interactions**.

[![Watch the demo](assets/demo-thumbnail.png)](https://livesend.microsoft.com/i/s9RfdNAynwk6NZ___S8ndeSs1qRVrkj8CbBc5IgpvNi61lXmP8yJVjvMUr6jtyKTpSIR2HmPqspWsGK8RNj5OkbFTYL3apndt6nJPLUSSIGNGyD9Kacr2TFN9gK13mB56UINAJIym)



## ⭐ Business Value (Start Here)

### 1. External System Connectivity (Real Integration)

This demo showcases **true external system connectivity**, not a closed chatbot.

- Uses **ServiceNow connectors** to:
  - Create incidents
  - Retrieve user‑specific tickets
  - Interact with the system of record

**Why this matters**  
Copilot Studio acts as an **orchestration layer**, coordinating actions across systems instead of acting as a thin UI on top of ServiceNow.

---

### 2. Simplicity of Capture (Time to Value)

The agent is built with:

- Minimal instructions
- No complex prompt engineering
- No custom middleware or glue code

**Why this matters**  
Teams can move from idea to working agent **quickly**, without specialized AI skills or heavy maintenance overhead.

---

### 3. General Knowledge Viability (Safe AI Adoption)

Knowledge usage is intentionally constrained:

- Connected only to **approved ServiceNow knowledge articles**
- Used strictly for factual lookup and troubleshooting
- Not relied on as the sole resolution mechanism

**Why this matters**  
Demonstrates safe, compliant AI adoption without exposing the full ServiceNow instance or creating security risk.

---

### 4. Connector Viability (Enterprise Readiness)

The demo highlights **production‑relevant connectors**:

- Incident creation
- Ticket retrieval by user context

Clear separation between:
- **Knowledge** (read‑only, informational)
- **Tools** (action‑oriented, auditable)

**Why this matters**  
Builds confidence that the solution scales beyond demos into real environments.


## 🤖 Agent Design Philosophy

### Conversational First

- No visible instructions to the user
- Agent explains options naturally
- Reduces cognitive friction throughout the interaction

---

### Minimal Instruction Strategy

- Short, focused agent instructions
- Avoids large, brittle prompt blocks
- Leverages Copilot Studio orchestration instead of custom logic

---

### Persona & Engagement

- Demo uses a light **Elvis‑style persona**
- Shows how tone and personality improve engagement
- Persona is optional and easily replaced


# ⚠️ Disclaimer

This repository contains **demonstration / sample code** intended for
educational and illustrative purposes only.

- ❌ Not production-ready
- ❌ No security hardening
- ❌ No SLA or support commitment

Use at your own risk. The authors assume no responsibility for use of this
code in production environments.

# CopilotStudioSNOWAgent
Accelerator for Copilot Studio ServiceNow Agent


# ⚠️ Disclaimer

This repository contains **demonstration / sample code** intended for
educational and illustrative purposes only.

- ❌ Not production-ready
- ❌ No security hardening
- ❌ No SLA or support commitment

Use at your own risk. The authors assume no responsibility for use of this
code in production environments.


## Prerequisites

A Power Platform Environment with permissions to create connections and import solutions

**The target environment must have a dataverse data store**
This will be needed to import the solution as well as store the indexed knowledge articles.

A ServiceNow dev instance with read right access to knowledge and incidents records (steps in guide on how to provision a demo space)

Before importing this solution, ensure the following managed solution is installed in the target Power Platform environment.

| Requirement | Value |
|------------|-------|
| Managed Solution Name | AI Solution default templates |
| Unique Name | msdyn_AISolutionDefaultTemplates |
| Minimum Version | ${AI_SOLUTION_DEFAULT_TEMPLATES_VERSION} |

> ⚠️ **Important**  
> Import will fail if this managed solution is not present in the environment.


### Version Parameters

```text
AI_SOLUTION_DEFAULT_TEMPLATES_VERSION=202601.2.6.1

> ✅ **Deployment Note**
> The `AI Solution default templates` managed solution is automatically available in environments where Copilot Studio is enabled.  
> If importing into a restricted or newly provisioned environment, verify that Copilot Studio has been initialized before importing this solution.
``
