# Fosko Website Workflow

## Standard flow

```text
Request
  ↓
Designer
  ↓
Engineer
  ↓
Security Review
  ↓
Legal Review
  ↓
QA / Release Review
  ↓
Deploy / Release
```

Keep review depth proportional to the change.

## 1. Task brief
Every task starts with:
- Objective
- Files in scope
- Expected visible outcome
- What must not change
- Whether copy/legal/security behavior is affected

## 2. Designer handoff
Use for appearance, layout, typography, hierarchy, responsive behavior, or UX.

Designer outputs:
- Problem
- Intended outcome
- Exact affected elements
- Constraints
- Minimal implementation direction

Designer does not implement.

## 3. Engineer implementation
Engineer:
- Reads the task and Designer handoff.
- Makes the smallest safe diff.
- Does not broaden scope.
- Does not rewrite copy unless approved.
- Preserves unrelated behavior.
- Reviews the diff.

Engineer handoff:
- Files changed
- What changed
- What was intentionally not changed
- Any unresolved issue

## 4. Security review
Required when changes affect public repo contents, external scripts/services, analytics, forms, authentication, user data, deployment, DNS/domain behavior, or new dependencies.

## 5. Legal review
Required when changes affect privacy, analytics/tracking, company information, claims/representations, contact/data collection, terms, payments, user accounts, marketing, or recruitment.

## 6. QA / Release
At minimum:
- Desktop
- Mobile
- Navigation
- Links
- No overlap/regression
- HTTPS
- Production deployment

## Fast path for tiny changes
```text
Request
  ↓
Designer (only if visual judgment is needed)
  ↓
Engineer
  ↓
Targeted Security/Legal check only if affected
  ↓
QA
```

Avoid unnecessary agent work.

## Stop conditions
Do not release if:
- A Security BLOCKER exists.
- A LEGAL BLOCKER exists.
- QA returns FAIL.
- The requested outcome is not met.
- The diff contains unexplained unrelated changes.

## Public repository rule
Only information safe for public disclosure belongs here.
Internal business plans, customer data, private legal discussions, credentials, and sensitive operational information belong elsewhere.
