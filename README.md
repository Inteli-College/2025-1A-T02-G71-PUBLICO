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

---

# Module 2 - Development Report – Prosply

## Project Context

**Prosply** continues its mission to streamline lead prospecting through automation and AI. Building on the solid foundation laid in Module 1, Module 2 focused on evolving the platform from a functional MVP into a more robust, scalable, and user-centric product. 

Key priorities included enabling flexibility in lead sourcing, expanding campaign customization options, restructuring the system architecture for maintainability and deployment, and refining the lead enrichment pipeline. A major product pivot was made this module: the lead generation engine now uses **LinkedIn-based filters** instead of relying solely on a Brazilian company database. Additionally, we introduced a new capability allowing users to **import their own lead lists**, addressing a common demand observed in user interviews.

Experiments with third-party data providers such as Bright Data and services available on RapidAPI helped guide architectural decisions and validate potential external APIs for Linkedin Integration.

---

## Key Deliverables of the Module

- Launch of the **Lead List Upload feature**, with support for versioning, file structure validation, editing, and management;
- Migration of the **lead segmentation filters** from CNPJ criteria to LinkedIn-based attributes;
- Full **dockerization** of the application for development and production environments;
- Major backend refactors: SQLAlchemy ORM migration, Alembic migrations, schema standardization in English;
- Creation of **dynamic lead and message filters** with real-time visual feedback;
- Setup of **RabbitMQ queues** for campaign generation and lead enrichment pipelines;
- Implementation of new user settings: profile editing, password update, and UI preferences (theme, timezone, language);
- Mocked architecture for **lead generation and enrichment services**, fully integrated with message queues.

---

## Sprint Breakdown

### Sprint 1

**Focus:** Planning refinement and continued backend-frontend integration.

- Finalized updated TAPI document and revised the delivery schedule for the semester;
- Continued backend-frontend integration for the Messaging module, a core part of the campaign execution flow.

---

### Sprint 2

**Focus:** New feature: Lead List Upload.

- Developed a new functionality that allows companies to upload and manage lists of cold leads;
- Enabled file import, multi-sheet navigation, data visualization, and personalized descriptions;
- Allowed users to save and edit list versions for better usability and version control.

---

### Sprint 3

**Focus:** Architectural and deployment improvements.

- Migrated all raw SQL queries to ORM using **SQLAlchemy**;
- Introduced **Alembic** for version-controlled migrations;
- Renamed all database fields to English for greater consistency and maintainability;
- Completed **Dockerization** with separate environments for dev and prod;
- Added automated scripts for database setup and deploy routines;
- Refactored key code structures, introducing **Enums** for better typing and clarity.

---

### Sprint 4

**Focus:** Campaign module revamp and backend infrastructure.

- Complete refactor of the Campaign Creation module to support **LinkedIn-based segmentation filters**;
- Implemented **frontend caching** for campaigns and leads;
- Developed **real-time dynamic filters** for Leads and Messaging modules;
- Configured **RabbitMQ** with Docker and management interface for observability;
- Created the **producer-consumer logic** for campaign message queues.

---

### Sprint 5

**Focus:** Advanced feature integration and enrichment logic.

- Enabled users to choose between lead list upload or LinkedIn filters during campaign creation;
- Updated database schema to associate leads with specific lists;
- Added **template download** and format validation for uploaded lead files;
- Fully integrated **lead list UI management** on the frontend;
- Delivered **user profile** screen with name/email editing and **settings page** for preferences;
- Developed **password change functionality** (frontend and backend);
- Mocked the **lead generation and enrichment services**, including message queue orchestration;
- Implemented functioning RabbitMQ flow: campaigns trigger lead capture (mocked), which triggers enrichment (mocked).

---

## Screenshots

### Lead List Upload interface

**Upload lead list**
![image](https://github.com/user-attachments/assets/e2062828-fcc3-4e0b-8374-1a2fdd999b67)

**Lead list historic**
![image](https://github.com/user-attachments/assets/ee87ed0b-18f1-4481-91b7-d8fd2847ad87)

**Lead list view**
![image](https://github.com/user-attachments/assets/c5254285-fc62-48a6-bbc4-5e9d0b147f72)
![image](https://github.com/user-attachments/assets/0f42cbe9-dce5-4fbb-b877-dfdf7c4d30d2)

### Campaign Creation with LinkedIn filters  

**Segmentation filters**
![image](https://github.com/user-attachments/assets/2705c685-d7f9-48de-a9df-7cff4252b4f4)
![image](https://github.com/user-attachments/assets/a0161d52-4e83-4c9e-a665-4ba7c4baacd7)

**Lead list selection**
![image](https://github.com/user-attachments/assets/aa105af0-3c47-4932-a9e1-852f869a5265)

### Lead module 

**Filters update in real time while you type.**
![image](https://github.com/user-attachments/assets/69b42de9-6a8b-470c-a713-e88e41bdb791)

### User Settings and Profile screens  

**User profile**
![image](https://github.com/user-attachments/assets/0f08762c-973d-4af0-b12a-0c40819f2c9d)

**User settings**
![image](https://github.com/user-attachments/assets/0141d3a0-625c-4d42-ad10-7ba106759cf6)
![image](https://github.com/user-attachments/assets/6a9c0ba6-528d-4b9c-afde-4fdbcec38b0a)
![image](https://github.com/user-attachments/assets/3010ee9c-51d5-4507-bc15-ba66b8269676)
![image](https://github.com/user-attachments/assets/48db8fe4-a353-4929-8753-542beda9276c)

---

## Conclusion

Module 2 brought important improvements to Prosply's functionality and structure. We implemented key user-facing features such as the lead list upload and updated campaign creation flows, while also making substantial changes to the backend architecture, including database refactors, queue-based processing, and containerization.

These enhancements improved the maintainability, flexibility, and scalability of the system, while aligning the product more closely with real user needs identified in interviews and testing.

---

# Module 3 - Development Report – Prosply

## Project Context

In this module, **Prosply** advanced toward completing its full end-to-end automation flow, from campaign creation to personalized message delivery, integrating all previously developed components into a cohesive, production-ready system.

While the previous modules focused on architecture, data flow, and enrichment pipeline setup, Module 3 emphasized building **intelligent automation** across enrichment, qualification, and communication processes. 

---

## Key Deliverables of the Module

- Implementation of the **Lead Enrichment pipeline** in production, integrating data from LinkedIn (via RapidAPI) and Google Search (via Serper API);
- Development of the **Lead Qualification logic**, assigning a status, score, and reasoning for each lead based on campaign data and enrichment results;
- Creation of **asynchronous queue flows** connecting enrichment, qualification, contact lookup, and message sending;
- Deployment of the **automated email sending system**, enabling full end-to-end campaign communication;
- Development of the **personalized message generation module**, using campaign and lead data to create contextualized communication;
- Comprehensive **Draw.io system documentation**, detailing routers, services, models, repositories, and the visual representation of all queue flows.

---

## Sprint Breakdown

### Sprint 1

**Focus:** Review and planning.

- Conducted a full review and documentation of all features already implemented in the platform;
- Defined pending functionalities required to complete the project’s scope;
- Created the Module 3 execution plan, including deliverables for each sprint.

---

### Sprint 2

**Focus:** Lead Enrichment pipeline in production.

- Implemented the enrichment logic in production (previously only experimental notebooks);
- Established automated flow: campaign creation → leads added to enrichment queue;
- Enrichment pipeline retrieves data from LinkedIn (via RapidAPI) and Google (via Serper API);
- Created a second queue for enriched leads, preparing them for the qualification stage.

---

### Sprint 3

**Focus:** Lead Qualification logic.

- Developed and deployed the lead qualification service in production;
- Leads from the enrichment stage are now automatically evaluated against the originating campaign’s segmentation, offer, and strategy;
- System assigns qualification status (qualified or not), relevance score, and reasoning;
- Qualified leads are published to a new queue for **contact lookup** (consumer implemented, logic pending).

---

### Sprint 4

**Focus:** Automated email delivery flow.

- Implemented the logic for fully **automated email sending**;
- Leads passing through the contact lookup queue are sent to the email sending queue;
- The queue triggers the email dispatch process, completing the automated communication loop.

---

### Sprint 5

**Focus:** Personalized message generation and full system documentation.

- Developed the **message generation logic**, now integrated into the email sending pipeline;
- The agent uses campaign and enriched lead data to create personalized, context-aware messages;
- Once generated, the message is saved in the database with pending status, then automatically sent through the email queue and marked as delivered;
- Created detailed **Draw.io documentation**, describing routers, services, database models, repositories, and a visual diagram of all lead-processing queues.

---

## Screenshots

### Visual diagram showing the queue flow

<img width="1764" height="955" alt="image" src="https://github.com/user-attachments/assets/47ce78b7-d015-4269-a488-7f958c56e26c" />
<img width="1760" height="971" alt="image" src="https://github.com/user-attachments/assets/ce2a494b-d93f-4aa7-9bd3-59a342182ff9" />
<img width="1759" height="933" alt="image" src="https://github.com/user-attachments/assets/064eff5b-2056-452b-91b1-b7c9d9c4d93d" />

### Example of an automated email successfully received (without the personalized message content)

<img width="1865" height="694" alt="image" src="https://github.com/user-attachments/assets/b8fefcac-3404-4fb7-9c97-5652e2d8e830" />

---

## Conclusion

Module 3 represented a major step toward completing the functional scope of Prosply. 

The main delivary was the connection of all previous modules resulting in a pipeline capable of generating, evaluating, and contacting leads automatically.

The system now supports a complete workflow from campaign creation to email delivery, with extensible queue-based architecture ensuring scalability and reliability. 

---
