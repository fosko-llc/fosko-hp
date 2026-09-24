# Fosko Website Agent Rules

This repository is a minimal public corporate website for Fosko LLC.

## Core principles
- Keep the site minimal, static, fast, and easy to maintain.
- Prefer the smallest safe change that satisfies the request.
- Do not introduce frameworks, build tools, dependencies, or services unless explicitly requested.
- Preserve the existing visual language and copy unless the task explicitly requires a change.
- Treat mobile behavior as a first-class requirement.
- Review the final diff before considering work complete.
- Never add secrets, credentials, API keys, private keys, `.env` contents, internal notes, customer information, or private company information to this repository.
- Do not expose residential addresses or other unnecessary personal information.
- Do not modify analytics snippets, DNS-related settings, canonical URLs, or legal text unless the task explicitly requires it.

## Current public site characteristics
- Static HTML/CSS/JavaScript
- Primary domain: `https://fosko.jp/`
- Corporate name: Fosko合同会社 / Fosko LLC
- Brand line: `Make possibility tangible.`
- Primary pages: `index.html`, `privacy.html`
- Primary visual asset: `fosko-mark.png`

## Role separation
1. **Web Designer** — visual and UX decisions. No code implementation unless explicitly asked.
2. **Web Engineer** — implementation using minimal diffs. No independent redesign or copy rewrite.
3. **Security Reviewer** — secrets, public-repo safety, third-party scripts, HTTPS, browser-side security.
4. **Legal Reviewer** — privacy, disclosures, representations, terms, compliance.
5. **QA / Release Reviewer** — final regression, mobile/desktop, links, semantics, analytics, deployment.

## Change authority
- Designer may propose visual changes.
- Engineer may implement approved changes.
- Security and Legal may block release.
- QA may block release when a regression or release defect is found.
- No role should silently expand the task.

## Default output discipline
For every task:
- State the problem.
- State the minimum change required.
- State what must not change.
- Make or propose only that change.
- Report blockers separately.
