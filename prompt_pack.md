# Prompt Pack — InnovatePro Assignment

This file contains a canonical, reusable set of prompts to generate five website sections using Tailwind CSS. Use these prompts verbatim in your preferred AI/code generation tool (ChatGPT, Claude, etc.). They are intentionally long, detailed, and structured so they produce consistent, high-quality HTML + Tailwind outputs.

---

## Meta-Prompt (Run once before section prompts)

You are an expert Front-End Development AI Assistant specializing in generating clean, modern, accessible, and responsive UI components using HTML and Tailwind CSS (v3+ syntax). Follow these constraints for every output:

- Output ONLY the pure HTML snippet (or full HTML file when requested) with inline Tailwind utility classes; do NOT include any surrounding explanation, markdown, or commentary.
- Do NOT include any external CSS files; using Tailwind utility classes only is required. You may include a small inline `<script>` only if necessary for minimal UI interactions (e.g., mobile menu toggle) and keep it vanilla JS, no frameworks.
- Use a minimalist, professional aesthetic suitable for a B2B SaaS company.
- Primary accent color: `indigo-600`. Neutral background and text colors: whites/grays/blacks. Use accessible contrast ratios (WCAG AA) for text and CTA buttons.
- Typography: use a system UI stack (e.g., `ui-sans-serif, system-ui, -apple-system, "Segoe UI", Roboto`). Keep font-size scales consistent (mobile first). Use `text-3xl/4xl/5xl` for hero headings as appropriate.
- Spacing scale: mobile: `p-4`–`p-8`, desktop sections: `p-8`–`p-16`. Use consistent gaps between elements.
- Responsiveness: use Tailwind breakpoints `sm:`, `md:`, `lg:`. Ensure mobile-first layout stacks vertically and desktop uses multi-column layouts where specified.
- Accessibility: add `role`, `aria-label`, `aria-expanded`, and `sr-only` where appropriate. Ensure interactive elements have visible focus styles (e.g., `focus:outline-none focus:ring-2 focus:ring-indigo-300`). Use semantic HTML (`nav`, `header`, `main`, `section`, `footer`, `form`, appropriate headings).
- Images: use descriptive `alt` text and `loading="lazy"` for non-critical images. Use placeholder comments or Unsplash/Undraw links when needed.
- Mobile menu: if included, implement minimal JS toggle that updates `aria-expanded` and manages focus.
- Output must be self-contained and render correctly with the Tailwind CDN: `<script src="https://cdn.tailwindcss.com"></script>` if a full HTML file is requested.

---

## 1) Navigation Bar Prompt

Generate a sticky, top-aligned, responsive Navigation Bar component in Tailwind CSS with the following exact requirements. Output only the HTML snippet (or full header block) with minimal JS for mobile toggle:

- Container: centered within `max-w-7xl mx-auto` with `px-4 sm:px-8 lg:px-16` and vertical padding matching the section scale.
- Left: Brand name text (use placeholder `InnovatePro`) styled bold and legible.
- Center: Four navigation links: `Product`, `Solutions`, `Resources`, `Blog`. Links should have subtle hover color change and visible focus rings.
- Right: two actions: a `Sign In` text link and a primary `Sign Up` button styled with `bg-indigo-600 text-white` and hover darkening (`hover:bg-indigo-700`). Both must be keyboard-accessible and have focus styles.
- Behavior: On screens `<768px`, collapse the nav into an off-canvas mobile menu triggered by a button. Use only minimal vanilla JS for toggling and update `aria-expanded` on the button and `aria-hidden` on the menu. When opened, the first link in the menu should receive focus.
- Accessibility: Add `role="navigation" aria-label="Main Navigation"` to the header. Use `sr-only` labels where appropriate.

---

## 2) Hero Section Prompt

Generate a responsive hero section (two-column on desktop, stacked on mobile) that follows these rules. Output pure HTML/Tailwind:

- Left column: headline (very large, bold), subtext paragraph (smoke-gray), and two CTAs: primary (indigo-600) and secondary (text link). Primary CTA should be prominent and accessible.
- Right column: an image container with rounded corners and subtle shadow. Provide an Unsplash or Undraw placeholder image and include descriptive `alt` text and `loading="lazy"`.
- Layout: On mobile the text stacks above the image and is centered; on large screens text left-aligned and a two-column split using `lg:grid lg:grid-cols-2`.
- Spacing: `py-8` mobile, `py-16` on desktop (use `sm:`, `lg:` accordingly).

---

## 3) Services / Features Section Prompt

Generate a features section with a centered small subheading (e.g., "Our Capabilities") and a main title (e.g., "Designed for Scale"). Provide 3–6 feature cards; the prompt should produce exactly six. Requirements for each card:

- Icon placeholder at top-left in a circular indigo-50 background with `text-indigo-600` icon SVG.
- Card should include a bold title and a short description (1–2 lines) using muted gray text.
- Layout must be `grid-cols-1` on mobile, `sm:grid-cols-2` on tablet, `lg:grid-cols-3` on desktop, with consistent gaps.
- Card style: subtle border, rounded corners, small shadow, and generous padding.

---

## 4) Contact / Lead Form Prompt

Generate a left-aligned contact form with these fields: `Name`, `Email Address`, `Company Name`, `Message` (textarea), a required privacy checkbox, and a full-width submit button styled `bg-indigo-600 text-white`.

- Inputs should use clear placeholder text, `required` attributes where appropriate, and `aria` labels (or use `<label class="sr-only">`).
- Form layout: single column on mobile, two-column optional layout only for supporting text or side content. For this task return a form that is responsive and full-width on mobile.
- Include minimal client-side validation attributes (e.g., `type="email" required`) and use `novalidate` only if you plan to implement custom validation (do NOT add `novalidate`).

---

## 5) Footer Prompt

Generate a dark footer (`bg-gray-900 text-gray-300`) with a four column layout on desktop:

- Column 1: Brand name and one-line mission statement.
- Column 2: `Product` links (4 items).
- Column 3: `Company` links (4 items).
- Column 4: `Resources` links (4 items).
- Bottom: a thin border-top, social icon placeholders (X, LinkedIn, Facebook), and a copyright line format `© 2025 InnovatePro. All rights reserved.`

---

## Usage Notes

- Run the Meta-Prompt first to set the stylistic rules, then run each section prompt separately to get consistent outputs.
- If you need a single-page result, ask the model to "Combine all sections into a single responsive page using the same Tailwind constraints; deliver only the full HTML file that includes the Tailwind CDN script." Use the meta-prompt constraints for final verification.

---

End of Prompt Pack.
