# Laboratories Directory

**Software Quality and Security Laboratory**

This directory contains all student laboratory submissions, organized by laboratory number, section, and student.

---

## Directory Structure

```
laboratories/
├── README.md                          ← this file
├── lab-01/
│   ├── bscs-3a/
│   │   ├── 2026-0001-dela-cruz-juan/
│   │   │   ├── README.md
│   │   │   ├── src/
│   │   │   ├── tests/
│   │   │   ├── screenshots/
│   │   │   └── reports/
│   │   └── 2026-0002-santos-maria/
│   │       └── ...
│   └── bscs-3b/
│       └── ...
├── lab-02/
│   └── ...
└── lab-XX/
    └── ...
```

---

## Naming Rules

### Laboratory Folder

```
lab-XX
```

- `XX` is a **two-digit, zero-padded** number.
- Assigned by the instructor.
- Do not create laboratory folders arbitrarily.

| Correct | Incorrect |
|---|---|
| `lab-01` | `lab-1`, `lab1`, `Lab-01`, `LAB01` |
| `lab-12` | `lab12`, `laboratory-12` |

---

### Section Folder

```
section-name
```

- All lowercase, words separated by hyphens.
- Must match the official section code for the course.

| Correct | Incorrect |
|---|---|
| `bscs-3a` | `BSCS3A`, `bscs3a`, `bscs_3a` |
| `bsit-2b` | `BSIT-2B`, `bsit2b` |

---

### Student Folder

```
student-number-surname-given-name
```

- All lowercase.
- Hyphens separate all parts including within names.
- Use the student's full institutional student number.
- Multiple given names or surnames use hyphens.

| Correct | Incorrect |
|---|---|
| `2026-0001-dela-cruz-juan` | `2026_0001_dela_cruz_juan` |
| `2026-0002-santos-ana-marie` | `2026-0002-Santos-AnaMarie` |
| `2026-0003-garcia-carlos` | `garcia-carlos-2026-0003` |

---

## Student Folder Contents

Each student folder should contain:

```
STUDENT-FOLDER/
├── README.md          ← completed from templates/student-readme-template.md
├── src/               ← source code
├── tests/             ← test files
├── screenshots/       ← screenshots of running program and test results
└── reports/           ← laboratory report (from templates/laboratory-report-template.md)
```

All items are required unless the laboratory activity explicitly excludes one.

---

## Who Creates Laboratory Folders

| Folder | Created by |
|---|---|
| `laboratories/lab-XX/` | Instructor (or may be pre-created in the repository) |
| `laboratories/lab-XX/section/` | Instructor (or may be pre-created) |
| `laboratories/lab-XX/section/student-folder/` | **Student** — in their own fork and pull request |

Students must **not** create laboratory folders for laboratories they are not currently submitting.

Students must **not** create or modify section folders other than their own.

---

## Submission Path Validation

Before opening a pull request, verify your submission path:

1. Laboratory folder: `lab-XX` with zero-padded number.
2. Section folder: matches your enrolled section exactly.
3. Student folder: `student-number-surname-given-name` all lowercase.
4. All required subfolders (`src/`, `tests/`, `screenshots/`, `reports/`) present.
5. `README.md` present and completed at the student folder level.

A pull request with an incorrect path will be rejected without review.

---

## What Does Not Belong Here

- Files not related to a specific student's submission (e.g., shared utilities).
- Instructor answer keys, solution files, or grade sheets.
- Temporary files, editor backups, or operating-system files (see `.gitignore`).
- Any file containing passwords, tokens, API keys, or personal data.

---

## Questions

See [SUBMISSION_GUIDE.md](../SUBMISSION_GUIDE.md) for the full submission workflow. Contact your instructor through the official course channel for questions not covered there.
