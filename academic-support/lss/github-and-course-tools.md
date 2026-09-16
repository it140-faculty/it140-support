# IT 140 LSS | GitHub and Course Tools

LSS should understand the IT 140 development workflow well enough to help
students **use the tools as part of learning** and to recognize when a problem
requires technical support.

LSS are not expected to perform deep Git recovery, operating-system repair, or
course automation maintenance.

## Start With the Current Activity README

When a student asks how to use an assignment/project repository:

1. open the current activity repository;
2. start with its top-level `README.md`;
3. follow the activity-specific workflow; and
4. use the shared [GitHub Workflow](../shared/github-workflow.md) for common
   repository concepts.

Do not reconstruct commands from memory if the live README provides them.

## The Three-Copy Model

Be able to identify:

* the **GC-STEM public course template**;
* the **student's private GitHub repository**; and
* the **student's local clone** in `~/Repos`.

See
[Course Repository Architecture](../shared/course-repository-architecture.md#the-three-copy-model).

<!-- screenshot placeholder; show the GitHub owner/repository breadcrumb on a
GC-STEM template and on a private student repository so LSS can distinguish the
two -->

A student can appear to have "lost" work simply because the wrong repository
copy or local folder is open.

## Current Repository Setup Pattern

For Module Two and later assignment/project repositories, students should
follow the complete repository-setup command block in the current activity
README.

> [!IMPORTANT]
> Students should **not click Fork or Use this template** on the public GC-STEM
> repository. The activity README uses a GitHub CLI command such as
> `gh repo create ... --template ... --private --clone` to create the student's
> private repository.

The use of `--template` in the documented CLI command is intentional. It does
not mean the student should choose GitHub's browser **Use this template**
button.

## What LSS Can Help Explain

Appropriate learning-level tool support includes:

* why the student works in the local clone;
* why commits and pushes preserve Git history and the GitHub copy;
* what `git status` communicates;
* why a private student repository differs from the GC-STEM template;
* why the student follows the activity README instead of clicking Fork or Use
  this template;
* why `it140-projects` continues across Modules Five through Seven;
* why a missing local folder may be restored from an existing private GitHub
  repository;
* why one development environment is simpler than alternating between devices;
  and
* where repository instructions, tests, and supporting files are located.

Use the canonical [GitHub Workflow](../shared/github-workflow.md) rather than
duplicating procedural details here.

## Safe Device-Switch Concept

When a student works on more than one device, the course workflow requires the
student to push completed local work before switching and to run
`git pull --ff-only` on the next existing local clone before making new edits.

LSS may explain **why** this sequence keeps the GitHub copy and local copies in
sync.

If `git pull --ff-only` or `git push` fails, or Git reports that histories
cannot be fast-forwarded, stop at the learning-support boundary. The student
should not continue editing on either device or experiment with merge, reset,
rebase, or force-push commands. Route the case to technical support.

See
[Working on More Than One Device](../shared/github-workflow.md#working-on-more-than-one-device).

## Private Repository Access

A student's assignment/project repository is private.

If direct LSS review of the repository is appropriate, the student may grant
collaborator access through the approved GitHub workflow.

Do not ask a student to make graded work public to obtain help.

When reviewing a student's private repository:

* focus on the support question;
* do not redistribute private student work;
* avoid changing or committing to the repository unless an approved support
  process specifically requires it; and
* keep the student engaged in explaining and changing their own work.

## Useful Read-Only Information

When trying to understand repository state, useful non-secret information can
include:

```bash
git status
git remote -v
```

For GitHub CLI authentication:

```bash
gh auth status
```

LSS may use the output to recognize that a problem is technical.

Do not ask students to send:

* passwords;
* two-factor authentication codes;
* recovery codes;
* device codes;
* access tokens; or
* passkeys.

## Course IDE and CVD

The CVD is the IT 140 reference environment.

LSS may help students with normal learning-level use such as:

* opening the correct repository in VS Code;
* locating the Terminal;
* running Python;
* interpreting Python output;
* running course-provided tests when the activity documents them; and
* locating course files.

The common repository-opening pattern is:

```bash
cd ~/Repos/<repository-name>
code .
```

If VS Code opens an IT 140 repository under `~/Repos` in **Restricted Mode**,
use the activity README or shared
[VS Code Restricted Mode](../shared/github-workflow.md#vs-code-restricted-mode)
guidance. Do not advise students to disable VS Code security protections
broadly.

See [Supported Environments](../shared/supported-environments.md) for the
canonical environment facts.

## Student CI Feedback

LSS may help a student **read** repository feedback, but the GitHub Actions
result is not a grade.

Useful high-level points are:

* a fresh untouched personal repository is intended to be neutral;
* after graded work begins, CI may provide formative structural/completion
  feedback;
* a green check does not prove rubric compliance or submit the activity; and
* Ruff feedback in the Projects repository is advisory and does not by itself
  make student CI fail.

Questions about whether the work meets the rubric remain with faculty.
Unexpected infrastructure behavior or repeated CI failures across students may
need technical escalation.

## Stop at the Technical Boundary

Route to technical support when the issue is primarily:

* CVD access or launch;
* local course IDE installation/configuration;
* Python itself cannot run;
* VS Code will not launch;
* GitHub authentication fails;
* `gh` fails to access the intended account;
* the current activity README repository-setup or clone command fails;
* the student used Fork/Use this template and the resulting repository state
  must be assessed;
* `git pull --ff-only` or `git push` fails;
* repository recovery risks losing student work; or
* Verify reports `NOT COMPLIANT` or another environment failure.

Use [Service Desk Triage](../service-desk/triage.md) as the technical-support
reference.

## Do Not Use "Start Over" as the First Fix

A repository problem can involve multiple copies of the student's work.

Before any destructive action, preserve student work and use the documented
repository recovery path.

See:

* [Recovering a Damaged Local Copy](../shared/github-workflow.md#recovering-a-damaged-local-copy)
* [Starting Over From the Course Template](../shared/github-workflow.md#starting-over-from-the-course-template)

Technical recovery beyond ordinary documented steps should move to the Service
Desk.

Return to the [LSS Support Guide](README.md).
