# Presenter Notes — Devpost Learning Hackathon Demo (`demo-walkthrough`)

> **Audience:** Enterprise Executive Buyers (CTO, VP of Engineering, Head of AI Adoption, L&D / People Leaders).  
> **Target Run Time:** 3 to 4 minutes.  
> **Screen Sharing Tip:** Share only your terminal or browser window running the agent. Keep this document open on your second screen or notes pane.

---

## Executive Pitch Narrative & Framing (Pre-Demo)

### The Hook (Say This Before Triggering the Command):
> *"Most companies give their workforce AI tools like GitHub Copilot or ChatGPT, but 90% of employees get stuck in the 'tinkering trap'—playing with disconnected prompts without producing real business value. Meanwhile, traditional hackathons often end up as 'pizza and innovation theater' with throwaway code.*  
> *Devpost's Learning Hackathon framework solves this. Let me show you what the participant experience actually looks like in 3 minutes for a mildly technical employee building an internal tool."*

---

## Stop 1: Flipped Kickoff & Learner Calibration

### What the Prospect Sees on Screen:
The agent welcomes Alex (a Technical PM), interviews them about their goals and technical comfort, and produces a calibrated `learner-profile.md` rather than immediately generating code.

### 🎙️ What You Say (Talking Points):
* **Flipped Interaction:** *"Notice the dynamic here. The agent doesn't ask 'what code should I write?' It flips the relationship: the agent interviews the employee. The human brings the problem and business judgment; the agent provides the guardrails."*
* **Skill Calibration for the Broader Workforce:** *"Alex is a PM who understands APIs but doesn't build web frontends. The agent automatically detects this and calibrates its explanations to data flow and logic, instead of dumping overwhelming boilerplate or talking down to them."*
* **Governed Onboarding:** *"In under two minutes, an employee is guided into an enterprise-safe sandbox with clear parameters before a single line of code is written."*

### Transition Cue:
*(Hit Enter or type `next`)*  
> *"Now that the employee is calibrated, watch what happens when we define what to build."*

---

## Stop 2: Plan-First Scoping & Boundary Enforcement

### What the Prospect Sees on Screen:
Alex asks for 3 complex external integrations (Jira, Salesforce, PagerDuty). The agent pushes back, explains the risks of auth rabbit holes in a short sprint, and locks a clean Proof of Concept boundary (`scope.md` and `prd.md`).

### 🎙️ What You Say (Talking Points):
* **Autonomous Guardrails Against Scope Creep:** *"This is the number one failure mode for non-engineers using AI: they ask for five massive integrations in their initial prompt, hit an authentication wall in hour two, get frustrated, and quit."*
* **The Agent Enforces Discipline:** *"Notice the agent actively pushes back. It guides Alex to a high-value, testable proof-of-concept—generating one-click clipboard snippets first, and saving live webhooks for phase two."*
* **Real Architectural Artifacts:** *"Within 10 minutes, the participant has produced a structured PRD and technical specification aligned with corporate standards. We plan before we code."*

### Transition Cue:
*(Hit Enter or type `next`)*  
> *"With an approved plan, we move into the build phase. Notice this is not a black-box code generator."*

---

## Stop 3: Governed Build in 'Learn Mode' & The App Map

### What the Prospect Sees on Screen:
The agent executes `checklist.md` slice-by-slice. It runs automated mechanical verification tests, pauses for a "Learning Checkpoint" explaining structured JSON output, and generates the visual `app-map.html`.

### 🎙️ What You Say (Talking Points):
* **Upskilling vs. Code Dumps:** *"This is why we call it a Learning Hackathon. The agent operates in 'Learn Mode'—it explains architectural principles, like enforcing structured JSON payloads so the UI never crashes on malformed data."*
* **Slice-by-Slice Verification:** *"Code is never written in a monolithic 1,000-line block. It's built in small, verified slices. If something breaks, automated checks catch it immediately and rollback is instant."*
* **Visual Knowledge Retention (App Map):** *"At the end of the build, the agent generates an interactive App Map. Alex can click through every component to see how the frontend talks to the backend and the AI model. They walk away actually understanding the system they built."*

### Transition Cue:
*(Hit Enter or type `next`)*  
> *"Finally, let's look at how this turns into governed enterprise output and measurable ROI for leadership."*

---

## Stop 4: Enterprise Submission & Devpost for Teams Telemetry

### What the Prospect Sees on Screen:
The agent runs an automated security audit (`.gitignore` verification, secret scanning), prepares demo deliverables, and displays the executive telemetry scorecard in Devpost for Teams.

### 🎙️ What You Say (Talking Points):
* **Security & Secret Hygiene:** *"Before anything is submitted, the agent verifies that zero API keys, secrets, or internal customer PII are committed to git repositories."*
* **Beyond 'Who Won a Prize':** *"For leadership, this solves the measurement gap. Devpost for Teams provides hard telemetry: how many employees participated, what percentage were non-traditional developers, and how many internal API calls were made to your approved AI stacks (Azure AI Foundry, Copilot, Bedrock)."*
* **Real Internal Utilities:** *"Tools like FeedbackPulse don't get thrown in the trash after the weekend. They become working internal utilities built by the people who actually feel the day-to-day operational pain."*

---

## Objection Handling & FAQ (Quick Reference)

### Q: "We already purchased GitHub Copilot licenses. Why do we need a hackathon?"
> *"Copilot gives your engineers the keyboard, but it doesn't give them the habit or the workflow. A Learning Hackathon creates an intensive, time-boxed environment where employees move from passive autocomplete to building complete, end-to-end applications using your approved enterprise models."*

### Q: "Can our non-technical or mildly technical employees really build working apps?"
> *"Yes. As you just saw with Alex, the flipped interaction model and calibrated 'Learn Mode' provide the guardrails. We regularly see 50–60% non-developer participation in enterprise sprints, with completion rates exceeding 85%."*

### Q: "How do we prevent employees from spinning up unauthorized cloud resources or racking up bills?"
> *"We work with your cloud team to enforce strict sandboxes or managed budget caps (e.g., $250/team), ensuring participants experiment within defined corporate security boundaries."*
