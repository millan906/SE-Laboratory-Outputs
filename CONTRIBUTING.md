# Contributing Guidelines

**Software Quality and Security Laboratory**

These rules define what students may and may not change in this repository. Violations may result in pull-request rejection or academic-integrity review.

---

## Scope of Permitted Changes

Students may **only** modify files inside their own assigned submission folder:

```
laboratories/lab-XX/section/student-number-surname-given-name/
```

**Everything outside that folder is off-limits.** Do not edit, rename, move, or delete any file that is not inside your assigned folder.

---

## Folder and Branch Naming Requirements

### Submission Folder

```
laboratories/lab-XX/section/student-number-surname-given-name/
```

| Part | Format | Example |
|---|---|---|
| `lab-XX` | Two-digit, zero-padded | `lab-01`, `lab-12` |
| `section` | Lowercase, hyphens | `bscs-3a`, `bsit-2b` |
| `student-number` | Institutional format | `2026-0001` |
| `surname` | Lowercase, hyphens | `dela-cruz` |
| `given-name` | Lowercase, hyphens | `juan-miguel` |

**Full example:** `laboratories/lab-01/bscs-3a/2026-0001-dela-cruz-juan/`

### Branch Name

```
lab-XX-student-number
```

**Example:** `lab-01-2026-0001`

One branch per laboratory. Do not reuse the same branch for multiple laboratories.

### Pull-Request Title

```
[LAB-XX][SECTION] StudentNumber Surname, GivenName
```

**Example:** `[LAB-01][BSCS-3A] 2026-0001 Dela Cruz, Juan`

---

## Commit Message Conventions

Use [Conventional Commits](https://www.conventionalcommits.org/):

```
type(scope): short description in imperative mood
```

| Type | When to use |
|---|---|
| `feat` | New work, new file, new feature |
| `fix` | Correcting a defect or addressing review feedback |
| `docs` | Documentation only (reports, README) |
| `test` | Adding or updating tests |
| `refactor` | Restructuring without changing behavior |

**Examples:**

```
feat(lab-01): implement static analysis with PMD
fix(lab-02): correct SQL injection vulnerability
docs(lab-01): add laboratory report and reflection
test(lab-03): add unit tests for authentication module
```

**Rules:**
- Keep the subject line under 72 characters.
- Write in imperative mood ("add", not "added").
- Reference the specific lab in the scope.
- Do not write vague messages like `update`, `fix stuff`, or `final final`.

---

## Required Evidence and Documentation

Each submission folder must contain:

| Item | Location | Required |
|---|---|---|
| Completed student README | `README.md` | Yes |
| Source code | `src/` | Yes |
| Tests | `tests/` | Yes |
| Screenshots of running program and test results | `screenshots/` | Yes |
| Laboratory report | `reports/` | Yes |

Use the templates in the `templates/` folder. Copy them into your folder and fill in every section.

---

## Initial Submission Procedure

1. Sync your fork from `upstream` (see [SUBMISSION_GUIDE.md](SUBMISSION_GUIDE.md)).
2. Create a new branch: `lab-XX-STUDENT-NUMBER`.
3. Create your folder at the correct path.
4. Copy and complete templates.
5. Add source code, tests, screenshots, and reports.
6. Commit with a meaningful message.
7. Push to your fork.
8. Open **one** pull request to `millan906/SE-Laboratory-Outputs` with the required title.

---

## Correction and Resubmission Procedure

When the instructor requests changes:

1. Read each review comment.
2. Make the required corrections locally.
3. Commit with `fix(lab-XX): address review — DESCRIPTION`.
4. Push to the **same branch**.

The open pull request updates automatically. Do **not** open a new pull request.

---

## Citing External Code, Libraries, Tutorials, and AI Assistance

### External Code or Libraries

If you copied, adapted, or studied code from any external source:
- Add a comment in the source file identifying the origin.
- Include the URL, author, license, and date accessed.
- Document the citation in your laboratory report's References section.

```python
# Adapted from: https://example.com/source-article
# Author: Jane Smith | License: MIT | Accessed: 2026-08-01
```

### AI Assistance

If you used any AI tool (ChatGPT, GitHub Copilot, Claude, Gemini, etc.):
- Disclose the tool name, the prompt or task you gave it, and what you used from its output.
- Document this in the AI-assistance disclosure section of your student README and laboratory report.
- Course policy on AI assistance is **instructor-defined** — follow your instructor's specific guidelines.

Undisclosed AI assistance may be treated as academic dishonesty.

---

## Prohibited Actions

The following will result in immediate pull-request rejection and possible academic-integrity review:

- Modifying any file outside your assigned submission folder.
- Editing, overwriting, or deleting another student's files.
- Including passwords, tokens, API keys, `.env` files, certificates, or private keys.
- Including grades, class lists, or personal student records.
- Submitting work that is not your own without proper citation.
- Opening duplicate pull requests for the same laboratory.
- Using force-push (`git push --force`) to rewrite shared history.
- Attempting to merge your own pull request.

---

## Pull-Request Rejection Conditions

Pull requests may be rejected without review if they:

- Are missing required files or documentation.
- Contain files outside the student's assigned folder.
- Have malformed folder or branch names.
- Include unrelated changes to other parts of the repository.
- Contain prohibited content (secrets, personal data, etc.).
- Have a title that does not match the required format.

A rejected pull request is **not** an accepted submission. The student must fix the issue and resubmit before the deadline.

---

## Questions

Contact your instructor through the official course channel. Do not ask for grade information in pull-request comments or GitHub issues.
