# Architecture

EnClose is a static page. `docs/index.html` contains navigation, hero, services, and contact markup. `docs/style.css` contains generated Tailwind output plus custom styles imported from `src/input.css`. `main.js` exposes `openMenu`, which hides service panels and displays the selected panel.

There is no application server, database, authentication, or API in this repository. External W3.CSS and Google Fonts resources are loaded by the page.
