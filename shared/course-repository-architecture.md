# IT 140 Course Repository Architecture

This page explains how the IT 140 GitHub repositories fit together and how to
distinguish a **course repository**, a **student's private GitHub repository**,
and a **local cloned repository**.

This distinction is essential for support. The same repository name may appear
in all three places, but each copy has a different owner and purpose.

## The Three-Copy Model

For assignment and project work, support personnel should think in terms of
three related copies:

```text
GC-STEM public course template
          │
          │ activity README setup command
          ▼
Student's private GitHub repository
          │
          │ clone
          ▼
Student's local repository in ~/Repos
```

> [!IMPORTANT]
> The current assignment/project workflow uses the public repository as a
> template through the activity README's GitHub CLI command. Students should
> **not click Fork or Use this template** on the public GC-STEM repository.

### 1. Public Course Repository

A public course repository is maintained by **GC-STEM**.

Examples:

* `GC-STEM/it140-m2-assignment`
* `GC-STEM/it140-m3-assignment`
* `GC-STEM/it140-m4-assignment`
* `GC-STEM/it140-projects`

These repositories provide the current course starting point, instructions,
starter files, configuration, and other supporting resources.

Students normally **do not edit the GC-STEM course repository**.

### 2. Student's Private GitHub Repository

For assignment and project repositories, the student uses the current activity
README commands to create a **private repository in the student's own GitHub
account** based on the current GC-STEM course template.

The student repository normally has the same repository name as the course
template.

Example:

```text
Course template:
https://github.com/GC-STEM/it140-m3-assignment

Student repository:
https://github.com/<student-username>/it140-m3-assignment
```

The student's private GitHub repository is the remote copy of the student's
work and Git history.

### 3. Student's Local Clone

The activity README creates or clones the student's private GitHub repository
into the course development environment.

The expected course workspace is normally:

```text
~/Repos/
```

Examples:

```text
~/Repos/it140-m2-assignment/
~/Repos/it140-m3-assignment/
~/Repos/it140-m4-assignment/
~/Repos/it140-projects/
```

This local clone is the copy the student normally opens in VS Code and edits.
The common opening pattern is `cd ~/Repos/<repository-name>` followed by
`code .`.

> [!IMPORTANT]
> A supporter should identify **which copy is being discussed before changing,
> deleting, renaming, recreating, or recloning anything**.

<!-- screenshot placeholder; show the GitHub owner/repository breadcrumb on a
GC-STEM course template and on a student's private repository so the difference
in repository ownership is visually clear -->

## Course Repository Catalog

### Main Course Repository

**Repository:** [`GC-STEM/it140`](https://github.com/GC-STEM/it140)

The main repository is the central technical hub for IT 140. It contains:

* course development-environment automation;
* course-wide configuration;
* technical status information;
* links to activity repositories;
* technical documentation and Wiki pages; and
* course-wide Issues and Discussions.

Students do **not** normally clone the main repository for course work. Course
automation obtains the files it needs.

### Module One Setup Tasks

**Repository:**
[`GC-STEM/it140-m1-setup-tasks`](https://github.com/GC-STEM/it140-m1-setup-tasks)

This repository provides the Module One setup workflow for:

* GitHub account preparation;
* Codio Virtual Desktop (CVD) configuration;
* supported local course IDE setup; and
* setup-specific troubleshooting.

Students normally follow the repository instructions in the browser rather
than cloning this repository.

### Module Two Assignment

**Repository:**
[`GC-STEM/it140-m2-assignment`](https://github.com/GC-STEM/it140-m2-assignment)

Students follow the current activity README to create a private repository
based on this course template and use it for the Module Two assignment.

The activity introduces the course repository workflow while students complete
a beginner Python program and related IDE reflection work.

### Module Three Assignment

**Repository:**
[`GC-STEM/it140-m3-assignment`](https://github.com/GC-STEM/it140-m3-assignment)

Students follow the current activity README to create a private repository
based on this course template and use it for the Module Three design
assignment.

The repository uses a simplified development structure:

```text
analysis/
design/
src/
tests/
```

The graded work is design-focused; construction and testing may be included as
practice. The current D2L Brightspace Guidelines and Rubric remain authoritative
for what is graded.

### Module Four Assignment

**Repository:**
[`GC-STEM/it140-m4-assignment`](https://github.com/GC-STEM/it140-m4-assignment)

Students follow the current activity README to create a private repository
based on this course template and use it for the Module Four assignment.

The repository continues the simplified software-development workflow while
the graded work focuses on pseudocode design. Refer to the current D2L
Brightspace Guidelines and Rubric for exact requirements.

### Projects | Modules Five Through Seven

**Repository:**
[`GC-STEM/it140-projects`](https://github.com/GC-STEM/it140-projects)

Students follow the current activity README to create this private repository
**once in Module Five** and continue using the same repository through Module
Seven.

The repository carries the student's work through:

* **Module Five / Project One:** game design;
* **Module Six / Milestone:** simplified movement prototype; and
* **Module Seven / Project Two:** final text-based game.

Important project folders include:

```text
design/
prototype/
src/
tests/
```

A student should not create a second `it140-projects` repository for the
Module Six Milestone or Project Two.

### IT 140 Support Repository

**Repository:**
[`GC-STEM/it140-support`](https://github.com/GC-STEM/it140-support)

This repository contains support documentation for:

* faculty;
* Learning Support Specialists (LSS);
* academic advisors; and
* IT Service Desk personnel.

It is a **support repository**, not a student assignment repository.

### Assignment and Project Repository Template

**Repository:**
[`GC-STEM/it140-m0-template`](https://github.com/GC-STEM/it140-m0-template)

This repository provides a standardized development template used when
building IT 140 assignment and project repositories.

It is not a normal student activity repository. Students should not use it as
a substitute for the module-specific assignment or project template unless
course instructions explicitly direct them to do so.

## Repository READMEs and Wikis

Most IT 140 repositories use the following division of responsibility:

### README Files

README files contain the instructions needed to complete or use the repository.

A top-level `README.md` typically explains:

* what the repository is for;
* what the student or supporter should do;
* which files or folders matter;
* what order to follow;
* where to find help; and
* where to go next.

Nested README files may provide instructions for a particular SDLC phase or
activity folder.

### Repository Wikis

Repository Wikis provide supplemental material such as:

* background explanations;
* terminology;
* technical details;
* FAQs;
* optional learning resources; and
* troubleshooting context.

For a course activity, start with the repository's top-level `README.md` rather
than assuming the Wiki is a prerequisite.

## D2L Brightspace and GitHub Have Different Jobs

The repository architecture does not replace the course LMS.

For graded activities:

* **D2L Brightspace** is authoritative for requirements, grading criteria,
  submission instructions, deadlines, and instructor feedback.
* **GitHub repositories** provide development resources, working files,
  technical instructions, and backup/version-control workflows.

A student's GitHub repository is not the assignment submission unless the
current Guidelines and Rubric explicitly says otherwise.

## Repository Availability and Development Status

Not every course repository or activity is necessarily released or finalized
at the same time.

Before treating a missing or changing repository as an incident:

1. Check the current repository table in
   [`GC-STEM/it140`](https://github.com/GC-STEM/it140).
2. Check the relevant activity repository README.
3. Check current course status information when available.

<!-- screenshot placeholder; show the Course Repositories table in the main
GC-STEM/it140 README with module, activity, local folder, and status columns
visible -->

Do not rely on an old screenshot, copied command, or previous term's repository
state when the live course repository provides newer information.

## Repository Lifecycle and Recovery

Students normally create each assignment or project repository once and then
continue using that repository for the activity. Missing, damaged,
previous-term, reset, or multi-device local copies require different recovery
or synchronization workflows.

For the canonical procedures for:

* returning to existing work;
* safely switching between existing local clones on more than one device;
* moving to another environment or a reset CVD;
* restoring a local clone from GitHub;
* starting over from the current course template;
* identifying the exact repository during troubleshooting; and
* handling repositories for repeat-course attempts,

see [GitHub Workflow](github-workflow.md).

> [!CAUTION]
> Before changing, deleting, renaming, recreating, or recloning a repository,
> identify which copy is involved and preserve the student's work.

## Common Architecture Mistakes

Examples include:

* clicking **Fork** or **Use this template** instead of running the current
  activity README repository-setup commands;
* cloning the public GC-STEM template instead of creating the student's private
  repository through the documented workflow;
* opening the wrong copy of a similarly named repository;
* creating a second personal repository when one already exists;
* editing on two local copies without pushing before the switch and pulling
  with `git pull --ff-only` before new work;
* creating separate `it140-projects` repositories for Modules Five, Six, and
  Seven;
* treating a GitHub backup as a Brightspace submission;
* deleting a local repository before confirming the student's work exists
  elsewhere;
* reusing a previous course attempt's repository instead of creating one from
  the current template; and
* editing course-managed files that the activity README says to leave
  unchanged.

## Related Shared Documentation

* [Course Overview](course-overview.md)
* [Course Glossary](glossary.md)
* [Supported Environments](supported-environments.md)
* [GitHub Workflow](github-workflow.md)
* [Support Boundaries](support-boundaries.md)
* [Escalation Model](escalation-model.md)

Return to the [Shared Documentation Index](README.md).
