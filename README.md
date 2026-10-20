<p align="center">
  <picture>
    <source media="(prefers-color-scheme: dark)" srcset=".github/assets/hero-dark.png">
    <img src=".github/assets/hero.png" alt="market.me.at landing page" width="880">
  </picture>
</p>

<h1 align="center">market.me.at</h1>

<p align="center"><strong>Publish once per network. Track the threads that mention you.</strong></p>

<p align="center">
  <img src="https://img.shields.io/badge/status-in%20development-171717?style=flat-square" alt="Status: in development">
  <img src="https://img.shields.io/badge/license-source--available-404040?style=flat-square" alt="License: source-available">
  <img src="https://img.shields.io/badge/self--host-supported-525252?style=flat-square" alt="Self-host: supported">
  <img src="https://img.shields.io/badge/part%20of-me.at-737373?style=flat-square" alt="Part of me.at">
</p>

<p align="center">
  <a href="#features">Features</a> ·
  <a href="#how-it-works">How it works</a> ·
  <a href="#built-with">Built with</a>
</p>

Cross-posting tools tend to treat every network the same, and a retry at the wrong moment posts twice to a real audience. I built market.me.at for social-post scheduling with exactly-once delivery: compose a post once, preview it against each network's real constraints, schedule it, and publish through per-network drivers. It also listens: watches check public sources for your name, your competitors and questions you can answer, and you follow each thread from found to replied.

<p align="center">
  <picture>
    <source media="(prefers-color-scheme: dark)" srcset=".github/assets/overview-dark.svg">
    <img src=".github/assets/overview.svg" alt="market.me.at at a glance: compose once, posted exactly once, listen then reply, guardrails built in" width="880">
  </picture>
</p>

## Why market.me.at

| The usual post scheduler | market.me.at |
| --- | --- |
| A retry can post twice | One delivery record per post and network, so a retry never double-posts |
| One preview for every network | A preview per network, against that network's own limits |
| Approvals that survive later edits | Approvals that expire when the post changes |
| Posting only | Listening too, with a feed that puts questions above chatter |

## Features

- **Compose once, preview per network**: one text box with a preview for each connected network, checked against that network's own limits (weighted length, media, links) before anything is scheduled.
- **Exactly-once publishing**: one delivery record per post and network, so a retry updates that record and never posts a second time.
- **Scheduling and posting rhythm**: pick a time, or add a post to a network's queue and let declared posting slots place it.
- **Many destinations**: Mastodon, Bluesky, LinkedIn, Ghost, WordPress, dev.to and Forem, Discord and Slack webhooks, and an owned RSS feed.
- **Listening**: watches read public sources (RSS, Google News, Reddit and others) about every 15 minutes, and a ranked feed puts questions above chatter.
- **Places**: save a thread, answer it in your own voice, and mark it replied with a link to what you said. Nothing is posted for you.
- **Campaigns, analytics and benchmark**: group posts under a goal, read delivery and engagement per channel, and see share of voice against competitors, with every figure showing what it was counted from.
- **Guardrails**: approvals that expire when the post changes, a pre-publish link check, and daily caps that protect provider standing.
- **Self-hostable**: a self-hosted deployment owns its own provider apps and keys, nothing is shared with the hosted instance, and a network whose keys are missing is simply not offered.

## How it works

<p align="center">
  <picture>
    <source media="(prefers-color-scheme: dark)" srcset=".github/assets/flow-dark.svg">
    <img src=".github/assets/flow.svg" alt="How market.me.at works: compose, approve, schedule, publish, measure" width="880">
  </picture>
</p>

A post is composed once and previewed against each network's limits, then approved, and the approval expires if the post changes. It is placed at a set time or in a posting slot, and per-network drivers publish it with one delivery record per network, so a retry never posts twice. Delivery and engagement are then read back per channel.

## Built with

<p>
  <img src="https://img.shields.io/badge/Next.js-16-000000?style=flat-square&logo=nextdotjs&logoColor=white" alt="Next.js 16">
  <img src="https://img.shields.io/badge/React-19-171717?style=flat-square&logo=react&logoColor=white" alt="React 19">
  <img src="https://img.shields.io/badge/TypeScript-5-262626?style=flat-square&logo=typescript&logoColor=white" alt="TypeScript">
  <img src="https://img.shields.io/badge/Tailwind%20CSS-4-404040?style=flat-square&logo=tailwindcss&logoColor=white" alt="Tailwind CSS 4">
  <img src="https://img.shields.io/badge/Drizzle-Postgres-525252?style=flat-square&logo=drizzle&logoColor=white" alt="Drizzle ORM and Postgres">
  <img src="https://img.shields.io/badge/oRPC-TanStack%20Query-737373?style=flat-square&logo=reactquery&logoColor=white" alt="oRPC and TanStack Query">
</p>

- Next.js 16 (App Router), React 19, TypeScript
- Tailwind CSS 4
- Drizzle ORM + Postgres
- Better Auth
- oRPC + TanStack Query
- Per-network provider drivers behind one contract
- Optional AI analysis: Anthropic or a local model

## Part of the me.at family

market.me.at is one of my [`*.me.at`](https://me.at) apps. They share one design system, one account, and one app shell. Development happens in a private monorepo; this repository is the project's public-facing home.

## License

Source-available. See [LICENSE](LICENSE).
