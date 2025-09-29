⚖️ Lex: NaijaLawGPT - Virtual Legal Assistant
​Overview
​Lex is a full-stack, AI-powered legal assistant specializing in Nigerian law. It provides legal professionals with tools to accelerate their practice by leveraging large language models (LLMs) and structured data.
​The tool operates in three primary modes, selectable through the user-friendly interface:
​Legal Research: Finds and summarizes relevant Nigerian case law and statutes.
​Document Drafting: Generates initial drafts of legal documents (e.g., agreements, deeds) based on Nigerian legal precedents.
​Data Analytics: (Mock feature in frontend) Provides high-level insights and trends on court outcomes.
​The project is built on a decoupled architecture, consisting of a single-file React frontend (PWA) and a powerful backend workflow orchestrated by n8n.
​Installation
​This project requires two separate deployment steps for the frontend and the backend workflow.
​Frontend (User Interface)
​The frontend is a single-file React application using Babel and CDN links, designed for easy static hosting.
​Create Repository: Place the final index.html file (which contains all the React/JSX logic) in the root of your GitHub repository.
​Configure Webhook URL: Crucially, ensure the WEBHOOK_URL constant within the <script type="text/babel"> section of index.html points to the public endpoint of your deployed n8n workflow (see below).
​Deploy with GitHub Pages: Enable GitHub Pages in your repository settings, pointing the source to the main branch and the / (root) folder.
​Backend (n8n Workflow)
​The backend is managed entirely by the n8n automation platform.
​Host n8n: Deploy or access your n8n instance.
​Import Workflow: Import the contents of the lex_n8n_workflow.json file into your n8n environment to set up the processing pipeline.
​Activate Webhook: Activate the Webhook node and copy the production URL. This is the WEBHOOK_URL you need for the frontend.
​Usage
​Instructions for running and interacting with the Lex platform are detailed in the USAGE.md file.
​A summary of the interaction process:
​Access the deployed frontend application (e.g., your GitHub Pages link).
​Select the Task Type (Research, Drafting, or Analytics).
​Enter your command and agree to the NDPR Consent.
​Click "Run Lex Workflow" to execute the command via the n8n backend.
​Requirements
​Runtime Dependencies
