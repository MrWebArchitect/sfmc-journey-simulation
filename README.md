# Salesforce Marketing Cloud Journey Simulation 

This project simulates a full coustomer journey using Salesforce Marketing Cloud (SFMC) concepts, including:
- A multi-step journey flow (modeled in Markdown)
- Modular, responsive HTML email templates
- Personalizaiton logic (AMPscript-style pseudocode)
- Sample segmentation rules
- QA & rendering verification (Litmus screenshots)

### Technologies Simulated: 
- Journey Builder
- Email Studio / Content Builder
- AMPscript (basic personalization)
- Responsive HTML
- Segmentation & A/B logic

---

## Journey Overview

The journey include the following email steps: 

1. **Welcome Email**
2. **Onboarding Tips**
3. **Personalized Promo Offer**
4. **Re-engagement Nudge**

Each email was hand-coded using inline CSS, built with a modular system for reusability and rapid scaling.

---

## Templates
- Header
- Footer
- Hero Banner
- CTA Block

build using basic components to mat SFMC's Content Builder logic.

---

## Files of Interest

- [`journey-map.md`](journey-map.md) - Simulated journey flow with logic steps
- [`emails/`](emails/) - HTML emails, all responsive and QA-ready
- [`segmentation-rules.md`](segmentation-rules.md) - Audience logic based on behavior & attributes
- [`personalization-rules.md`](personalization-rules.md) - Conditional logic for dynamic content

---

## QA 

- All emails were testing using [Litmus PutsMail](https://putsmail.com/) across common devices and clients 
- Preview images are in `/assets/`

---

## Goal

This repo demonstrates my ability to simulate real-world Salesforce Marketing Cloud campaign structure, even outside of a live SFMC environment. It reflects my experience as an email developer and my commitment to mastering the tools used by top-tier marketing teams like Razorfish.