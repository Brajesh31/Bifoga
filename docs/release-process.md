# 🚢 Release Process

## 1. Release model

The repository is a static website with npm development tooling. A release consists of a reviewed source state and the corresponding static files served by the chosen host. No automated production deployment is assumed by this guide.

## 2. Before release

- Review the complete diff against the previous release.
- Run `npm ci` from a clean checkout.
- Regenerate CSS using the documented Tailwind command if styles changed.
- Serve the `docs/` directory and inspect the page.
- Check navigation, tab behavior, local assets, mobile layout, and keyboard access.
- Confirm the contact form is not presented as operational unless a real handler is deployed.
- Verify README links, diagrams, and version information.
- Review dependency and workflow changes.
- Confirm no secrets, local machine files, or unlicensed assets are included.

## 3. Versioning

Use Semantic Versioning when the project begins publishing tagged versions:
- MAJOR: incompatible public or operational change.
- MINOR: backward-compatible feature addition.
- PATCH: backward-compatible fix.

Do not invent a release number or claim a deployment occurred without a corresponding tag or host deployment record.

## 4. Release notes

Summarize user-visible changes, maintenance changes, known limitations, and migration steps. Update `CHANGELOG.md` with changes that have actually shipped.

## 5. Rollback

For a static-hosted release, restore the last known-good deployed artifact or redeploy the last known-good commit. Verify the restored page and asset paths. Preserve logs needed to understand the incident without retaining unnecessary visitor data.
