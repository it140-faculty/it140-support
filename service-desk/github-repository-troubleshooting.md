# IT 140 GitHub and Repository Troubleshooting

Use this page for GitHub authentication, repository setup, cloning, remote,
synchronization, and repository-location problems.

Before changing anything, understand the
[Three-Copy Model](../shared/course-repository-architecture.md#the-three-copy-model):

```text
GC-STEM public course template
          ↓ activity README setup command
Student's private GitHub repository
          ↓ clone
Student's local repository in ~/Repos
```

> [!IMPORTANT]
> Students should **not click Fork or Use this template** on the public GC-STEM
> assignment/project repository. The current activity README creates the
> student's private repository through its documented GitHub CLI setup block.

## First: Identify the Exact Repository

Collect:

```text
GitHub username:
Repository name:
Repository owner:
Repository visibility:
GitHub repository URL:
Local repository path:
```

From the local repository root, run:

```bash
git status
git remote -v
```

The normal student assignment/project local clone should point to the student's
private GitHub repository, not directly to `GC-STEM`.

<!-- screenshot placeholder; show GitHub repository breadcrumbs for a GC-STEM
public template and a student private repository, emphasizing the different
owner names -->

## GitHub Authentication

From a Terminal/PowerShell window, run:

```bash
gh auth status
```

Confirm the active GitHub account is the account the student intends to use for
IT 140.

If authentication is missing or the wrong account is active, use the current
course setup/configuration workflow rather than collecting the student's
password or token.

> [!WARNING]
> Never ask the student to send a GitHub password, device code, two-factor
> authentication code, recovery code, passkey, personal access token, or other
> credential.

## Current Repository-Setup Rule

The activity README is the source for the repository-setup command. A typical
pattern includes:

```bash
cd ~/Repos
gh auth setup-git
gh repo create <repository-name> --template GC-STEM/<repository-name> --private --clone
cd <repository-name>
git remote -v
```

The `--template` option in this CLI command is intentional. It does **not** mean
the student should click GitHub's browser **Use this template** control.

Do not reconstruct the setup sequence from memory when the live activity
README provides the complete command block.

## Student Clicked Fork

A fork is not the intended IT 140 assignment/project repository workflow.

Before changing anything:

1. Identify the fork owner and repository URL.
2. Determine whether the student has already added work to the fork or a local
   clone of it.
3. Preserve the student's work and Git history.
4. Follow the current activity README to establish the correct private
   repository workflow.
5. Move/copy only the appropriate student work into the correct repository as
   directed by the approved support process.

Do not push student work into the public GC-STEM repository, and do not delete
the fork until the student's work is safely preserved elsewhere.

## Student Clicked Use This Template

Clicking **Use this template** can create a repository outside the intended
activity setup sequence. Treat it as a repository-state problem rather than
assuming the student must immediately delete everything.

Determine:

* who owns the created repository;
* whether it is public or private;
* whether the expected repository name was used;
* whether student work already exists there; and
* whether a local clone is connected to it.

Preserve work first. Then use the current activity README and the canonical
[GitHub Workflow](../shared/github-workflow.md) to establish the intended
private-repository state.

## Repository Already Exists

An "already exists" message is usually a **state-identification problem**, not
a reason to delete the repository immediately.

Determine whether:

* the student's private GitHub repository already exists;
* the local folder already exists;
* both exist and are connected correctly; or
* one copy is missing.

Use the canonical recovery paths in
[GitHub Workflow](../shared/github-workflow.md#returning-to-an-existing-assignment).

## Local Folder Missing, GitHub Repository Exists

If the student's private GitHub repository contains the current work but the
local clone is missing, clone the **existing private repository**.

Do not create a second repository from the public course template merely
because the local folder is absent.

See
[Moving to Another Computer or a Reset CVD](../shared/github-workflow.md#moving-to-another-computer-or-a-reset-cvd).

## Local Clone Damaged, GitHub Copy Is Good

Preserve or rename the existing local folder before recloning the student's
existing private repository.

Do not delete the old local copy until the replacement clone has been verified.

See
[Recovering a Damaged Local Copy](../shared/github-workflow.md#recovering-a-damaged-local-copy).

## Student Cloned the GC-STEM Template Directly

A direct clone of `GC-STEM/it140-mX-...` is not the normal student assignment
workflow.

Before replacing it:

1. Check whether the student has added work to the direct clone.
2. Preserve that work.
3. Use the activity README to create the student's private repository through
   the documented setup commands.
4. Move/copy only the appropriate student work into the correct
   private-repository workflow as directed by the activity/support process.

Do not push student work into the public GC-STEM repository.

## Wrong Remote

If `git remote -v` points somewhere unexpected, stop before pushing.

Record the output and determine which repository should be `origin`.

Do not rewrite remotes blindly when the student's current work or Git history
has not been assessed.

## More Than One Local Clone

The simplest course workflow is to use one development environment for an
activity whenever practical.

When a student intentionally switches between two existing local clones, the
course workflow is:

1. On the device being left, save, stage, commit, and `git push` the intended
   work.
2. On the next device, before editing, run:

   ```bash
   cd ~/Repos/<repository-name>
   git pull --ff-only
   git status
   ```

3. Begin editing only after the pull succeeds and the repository state is
   understood.

See
[Working on More Than One Device](../shared/github-workflow.md#working-on-more-than-one-device).

## Pull or Push Cannot Fast-Forward

If `git pull --ff-only` or `git push` fails, or Git reports that histories
cannot be fast-forwarded:

1. **Stop the student from making additional changes on either device.**
2. Record `git status` and `git remote -v` from the affected clone.
3. Identify whether unpushed work exists on either device.
4. Preserve both local copies until the histories and student work are
   assessed.
5. Escalate when resolution requires Git history reconciliation beyond the
   documented course recovery steps.

Do **not** use merge, reset, rebase, force-push, or remote-rewrite commands as a
first-line fix. Those actions can overwrite or obscure student work when the
repository state is not yet understood.

## Opening the Correct Repository in VS Code

The common cross-platform opening pattern is:

```bash
cd ~/Repos/<repository-name>
code .
```

The repository itself should be the top-level folder shown in the VS Code
Explorer. If the wrong folder is open, identify the correct local clone before
changing Git state.

If VS Code opens the repository in Restricted Mode, continue with
[Environment Troubleshooting](environment-troubleshooting.md#vs-code-restricted-mode).

## Projects Repository Across Modules Five Through Seven

Students create `it140-projects` **once in Module Five** and continue using that
same private repository for Modules Five, Six, and Seven.

Creating separate project repositories for each of those modules is not the
intended workflow.

See
[Projects | Modules Five Through Seven](../shared/course-repository-architecture.md#projects--modules-five-through-seven).

## Student GitHub Actions or CI Looks Wrong

Student CI is formative and activity-specific. A green check is not a grade or
a Brightspace submission.

Before treating a student CI result as a technical defect:

1. Confirm which activity repository and personal repository are involved.
2. Read the activity's `.github/ci/README.md` when available.
3. Determine whether the student has begun changing graded files.
4. Distinguish expected student feedback from an infrastructure/workflow
   failure.

Current version 1.0.4 behavior includes:

* untouched fresh personal repositories are intended to be neutral;
* Module Three/Module Four optional Python practice is not a student CI
  requirement; and
* Projects Ruff feedback is advisory and does not by itself make student CI
  fail.

A repository/CI defect is more likely when an untouched fresh personal
repository fails contrary to the documented lifecycle, GitHub Actions fails in
checkout/setup infrastructure, the feedback does not match the repository
state, or several students report the same unexpected failure.

## Repeat Students

A student repeating part or all of IT 140 should use a repository based on the
**current course template** for the new course attempt and follow the current
activity README setup commands rather than using an old assignment/project
repository as the active repository.

See [Repeat Students](../shared/github-workflow.md#repeat-students).

## Starting Over

Starting over from the current course template is different from restoring the
student's existing GitHub repository.

Before starting over:

* preserve local work;
* preserve/rename the existing private GitHub repository;
* use the activity's current reset/start-over instructions; and
* do not delete the only copy of student work.

See
[Starting Over From the Course Template](../shared/github-workflow.md#starting-over-from-the-course-template).

## When the Public Course Repository Looks Wrong

If a current GC-STEM repository is missing, unavailable, or appears defective:

1. Check [Course Status](https://github.com/GC-STEM/it140/wiki/Course-Status).
2. Confirm the current activity README/URL from Brightspace or the main course
   repository.
3. Reproduce the problem without using private student data when possible.
4. Escalate through
   [Course Technical Maintenance Escalation](escalation.md#course-technical-maintenance-escalation).

Do not create a workaround that permanently diverges the student's repository
from the current course template unless course support directs it.

Return to the [Service Desk Triage and Escalation Runbook](README.md).
