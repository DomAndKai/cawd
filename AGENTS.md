# Repository Guidelines

## Project Structure & Module Organization

This repository contains the public-facing static site for Cawd, including the landing page, privacy policy, and visual assets. Keep root pages such as `index.html` and `privacy.html` simple and GitHub Pages-friendly. Store brand images, screenshots, and icons in `assets/`. Place tests beside the code they cover or in a top-level `tests/` directory if a test setup is added, and avoid committing generated output such as `dist/`, `.next/`, `coverage/`, or `node_modules/`.

## Build, Test, and Development Commands

No package manifest or build scripts are present yet. Once a frontend stack is added, document the canonical commands here and keep them aligned with `package.json`.

Expected command patterns:

```sh
npm install      # install project dependencies
npm run dev      # start the local development server
npm run build    # create the production build
npm test         # run the test suite
npm run lint     # run static checks
```

If the site remains static HTML/CSS, include the exact local preview command, such as `python3 -m http.server 8000`.

## Coding Style & Naming Conventions

Use consistent two-space indentation for JavaScript, TypeScript, JSON, CSS, HTML, and Markdown. Prefer descriptive, product-oriented names such as `PrivacyPolicy`, `HeroSection`, or `cawd-feature-card` over abbreviations. Keep copy concise and user-facing; this repository represents public Cawd content, so avoid placeholder text in committed pages. If formatting or linting tools are introduced, make them runnable through `npm run format` and `npm run lint`.

## Testing Guidelines

There is no test framework configured yet. When adding one, prefer focused tests for page rendering, routing, forms, analytics events, and policy-page availability. Name tests after the behavior under test, for example `privacy-policy.spec.ts` or `landing-page.test.tsx`. Add regression tests for bugs that affect public content, accessibility, or conversion flows.

## Commit & Pull Request Guidelines

Git history currently shows a single `Initial commit`, so no detailed convention has been established. Use short, imperative commit messages, for example `Add privacy policy page` or `Update landing page copy`. Pull requests should include a concise summary, testing notes, linked issue when applicable, and screenshots or screen recordings for visual changes. Call out any changes to public legal copy, analytics, or environment configuration.

## Security & Configuration Tips

Do not commit secrets, local `.env` files, API keys, analytics tokens, or production credentials. Use `.env.example` for documented configuration values, and keep generated caches and build artifacts ignored.
