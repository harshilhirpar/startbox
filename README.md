Goal: Build a web-based tool that takes a natural language prompt and generates a production-ready full-stack application scaffold with auth, billing, and analytics.

Step 1: Define the MVP Scope
- Objective
Build a tool that:
    - Accepts a prompt describean app idea
    - Parses the prompt to extract entities and features
    - Generates a full-stack scaffold
    - Includes optional modules: Auth, Billing, Analytics
    - Outputs a downloadable .zip or GitHub repo

There will be a prompt parsing engine and the goal of it is to convert a natural language prompt into structured data

Example: "Build a SaaS freelancers to manage clients and invoices"

Expected Output
```
{
    "entities" : ["user", "client", "invoice"],
    "features" : ["Auth", "Billing", "Dashboard"],
    "stack": {
        "frontend" : "Next.js",
        "backend" : "tRPC",
        "db" : "PostgreSQL"
    }
}

```

Tasks for AI parser
- Design promt format
- Call OpenAI API with system prompt
- Parse and validate response
- Log and store prompt history

For scaffolded codebase
- Create templates
    - Auth (Clerk/Auth.js)
    - Billing (Stripe)
    - Analytics (PostHog)
    - CRUD modules (Prisma + API routes)
- Use file systems APIs to generate files dynamically
- Package into .zip or push to github

Break down Step 1: MVP Scope Definition

The goal of the MV is to build a functional prototype of StartBox that can:
- Accept a natural language prompt describing a startup idea
- Parse the prompt to extract relevnt entities and features.
- Generate a production-ready full-stack codebase with:
    - Authentication
    - Billing
    - Analytics
    - CRUD operations for code entities
- Package the codebase into a downloadable .zip file or push it to GitHub.
- Include a generate README.md with setup instruction.

At this moment this MVP will not include advanced features like live deployment, UI customization, or a plugin marketplace - those are reserved for later phases.

# Core Features
- Prompt Input UI: A simple web from where users describe their app idea in natural language.
- Prompt parse (AI): Uses OenAI API to extract entities, features, and tech stack from the prompt.
- Code Generator: Dynamically generates a full-stack scaffold using templates and parsed data.
- Optional Modules: Toggle options for Auth, Billing, and Analytics
- Output Delivery: Provides a downloadable .zip file or GitGub repo with the generated code.
- README Generator: Auto-generates a README.md with setup instructions and tech overview.

# User Flow
- User visits StartBox
- User enters a prompt
- User selects optional modules
- System parses the prompt
- System generates codebase with selected features
- User downloads the .zip or gets a GitHub repo link
- User run the app locally using the README instructions.

# Code Generation Scope
The generated codebase will include:
- Project structure with frontend, backend, and prisma folders
- Auth setup (login, signup, sessoion handling)
- Strip integration (basic subscription flow)
- Analytics script integration
- CRUD APIs and pages for core entities
- Environment variable setup
- Tailwind + basic layout component
- README with setup instructions

# Out of Scope for MVP (At this moment)
- Live deployment to Vercel/Railway
- UI customization or drag-and-drop builder
- Plugin marketplace
- Team collaboration features
- AI-generated UI components
- Versioning or history of generted projects

# High Level Architecture Overview

Frontend ---> Backend ---> Template Engine ---> Output Layer

# What frontend will contain
- Prompt Input
- Feature Toggles
- Download/Deploy UI

# What Backend API layer will contain
- Promt Parser (LLM)
- Code Generator Engine
- File Packager (.zip)
- Github Integration

# What Template Engine wil contain
- Auth Templates
- Billing Templates
- Analytics Templates
- CRUD Templates

# What Output Layer will contain
- .zip File Generator
- README Generator
- GitHub Repo Creator

