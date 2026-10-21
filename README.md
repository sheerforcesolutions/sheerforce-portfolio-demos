# Katherine Perron: Interactive Technology & Operations Portfolio

**Focus:** AI voice products, public safety operations, implementation and training, customer experience, and workflow reliability.

This repository is a public portfolio of **browser-only demonstrations** based on my operational and product work. Every demo is an original, self-contained simulation using fictional businesses and data. None of them connect to production systems, and none of them contain private source code.

## Projects

### 1. Customer Operations Simulator
File: [`01_Customer_Operations_Simulator.html`](01_Customer_Operations_Simulator.html) · [Case study](CASE_STUDY_01_Customer_Operations.md)

A fictional service-intake decision tree. It shows how an intake process separates routine requests (appointments, estimates) from situations that need a human or an urgent safety escalation.

**Demonstrates:** requirements thinking, customer journeys, decision rules and escalation design.

### 2. Automation Reliability Lab
File: [`02_Automation_Reliability_Lab.html`](02_Automation_Reliability_Lab.html)

A fictional lead-intake process that shows input validation, duplicate-record protection, a simulated service failure, retries and event logging.

**Demonstrates:** workflow quality controls, exception handling, reliability thinking and test scenarios.

### 3. SheerForce Voice: AI Phone Receptionist (public demo)
File: [`03_SheerForce_Voice_Demo.html`](03_SheerForce_Voice_Demo.html) · [Case study](CASE_STUDY_03_SheerForce_Voice.md)

A simulated phone call with an AI receptionist for a fictional pizzeria and a fictional heating and plumbing company. Next to the call, an "engine view" shows the order or service request, its current state, which guardrails fired, and a log of every action. The point: **the AI holds the conversation, and the rules engine owns every price, time and promise.**

**Demonstrates:** AI product design, state machines, read-back and confirmation logic, safe failure handling, emergency (911) rules and human handoff.

## What these demos are, and aren't
- Self-contained HTML/JavaScript that runs entirely in your browser
- Fictional, non-sensitive data, with no APIs, AI models, phone calls, payments, CRMs or 911 systems
- Original simulations, **not** copies of SheerForce production code. Product source, prompts, integrations and customer data stay private.
- Built with AI-assisted development tools. I set the operational requirements, use cases and rules, and reviewed the results.

## View the demos
Open `index.html` from this repository's GitHub Pages site, or download any `.html` file and open it in a browser. No build step is needed.
