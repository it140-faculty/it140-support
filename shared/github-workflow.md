# IT 140 GitHub Workflow

This page describes the common GitHub workflow used for IT 140 assignments and
projects.

It explains the shared workflow rather than replacing the instructions in an
activity repository. When supporting a specific assignment or project, follow
that repository's current `README.md` for exact commands and files.

## GitHub's Role in IT 140

GitHub is used to:

* host public course repositories;
* create private student assignment and project repositories from course
  templates;
* maintain remote backups of student work;
* practice Git-based development workflows;
* provide repository Issues, Discussions, and Wikis where appropriate; and
* support course technical documentation and automation.

GitHub is **not** the grading or submission system for normal IT 140
assignments and projects.

D2L Brightspace remains authoritative for:

* activity requirements;
* what to submit;
* grading;
* deadlines; and
* instructor feedback.

## Before Module Two

Course instructions beginning in Module Two assume that the student has:

* access to a GitHub account;
* completed the GitHub account readiness steps in Module One;
* configured two-factor authentication as required by GitHub;
* identified the GitHub username used for IT 140;
* recorded the GitHub-provided `@users.noreply.github.com` email address used
  for Git configuration; and
* access to a configured course IDE.

For exact account-setup instructions, use the current
[`Module One GitHub Account Setup`](https://github.com/GC-STEM/it140-m1-setup-tasks/blob/main/github/README.md).

## The Standard Assignment Workflow

For a new assignment repository, the normal flow is:

```text
Read Brightspace Guidelines and Rubric
              ↓
Read the GC-STEM activity README
              ↓
Confirm the correct GitHub account
              ↓
Run the activity README repository-setup command block
              ↓
Create and clone the student's private repository into ~/Repos
              ↓
Open the local clone in VS Code
              ↓
Complete work
              ↓
Commit and push periodically
              ↓
Submit required deliverables in D2L Brightspace
```

> [!IMPORTANT]
> Students should **not click Fork or Use this template** on the public GC-STEM
> assignment/project repository. The current activity READMEs create the
> student's private repository through a GitHub CLI command that uses the
> course repository as a template.

<!-- screenshot placeholder; show the Fork and Use this template controls on a
GC-STEM activity repository marked Do not use, then show the activity README
repository-setup command block -->

## Confirm the Correct GitHub Account

The course repositories commonly use GitHub CLI.

A useful first check is:

```bash
gh auth status
```

Confirm that the active account is the GitHub account the student intends to
use for IT 140.

When multiple GitHub accounts are configured, the activity README may direct
the student to switch accounts.

Do not create a new assignment repository until the correct active account is
confirmed.

## Create a Private Repository Using the Activity README

The public assignment/project repository is a GitHub template repository, but
students should create their private working repository by running the
**complete setup command block in the current activity README**.

A typical activity command pattern is:

```bash
cd ~/Repos
gh auth setup-git
gh repo create <repository-name> --template GC-STEM/<repository-name> --private --clone
cd <repository-name>
git remote -v
```

The `--template` option in the documented `gh repo create` command is part of
the intended course workflow. It is **not** an instruction to click GitHub's
**Use this template** button in the browser.

The exact activity README may include additional commands, such as starring
the public course repository. Use the complete command block from the current
activity README rather than reconstructing it from this example.

### Why `git remote -v` Matters

After creation and cloning, `git remote -v` shows which GitHub repository the
local copy is connected to.

For normal student work, the local assignment/project repository should point
to the **student's private repository**, not directly to the GC-STEM public
course repository.

## Work in the Local Clone

Students normally work in a repository folder under:

```text
~/Repos/
```

Examples:

```text
~/Repos/it140-m2-assignment
~/Repos/it140-m3-assignment
~/Repos/it140-m4-assignment
~/Repos/it140-projects
```

The repository itself should be the top-level folder shown in the VS Code
Explorer.

The common cross-platform command pattern for opening an existing repository
is:

```bash
cd ~/Repos/<repository-name>
code .
```

In these commands, `~` means the user's home folder and `.` means the current
working directory. The activity READMEs use `cd ...` followed by `code .`
rather than embedding a full repository path in the `code` command.

The student edits the files identified by the activity README.

Provided READMEs, configuration, tests, SRS/SDD documents, and other
course-managed files should remain unchanged unless the activity explicitly
permits or requires editing them.

## VS Code Restricted Mode

Module One course IDE configuration is intended to trust the student's entire
`~/Repos` folder. Normally, a correctly configured course environment should
not open IT 140 activity repositories in VS Code Restricted Mode.

If VS Code displays a **Restricted Mode** warning bar while an IT 140
repository under `~/Repos` is open:

![Restricted Mode warning bar in VS Code](https://raw.githubusercontent.com/GC-STEM/it140-m2-assignment/main/.github/assets/22_vscode_restricted_mode_bar.png)

1. Click **Manage** on the **Restricted Mode** warning bar.
2. In **Workspace Trust**, find **Trusted Folders & Workspaces**.
3. Use the control in that section to add a trusted folder.
4. In the folder selection window, go to the user's home folder and select the
   entire **Repos** folder.

Trust the course workspace described by the current course setup instructions;
do not broadly disable VS Code security protections or trust unrelated
folders merely to remove a warning.

## Commit and Push

Saving a file in VS Code saves it to the local filesystem. It does **not**
automatically place the latest work on GitHub.

Students periodically use Git to:

1. review changes;
2. stage the intended files;
3. commit those changes; and
4. push commits to GitHub.

Typical commands include:

```bash
git status
git add <files>
git commit -m "Describe the saved work"
git push
```

Activity READMEs may provide a specific `git add` command that stages only the
student working and deliverable files for that activity.

Supporters should prefer the activity-specific command when available.

If `git commit` reports **nothing to commit**, that is not automatically an
error. It means Git does not currently see staged or tracked changes that need
a new commit. Use `git status` and the activity README to determine whether the
student saved the intended file and staged the intended work.

A successful push updates the student's GitHub copy; it does **not** submit the
assignment in D2L Brightspace.

## Returning to an Existing Assignment

A student normally creates the private repository **once**.

When returning later on the same computer:

1. open the existing repository folder in `~/Repos`;
2. confirm the repository is the expected local clone; and
3. continue working.

A typical opening sequence is:

```bash
cd ~/Repos/<repository-name>
code .
```

Do **not** create another repository merely because the student is returning
to the assignment.

## Working on More Than One Device

The simplest course workflow is to use **one development environment for an
activity whenever practical**. This reduces the chance that two local copies
will develop different Git histories.

When a student intentionally switches between two existing local clones:

1. On the device being left, save the work, follow the activity README to stage
   the intended files, commit, and `git push`.
2. On the device being used next, open the existing local repository and pull
   before making new edits:

   ```bash
   cd ~/Repos/<repository-name>
   git pull --ff-only
   git status
   ```

3. Begin editing only after the pull completes successfully and the repository
   state is understood.

> [!WARNING]
> If `git pull --ff-only` or `git push` reports an error, or Git says the
> histories cannot be fast-forwarded, **stop and do not make additional
> changes on either device until the repository state is reviewed**. Do not
> experiment with merge, reset, rebase, or force-push commands as a first-line
> fix.

See the current activity README for its exact device-switch instructions.

## Moving to Another Computer or a Reset CVD

If the student's private GitHub repository already exists but the local clone
does not:

* clone the student's existing private repository;
* do not create another private repository from the public course repository;
  and
* verify the clone before continuing work.

A common pattern is:

```bash
cd ~/Repos
gh repo clone "$(gh api user --jq .login)/<repository-name>"
cd <repository-name>
git status
```

Use the current activity README for the exact command.

If the repository already exists locally on the new device, use the
[Working on More Than One Device](#working-on-more-than-one-device) procedure
instead of cloning another copy over it.

## Project Workflow Across Modules Five Through Seven

`it140-projects` is different from the one-module assignment repositories.

The student creates the private `it140-projects` repository **once in Module
Five** and continues using the same repository through:

* Module Five / Project One;
* Module Six / Milestone; and
* Module Seven / Project Two.

The student should not create a new `it140-projects` repository for each
module.

## Recovering a Damaged Local Copy

If:

* the local folder is damaged, confusing, or incomplete; but
* the student's private GitHub repository contains a good current copy,

the normal recovery model is:

1. preserve or rename the current local folder;
2. clone the existing private GitHub repository again; and
3. verify the new local clone before deleting any backup.

Activity repositories may provide exact **Restore Your Local Copy From GitHub**
commands.

> [!CAUTION]
> Never delete the student's only copy of work before confirming that a good
> copy exists elsewhere.

## Starting Over From the Course Template

Starting over is appropriate only when the student intentionally needs a fresh
copy of the current course starting point.

The normal course recovery pattern preserves the previous work by renaming:

* the existing local repository; and
* the existing private GitHub repository,

before running the current activity README's repository-setup commands again.

This is different from recloning an existing student repository.

Use the activity's current **Start Over From the Original Course Template**
instructions when available.

## Repeat Students

Students repeating part or all of IT 140 should create and use repositories
based on the **current course templates** for the new course attempt, using the
current activity README commands.

They should not use an old assignment or project repository as the active
working repository for the new attempt.

Using the current template ensures that the student receives the current:

* repository layout;
* instructions;
* starter files;
* tests;
* configuration; and
* support resources.

A prior repository may be preserved under a different name for reference or
backup, subject to applicable course and academic-integrity requirements.

## Private Repository Access for Support

A student's assignment or project repository is private.

When an instructor or LSS needs to inspect the repository directly, the
student may grant collaborator access when that support workflow is
appropriate.

Do not require a student to make a graded-work repository public merely to
obtain support.

Role-specific guides should explain when direct repository access is useful
and how the supporter should handle student work.

## GitHub Issues and Discussions

Public course repositories may provide:

* **Issues** for technical problems or requested improvements; and
* **Discussions** for repository-related questions or course-community
  discussion when appropriate.

Do not post in public GitHub areas:

* passwords;
* authentication or verification codes;
* personal access tokens;
* recovery codes;
* private identifying information;
* confidential student information; or
* complete solutions to graded assignments.

Questions about assignment requirements, grading, deadlines, accommodations,
and instructor feedback belong through the course/instructor support path
rather than a public repository issue.

## Star, Watch, Fork, and Template

These GitHub features and terms serve different purposes in the current course
workflow:

* **Star** — bookmark a public course repository so it is easier to find;
  recommended where the activity README says to star it.
* **Watch** — receive repository notifications; generally optional for
  students.
* **Fork** — create a linked fork of another repository; **students should not
  use this for IT 140 assignment/project setup**.
* **Use this template** — GitHub browser control for creating a repository;
  **students should not click this for IT 140 assignment/project setup**.
* **`gh repo create --template ...`** — the GitHub CLI mechanism used by the
  activity README to create the student's private repository from the current
  course starting point.

The distinction matters: the course still uses GitHub template repositories,
but the student follows the **documented CLI setup block** rather than choosing
GitHub repository-creation options independently.

## Common GitHub Troubleshooting Questions

Before changing a repository, identify:

```text
GitHub username:
Repository name:
Repository owner:
Repository visibility:
Local path:
Remote URL:
```

Useful commands include:

```bash
gh auth status
git status
git remote -v
```

These checks often reveal whether the problem is:

* the wrong GitHub account;
* the wrong repository owner;
* the wrong local folder;
* a missing local clone;
* a local clone connected to an unexpected remote;
* a repository that already exists;
* a repository created by clicking **Fork** or **Use this template** instead of
  following the activity README; or
* two local copies whose histories have diverged.

## Do Not Use Repository Recreation as the First Fix

A failed command or confusing local folder does not automatically mean the
student should start over.

Before recreating a repository:

1. identify the student's existing GitHub repository;
2. determine whether current work has been pushed;
3. determine whether the local clone can be recovered;
4. preserve existing work; and
5. use the activity's documented reset process if a restart is truly needed.

## Related Shared Documentation

* [Course Overview](course-overview.md)
* [Course Repository Architecture](course-repository-architecture.md)
* [Course Glossary](glossary.md)
* [Supported Environments](supported-environments.md)
* [Support Boundaries](support-boundaries.md)
* [Escalation Model](escalation-model.md)

Return to the [Shared Documentation Index](README.md).
