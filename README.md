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