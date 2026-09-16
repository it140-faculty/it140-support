# IT 140 Faculty | GitHub and Student Repositories

Faculty do not need to administer GitHub repositories for students, but they
should understand the course repository model well enough to recognize common
workflow problems and review a student's private repository when appropriate.

## Start With the Three-Copy Model

The course distinguishes among:

1. the **GC-STEM public course template**;
2. the **student's private GitHub repository**; and
3. the **student's local clone** in the course development environment.

See
[Course Repository Architecture](../shared/course-repository-architecture.md#the-three-copy-model).

These copies can have the same repository name. Confirm the **owner and
location** before giving repository-specific advice.

## Normal Student Workflow

The canonical workflow is documented in
[GitHub Workflow](../shared/github-workflow.md).

At a high level, students read the current activity README → run its repository-setup command block → work in the private repository's local clone under `~/Repos` → commit/push → submit the required deliverable in D2L Brightspace

> [!IMPORTANT]
> Students should **not click Fork or Use this template** on the public GC-STEM
> activity repository. The activity README uses a documented GitHub CLI command
> such as `gh repo create ... --template ... --private --clone` to create the
> student's private repository.

Do not replace the current activity README with remembered commands from a
previous term.

The common cross-platform opening pattern is:

```bash
cd ~/Repos/<repository-name>
code .
```

## When a Student Cannot Find Their Work

Before telling a student to start over, determine whether:

* the private GitHub repository still exists;
* the work was pushed to GitHub;
* only the local clone is missing;
* the student opened the wrong local folder; or
* the student is signed into the wrong GitHub account.

A missing local folder does **not** mean the private GitHub repository must be
recreated.

For recovery, use [GitHub Workflow](../shared/github-workflow.md) or the current
activity README.

## Working on More Than One Device

Using one development environment for an activity is the simplest course
workflow and reduces the chance of divergent Git histories.

If a student intentionally switches between existing local clones, the current
activity READMEs require the student to:

1. save, commit, and `git push` on the device being left;
2. run `git pull --ff-only` before editing on the next device; and
3. begin new work only after the pull succeeds and the repository state is
   understood.

If `git pull --ff-only` or `git push` fails, or Git reports that histories
cannot be fast-forwarded, instruct the student to **stop making changes on both
devices and obtain technical help**. Do not recommend random merge, reset,
rebase, or force-push commands.

See
[Working on More Than One Device](../shared/github-workflow.md#working-on-more-than-one-device).

## Reviewing a Private Student Repository

Student assignment/project repositories are private.

When direct repository review is appropriate, the student may grant an
instructor access as a collaborator using the current approved support
workflow.

Do **not** ask a student to make a graded repository public merely so faculty
can inspect it.

When reviewing a repository:

* confirm the repository owner is the student;
* respect the student's privacy;
* focus on the files relevant to the support/grading question;
* avoid changing or committing to the student's repository unless an approved
  workflow explicitly requires it; and
* continue to use Brightspace for the official graded submission and feedback.

<!-- screenshot placeholder; show the GitHub owner/repository breadcrumb for a
GC-STEM course template and a private student repository so faculty can
visually distinguish the two -->

## Useful Repository Evidence

When a repository problem is unclear, a student can provide non-secret output
such as:

```bash
git status
git remote -v
```

For GitHub CLI authentication state:

```bash
gh auth status
```

Faculty do not need to diagnose every Git/GitHub failure. These checks can help
identify whether the problem belongs in the technical support path.

Never request passwords, two-factor codes, device codes, recovery codes,
access tokens, passkeys, or other authentication secrets.

## Projects Repository

Students create `it140-projects` once in Module Five and continue using that
repository through Modules Five, Six, and Seven.

Do not direct a student to create a separate project repository for the Module
Six Milestone or Project Two.

See
[Projects | Modules Five Through Seven](../shared/course-repository-architecture.md#projects--modules-five-through-seven).

## Repeat Students

Students repeating part or all of IT 140 should use repositories based on the
**current course templates** for the new course attempt and follow the current
activity README setup commands.

They should not use a previous attempt's repository as the active repository
for current coursework.

See [Repeat Students](../shared/github-workflow.md#repeat-students).

## Repository Problems That Belong to Technical Support

Refer technical failures such as:

* GitHub authentication does not work;
* `gh` cannot access the intended account;
* the activity README repository-setup command fails;
* cloning fails;
* the student used **Fork** or **Use this template** and the resulting
  repository state must be assessed;
* a remote is incorrect and the correct recovery is unclear;
* `git pull --ff-only` or `git push` fails after work across multiple devices;
* local and GitHub copies have diverged in a way that risks student work; or
* repository recovery requires technical Git intervention.

See
[Service Desk GitHub and Repository Troubleshooting](../service-desk/github-repository-troubleshooting.md).

## Course Repository Defects

If the **public GC-STEM repository itself** appears incorrect:

1. check [Course Status](https://github.com/GC-STEM/it140/wiki/Course-Status);
2. confirm the current activity URL/README;
3. reproduce without private student data when possible; and
4. follow
   [Technical Issues and Escalation](technical-issues-and-escalation.md).

Return to the [Faculty Support Guide](README.md).
