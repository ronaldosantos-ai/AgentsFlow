# AgentsFlow SaaS

## Overview
AgentsFlow is a single-tenant SaaS for WhatsApp marketing automation, built with Next.js 16 (App Router), React 19, Supabase (PostgreSQL), and Upstash QStash. It integrates Meta WhatsApp Cloud API for template messaging and Vercel AI SDK v6 for content generation.

## Recent Changes
- 2026-02-11: Initial Replit setup. Configured Next.js for port 5000, allowed all dev origins, removed X-Frame-Options SAMEORIGIN header for iframe compatibility.

## Project Architecture
- **Framework**: Next.js 16 with Turbopack, React 19, TypeScript
- **Styling**: Tailwind CSS v4, shadcn/ui (new-york style)
- **Database**: Supabase (PostgreSQL)
- **Queue**: Upstash QStash
- **AI**: Vercel AI SDK v6 with multiple providers (OpenAI, Anthropic, Google, Cohere)
- **Auth**: Single-tenant, master password login + API keys

### Key Directories
```
app/           - Next.js App Router (auth, dashboard, API routes)
components/    - UI components (features, ui, builder)
hooks/         - Controller hooks (React Query pattern)
services/      - API client layer
lib/           - Business logic & utilities
supabase/      - SQL migrations
```

### Frontend Pattern
Page -> Hook -> Service -> API Route -> Supabase DB

## User Preferences
- Code in English, comments/docs/UI in Portuguese (pt-BR)
- Primary colors: emerald/green (primary-400/500/600)
- Icons: lucide-react exclusively

## Running
- Dev server: `npx next dev --turbopack -H 0.0.0.0 -p 5000`
- Build: `npm run build`
- Production: `npm run start`
