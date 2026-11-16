# 🚀 Runbook: Static Release

## Purpose

Prepare a reviewed static-site change for publication by the configured hosting owner.

## Pre-release checklist

- [ ] Confirm the target commit and branch.
- [ ] Review the complete diff and ensure original files were not removed unintentionally.
- [ ] Run `npm ci`.
- [ ] Regenerate Tailwind output if relevant styles changed.
- [ ] Serve the `docs/` directory locally.
- [ ] Verify page load, links, images, navigation and tab interaction.
- [ ] Check keyboard navigation, focus indicators and mobile reflow.
- [ ] Confirm the contact form is not represented as operational without a real handler.
- [ ] Review dependencies and workflow permissions.
- [ ] Confirm no secrets or private data are included.
- [ ] Confirm the release notes describe only changes actually included.

## Publication

Use the deployment procedure for the actual hosting provider. This repository does not define a provider-specific production deployment command. Do not assume GitHub Pages or another host is configured based solely on the presence of a static `docs/` directory.

## Post-release verification

1. Open the public URL over HTTPS.
2. Verify the page and all assets load from the deployed paths.
3. Test key navigation and responsive layout.
4. Check browser console and network errors.
5. Record the deployed commit and deployment timestamp in the release record.

## Rollback

Restore the previous known-good static artifact or redeploy the previous verified commit through the hosting provider. Verify the restored site and record the incident.
