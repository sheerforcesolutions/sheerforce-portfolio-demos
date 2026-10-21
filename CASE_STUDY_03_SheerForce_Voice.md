# SheerForce Voice: AI Phone Receptionist
## Portfolio case study, Katherine Perron

**Live demo:** [`03_SheerForce_Voice_Demo.html`](03_SheerForce_Voice_Demo.html)
**Role:** Founder and product owner. I define the requirements, safety rules and business logic, build with AI-assisted development tools, and test it on real phone calls.
**Status of the real product:** in controlled pilots. Phone answering, restaurant ordering and the home-services receptionist have been verified on live test calls. There are no paying customers yet.

> The product's source code, prompts, integrations and customer data are private. This repository holds only an original browser simulation and this write-up.

## The problem
Small businesses miss calls when everyone is busy. Every missed call can be a lost order or job. Basic AI answering services can cause a second problem: they make things up. They quote wrong prices, "book" times that aren't open, or say an order went through when it didn't.

## The design rule
**The AI holds the conversation. The rules engine owns the facts.**

The voice AI listens, talks and picks an action. Everything that has to be right — menu, prices, totals, hours, service area, open appointment times and order status — lives in a rules engine the AI can't override.

This comes from 911. A dispatcher's words have to match what's in the system, and you never tell a caller help is on the way unless it is.

## What the demo shows

| Scenario | What happens |
| --- | --- |
| Half-and-half pizza | Topping placement is stored as data (left, right, whole), so the price and the kitchen ticket are correct. |
| Caller changes the order | The stored order is updated and its version number goes up. |
| Caller adds something after the read-back | The old "yes" no longer counts. The agent reads the whole order back again first. |
| Kitchen system fails | The order goes to staff and the caller is told the truth. It's never resent automatically, so there's no risk of a double order. |
| Allergy question | Handed to staff. The AI never guesses about ingredients. |
| Caller starts reading a card number | Refused on the call, and never written to the order or the logs. |
| Gas smell (home services) | The first sentence tells the caller to leave and call 911. The on-call tech is alerted. |
| Outside the service area | No visit is promised. The request goes to the office for review. |
| "Can I talk to a person?" | Transferred, with the details passed along. |

## How the real product is built (high level)
- **Voice:** a realtime speech-to-speech AI model, connected to a phone number through a telephony provider
- **Rules engine:** a Python web service with an explicit order lifecycle (draft → read back → confirmed → sent, or failed → handed to staff)
- **Adapters:** a point-of-sale connection (tested in the POS vendor's sandbox), calendar booking, owner alerts and an owner dashboard
- **Quality:** an automated test suite, plus scheduled test calls that check the live phone lines every night
- **Privacy:** no call recordings or transcripts are stored, only a structured outcome and a short note for each call

**Skills used:** product requirements, conversation and escalation design, API integration, state machines, automated testing, safety rules, and AI-assisted development.

## What I'd say in an interview
"I ran NYPD 911 floors for years, where what you tell a caller has to match what's actually happening. I built SheerForce Voice on that rule: the AI handles the conversation, but it can't invent a price, promise a time or claim an order went through unless the system confirms it. And when something goes wrong, a person takes over."

## Honest limits of this demo
- The page uses scripted caller lines and a small engine written for the demo. It doesn't use a real AI model, phone call or network connection.
- The businesses, menu, prices and people are fictional.
- It shows the design principles, not the product's code, prompts or integrations.
