# Installation

Install Node.js and npm, then run:

```powershell
npm ci
npx serve docs
```

Open the URL printed by the static server. A local server is preferred because the page uses root-relative resources and a form target.

For Tailwind development, run `npm run tailwind`. The command watches `src/input.css` and writes `docs/style.css`.
