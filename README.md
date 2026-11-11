# Claude BullMQ Specialist Skill

A skill for designing and operating reliable background job processing with BullMQ, Redis, and Node.js or TypeScript applications.

## What It Covers

- **Queue design:** Structure Redis-backed queues for decoupled background processing.
- **Scheduling:** Use delayed and repeatable jobs for scheduled workflows.
- **Priorities and rate limits:** Control job ordering and execution throughput.
- **Workers:** Configure worker patterns and concurrency for stable processing.
- **Job events:** Observe queue lifecycle events and handle operational failures.
- **Flows and dependencies:** Model multi-step processes with parent-child job relationships.
- **Reliability:** Avoid oversized payloads, uncontrolled concurrency, and missing dead-letter handling.

## Installation

Clone the repository into your Claude skills directory:

```bash
git clone https://github.com/Brajesh31/claude-bullmq-specialist-skill.git ~/.claude/skills/bullmq-specialist
```

Install BullMQ and a Redis client in your Node.js project:

```bash
npm install bullmq ioredis
```

## Using the Skill

Example request:

```text
Use the bullmq-specialist skill to design a background job pipeline
with retries, delayed jobs, concurrency limits, and failure handling.
```

Read [SKILL.md](SKILL.md) for the queue setup patterns, scheduled jobs, job flows, anti-patterns, and related skills.

## Recommended Practices

Keep job payloads small and pass identifiers for large data. Define retry and backoff behavior intentionally, make job handlers idempotent, monitor failed and stalled jobs, and configure concurrency based on Redis, worker, and downstream service capacity.
