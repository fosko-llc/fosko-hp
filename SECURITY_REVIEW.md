# Fosko Web Security Review

Review first. Do not modify code unless explicitly asked.

## 1. Secrets and repository exposure
Check for API keys, access tokens, passwords, private keys, `.env` files, credentials, internal endpoints, private notes, customer/partner information, unnecessary personal information, and sensitive Git history.

Any confirmed secret in the repository or Git history is a **BLOCKER**.

## 2. Third-party resources
Review fonts, analytics, scripts, images, and APIs.
Confirm HTTPS, necessity, intentional use, and absence of unexpected tracking.

## 3. Browser-side security
Check for unsafe DOM injection, `innerHTML` with untrusted content, dynamic script creation, mixed content, unsafe external links, unnecessary storage, unexpected cookies, and exposed internal endpoints.

## 4. Public deployment
Confirm HTTPS, correct custom domain, correct canonical URLs, no unintended published files, and no exposed backups/dumps/temp artifacts.

## 5. Analytics and privacy alignment
Confirm actual analytics behavior matches `privacy.html`.

## Severity
- **BLOCKER**
- **SHOULD FIX**
- **ACCEPTABLE**
- **INFORMATIONAL**

For every BLOCKER or SHOULD FIX:
- Exact file / section
- Concrete issue
- Why it matters
- Minimum corrective action

Do not recommend security tooling without a concrete need.
