# Security Policy

**Software Quality and Security Laboratory**

---

## What Must Never Be Committed

The following must **never** appear in any commit in this repository, including in commit history, pull-request descriptions, or issue comments:

- Passwords, passphrases, or secret answers
- API keys, access tokens, OAuth tokens, or bearer tokens
- `.env` files or any file containing environment secrets
- TLS/SSL certificates or private keys
- SSH private keys
- Database connection strings containing credentials
- Grades, final marks, or grade-related records
- Class lists, enrollment records, or teaching loads
- Signed certificates or institutional documents containing personal data
- Any personally identifiable information beyond what is required for folder naming

If you are unsure whether something is sensitive, **do not commit it**. Ask your instructor first.

---

## What to Do If a Secret Is Accidentally Exposed

1. **Do not attempt to fix it silently** by deleting the file in a later commit. Removing a secret in a new commit does **not** remove it from Git history — anyone with access to the repository can still retrieve it.
2. **Notify your instructor immediately and privately** through the official course communication channel (not through a public GitHub issue or pull-request comment).
3. The instructor will assess the exposure and determine the appropriate response, which may include:
   - Invalidating the exposed credential immediately (rotate/revoke it).
   - Rewriting repository history.
   - Reporting the incident if institutional data is affected.
4. If the exposed credential belongs to an external service (cloud provider, database, API service), revoke it from that service's dashboard **immediately**, regardless of whether the repository history is cleaned.

> **Reminder:** Reporting a secret exposure is not an academic-integrity violation. Concealing one may be.

---

## Intentionally Vulnerable Applications

Some laboratory activities require you to write or analyze intentionally vulnerable code (e.g., SQL injection, XSS, buffer overflow demonstrations).

**Rules for vulnerable code:**

- Intentionally vulnerable applications are for **controlled educational use only**.
- Vulnerable applications must **not** be deployed on public-facing production infrastructure. Run them only on your own local machine or on isolated, non-public lab environments.
- Clearly mark intentionally vulnerable code with a comment:
  ```
  # WARNING: This code is intentionally vulnerable for educational purposes.
  # Do not deploy in production.
  ```
- Never use real user data, real credentials, or real databases when demonstrating vulnerabilities.

---

## Reporting Security Issues in This Repository

If you discover a genuine security vulnerability in this repository's configuration, templates, or workflows (not in a student's intentionally vulnerable lab submission):

- **Do not** open a public GitHub issue if the report involves sensitive information.
- Contact your instructor privately through the official course communication channel.
- Provide a clear description of the issue, the potential impact, and reproduction steps if applicable.

*The instructor's contact information and official communication channel are provided through the course management system. No email address is published here.*

---

## Privacy in Pull Requests and Issues

Pull requests and issues in this repository may be visible to other students and to the public (depending on repository visibility settings).

- Do not include personal data beyond your name, student number, and section in pull-request descriptions.
- Do not post another student's personal information.
- Do not post grades, scores, or feedback in public comments.
- If an instructor's review comment inadvertently contains sensitive information, notify the instructor so it can be edited.

---

## Scope

This policy applies to all contributors to this repository, including students, instructors, and teaching assistants. Violations may result in pull-request rejection, repository access revocation, or referral to the institution's academic-integrity or data-privacy office.
