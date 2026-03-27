# Technical Guidelines

<!-- Customize this for your tech stack. Delete what doesn't apply, add what's missing. -->

## Code Standards

- Write complete, runnable code only - NO placeholders, NO omissions, NO "// ... rest of implementation"
- Include all imports, type definitions, and error handling
- Prefer explicit over implicit; verbose over clever
- All code must be copy-paste ready
- On character limits, stop abruptly; I will send "continue"

## Stack Preferences

<!-- Replace with your actual tech stack -->

| Layer | Technology |
|-------|------------|
| **Frontend** | React/Next.js with TypeScript |
| **Backend** | Python (FastAPI) or Node.js (Express/Fastify) |
| **Database** | PostgreSQL with proper migrations |
| **AI/ML** | Anthropic Claude API, OpenAI API as fallback |
| **Infrastructure** | Vercel, AWS, or GCP |

## Naming Conventions

- Use descriptive, domain-specific names
- [Your domain]-specific terminology should be accurate
- Variables: camelCase (JS/TS), snake_case (Python)
- Files: kebab-case for routes, PascalCase for components

## File Structure Convention

```
/src
  /components      # Reusable UI components
  /pages           # Route pages (Next.js) or views
  /api             # API routes/endpoints
  /lib             # Shared utilities and helpers
  /services        # Business logic and external API clients
  /types           # TypeScript type definitions
  /hooks           # Custom React hooks
  /contexts        # React context providers
/prisma            # Database schema and migrations
/tests             # Test files mirroring src structure
/docs              # Documentation
/scripts           # Build, deploy, and utility scripts
```

## Environment Variables Convention

```
# API Keys
ANTHROPIC_API_KEY=
OPENAI_API_KEY=

# Database
DATABASE_URL=
DATABASE_URL_UNPOOLED=

# Authentication
NEXTAUTH_SECRET=
NEXTAUTH_URL=

# External Services
STRIPE_SECRET_KEY=
STRIPE_WEBHOOK_SECRET=

# Feature Flags
ENABLE_AI_FEATURES=true
ENABLE_BETA_FEATURES=false
```

## Documentation Requirements

- Every function needs JSDoc/docstring with:
  - Purpose
  - Parameters with types
  - Return value
  - Example usage for complex functions
- README.md in every significant directory

## Testing Requirements

- Unit tests for all business logic
- Integration tests for API endpoints
- E2E tests for critical user flows
- Test edge cases specific to your domain thoroughly

## Security Checklist

- [ ] Input validation on all user inputs
- [ ] SQL injection prevention (use parameterized queries/ORM)
- [ ] XSS prevention (sanitize outputs)
- [ ] CSRF protection enabled
- [ ] Rate limiting on public endpoints
- [ ] Proper authentication/authorization checks
- [ ] Sensitive data encrypted at rest and in transit
- [ ] No secrets in code or version control
- [ ] Audit logging for sensitive operations
