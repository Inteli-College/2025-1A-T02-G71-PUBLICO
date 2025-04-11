# Module 1 - Development Report – Prosply

## Project Context

**Prosply** is a SaaS platform that automates lead prospecting using artificial intelligence to simplify the creation of personalized campaigns and automate initial contact through channels such as email, WhatsApp, and LinkedIn. The goal is to enable companies—especially small and medium-sized ones—to reduce time spent on operational tasks and focus exclusively on closing deals with qualified leads.

Throughout the module (10 weeks divided into 5 sprints), we focused on designing the technical architecture, developing essential features, and continuously validating with stakeholders and sales professionals from various companies (**K2 Partnering Solutions, Tractian, Conta Simples, Ecocil Incorporações, Axenya, Holu**). This allowed us to deeply understand market pains and shape the product around real needs.

## Key Deliverables of the Module

- Definition of the technical architecture (Frontend, Backend, Infrastructure on Azure);
- Initial modeling and implementation of the databases (PostgreSQL);
- Frontend development with Next.js, covering key modules like Campaigns, Leads, and Messaging;
- Backend development with FastAPI;
- First experimental version of the AI-powered lead enrichment agent using LLM;
- Azure infrastructure setup, including resources for PostgreSQL, Azure OpenAI, and data storage;
- Ongoing market research and validation with professionals to refine features and value proposition.

---

## Sprint Breakdown

### Sprint 1

**Focus:** Initial research, ideation, and requirement gathering.

- Clearer ideation of the project and definition of Prosply’s value proposition;
- Planning of the module’s work schedule, with macro deliverables per sprint;
- Beginning of market understanding through interviews with sales professionals (SDRs, Sales Coordinators);
- Initial mapping of core MVP functionalities;

### Sprint 2

**Focus:** Technical definition and implementation kick-off.

- Detailed documentation of the system architecture (Frontend, Backend, ETL, Redis Streams, Enrichment Service);
- Clear definition of functional and non-functional requirements;
- Initial user flow diagram and key journeys within the platform;
- Implementation of the data download pipeline for Brazilian company information.

### Sprint 3

**Focus:** Infrastructure and development environment setup.

- Azure environment configuration (Startup Program participation);
- Organization setup on Azure DevOps for versioning and CI/CD processes;
- Initial creation and setup of core Azure services (PostgreSQL, Azure OpenAI, Azure Storage).

### Sprint 4

**Focus:** Frontend development and Backend initiation.

- Implementation of main Frontend modules (Next.js): Overview, Campaign Management, Lead Management, and Messaging Module;
- Start of detailed database modeling (schemas `CNPJ_BR` and `PROSPLY_APPLICATION`);
- Initial backend development using FastAPI, with basic route and structure implementation.

### Sprint 5

**Focus:** Backend development and initial frontend integration.

- Significant progress in backend development with essential routes for managing campaigns and leads;
- First backend-frontend integration to validate main flows such as campaign and lead management;
- First experimental version of the AI-based lead research and enrichment agent;
- **Note:** The messaging module was implemented only in the frontend; backend development and integration remain as next steps.

---

## Conclusion

Throughout this module, the team made significant progress in defining the technical foundation, implementing core features, and continuously validating with market professionals. The next steps will involve final integrations (especially the messaging module in the backend), platform performance optimization, and extending the capabilities of the AI-driven lead enrichment agent.
