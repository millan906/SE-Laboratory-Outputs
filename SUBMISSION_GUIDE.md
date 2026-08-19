# Student Submission Guide

**Software Quality and Security Laboratory**
A beginner-friendly, step-by-step guide to submitting laboratory work.

---

## Before You Begin

- You need a **GitHub account**. If you don't have one, go to <https://github.com> and sign up for free.
- You need **Git** installed on your computer. Download it from <https://git-scm.com>.
- Read this guide fully before running any commands.

Replace every `ALL-CAPS-PLACEHOLDER` with your actual information before running a command.

---

## Step 1 — Create a GitHub Account

1. Go to <https://github.com>.
2. Click **Sign up** and follow the prompts.
3. Verify your email address.
4. Share your GitHub username with your instructor so you can be identified as the author of your submissions.

---

## Step 2 — Fork the Original Repository

Forking creates your own personal copy of the repository on GitHub.

1. Go to the original repository: `https://github.com/millan906/SE-Laboratory-Outputs`
2. Click the **Fork** button in the top-right corner.
3. Under "Owner," select your personal GitHub account.
4. Leave the repository name unchanged.
5. Click **Create fork**.

You now have a copy at `https://github.com/STUDENT-USERNAME/SE-Laboratory-Outputs`.

---

## Step 3 — Clone Your Fork to Your Computer

Cloning downloads your fork so you can work on it locally.

```bash
git clone https://github.com/STUDENT-USERNAME/SE-Laboratory-Outputs.git
cd SE-Laboratory-Outputs
```

Replace `STUDENT-USERNAME` with your actual GitHub username.

---

## Step 4 — Add the Original Repository as `upstream`

This lets you receive updates from the original (instructor's) repository.

```bash
git remote add upstream https://github.com/millan906/SE-Laboratory-Outputs.git
```

Verify your remotes:

```bash
git remote -v
```

Expected output:

```
origin    https://github.com/STUDENT-USERNAME/SE-Laboratory-Outputs.git (fetch)
origin    https://github.com/STUDENT-USERNAME/SE-Laboratory-Outputs.git (push)
upstream  https://github.com/millan906/SE-Laboratory-Outputs.git (fetch)
upstream  https://github.com/millan906/SE-Laboratory-Outputs.git (push)
```

---

## Step 5 — Synchronize Your Fork Before Starting

Always sync before you start any new laboratory to avoid conflicts.

```bash
git fetch upstream
git switch main
git merge --ff-only upstream/main
git push origin main
```

- `git fetch upstream` — downloads the latest changes from the original repository.
- `git merge --ff-only upstream/main` — applies those changes to your local `main` without creating a merge commit.
- `git push origin main` — updates your GitHub fork.

---

## Step 6 — Create a Lab-Specific Branch

Never work directly on `main`. Create a new branch for each laboratory.

```bash
git switch -c lab-XX-STUDENT-NUMBER
```

**Branch naming:** `lab-XX-STUDENT-NUMBER`

| Placeholder | Replace with | Example |
|---|---|---|
| `XX` | Two-digit lab number | `01`, `12` |
| `STUDENT-NUMBER` | Your student number | `2026-0001` |

**Example:**

```bash
git switch -c lab-01-2026-0001
```

---

## Step 7 — Create Your Submission Folder

Create your folder inside the correct laboratory and section directory.

**Path format:**

```
laboratories/lab-XX/SECTION/STUDENT-NUMBER-SURNAME-GIVEN-NAME/
```

**Example:**

```bash
mkdir -p laboratories/lab-01/bscs-3a/2026-0001-dela-cruz-juan/src
mkdir -p laboratories/lab-01/bscs-3a/2026-0001-dela-cruz-juan/tests
mkdir -p laboratories/lab-01/bscs-3a/2026-0001-dela-cruz-juan/screenshots
mkdir -p laboratories/lab-01/bscs-3a/2026-0001-dela-cruz-juan/reports
```

| Placeholder | Convention | Example |
|---|---|---|
| `SECTION` | Lowercase, hyphens | `bscs-3a` |
| `SURNAME` | Lowercase, hyphens | `dela-cruz` |
| `GIVEN-NAME` | Lowercase, hyphens | `juan` |

---

## Step 8 — Copy and Complete the Required Templates

Copy the templates from the `templates/` folder into your submission folder.

```bash
cp templates/student-readme-template.md \
   laboratories/lab-XX/SECTION/STUDENT-FOLDER/README.md

cp templates/laboratory-report-template.md \
   laboratories/lab-XX/SECTION/STUDENT-FOLDER/reports/laboratory-report.md
```

Open each copied file and fill in every placeholder. Delete placeholder instructions after filling them in.

---

## Step 9 — Add Your Source Code, Tests, Screenshots, and Reports

Place files in the correct subfolder:

| Subfolder | Contents |
|---|---|
| `src/` | All source code files |
| `tests/` | Test files and test documentation |
| `screenshots/` | Evidence screenshots (PNG or JPG) |
| `reports/` | Laboratory report, analysis documents |

Work **only inside your assigned folder**. Do not touch any other file or folder.

---

## Step 10 — Review Your Changed Files

Before committing, check exactly what you have changed.

```bash
git status
git diff --stat
```

Make sure:
- Only files inside your submission folder appear.
- No `.env` files, passwords, tokens, or private keys appear.
- No files belonging to another student appear.

---

## Step 11 — Write Meaningful Commits

Stage your submission folder and commit with a clear message.

```bash
git add laboratories/lab-XX/SECTION/STUDENT-FOLDER
git commit -m "feat(lab-XX): BRIEF DESCRIPTION OF WHAT YOU DID"
```

**Examples of good commit messages:**

```
feat(lab-01): complete static analysis activity with PMD
feat(lab-02): implement unit tests for calculator module
docs(lab-01): add laboratory report and screenshots
fix(lab-01): correct SQL query to use parameterized input
```

**Rules:**
- Use `feat` for new work, `fix` for corrections, `docs` for documentation, `test` for tests.
- Keep the message under 72 characters.
- Write in the imperative mood ("complete", "add", "fix" — not "completed", "added", "fixed").

---

## Step 12 — Push Your Branch to Your Fork

```bash
git push -u origin lab-XX-STUDENT-NUMBER
```

The `-u` flag sets the upstream tracking branch so future pushes only need `git push`.

**Example:**

```bash
git push -u origin lab-01-2026-0001
```

---

## Step 13 — Open a Pull Request to the Original Repository

1. Go to your fork on GitHub: `https://github.com/STUDENT-USERNAME/SE-Laboratory-Outputs`
2. GitHub will show a banner: **"Compare & pull request"** — click it.
3. Make sure the **base repository** is `millan906/SE-Laboratory-Outputs` and the **base branch** is `main`.
4. Set the **pull request title** to:
   ```
   [LAB-XX][SECTION] STUDENT-NUMBER Surname, GivenName
   ```
   **Example:** `[LAB-01][BSCS-3A] 2026-0001 Dela Cruz, Juan`
5. Fill in the pull-request template that appears in the description box.
6. Click **Create pull request**.

> The timestamp when you click **Create pull request** is your **official submission time**.

---

## Step 14 — Respond to Review Comments

If the instructor requests changes:

1. Read each comment carefully.
2. Make the required corrections in your local repository.
3. Push the corrections to the **same branch** (Step 15).

Do **not** open a new pull request.

---

## Step 15 — Push Corrections to the Same Branch and Pull Request

After making corrections locally:

```bash
git add laboratories/lab-XX/SECTION/STUDENT-FOLDER
git commit -m "fix(lab-XX): address review comments — BRIEF DESCRIPTION"
git push origin lab-XX-STUDENT-NUMBER
```

The existing pull request will update automatically. You do **not** need to open a new one.

---

## Step 16 — Avoid Duplicate Pull Requests

- Open **exactly one** pull request per laboratory.
- If you accidentally open a duplicate, close the extra one and leave a comment explaining which PR is the correct submission.
- Pushing new commits to the correct branch automatically updates the open PR.

---

## Step 17 — Confirm Your Final Submission Status

Check your pull request page on GitHub to confirm:
- Status is **Open** (submitted, awaiting review).
- All your commits appear in the pull request timeline.
- No additional review comments remain unaddressed.

Your submission is **officially accepted** when the instructor approves and **archived** when they merge it.

---

## Quick Command Reference

```bash
# Clone your fork
git clone https://github.com/STUDENT-USERNAME/SE-Laboratory-Outputs.git
cd SE-Laboratory-Outputs

# Add upstream
git remote add upstream https://github.com/millan906/SE-Laboratory-Outputs.git

# Sync before starting
git fetch upstream
git switch main
git merge --ff-only upstream/main
git push origin main

# Create lab branch
git switch -c lab-01-STUDENT-NUMBER

# Stage and commit
git add laboratories/lab-01/SECTION/STUDENT-FOLDER
git commit -m "feat(lab-01): complete static analysis activity"

# Push to fork
git push -u origin lab-01-STUDENT-NUMBER
```

---

## Getting Help

Contact your instructor through the official course communication channel. Do not post personal information, student numbers, or grades in GitHub issues or pull-request comments.
