# Academic Website Style Guide

## 1. Design intent

Create a personal academic website that feels:

- Fresh and modern
- Calm, readable, and content-first
- Personal rather than institutional
- Structured enough for serious academic material
- Lightweight and easy to maintain

The site should take inspiration from the restraint and editorial clarity of [elliptic.space](https://elliptic.space/), without copying its layout, typography, wording, or visual identity.

## 2. Core principles

### Clarity over density

Every page should have one obvious purpose. Use short introductions, descriptive headings, and generous spacing. Avoid making visitors decode a dashboard.

### Content over interface

Academic content should remain the primary visual element. Prefer plain links, lists, and paragraphs to cards, filters, badges, accordions, or decorative UI.

### Personality over polish

Use a direct, conversational voice. The site should feel like a thoughtful person’s home on the web, not a university template or personal-brand landing page.

### Quiet confidence

Use a restrained visual system with one distinctive accent. Motion, decoration, and visual effects should support orientation—not compete with the content.

### Maintainability

Prefer semantic HTML, simple CSS, static content, and minimal JavaScript. New pages should be easy to add without introducing a new component system or content workflow.

## 3. Information architecture

Recommended primary navigation:

1. About
2. Research
3. Publications
4. Teaching
5. Talks
6. CV

Optional links can include Code, Notes, or Contact, but the primary navigation should remain compact.

### Homepage

The homepage should answer four questions quickly:

- Who is this?
- What do they work on?
- Where are they based or affiliated?
- Where should I go next?

Suggested sections:

1. Name and role
2. One-paragraph introduction
3. Current research interests
4. Selected links or recent work
5. Contact details

### Content pages

Each content page should use the same basic rhythm:

1. Page title
2. Brief orientation paragraph
3. Clearly grouped content
4. Useful links and downloads

Avoid turning every category into a separate visual module.

## 4. Visual direction

### Overall character

- Light, spacious, and editorial
- Mostly neutral surfaces
- Dark, high-contrast text
- One memorable accent color for links and selected details
- Subtle geometric or mathematical references are welcome
- No gradients, glassmorphism, excessive shadows, or decorative noise

### Distinctive elements

The site should establish its own identity through a small number of choices:

- A recognizable type pairing
- A consistent accent color
- A small personal mark or geometric motif
- A non-generic homepage composition
- Carefully written microcopy

These elements should be used consistently, not repeated everywhere.

## 5. Layout system

### Page frame

- Full-width outer background
- Centered content frame
- Comfortable horizontal padding on small screens
- A readable text measure rather than a wide, dashboard-like layout

Suggested starting values:

```css
:root {
  --content-max: 72rem;
  --reading-max: 46rem;
  --page-gutter: clamp(1.25rem, 4vw, 4rem);
  --section-gap: clamp(3rem, 8vw, 7rem);
}
```

### Navigation

Navigation should be compact, persistent, and easy to scan. It may sit in a slim top bar or a small side rail, but it should not dominate the page.

Use:

- Clear active-page state
- Text links with generous hit areas
- A simple mobile menu if needed
- No large hero navigation or oversized button groups

### Responsive behavior

The design should adapt by reflowing, not by hiding important content. On small screens:

- Collapse navigation cleanly
- Preserve readable line length
- Keep headings proportional
- Stack multi-column sections
- Keep contact and publication links easy to use

## 6. Typography

Typography should feel contemporary and literary, with excellent support for mathematical notation and long academic titles.

Recommended hierarchy:

- Display/name: distinctive but restrained
- Page titles: clear and confident
- Section headings: compact and informative
- Body: highly readable, comfortable line height
- Metadata: smaller, quieter, but still accessible

Starting tokens:

```css
:root {
  --font-sans: "Inter", "Avenir Next", system-ui, sans-serif;
  --font-serif: "Source Serif 4", Georgia, serif;
  --font-mono: "IBM Plex Mono", ui-monospace, monospace;

  --text-base: 1.05rem;
  --leading-body: 1.7;
  --tracking-tight: -0.02em;
}
```

Use a serif or humanist face for body copy only if it improves the site’s personality and remains comfortable for lists and technical prose. Mathematical notation must remain legible.

## 7. Color

Begin with a neutral foundation and one accent. The final palette should be selected after the typography and personal mark are chosen.

```css
:root {
  --color-bg: #f8f8f5;
  --color-surface: #ffffff;
  --color-text: #202124;
  --color-muted: #6b6d70;
  --color-rule: #dedfda;
  --color-accent: #315c8c;
  --color-accent-hover: #21466e;
}
```

Guidelines:

- Body text must meet accessible contrast requirements.
- Accent color is for links, active states, and occasional emphasis.
- Do not introduce a new color for every section.
- Links should be visibly identifiable without relying only on hover.

## 8. Components and patterns

Keep the component vocabulary small:

- Site header and navigation
- Intro/profile block
- Section heading
- Publication list
- Talk or event list
- Link group
- Metadata line
- Footer/contact block

Prefer semantic lists for publications, talks, courses, and code projects. Use cards only when each item genuinely needs separation or a visual preview.

### Publications

Each entry should prioritize:

1. Title
2. Authors
3. Venue or status
4. Year
5. Links such as PDF, DOI, arXiv, or code

Avoid oversized publication cards and decorative thumbnails unless a visual abstract is important.

### Research

Organize research by meaningful themes rather than by technology or page type. Each theme should begin with a short explanation before linking to papers or projects.

### Teaching

Use a concise list of courses, notes, and advising information. Make expectations and contact guidance explicit, but keep the tone welcoming.

## 9. Content voice

Write in first person when appropriate. Be specific, concrete, and modest.

Prefer:

> I study mathematical questions arising in quantum information, with a focus on …

Over:

> My research interests encompass a broad range of interdisciplinary topics …

Avoid:

- Marketing language
- Generic claims about being passionate or innovative
- Long institutional biographies
- Unexplained acronyms
- Dense blocks of unstructured publication metadata

## 10. Motion and interaction

Interaction should be subtle and functional:

- Short link and navigation transitions are acceptable.
- Avoid scroll-jacking, parallax, animated backgrounds, and attention-grabbing loaders.
- Respect `prefers-reduced-motion`.
- Every important destination must work without JavaScript.

## 11. Technical guardrails

- Use semantic HTML and accessible landmarks.
- Keep the site usable with keyboard navigation.
- Make external links visually and programmatically clear.
- Optimize for fast initial load.
- Keep content separate from presentation where practical.
- Do not add a framework, CMS, or animation library without a clear need.
- Test the site at mobile, tablet, and desktop widths.
- Check long paper titles, author lists, and mathematical notation explicitly.

## 12. Definition of done

A page is ready when:

- Its purpose is clear within a few seconds.
- The typography is comfortable for sustained reading.
- The page works without JavaScript.
- Navigation remains obvious on mobile.
- Links, downloads, and external destinations are easy to identify.
- The page feels like part of the same personal site without looking repetitive.
- It has a distinct identity rather than resembling a direct copy of elliptic.space.

