⚖️ Lex: NaijaLawGPT - Virtual Legal Assistant
Overview
Lex is a full-stack, AI-powered legal assistant specializing in Nigerian law. It provides legal professionals with tools to accelerate their practice by leveraging large language models (LLMs) and structured data.
The tool operates in three primary modes, selectable through the user-friendly interface:
 * Legal Research: Finds and summarizes relevant Nigerian case law and statutes.
 * Document Drafting: Generates initial drafts of legal documents (e.g., agreements, deeds) based on Nigerian legal precedents.
 * Data Analytics: (Mock feature in frontend) Provides high-level insights and trends on court outcomes.
The project is built on a decoupled architecture, consisting of a single-file React frontend (PWA) and a powerful backend workflow orchestrated by n8n.
Installation
This project requires two separate deployment steps for the frontend and the backend workflow.
Frontend (User Interface)
The frontend is a single-file React application using Babel and CDN links, designed for easy static hosting.
 * Create Repository: Place the final index.html file (which contains all the React/JSX logic) in the root of your GitHub repository.
 * Configure Webhook URL: Crucially, ensure the WEBHOOK_URL constant within the <script type="text/babel"> section of index.html points to the public endpoint of your deployed n8n workflow (see below).
 * Deploy with GitHub Pages: Enable GitHub Pages in your repository settings, pointing the source to the main branch and the / (root) folder.
Backend (n8n Workflow)
The backend is managed entirely by the n8n automation platform.
 * Host n8n: Deploy or access your n8n instance.
 * Import Workflow: Import the contents of the lex_n8n_workflow.json file into your n8n environment to set up the processing pipeline.
 * Activate Webhook: Activate the Webhook node and copy the production URL. This is the WEBHOOK_URL you need for the frontend.
Usage
Use the Task Type Selector on the main interface to define the context for your query. Then, enter a natural language command into the input box.
| Task Type | Example Command | Expected Output |
|---|---|---|
| Legal Research | Find recent Supreme Court rulings on tenant abandonment under the Lagos Tenancy Law 2011. | Summarized case facts and Nigerian Law Report (NLR) citations. |
| Document Drafting | Draft a simple confidentiality agreement for two startups based in Kano State. | A structured Markdown draft of the legal document ready for review. |
| Data Analytics | Analyze trends for land dispute outcomes in Rivers State over the last 3 years. | (Mock) Statistical summary of case outcomes and categorized trends. |
NDPR Compliance: You must check the NDPR Consent box to enable the workflow to proceed, as all requests are logged for compliance and auditing purposes.
Requirements
Runtime Dependencies
| Component | Requirement | Notes |
|---|---|---|
| Backend Orchestration | Hosted n8n Instance | Essential for running the AI logic and managing the webhook. |
| LLM | Anthropic API Key (Claude 3.5 Sonnet) | Required for the HTTP Request Claude node for legal reasoning. |
| Data Grounding | Legal Data API Key (Mock) | Required for the HTTP Request Data node to simulate querying Nigerian legal databases. |
| Frontend | Modern Web Browser | Runs React, Tailwind, and Babel via CDNs. |
Development Dependencies
 * React, ReactDOM, and Babel (via CDNs in index.html)
 * Tailwind CSS (via CDN)
 * Lucide Icons (for the interface)
License
This is a private project.
All rights to the source code, documentation, and assets are reserved by the author(s). Unauthorized copying, reproduction, or distribution is prohibited. This project is currently unlicensed and is not available for public use or modification without explicit written permission.
That's perfectly normal for a new project! Until you decide on a formal license, it's best practice to explicitly state that all rights are reserved and that the code is private.
Here is the updated README content with the modified License section.
⚖️ Lex: NaijaLawGPT - Virtual Legal Assistant
Overview
Lex is a full-stack, AI-powered legal assistant specializing in Nigerian law. It provides legal professionals with tools to accelerate their practice by leveraging large language models (LLMs) and structured data.
The tool operates in three primary modes, selectable through the user-friendly interface:
 * Legal Research: Finds and summarizes relevant Nigerian case law and statutes.
 * Document Drafting: Generates initial drafts of legal documents (e.g., agreements, deeds) based on Nigerian legal precedents.
 * Data Analytics: (Mock feature in frontend) Provides high-level insights and trends on court outcomes.
The project is built on a decoupled architecture, consisting of a single-file React frontend (PWA) and a powerful backend workflow orchestrated by n8n.
Installation
This project requires two separate deployment steps for the frontend and the backend workflow.
Frontend (User Interface)
The frontend is a single-file React application using Babel and CDN links, designed for easy static hosting.
 * Create Repository: Place the final index.html file (which contains all the React/JSX logic) in the root of your GitHub repository.
 * Configure Webhook URL: Crucially, ensure the WEBHOOK_URL constant within the <script type="text/babel"> section of index.html points to the public endpoint of your deployed n8n workflow (see below).
 * Deploy with GitHub Pages: Enable GitHub Pages in your repository settings, pointing the source to the main branch and the / (root) folder.
Backend (n8n Workflow)
The backend is managed entirely by the n8n automation platform.
 * Host n8n: Deploy or access your n8n instance.
 * Import Workflow: Import the contents of the lex_n8n_workflow.json file into your n8n environment to set up the processing pipeline.
 * Activate Webhook: Activate the Webhook node and copy the production URL. This is the WEBHOOK_URL you need for the frontend.
Usage
Use the Task Type Selector on the main interface to define the context for your query. Then, enter a natural language command into the input box.
| Task Type | Example Command | Expected Output |
|---|---|---|
| Legal Research | Find recent Supreme Court rulings on tenant abandonment under the Lagos Tenancy Law 2011. | Summarized case facts and Nigerian Law Report (NLR) citations. |
| Document Drafting | Draft a simple confidentiality agreement for two startups based in Kano State. | A structured Markdown draft of the legal document ready for review. |
| Data Analytics | Analyze trends for land dispute outcomes in Rivers State over the last 3 years. | (Mock) Statistical summary of case outcomes and categorized trends. |
NDPR Compliance: You must check the NDPR Consent box to enable the workflow to proceed, as all requests are logged for compliance and auditing purposes.
Requirements
Runtime Dependencies
| Component | Requirement | Notes |
|---|---|---|
| Backend Orchestration | Hosted n8n Instance | Essential for running the AI logic and managing the webhook. |
| LLM | Anthropic API Key (Claude 3.5 Sonnet) | Required for the HTTP Request Claude node for legal reasoning. |
| Data Grounding | Legal Data API Key (Mock) | Required for the HTTP Request Data node to simulate querying Nigerian legal databases. |
| Frontend | Modern Web Browser | Runs React, Tailwind, and Babel via CDNs. |
Development Dependencies
 * React, ReactDOM, and Babel (via CDNs in index.html)
 * Tailwind CSS (via CDN)
 * Lucide Icons (for the interface)
License
This is a private project.
All rights to the source code, documentation, and assets are reserved by the author(s). Unauthorized copying, reproduction, or distribution is prohibited. This project is currently unlicensed and is not available for public use or modification without explicit written permission.

