# Documentation project instructions

## About this project

- This is API documentation for **Vision** — a computer vision product for churches that counts and identifies demographic info of church attendees
- Built on [Mintlify](https://mintlify.com) using OpenAPI-driven endpoint documentation
- Pages are MDX files with YAML frontmatter referencing the OpenAPI spec
- Configuration lives in `docs.json`
- OpenAPI specification at `api-reference/openapi.json`
- Run `npx mintlify dev` to preview locally

## Terminology

- **Vision**: The computer vision product — always capitalize
- **Event**: A church service or gathering being tracked (not a generic software event)
- **Capture Session**: A video capture run from a single camera during an event
- **Capture Source**: A camera/RTSP stream configuration (not "camera" in the API)
- **Capture Device**: Physical IoT hardware running capture sources
- **Person Track**: A continuous detection of one person in a video
- **Face Match**: Cross-event face comparison result with similarity score
- **Individual**: A church member record in the broader system (distinct from Vision's "Person")
- Use "staff user" not "authenticated user" when describing auth requirements
- Use "admin user" for billing/credits endpoints

## Style preferences

- Use active voice and second person ("you")
- Keep sentences concise — one idea per sentence
- Use sentence case for headings
- Include permission requirements in endpoint descriptions
- Document behavioral constraints (e.g., locked events, polygon requirements)
- Write for LLM agent consumption — be precise and unambiguous

## Content boundaries

- Only document customer-facing Vision API endpoints
- Do not document internal/employee-only endpoints (workflow runs, processing jobs, internal device management)
- Focus on API endpoint documentation, not how-to guides or tutorials
- The OpenAPI spec is the source of truth for endpoint details
