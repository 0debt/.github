<div align="center">
  <h1 align="center">
  <img
    width="100"
    height="100"
    alt="0debt logo"
    src="https://github.com/user-attachments/assets/22c68a9c-9923-4880-8779-16bb79158a64"
  /><br>
  0debt
</h1>
   
<h4 align="center">A cloud-native microservices platform to simplify shared expense management and split bills effortlessly.</h4>
  
  <p align="center">
    <img src="https://img.shields.io/badge/Runtime-Bun-black?style=flat-square&logo=bun" alt="Bun">
    <img src="https://img.shields.io/badge/Framework-Hono-E36002?style=flat-square&logo=hono" alt="Hono">
    <img src="https://img.shields.io/badge/Frontend-Next.js_16-black?style=flat-square&logo=next.js" alt="Next.js">
    <img src="https://img.shields.io/badge/Infra-Coolify-6B21A8?style=flat-square&logo=coolify" alt="Coolify">
  </p>
</div>

**0debt** is a scalable, distributed financial application built on modern cloud-native principles. It solves the complexity of "who owes who" in group activities through a resilient microservices architecture, real-time event processing, and a clean user experience.

## Microservices Ecosystem

The 0debt platform consists of loosely coupled services communicating via HTTP and Redis Pub/Sub:

### Core Services

- **[users-service](https://github.com/0debt/users-service)**: The source of truth for identity. Handles authentication (JWT), secure password hashing, and subscription pricing plans.
- **[groups-service](https://github.com/0debt/groups-service)**: Manages collaboration spaces, membership logic, and synchronization with user profiles.
- **[expenses-service](https://github.com/0debt/expenses-service)**: The financial engine. Records transactions and executes the debt simplification algorithm. Orchestrates distributed transactions (Saga pattern).

### Business & Support Services

- **[analytics-service](https://github.com/0debt/analytics-service)**: Provides financial health insights and budget tracking. Generates visual reports and consumes data from the expense core.
- **[notifications-service](https://github.com/0debt/notifications-service)**: An event-driven service that handles transactional emails via Resend and background serverless jobs.

### Infrastructure

- **[api-gateway](https://github.com/0debt/api-gateway)**: The edge entry point. A reverse proxy built with Hono that handles routing, global rate limiting, and centralized security validation.
- **[0debt-frontend](https://github.com/0debt/frontend)**: A modern SPA built with Next.js 16, Shadcn UI, and TailwindCSS, optimized for the Bun runtime.

## Documentation

For detailed architectural decisions and API specifications, visit:

- [Customer Agreement & Pricing](https://github.com/0debt/0debt-infra/docs/agreements/customer-agreement.md)
- [Pricing Plans](https://github.com/0debt/0debt-infra/docs/agreements/pricing.md)
- [Architecture Diagrams](https://github.com/0debt/0debt-infra/docs/diagrams/architecture.md)
- [Communication Flow](https://github.com/0debt/0debt-infra/docs/diagrams/communication-flow.md)

## License

Apache License 2.0
