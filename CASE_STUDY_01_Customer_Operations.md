# Customer Operations Simulator
## Portfolio case study — private draft for Katherine Perron

**Role focus:** AI Solutions / Implementation, technical product thinking, customer operations
**Format:** Standalone offline HTML/CSS/JavaScript demonstration
**Release status:** Private review only; not connected to SheerForce production systems

## The business problem
When a small service business misses or mishandles calls, requests can be lost, urgent issues can be delayed, and customers may be given promises the business cannot keep. An AI-assisted front desk must distinguish routine intake from situations requiring human judgment.

## What this demonstration shows
This interactive simulation takes a fictional customer's request and produces a decision, customer-facing response, and structured work ticket. Users can select a routine booking inquiry, quote request, human handoff, immediate danger, urgent property damage, or an out-of-area inquiry.

The decision flow explicitly demonstrates:
- Immediate safety guidance and alerting for dangerous situations rather than an unsafe transfer delay.
- Human handoff when the customer asks for a person.
- Urgent escalation without falsely claiming a confirmed appointment.
- A coverage check before promising services outside the available area.
- Quote intake without inventing technician prices.
- A booking *request* distinguished from a booked appointment.

## Katherine's relevant real-world experience
Katherine brings 21 years of NYPD emergency communications experience, including supervisory and command responsibilities, staffing and queue management, incident escalation, quality assurance, and training. The SheerForce Voice repository documents current work on AI-based telephone assistance, customer intake, business rules, and escalation design.

This case study is an **illustration of those operating principles**, not an assertion that this standalone browser simulation was deployed to paying customers or integrated with phone services.

## Technology and implementation
- Semantic HTML forms and responsive CSS
- Client-side JavaScript decision functions
- Structured JSON-like work-ticket display
- Accessible visible status updates
- No libraries, API keys, network calls, external assets, or storage

## Verification performed
Five simulated input categories were exercised programmatically: routine booking, quote, request for a person, immediate danger, and urgent service. The JavaScript syntax was checked. Katherine reviewed the demo visually. Before public release, also capture screenshots and document additional boundary tests.

## What I would say in an interview
"I spent years making operational decisions in a 911 environment, where escalation and communication rules matter. In SheerForce's AI product work, I apply that mindset to small-business customer journeys: define the process, decide what the system may do, require a verified result before making a commitment, and give humans control when needed. This separate offline simulator shows how I think about those requirements."

## Honest limitations
- Not a real conversational AI or voice caller.
- No calendar availability, CRM persistence, SMS, dispatch, or emergency-service integration.
- No measured reduction in missed calls, response time, or costs.
- Separate original simulation; it does not reveal or reproduce SheerForce Voice production code.

## Next improvements before publication
1. Add an architecture diagram showing the boundary between intake, policy decision, and external actions (as hypothetical integrations).
2. Record a 30–45 second screen walkthrough.
3. Add a small scenario test matrix, including missing name and out-of-coverage behavior.
4. Confirm Katherine's exact contribution wording and professional title.
