# SE-Laboratory-Outputs

**Software Quality and Security Laboratory**
Instructor-controlled central repository for student laboratory submissions.

---

## Purpose

This repository is the official submission hub for the **Software Quality and Security Laboratory** course. Students do **not** push directly to this repository. Instead, each student forks this repository, does their work in their personal fork, and opens a pull request back here for instructor review.

Grades, class lists, teaching loads, signed certificates, and any other sensitive student records must **never** be stored in this repository.

---

## Submission Workflow

```
Student forks repository
  → clones personal fork
  → creates lab-specific branch
  → adds work only inside assigned folder
  → commits and pushes to fork
  → opens pull request to this repository
  → instructor reviews
  → student pushes corrections to same branch / pull request
  → instructor approves and merges
```

See [SUBMISSION_GUIDE.md](SUBMISSION_GUIDE.md) for full step-by-step instructions.

---

## Required Directory Structure

```
laboratories/lab-XX/section/student-number-surname-given-name/
```

**Example:**

```
laboratories/lab-01/bscs-3a/2026-0001-dela-cruz-juan/
├── README.md
├── src/
├── tests/
├── screenshots/
└── reports/
```

### Naming Conventions

| Element | Convention | Example |
|---|---|---|
| Laboratory folder | `lab-XX` (two-digit, zero-padded) | `lab-01`, `lab-12` |
| Section folder | lowercase, hyphens | `bscs-3a`, `bsit-2b` |
| Student folder | `YEAR-NUMBER-surname-given-name` | `2026-0001-dela-cruz-juan` |
| Branch name | `lab-XX-student-number` | `lab-01-2026-0001` |
| Pull-request title | `[LAB-XX][SECTION] StudentNumber Surname, GivenName` | `[LAB-01][BSCS-3A] 2026-0001 Dela Cruz, Juan` |
| Commit message | Conventional Commits (`feat`, `fix`, `docs`, `test`) | `feat(lab-01): complete static analysis activity` |

---

## Submission States

| Repository State | Academic Status |
|---|---|
| Work exists only on student's computer | Not submitted |
| Work pushed only to student's fork | Not officially submitted |
| Pull request opened before deadline | **Submitted** |
| Instructor requests changes | Correction required |
| Corrections pushed to same pull request | Resubmitted |
| Pull request approved | Accepted |
| Pull request merged | Archived |
| Pull request opened after deadline | Late |

> **Important:** The pull-request creation timestamp is the official submission time. The instructor's merge timestamp is **not** the submission time.

---

## Rules at a Glance

- Work only inside your assigned `laboratories/lab-XX/section/student-folder/` path.
- Do **not** modify any other student's folder.
- Do **not** open duplicate pull requests for the same laboratory.
- Cite all external code, libraries, tutorials, and AI assistance.
- Never include passwords, tokens, API keys, `.env` files, private keys, grades, or personal data.

---

## Branch Protection (Manual Configuration Required)

The following branch-protection rules are **recommended** for `main` and must be configured manually by the repository owner in **GitHub → Settings → Branches → Branch protection rules**:

| Rule | Status |
|---|---|
| Require pull requests before merging | ⚠️ Must be enabled manually |
| Block force pushes | ⚠️ Must be enabled manually |
| Block branch deletion | ⚠️ Must be enabled manually |
| Require instructor approval before merge | ⚠️ Must be enabled manually |
| Require status checks to pass (when CI is added) | ⚠️ Must be enabled manually |
| Restrict direct pushes to authorized maintainers | ⚠️ Must be enabled manually |

Students must **not** receive direct write access to `main`.

---

## Key Documents

| Document | Purpose |
|---|---|
| [SUBMISSION_GUIDE.md](SUBMISSION_GUIDE.md) | Step-by-step guide for students |
| [CONTRIBUTING.md](CONTRIBUTING.md) | Rules for what students may and may not change |
| [SECURITY.md](SECURITY.md) | Security and privacy policy |
| [templates/student-readme-template.md](templates/student-readme-template.md) | Template for the student README inside each submission folder |
| [templates/laboratory-report-template.md](templates/laboratory-report-template.md) | Template for the formal laboratory report |
| [templates/rubric-template.md](templates/rubric-template.md) | Customizable grading rubric |
| [laboratories/README.md](laboratories/README.md) | How to organize laboratory and student folders |

---

## Academic Integrity

- All submitted work must represent the student's own effort unless otherwise disclosed.
- Copied or adapted code must be cited with source, author, and license.
- AI-assisted work must be disclosed according to course policy (instructor-defined placeholder).
- Commit history is preserved as authorship evidence.
- Oral code explanation may be required when authorship is uncertain.

---

## Contact

Direct questions to your instructor through the course's official communication channel. Do not post sensitive personal information in GitHub issues or pull-request comments.
