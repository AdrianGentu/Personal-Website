<!-- .github/copilot-instructions.md - Project-specific guidance for AI coding agents -->

This repository is a minimal, single-page personal website. Use these instructions to be immediately productive and avoid generic, irrelevant suggestions.

1) Project Big Picture
- Purpose: A static personal website with a single entry point at `index.html`.
- Structure: There are no build tools, package managers, or backend services — edits are made directly to `index.html` and static assets.

2) Key Files to Inspect
- `index.html`: single-page HTML. Heading and styling live here (Google Fonts are used for the main heading).
- `README.md`: repository description (no build/test info present).

3) Developer Workflow / Commands
- There is no build or test system. To preview changes, open `index.html` in a browser or use a local static preview from an editor (e.g., Live Server).
- Recommended commit style: small, focused commits. Example: `git add index.html && git commit -m "Header: use Merriweather font and add heading"`.

4) Project-specific Patterns & Conventions
- Semantic HTML: Prefer proper heading tags (`<h1>...`), not custom/unclosed tags. See `index.html` for examples.
- Fonts: Google Fonts are loaded directly via `<link>` in the `<head>`; update that link when changing heading typography.
- Styling: Minimal inline `<style>` exists in `index.html`; follow that pattern for small, page-scoped styles rather than introducing large CSS frameworks.

5) Examples (explicit edits you may be asked to make)
- Change the page heading text: edit the `<h1 class="site-heading">Adrian Gentu</h1>` line in `index.html`.
- Change the heading font: update the Google Fonts `href` in the `<head>` and adjust `.site-heading` font-family.

6) Integration Points & External Dependencies
- External: Google Fonts (network call from the page). No other external services are configured.
- No CI/CD, no automated tests, no package.json — assume manual edits and manual previews.

7) What Not To Suggest
- Do not suggest adding complex build tooling, test runners, or dependency managers unless the maintainer requests them.
- Avoid scaffolding a backend or server; this repo is intended as a static site.

8) When Asked About Model / Platform Settings
- If a user requests enabling or changing model offerings (for example, "Enable GPT-5 mini for all clients"), explain that this is an administrative/platform operation and cannot be changed from within the repository. Provide next steps: contact platform admin or follow the hosting/service provider's admin console documentation.

9) Quick patch example
To change the heading text and font, modify `index.html` as shown below:

```html
<!-- head includes Google Fonts -->
<link href="https://fonts.googleapis.com/css2?family=Merriweather:wght@700&display=swap" rel="stylesheet">
<!-- body -->
<h1 class="site-heading">Your Name Here</h1>
```

10) If you need more context
- Open `index.html` and `README.md`. If asked to add pages or tooling, first confirm whether the maintainer wants to keep the site static.

Keep guidance concise, prefer minimal changes, and always reference `index.html` as the source of truth for UI/text edits.
