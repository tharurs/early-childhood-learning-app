# Early Childhood Learning App

A parent-focused early learning app for children ages 2-5. The product supports play-based learning, real-world experiences, stories, vocabulary, values, creativity, movement, and parent-child interaction — without pressure or excessive screen time.

## Product vision

This app helps parents teach children through:
- play and everyday routines
- stories and conversations
- early language exposure
- movement and creativity
- values and social-emotional learning
- age-appropriate independence and safety habits
- English + Telugu support initially

## Core principles
- Age-appropriate learning for children ages 2–5
- No pressure for formal reading or writing at age 2
- Parent-led, low-screen experience
- Learning through real-life activities
- Focus on language, early math, values, creativity, independence, and physical development
- Support for English + Telugu from the start

## Main features
- Parent and child profiles
- Multiple children per parent
- Automatic age calculation from date of birth
- Skills and learning domains
- Daily activity recommendations
- Stories with morals and vocabulary
- English/Telugu vocabulary library
- Values and character education
- Progress tracking with no diagnostic claims

## Stack
- React Native + Expo
- Expo Router
- TypeScript
- Next.js
- PostgreSQL
- Prisma
- Supabase Auth + Storage
- Zod
- Zustand
- TanStack Query
- NativeWind
- Vitest + React Native Testing Library + Playwright

## Monorepo structure
```text
/apps
  /mobile
  /web
  /api

/packages
  /database
  /types
  /validation
  /ui
  /content
  /config
```

## MVP roadmap
1. Parent and child profile
2. Age-based home screen
3. Skills and learning categories
4. Activity database
5. Daily activity recommendations
6. Stories
7. English/Telugu vocabulary
8. Values
9. Progress tracking
10. Content management/admin system

## Local setup

1. Install dependencies:
```bash
npm install
```

2. Copy environment variables:
```bash
cp .env.example .env
```

3. Create PostgreSQL database:
```bash
createdb early_childhood_learning
```

4. Generate Prisma client:
```bash
npm run db:generate
```

5. Push schema to the database:
```bash
npm run db:push
```

6. Seed initial data:
```bash
npm run db:seed
```

7. Start the app stack:
```bash
npm run dev:mobile
npm run dev:web
npm run dev:api
```

## Environment variables
```env
DATABASE_URL="postgresql://postgres:postgres@localhost:5432/early_childhood_learning"
DIRECT_URL="postgresql://postgres:postgres@localhost:5432/early_childhood_learning"
NEXT_PUBLIC_SUPABASE_URL="https://your-project.supabase.co"
NEXT_PUBLIC_SUPABASE_ANON_KEY="your-anon-key"
SUPABASE_SERVICE_ROLE_KEY="your-service-role-key"
OPENAI_API_KEY="your-openai-key"
POSTHOG_KEY="your-posthog-key"
SENTRY_DSN="your-sentry-dsn"
NEXT_PUBLIC_APP_URL="http://localhost:3000"
```

## Database model summary
Core entities include:
- users
- children
- domains
- skills
- activities
- stories
- vocabulary
- values
- daily_plans
- skill_progress

## Content quality principles
- AI may assist with drafting, translation, and personalization
- Developmental claims should be backed by trusted sources
- Content should move through draft → review → approved → published → archived
- Source references should be captured for research-based content

## Notes
This project is intentionally structured so the content library can grow to thousands of activities and stories without changing the central architecture.

## Repository
- GitHub: https://github.com/tharurs/early-childhood-learning-app

## License
MIT
