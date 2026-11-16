# 🤝 Contributing to Bifoga / EnClose

Thank you for considering a contribution. This repository currently contains a static landing page and its development tooling. Contributions should preserve that scope unless a larger architectural change has been discussed and approved.

## 1. Before starting

- Read the [README](README.md) and [documentation hub](docs/README.md).
- Check existing issues and the [roadmap](ROADMAP.md).
- For a substantial architectural change, propose the problem and design before implementation.
- Never include credentials, private visitor data, or real contact submissions in examples.

## 2. Local setup

```bash
git clone https://github.com/Brajesh31/Bifoga.git
cd Bifoga
npm ci
npx serve docs
```

For Tailwind style development, run this in another terminal:

```bash
npm run tailwind
```

## 3. Working conventions

- Keep changes focused and explain the reason for each change.
- Preserve existing files, assets, and visual identity.
- Use semantic HTML and native controls where possible.
- Keep JavaScript small and avoid unsafe DOM insertion.
- Update `src/input.css` and regenerate `docs/style.css` when changing Tailwind source.
- Keep `package.json` and `package-lock.json` synchronized.
- Do not add a framework, backend, database, or dependency without a concrete need.
- Do not present the contact form as functional until a real handler is implemented and tested.

## 4. Verification

Before submitting:
- Run `npm ci`.
- Run `node --check main.js` after JavaScript changes.
- Serve `docs/` locally.
- Test page navigation, service panels, asset paths, responsive layout, and keyboard focus.
- Inspect the browser console and network panel.
- Update affected docs and diagrams.
- Include actual screenshots for visual changes.

The repository CI workflow currently performs basic static checks. It is not a substitute for manual browser and accessibility testing.

## 5. Pull requests

Use the repository pull request template. Include:
- Problem statement and intended outcome.
- Files changed and relevant design decisions.
- Verification steps and observed results.
- Accessibility, security, and privacy impact.
- Screenshots for visible changes.

## 6. Security

Report vulnerabilities privately using [SECURITY.md](SECURITY.md). Do not publish exploit details, secrets, or personal data in a public issue.

## 7. Code of conduct

Participation is governed by [CODE_OF_CONDUCT.md](CODE_OF_CONDUCT.md).
