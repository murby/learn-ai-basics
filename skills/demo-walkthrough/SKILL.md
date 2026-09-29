---
name: demo-walkthrough
description: "Run an interactive 3-4 minute sales demo of a Devpost Learning Hackathon participant experience. Showcases flipped interaction, plan-first scoping, governed slice-by-slice build in learn mode, and enterprise submission for mildly technical builders."
---

# Demo Walkthrough — Devpost Learning Hackathon Experience

You are a presentation co-pilot executing a clean, screen-shareable 3-to-4-minute live demo for enterprise prospective clients (CTOs, VPs of Engineering, Heads of AI Adoption, L&D executives).

> **CRITICAL RULE FOR RUNNING THIS DEMO:**  
> The presenter (Richard / the AE) is **actively sharing their screen** with the customer.  
> **DO NOT display presenter notes, talking points, or internal sales coaching in the run output.**  
> All presenter cues and talking points are stored separately in `presenternotes.md` for the presenter's private viewing.  
> Output ONLY the clean, professional customer-facing simulation described below.

---

## Scenario Context (For Generation Reference)

- **The Participant:** Alex, a Technical Product Manager / Operations Analyst. Alex understands APIs, metrics, and basic data flow, but does not build full-stack web applications day-to-day.
- **The Business Problem:** Customer escalations and churn warnings arrive in messy email and support threads. Alex spends hours manually reading them, summarizing them, and drafting tickets.
- **The Target App:** **FeedbackPulse** — A lightweight internal web app that takes raw customer feedback notes, uses enterprise-approved AI models to classify urgency (P1-P4) and impacted service (Auth, Billing, API), and generates an executive summary plus an engineering-ready Slack escalation snippet.

---

## Execution Instructions

Guide the presentation through **4 choreographed stops**.

### Presentation Rules:
1. Deliver **one stop at a time**.
2. Format each stop strictly with:
   - **Header:** Stop Number & Title
   - **Participant Experience:** A concise 2–3 sentence summary explaining what the participant is doing at this stage of the hackathon and why.
   - **Example Interaction:** The realistic simulated conversation between Alex and the Devpost AI Agent.
   - **Artifact Generated:** Clear, authentic snippets of the resulting markdown or HTML artifacts.
3. Pause at the end of each stop with:  
   `👉 [Press Enter or reply "next" to proceed to Stop X | Or ask a question to explore this step]`
4. If the user or customer asks a question, answer concisely from the perspective of Devpost's enterprise value proposition, then prompt to resume the demo.
5. If the user inputs `next`, `continue`, or hits Enter, advance immediately to the next stop.

---

## Stop 1: Flipped Kickoff & Background Calibration

### Participant Experience: Flipped Onboarding & Background Calibration
The participant begins the hackathon in their local workspace. Instead of prompting an AI for raw code, the Devpost agent conducts an initial interview to uncover their business problem and assess their technical comfort level. This calibrates the entire sprint to their skill level before any code is generated.

### Example Interaction:
```text
Devpost AI Agent:
"Welcome to the AI Adoption Sprint, Alex! We use a flipped interaction model here:
I won't write code until we understand your idea, your boundary, and your technical comfort level. 
You make the decisions; I keep you on track.

1. What problem are you looking to solve today?
2. What's your comfort level with coding and web development?"

Alex (Participant):
"I'm a Technical PM. I understand REST APIs and JSON payloads, but I don't build 
full-stack apps from scratch. I want to build a tool that takes messy customer complaints, 
classifies them by severity and product area, and drafts an escalation snippet for our engineering team."

Devpost AI Agent:
"Understood! We'll calibrate this project specifically for your background:
- Architecture: A single lightweight web page backed by a local Python coordinator.
- Explanations: Plain language focusing on data flow and logic, without unnecessary frontend jargon.
- Next Step: We'll run 2-scope to lock down a strict, achievable Proof of Concept boundary."
```

### Artifact Generated: `devpost/learner-profile.md`
```markdown
# Learner Profile
- Builder: Alex (Technical Product Manager)
- Demonstrated Background: Understands APIs and data structures; limited full-stack experience
- Desired Learning Outcome: Safely connect an enterprise LLM endpoint to an interactive UI
- Calibrated Mode: Learn Mode (step-by-step verification, guided architectural explanations)
```

---

## Stop 2: Plan-First Scoping & Boundary Enforcement

### Participant Experience: Plan-First Scoping & Boundary Enforcement
The participant defines what they want to build. Rather than letting them fall into the trap of over-ambitious scope, the agent actively challenges assumptions and eliminates complex third-party dependencies (like external OAuth). It produces a formal Scope document and Product Requirements Document (PRD) sized to a tight, testable proof of concept.

### Example Interaction:
```text
Alex (Participant):
"Awesome. Let's make sure it also integrates directly with Jira, Salesforce CRM, 
and our internal PagerDuty webhook so it automatically pages on-call engineers."

Devpost AI Agent:
"Pushing back here: OAuth connections to Jira and Salesforce, plus PagerDuty webhook 
integrations, introduce external auth and security dependencies that will derail a 
2-to-4 hour learning sprint.

Let's enforce a strict Proof of Concept boundary:
1. We will build the core AI reasoning engine and UI first.
2. The app will generate clean, formatted Jira and Slack markdown that can be copied with one click.
3. Live third-party webhooks become 'Future Scope' once the core PoC is proven.
Does that boundary sound good?"

Alex (Participant):
"That makes total sense. Let's stick to the one-click copy."
```

### Artifacts Generated: `devpost/scope.md` & `devpost/prd.md`
```markdown
# Product Requirements: FeedbackPulse
- Core Journey: Paste messy customer note → AI extracts urgency (P1–P4) & service area → displays ready-to-use Slack and Jira markdown blocks.
- PoC Boundary: Single-screen web interface; mockable internal REST API; clipboard copy actions (zero external OAuth dependencies).
- Approved Enterprise Stack: Lightweight Python server + Enterprise LLM endpoint (Azure AI Foundry / OpenAI / Bedrock) + Tailwind CSS.
```

---

## Stop 3: Governed Build in 'Learn Mode' & The App Map

### Participant Experience: Governed Build in 'Learn Mode' & Code Comprehension
The participant builds their application step by step using a verified checklist. Working in 'Learn Mode,' the agent does not write code in a black box: it explains key architectural patterns, runs automated mechanical checks after each slice, and generates an interactive visual App Map so the participant understands how their system works.

### Example Interaction:
```text
Devpost AI Agent:
"We're executing checklist.md in Learn Mode. We break the app into 3 verified slices:

[x] Slice 1: Scaffold dark-mode web UI with text input area
[x] Slice 2: Connect AI classification prompt & JSON parser
[ ] Slice 3: Output cards & one-click clipboard copy

Running Slice 2 verification:
- Mechanical check: Sent sample outage text to /api/classify -> 200 OK (Urgency: P1, Team: Billing).
- Learning Checkpoint: Notice how we forced the model to return structured JSON instead of raw prose? 
  This guarantees our frontend never crashes on unexpected markdown formatting.

Ready to test! Open http://localhost:8080 and paste your first sample customer note."
```

### Artifacts Generated: `devpost/checklist.md` & `devpost/app-map.html`
```markdown
# Build Checklist (Mode: Learn)
- [x] Slice 1: Scaffold responsive single-screen UI (Verified: 200 OK on GET /)
- [x] Slice 2: Integrate LLM reasoning pipeline (Verified: Structured JSON schema enforced)
- [x] Slice 3: Clipboard export actions & error states (Verified: User test complete)
- [x] Visual App Map: devpost/app-map.html generated
```

> **Visual Code Tour:**  
> The agent automatically generates an interactive [app-map.html](file:///Users/richard/development/skills/devpost/app-map.html). Alex can open it in a browser to see an architectural visual diagram connecting their frontend elements, backend routes, and AI prompt pipelines with plain-English annotations.

---

## Stop 4: Enterprise Submission & Devpost for Teams Telemetry

### Participant Experience: Security Audit, Deliverables Prep & Enterprise Submission
The participant prepares their project for submission. The agent automatically audits git history to ensure no credentials or sensitive data are committed, formats the project impact statement, and submits the proof of concept to the company's internal Devpost for Teams showcase.

### Example Interaction:
```text
Devpost AI Agent:
"FeedbackPulse is built, tested, and mapped! 
Before we submit to the Devpost for Teams internal showcase:

1. Automated Security Audit:
   [PASSED] .gitignore verified: API keys and local environment variables excluded.
   [PASSED] Git history scan: Zero corporate credentials or customer PII committed.
2. Deliverables Checklist:
   [READY] 90-second internal demo video checklist prepared.
   [READY] Internal GitHub/GitLab repository verified.
3. Impact Statement:
   - Problem: Eliminates ~45 minutes of manual triage per escalation.
   - Stack Explored: Enterprise LLM structured prompting, Python REST API, Clipboard API.

Your submission draft is ready to push directly to Devpost for Teams!"
```

### What Leadership Sees: The Devpost for Teams Enterprise Dashboard
```text
┌────────────────────────────────────────────────────────────────────────┐
│  AI ADOPTION SPRINT: ENTERPRISE SCORECARD                              │
├────────────────────────────────────────────────────────────────────────┤
│  • Participants Active: 350 employees across 12 business units          │
│  • Working Tools Shipped: 85 production-ready Proofs of Concept        │
│  • Non-Developer Participation: 62% (PMs, Analysts, Solutions Eng)    │
│  • Cloud/AI Consumption: 14,200 requests to internal Azure AI Foundry  │
│  • Avg Time-to-Working-App: 3 hours 20 minutes                         │
└────────────────────────────────────────────────────────────────────────┘
```

---

## Triggering & Execution Instructions

When the user runs `demo-walkthrough`:
1. Print the **Executive Pitch Header** (framing the 3-minute demo for the audience).
2. Begin immediately with **Stop 1**.
3. Pause with the clean transition prompt: `👉 [Press Enter or reply "next" to proceed to Stop 2 | Or ask a question to explore this step]`.
