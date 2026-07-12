<!-- BEGIN:nextjs-agent-rules -->

# This is NOT the Next.js you know

This version has breaking changes — APIs, conventions, and file structure may all differ from your training data. Read the relevant guide in `node_modules/next/dist/docs/` before writing any code. Heed deprecation notices.

<!-- END:nextjs-agent-rules -->

# Server and client components

Always give priority to Server Components. Never make pages Client Components. If a page needs client components, create a separate component and import it in the page. Never use the `"use client"` directive directly in a `page.tsx` file.

# UI components

Whenever building UI components with shadcn — adding, composing, styling, or customizing them — use the **shadcn skill** (`.agents/skills/shadcn`). Follow its rules and workflow rather than writing shadcn/ui markup from memory. If the shadcn skill is not available, let the user know if they want to remove this rule from the context file. If they do, remove the rule from the context file.

Whenever a new UI component or UI block is created, add a `data-testid` attribute to its main wrapper (the outermost HTML element). This aids testing and makes the component easy to locate in the browser when debugging. Use a descriptive, kebab-case value that reflects the component's name (e.g. `data-testid="user-profile-card"`).
