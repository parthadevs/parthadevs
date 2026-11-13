# Partha Sarker

**Software Engineer** · Backend and full stack · Dhaka, Bangladesh

I build backend systems and web applications that handle real users and real money. My main tools are TypeScript, NestJS, PostgreSQL, and Redis, and I build frontends with Next.js. I care most about correctness, data consistency and maintainable code.

[Portfolio](https://parthadevs.github.io/personal-website/) · [LinkedIn](https://www.linkedin.com/in/parthadevs/) · [Email](mailto:dev.parthasarker@gmail.com)

---

## Experience

**Full Stack Engineer, Dolphin IT Institute** (remote) · August 2024 to present

Backend development with NestJS, TypeScript, and PostgreSQL, and frontend development with Next.js and Tailwind CSS, on web application projects.

## Production Platforms

I have built the backend and frontend for reward and survey platforms, where users complete offers and tasks and earn money.

| Platform | Period | Scale |
| --- | --- | --- |
| [DollarPull](https://dollarpull.com/) | Apr to Jun 2026 | 17K+ users |
| [Cash2Wall](https://cash2wall.com/) | Feb to Mar 2026 | 5K+ daily survey completions |
| [EarnAppz](https://earnappz.com/) | Oct to Dec 2025 | 20K+ users |
| [Pollmake](https://pollmake.com) | 2026 | Offers, surveys, offer walls, referrals, leaderboard, cash out |

What I focused on in this work:

- **Partner callbacks.** Offerwall and survey partners notify the platform when a user completes a task. These callbacks are verified with HMAC signatures before any reward is applied.
- **Wallet safety.** Transactions are idempotent, so a repeated or retried callback cannot credit a user twice.
- **Performance.** Redis caching reduced core API response times by about 40%.
- **Background work.** Reward processing and other slow jobs run in queues rather than inside the request.

## Projects

### [Event-Driven Order System](https://github.com/parthadevs/event-driven-order-system) (in development)

A NestJS monorepo for an order platform split into services: API gateway, auth, order, payment, inventory, and notification. Each service owns its database, and services communicate through Kafka events.

I built it as a hands-on way to apply distributed-systems patterns: the transactional outbox (an order and its event are saved in one database transaction), idempotent consumers, retries with backoff, and dead letter queues.

Stack: NestJS, TypeScript, PostgreSQL, Prisma, Kafka, Redis, BullMQ, Docker

### [QuotaPlane](https://github.com/parthadevs/quotaplane) (in development)

Shared quota and rate limiting infrastructure that lets multiple API keys draw from one organization's quota pool, with atomic quota deduction in Redis.

Stack: NestJS, TypeScript, PostgreSQL, Prisma, Redis, BullMQ

### [URL Shortener](https://github.com/parthadevs/url-shortener)

A URL shortening service with link monetization. It uses Base62 short codes and multi-tier Redis caching to keep redirects fast.

Stack: TypeScript, Redis

### [EarnAppz Web](https://github.com/parthadevs/earnappz-web)

A real-time rewards platform with integrated offerwalls.

Stack: Next.js 14, Node.js, TypeScript, Socket.io, BullMQ, Redis, PostgreSQL

## Skills

| | |
| --- | --- |
| Languages | TypeScript, JavaScript |
| Backend | Node.js, NestJS, Express |
| Frontend | Next.js, React, Tailwind CSS |
| Databases | PostgreSQL, MySQL, MongoDB, Prisma |
| Messaging and caching | Apache Kafka, BullMQ, Redis |
| DevOps | Docker, GitHub Actions, AWS |

## Education and Research

**BSc in Computer Science and Engineering**, Dhaka International University (2021 to 2025)

Two accepted papers:

- Bengali speech recognition framework using conformers, Taylor & Francis
- Loan approval prediction, ICCIT 2025
