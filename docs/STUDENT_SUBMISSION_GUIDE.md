# Project VITAL — Student Submission Guide

This guide explains how teams will organize, version, and submit Project VITAL assignments.

Project VITAL uses **standard GitHub repositories** rather than GitHub Classroom. Your team's GitHub repository will serve as the technical record of your work throughout the course. The course Learning Management System (LMS) remains the official location for assignment submission records, grades, and instructor feedback.

---

# 1. Submission Model

Each team will maintain **one private GitHub repository for the entire Project VITAL course project**.

The general workflow is:

```text
Project VITAL Course Repository
        │
        │ provides assignments, environment, and documentation
        ▼
Your Team Repository
        │
        │ contains your team's work
        ▼
Git Tag
        │
        │ creates a fixed snapshot at the deadline
        ▼
Course LMS
        │
        └── submit repository reference + tag
```

You will continue using the same team repository as the course progresses.

Do **not** submit your assignments directly to the main Project VITAL repository.

---

# 2. Your Team Repository

The instructor will create one **private GitHub repository for each Project VITAL team** inside the `CSCI3364-Fall2026` GitHub organization.

Team repositories will use names such as `team-01`, `team-02`, `team-03`, and `team-04`.

Your assigned repository will be used for the entire semester. Do **not** create a separate repository for each assignment or create your own replacement Project VITAL repository unless the instructor explicitly asks you to do so.

---

# 3. Repository Access

The instructor will add the appropriate students to each private team repository.

Each student must:

1. Use their own GitHub account.
2. Accept the GitHub organization or repository invitation if prompted.
3. Verify that they can access the assigned private repository.
4. Verify that they can clone, commit, and push before the first submission deadline.

Do not share GitHub accounts or credentials.

The instructor retains administrative access to all course team repositories.

---

# 4. Course Repository vs. Team Repository

Project VITAL uses two different repositories:

- **Public course repository:** `CSCI3364-Fall2026/Project_VITAL` — official released assignments, documentation, environment, and course materials.
- **Private team repository:** `CSCI3364-Fall2026/team-XX` — your team's work, evidence, tests, and assignment submissions.

Do **not** submit work directly to the public course repository.

---

# 5. Clone the Team Repository

Each team member should clone the repository to their own computer.

For example:

```bash
git clone <YOUR-TEAM-REPOSITORY-URL>
cd team-XX
```

Do not copy one student's local repository between computers.

Each team member should clone and work through Git using their own account.

---

# 6. Recommended Repository Structure

Your private team repository will contain the work your team produces during the semester.

For Assignment 1, a recommended structure is:

```text
team-XX/
│
├── README.md
│
└── assignment-01/
    ├── exploration-log.md
    ├── exploration-challenges.md
    ├── network-observation.md
    ├── testing-opportunities.md
    ├── feature-map.*
    ├── reflection.md
    └── evidence/
```

The current assignment instructions are the authoritative source for required deliverables.

Additional assignment directories should be created only when those assignments are officially released.

---

# 7. Your Repository README

Create a `README.md` at the root of the team repository.

At minimum, include:

```markdown
# Project VITAL — Team XX

## Team Members

- Student Name — GitHub username
- Student Name — GitHub username
- Student Name — GitHub username

## Project

This repository contains our team's work for Project VITAL.
```

Do not include student ID numbers, grades, personal phone numbers, home addresses, or other unnecessary personal information.

---

# 8. Working with Git

During the project, use the normal Git workflow:

```bash
git status
git add .
git commit -m "Describe the work completed"
git push
```

Commit messages should briefly explain the work performed.

Good examples:

```text
Add patient exploration observations

Document appointment workflow

Add initial C4 container diagram

Trace vitals fields to database

Add accessibility test cases
```

Avoid meaningless commit messages such as:

```text
stuff

update

final

asdf

changes
```

---

# 9. Individual Contributions

Project VITAL assignments are team-based, but every team member is expected to make **meaningful contributions**.

Students should commit their own work using their own GitHub accounts.

The goal is **not** to maximize the number of commits.

For example, this is not useful:

```text
Student A — 57 tiny commits
Student B — 3 meaningful commits
```

The number of commits alone does not determine contribution.

The instructor may consider:

- Git history;
- quality and scope of contributions;
- pull requests where applicable;
- assignment artifacts;
- peer feedback;
- individual reflections or check-ins;

when evaluating individual participation.

Do not artificially divide work simply to increase commit counts.

Git history is one source of evidence used to understand individual contributions. The instructor may review the timing, content, and substance of commits together with assignment artifacts, peer feedback, and individual reflections. Automated or AI-assisted analysis may be used to help identify patterns in repository activity, such as primarily cosmetic changes, repeated deletion and re-addition of content, or commits made outside the assignment work period. These tools support the review process; they do not replace instructor judgment. Individual contribution will be evaluated based on the overall evidence of meaningful participation in the team's work.

---

# 10. Pull Before You Work

Because multiple people are using the same repository, get the latest version before beginning a work session.

```bash
git pull
```

A useful habit is:

```text
Start working
     ↓
git pull
     ↓
make changes
     ↓
git status
     ↓
git add
     ↓
git commit
     ↓
git push
```

Communicate with your teammates when multiple people are editing the same file.

---

# 11. What Must Never Be Committed

Do **not** commit:

- `.env` files;
- passwords;
- API keys;
- access tokens;
- private keys;
- database credentials;
- real patient information;
- protected health information (PHI);
- unnecessary personally identifiable information;
- grades or private peer-evaluation information;
- large generated datasets unless the assignment specifically requires them.

Before committing, always check:

```bash
git status
```

Review what Git is about to include.

---

# 12. Synthetic Data Only

Project VITAL uses healthcare software, but the course environment must contain **synthetic data only**.

Never enter information about:

- yourself;
- classmates;
- friends;
- family members;
- actual patients;
- other identifiable real people.

Names, addresses, dates, diagnoses, medications, and other patient information used for assignments should be fictional.

---

# 13. Preparing an Assignment for Submission

Before the deadline, review your assignment directory.

Confirm that:

- all required deliverables are present;
- links and diagrams work;
- screenshots are readable;
- required Markdown files render correctly on GitHub;
- no secrets or sensitive information are included;
- the latest work has been committed;
- all commits have been pushed to GitHub.

Check:

```bash
git status
```

Ideally, Git should report:

```text
nothing to commit, working tree clean
```

Then push one final time:

```bash
git push
```

---

# 14. Create the Submission Tag

Project VITAL uses a **Git tag** to identify the exact version of the repository being submitted.

This is important because your team will continue changing the repository after an assignment deadline.

For Assignment 1, for example:

```bash
git tag assignment-01
git push origin assignment-01
```

For Assignment 2:

```bash
git tag assignment-02
git push origin assignment-02
```

Future assignments will follow the same pattern:

```text
assignment-01
assignment-02
assignment-03
assignment-04
...
```

The assignment instructions will specify the required tag.

---

# 15. Why We Use Tags

Suppose Assignment 1 is due Friday.

Your repository might look like:

```text
Monday       Wednesday       Friday              Sunday
   │             │              │                   │
   ▼             ▼              ▼                   ▼
exploration → screenshots → assignment-01 → architecture work
                                TAG
```

The repository may continue changing after Friday.

The tag identifies:

> **This is the version our team submitted for Assignment 1.**

The instructor grades the tagged version rather than later changes to the repository.

---

# 16. Verify the Tag

After pushing your tag, verify that it exists.

You can run:

```bash
git tag
```

You should see the assignment tag listed.

You can also open your GitHub repository and view **Tags** to verify that the tag was pushed to GitHub.

Creating a tag only on your computer is **not sufficient**.

It must be pushed to GitHub.

---

# 17. Submitting to the LMS

Only **one team member** needs to submit the team assignment to the LMS unless your instructor specifies otherwise.

Submit the information requested by your instructor.

A typical submission should contain:

```text
Team: VITAL-Team-07

Team Members:
Student A
Student B
Student C

Repository:
<team repository URL>

Submission Tag:
assignment-01

Submission Notes:
(optional)
```

Do not upload a ZIP copy of the repository unless your instructor specifically requests one.

The Git tag is the authoritative technical submission.

---

# 18. What Version Will Be Graded?

The instructor will grade the repository state identified by the required assignment tag.

For example:

```text
assignment-01
```

means:

> Grade the repository exactly as it existed when this tag was created.

Changes pushed after the tag do not automatically become part of that submission.

---

# 19. Fixing Something After You Create a Tag

Do not silently move or replace a submission tag after the deadline.

If you discover a problem **before the deadline**, contact your instructor or follow the course resubmission policy.

If your instructor permits replacing a tag before the deadline, follow the instructions they provide.

If you discover a problem **after the deadline**, do not rewrite the submitted Git history or move the tag unless explicitly authorized.

The LMS timestamp and repository history may be used to determine when work was submitted.

---

# 20. Late Work

Late-work rules are determined by the course syllabus.

If a late submission is permitted, your instructor may ask you to use a separate tag such as:

```text
assignment-01-late
```

Do not create alternate submission tags unless instructed.

---

# 21. Branches

During the first Project VITAL assignments, your team may work primarily on:

```text
main
```

As the course progresses, you will be asked to use branches.

For example:

```text
main
 │
 ├── feature/patient-tests
 ├── feature/accessibility-tests
 └── feature/data-generator
```

Later assignments may require:

- feature branches;
- pull requests;
- code review;
- automated testing;
- continuous integration.

Do not introduce a complicated branching strategy unless the assignment requires it.

---

# 22. Repository History Is Part of the Engineering Record

Git is not only a submission mechanism.

It provides evidence of how a software project evolves.

During Project VITAL, repository history may help you understand:

- when tests were introduced;
- why a test changed;
- who investigated a particular issue;
- when a defect was discovered;
- how the testing strategy evolved;
- whether a regression was introduced;
- how the team collaborated.

Write commits with the assumption that another engineer may need to understand your work later.

---

# 23. Grades and Feedback

GitHub is used for technical project artifacts and version history.

The course LMS remains the official location for:

- grades;
- private instructor feedback;
- individual grading adjustments;
- private peer assessments;
- other protected education records.

Do not store grades or confidential peer feedback in the team GitHub repository.

---

# 24. GitHub Problems Near a Deadline

Do not wait until the final minutes before the deadline to push your work.

Before submission day, confirm that:

```bash
git pull
git status
git push
```

all work correctly.

Also verify that:

- every team member can access the repository;
- the instructor can access the repository;
- GitHub contains the latest commits;
- your assignment tag appears on GitHub.

If GitHub or another required service experiences a documented outage, follow your instructor's course policy.

---

# 25. Final Submission Checklist

Before submitting each assignment, verify:

### Repository

- [ ] Repository is private unless the instructor has authorized otherwise.
- [ ] All team members have access.
- [ ] Instructor has access.
- [ ] Required assignment directory exists.
- [ ] All required deliverables are present.

### Security and Privacy

- [ ] No `.env` file is committed.
- [ ] No passwords or tokens are committed.
- [ ] No real patient data is included.
- [ ] No unnecessary personal information is included.
- [ ] Screenshots contain only appropriate synthetic/course data.

### Git

- [ ] Latest work is committed.
- [ ] Latest commits are pushed to GitHub.
- [ ] `git status` shows no unintentionally uncommitted work.
- [ ] Required assignment tag has been created.
- [ ] Tag has been pushed to GitHub.
- [ ] Tag is visible on GitHub.

### LMS

- [ ] Correct team is identified.
- [ ] Repository reference is submitted.
- [ ] Correct assignment tag is submitted.
- [ ] Required team-member information is included.
- [ ] Submission was completed before the deadline.

---

# Quick Submission Reference

For a typical assignment:

```bash
# Get the latest team work
git pull

# Check your repository
git status

# Add and commit final changes if necessary
git add .
git commit -m "Complete Assignment 1"

# Push commits
git push

# Create the submission snapshot
git tag assignment-01

# Push the tag
git push origin assignment-01
```

Then verify the tag on GitHub and submit the required repository information and tag to the LMS.

---

# Need Help?

If you encounter a Git or GitHub problem:

1. Read the error message carefully.
2. Run `git status`.
3. Do not delete the repository or rewrite Git history as a first troubleshooting step.
4. Preserve your local work.
5. Ask for help before using destructive Git commands you do not understand.

Commands such as `reset --hard`, force-pushes, history rewriting, and deleting tags can permanently discard or obscure work.

When in doubt, **preserve the current state and ask for assistance**.
