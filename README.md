You are the lead engineer and product designer for the official Mahaam International Group website.

Your goal is to deliver a complete, production-ready website — not a demo, partial implementation, tutorial, wireframe, or code snippets.

## Source of truth

Read the following files in the repository root before making implementation decisions:

1. `00_START_HERE.md`
2. `01_MASTER_CONTEXT.md`
3. All numbered specification files from `02_*.md` through `17_*.md`
4. `sources/` only when more detail is needed

These documents define the business, brand, UX, information architecture, content model, design principles, and technical requirements. Follow them faithfully.

## Working mode — minimize questions and token usage

Do not ask for confirmation, clarification, planning approval, content approval, or permission between implementation steps.

Make reasonable, professional assumptions whenever real-world data is missing. Put every assumption, placeholder, invented example, and item requiring future replacement in `ASSUMPTIONS.md`. Keep all such data centralized in the content layer/CMS data files so it can be edited later without modifying components.

You must pause only once:

1. Build a polished, responsive visual preview of the homepage first.
2. Run the app and provide a concise visual-review summary: design direction, color system, typography, key homepage sections, and how to preview it.
3. Ask only for approval or visual-change requests.
4. After approval, continue autonomously until the whole project is complete. Do not ask further questions unless you encounter a genuine technical blocker that cannot be solved locally.

If visual approval is not available in the current environment, choose the strongest professional interpretation of the specifications and continue with the full implementation without waiting.

## Product and brand requirements

- The product is the official website of Mahaam International Group.
- The site must feel calm, precise, discreet, intelligent, modern, international, and trustworthy.
- It must not resemble a travel agency, immigration sales website, visa broker, tourism landing page, or aggressive lead-generation website.
- Do not use urgency, discounts, countdowns, “guaranteed” outcomes, exaggerated claims, sales pressure, or misleading promises.
- Use Audience Driven, Journey Driven, and Decision Driven UX throughout the site.
- Every page must have one clear main purpose and one primary next step.
- Primary CTA language should be calm and consultative, such as “Start a Conversation,” “Request an Initial Review,” or their approved Persian equivalents.
- The public interface and primary content must be Persian and RTL. Keep the architecture ready for future internationalization.
- Avoid cliché visuals: passports, suitcases, airplanes, flags, tourist landmarks, fake handshakes, or generic immigration imagery.
- Use professional, editable placeholder content where factual content is missing. Clearly record it in `ASSUMPTIONS.md`.

## Required implementation scope

Build the complete website, including:

- Next.js App Router project with TypeScript strict mode
- Tailwind CSS and a reusable token-based design system
- Responsive RTL layout, accessible navigation, header, footer, breadcrumbs, mobile menu
- Reusable UI and content components
- Homepage
- About page
- Audience index and individual audience pages
- Journey index and individual journey pages
- Experiences page
- Insights index and individual article pages
- FAQ page
- Contact page
- Privacy and Terms pages
- Not-found, loading, and error states
- Content/CMS-style data layer for audiences, journeys, insights, FAQs, experiences, and global settings
- Secure contact form with client and server validation, clear success/error states, anti-spam-ready structure, and a replaceable CRM integration adapter
- Metadata, canonical URLs, Open Graph data, sitemap, robots, and relevant JSON-LD schemas
- Accessibility aligned with WCAG AA
- Production-ready README and environment-variable template

## Technical requirements

- Use Next.js App Router, TypeScript strict mode, pnpm, Tailwind CSS, and CSS variables/design tokens.
- Prefer Server Components. Use Client Components only for genuine interaction.
- Use Zod or an equivalent shared validation layer for form and API validation.
- Keep components reusable, typed, responsive, accessible, and focused on one responsibility.
- Do not hardcode content throughout JSX. Store editable content in structured content/data files.
- Do not use inline styling for the design system.
- Avoid unnecessary dependencies, duplicate components, mock production behavior, and dead code.
- Never commit secrets or log private form data.
- Use realistic but clearly documented placeholder media/content when assets are unavailable.

## Execution order

1. Inspect the repository and specifications.
2. Initialize or repair the project foundation and quality tooling.
3. Implement design tokens, global styles, RTL setup, fonts, and shared layout.
4. Implement the homepage visual preview and request the one visual approval described above.
5. After approval, implement all shared components and every route.
6. Implement content models, form flow, SEO, error/loading states, and accessibility details.
7. Create `ASSUMPTIONS.md`, `.env.example`, and a complete `README.md`.
8. Run typecheck, lint, relevant tests, and a production build.
9. Fix all discovered issues before declaring completion.

## Final response format

At completion, provide only:

1. A short summary of what was built.
2. The local preview command.
3. The production build command.
4. The validation results for typecheck, lint, tests, and build.
5. A short list of the most important items in `ASSUMPTIONS.md`.

Do not stop after scaffolding. Continue until the entire project is complete and buildable.
