# Synvoraith — Intelligent Workflows. Smarter Business.

Synvoraith is a business automation website presenting practical ways to reduce repetitive work, connect everyday business tools, and improve operational workflows with AI-assisted solutions.

The website introduces Synvoraith's services, explains its delivery approach, highlights common business use cases, and provides an enquiry form for prospective projects.

> **Project scope:** This repository contains the public-facing Synvoraith website (a static HTML, CSS, and JavaScript site). It is a company/service website—not an AI model, automation execution platform, or backend service. The website describes services and possible solutions; it does not itself execute customer automations.

---

## Contents

- [About Synvoraith](#about-synvoraith)
- [Services](#services)
- [How We Work](#how-we-work)
- [Example Use Cases](#example-use-cases)
- [Website Features](#website-features)
- [Technology Stack](#technology-stack)
- [Repository Structure](#repository-structure)
- [Run Locally](#run-locally)
- [Deployment with GitHub Pages](#deployment-with-github-pages)
- [Contact Form Behaviour](#contact-form-behaviour)
- [Customization Guide](#customization-guide)
- [Security, Privacy, and Limitations](#security-privacy-and-limitations)
- [Roadmap Ideas](#roadmap-ideas)
- [Links](#links)

## About Synvoraith

Synvoraith focuses on making useful technology accessible to businesses. The goal is to identify time-consuming tasks and design practical improvements around the tools and processes a team already uses.

Areas presented on the website include:

- **Intelligent workflow automation** — connecting applications and automating repeatable steps.
- **AI assistants and agents** — helping teams handle common questions, internal information, and routine tasks.
- **Document processing** — extracting, classifying, and summarizing information from business documents.
- **Business process automation** — improving processes such as onboarding, approvals, reporting, and follow-ups.
- **Software integration** — connecting CRMs, spreadsheets, email, forms, databases, and other business tools.
- **Ongoing support and improvement** — maintaining and refining implemented workflows.

The right solution depends on the business process, available systems, data quality, and the level of human review required.

## Services

### 1. Workflow Automation
Connect business applications, trigger actions, route information, and reduce repetitive manual handoffs.

### 2. AI Assistants and Agents
Explore AI-supported experiences for customer questions, internal knowledge access, lead handling, and routine tasks. Appropriate testing and human oversight are important, especially for customer-facing or sensitive workflows.

### 3. Document Processing
Explore workflows that extract, classify, or summarize information from forms, invoices, PDFs, and other business documents.

### 4. Business Process Automation
Improve recurring activities such as onboarding, approvals, reporting, reminders, and follow-ups.

### 5. Software Integration
Connect tools such as CRMs, spreadsheets, email platforms, forms, and databases where supported integrations and permissions are available.

### 6. Ongoing Support and Improvement
Provide maintenance, troubleshooting, monitoring, and iterative improvements for implemented solutions.

These are service areas described by the website. A specific implementation, integration, or delivery commitment should be agreed upon for each project.

## How We Work

The website presents a four-stage approach:

1. **Discover the friction** — understand the repetitive work, tools, handoffs, and exceptions in the current process.
2. **Design the workflow** — select a practical approach, define safeguards, and agree on the expected outcome.
3. **Build and integrate** — connect the relevant systems and test realistic scenarios, retaining human review where needed.
4. **Support and improve** — maintain the solution and refine it as business requirements change.

The aim is to solve a clearly defined business problem rather than introduce technology without a measurable purpose.

## Example Use Cases

The website illustrates possible applications across business teams:

| Area | Example workflow |
|---|---|
| Sales | Capture enquiries, qualify leads, assign owners, and initiate follow-ups. |
| Operations | Prepare recurring reports, update records, send reminders, and route approvals. |
| Documents | Extract invoice details and route them for review or approval. |
| Customer support | Help answer common questions and direct complex cases to the appropriate person. |

These are examples of potential workflows, not claims that every integration is already implemented in this repository.

## Website Features

The current website includes:

- Responsive one-page layout for desktop, tablet, and mobile screens.
- Sticky navigation with mobile menu toggle.
- Hero section introducing Synvoraith's positioning.
- Service cards describing six service areas.
- Four-step process section.
- Example business use-case cards.
- Call-to-action section linking to the enquiry form.
- Contact form fields for name, company, email, area of interest, and project details.
- Email-app handoff with a pre-filled enquiry.
- Dynamic copyright year.
- Reduced-motion styling for visitors who prefer less animation.
- Dark visual theme with teal and cyan accents.

## Technology Stack

| Technology | Purpose |
|---|---|
| HTML5 | Page structure and content |
| CSS3 | Layout, responsive design, visual styling, and animations |
| Vanilla JavaScript | Mobile navigation, dynamic year, and contact form behaviour |
| GitHub | Source control and repository hosting |
| GitHub Pages | Suitable static hosting option |

The current site does not require a frontend framework, package manager, or build step.

## Repository Structure

```text
Synvoraith-AI/
├── index.html   # Complete website: HTML, CSS, and JavaScript
└── README.md    # Project documentation
```

## Run Locally

You can open `index.html` directly in a browser. For a local HTTP server, use Python:

```bash
# Clone the repository
git clone https://github.com/christian-tiaan/Synvoraith-AI.git

# Enter the project directory
cd Synvoraith-AI

# Start a local server
python -m http.server 8000
```

Then visit:

```text
http://localhost:8000
```

Stop the server with `Ctrl + C`.

No dependency installation or compilation is required for the current static website.

## Deployment with GitHub Pages

This repository can be hosted as a static site using GitHub Pages:

1. Open the repository's **Settings** on GitHub.
2. Select **Pages** in the sidebar.
3. Under **Build and deployment**, choose **Deploy from a branch** if that is the selected publishing method.
4. Choose the `main` branch and the `/(root)` folder.
5. Save the settings and wait for GitHub Pages to publish the site.
6. Open the published URL shown in the Pages settings.

The expected project URL for this repository is:

https://christian-tiaan.github.io/Synvoraith-AI/

If the repository's Pages configuration or custom domain changes, use the URL shown in GitHub Pages settings as the source of truth.

## Contact Form Behaviour

The current contact form is a **mailto-based demo form**. When a visitor submits valid fields, JavaScript:

1. Reads the entered form values.
2. Builds an email subject and message body.
3. Opens the visitor's configured email application using a `mailto:` link.

It does **not** submit data to a server, save enquiries in a database, or guarantee delivery. The visitor must have a compatible email application configured and must send the drafted email.

Before using the site for production enquiries, consider connecting a trusted form provider or a secure backend. Add spam protection, validation, a privacy notice, and appropriate data-retention practices. Never put private API keys or credentials in frontend JavaScript.

## Customization Guide

The current implementation is intentionally simple and can be edited directly in `index.html`.

- **Page title and search description:** edit the `<title>` and description meta tag in the `<head>`.
- **Branding and colours:** update the CSS custom properties in the `:root` block.
- **Navigation:** edit the links inside `#navLinks`.
- **Hero content:** edit the section with `id="home"`.
- **Services:** edit the cards inside `#services`.
- **Process steps:** edit the articles inside `#approach`.
- **Use cases:** edit the cards inside `#solutions`.
- **Contact interests:** edit the options in the `#interest` select element.
- **Enquiry recipient:** update the `mailto:` address in the contact form submit handler.
- **Footer:** edit the footer text; the year is populated automatically by JavaScript.

After making changes, test the layout at mobile and desktop widths and submit a test enquiry to confirm the email handoff behaves as expected.

## Security, Privacy, and Limitations

- This repository contains a static frontend; it does not include a server, database, authentication system, or workflow execution engine.
- The contact form uses the visitor's email application. It does not store submitted information on this website.
- The email recipient is visible in client-side source code. Use a public business contact address and expect it to be discoverable.
- Do not add secrets, access tokens, passwords, or private customer data to the repository.
- Any future AI or third-party integration should use secure server-side credentials and clearly documented data-handling practices.
- Validate external integrations, permissions, error handling, and human approval requirements before relying on them in business operations.
- The website's service descriptions and use cases should not be interpreted as proof that every example integration is already deployed.

## Roadmap Ideas

Possible future improvements, subject to project priorities:

- Move the contact form to a secure form service or backend.
- Add a privacy policy and clearer enquiry-consent information.
- Add project case studies with verified outcomes and implementation details.
- Improve accessibility checks, metadata, and search engine optimization.
- Add analytics only with appropriate privacy disclosures and consent where required.
- Publish technical demonstrations separately from service descriptions.
- Document supported integrations and delivery boundaries for each offering.

## Links

- **Website:** https://christian-tiaan.github.io/Synvoraith-AI/
- **GitHub repository:** https://github.com/christian-tiaan/Synvoraith-AI
- **Synvoraith on LinkedIn:** https://www.linkedin.com/company/synvoraith-ai/

---

## Contributing and Feedback

For corrections, documentation improvements, or suggestions, open an issue or submit a pull request in this repository. Please avoid including credentials, private business information, or personal data in public issues.

---

© Synvoraith. All rights reserved.
