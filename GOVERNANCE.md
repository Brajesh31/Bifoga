# 🏛️ Project Governance

## 1. Purpose

This document explains how decisions and contributions are handled in Bifoga. It supplements the repository's contribution, conduct, security, and support policies.

## 2. Project stewardship

The repository owner is responsible for:
- Reviewing and merging changes.
- Maintaining the default branch and repository settings.
- Reviewing security reports and coordinating remediation.
- Approving changes to project direction, branding, and release policy.
- Keeping project documentation aligned with the implementation.

A contributor does not gain maintainer authority merely by submitting a pull request or issue.

## 3. Decision-making

Routine changes should be evaluated on correctness, scope, accessibility, maintainability, security, and consistency with the existing static-site architecture.

Changes that introduce a backend, database, authentication, payments, AI services, or collection of personal information require explicit design review before implementation. Their operational and privacy costs must be documented.

For significant architectural changes, add an Architecture Decision Record under `docs/adr/`.

## 4. Contributions and review

All contributions are subject to the repository's `CONTRIBUTING.md` and code of conduct. Reviews should check:
- Whether the change solves a stated problem.
- Whether existing files and assets are preserved.
- Whether docs and diagrams match the code.
- Whether links and local asset paths work.
- Whether accessibility and responsive behavior are affected.
- Whether dependencies and workflows are necessary and safe.

## 5. Releases

A release should have a reviewed change summary, verified static output, and no known critical security or broken-link issue. Use the versioning guidance in `docs/release-process.md` when preparing a tagged release.

## 6. Changes to governance

Governance changes should be proposed transparently and recorded in the repository history. Security-sensitive details should be handled through the private reporting channel in `SECURITY.md`.
