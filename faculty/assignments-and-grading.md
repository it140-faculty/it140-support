# IT 140 Faculty | Assignments and Grading

This page explains how the GitHub course resources fit into faculty assignment
support and grading.

## Brightspace Is Authoritative

For graded activities, **D2L Brightspace is the authoritative source** for:

* assignment/project requirements;
* required deliverables;
* submission instructions;
* grading criteria;
* deadlines;
* instructor feedback; and
* the official student submission.

GitHub supports the student's development workflow. It does not replace
Brightspace as the grading system unless a future activity explicitly says
otherwise.

## Use Two Sources Together

Before supporting or grading an activity, review:

1. the current D2L Brightspace Guidelines and Rubric; and
2. the current activity repository `README.md`.

Use them for different purposes:

| Source | Primary Purpose |
| --- | --- |
| D2L Brightspace Guidelines and Rubric | What the student must do, submit, and be graded on |
| Activity repository README | How the student uses the provided files, folders, tools, repository workflow, and support resources |

<!-- screenshot placeholder; show an activity's D2L Guidelines and Rubric beside
the corresponding GitHub repository README to illustrate the two-source model -->

## Grade the Required Deliverables

Repositories may contain materials that support development but are not
themselves graded deliverables, such as:

* README files;
* requirements/design references;
* starter code;
* tests;
* configuration;
* Wiki resources; and
* optional practice folders.

Do not assign additional grading requirements merely because a support file
exists in the repository.

Likewise, do not treat a repository-provided automated test as an independent
grading rubric unless the current Brightspace activity explicitly makes that
test/result part of the graded requirement.

## GitHub Actions and Student CI Are Formative

The version 1.0.4 assignment/project repositories standardize GitHub Actions so
student CI provides **formative repository feedback**, not grading automation.

Faculty should interpret student CI using these principles:

* A **fresh personal repository is neutral**. An untouched starter should not
  fail merely because the student has not begun graded work.
* After graded work begins, CI may report incomplete, damaged, or unexpectedly
  changed artifacts.
* A **green check does not mean the work meets every rubric criterion** and does
  not submit anything to Brightspace.
* Module Three student CI focuses on the two graded design artifacts; its
  optional Python program and optional acceptance tests are not student CI
  requirements.
* Module Four student CI focuses on the graded pseudocode; its optional Python
  program and optional practice tests are not student CI requirements.
* The Projects repository uses progressive student CI across Module Five,
  Module Six, and Module Seven.
* In the Projects repository, **Ruff style/quality feedback is advisory** and
  does not by itself cause the student CI workflow to fail.

Each assignment/project repository contains a maintainer-facing CI guide under
`.github/ci/README.md` with the activity-specific behavior.

When a student's CI result is unexpected, distinguish normal formative
feedback from a possible repository/infrastructure defect before using the CI
result as evidence about the student's work.

## If Brightspace and GitHub Appear to Conflict

If a repository instruction appears inconsistent with the current Guidelines
and Rubric:

1. use the current Brightspace requirements for grading;
2. do not require a student to resolve the documentation conflict independently;
3. capture the conflicting wording/links; and
4. report the course documentation issue through
   [Technical Issues and Escalation](technical-issues-and-escalation.md).

Do not silently create a third interpretation.

## Project Progression

Modules Five through Seven use the same `it140-projects` repository, but the
graded work changes by module.

Faculty should use the current Brightspace Guidelines and Rubric for each stage
rather than grading later-stage functionality during an earlier
design/prototype activity.

For the shared repository structure and stage progression, see:

* [Course Overview](../shared/course-overview.md#course-development-progression)
* [Projects | Modules Five Through Seven](../shared/course-repository-architecture.md#projects--modules-five-through-seven)

## Student Repository Is Supporting Evidence, Not the Default Submission

A student's private GitHub repository may help faculty understand:

* the student's working files;
* repository state;
* development history;
* CI feedback; or
* a technical problem.

However, normal grading should follow the deliverables submitted through
Brightspace.

Do not require students to make private repositories public to be graded or
supported.

## Feedback and Technical Problems

When a graded deliverable fails because of student-created code or design work,
provide feedback aligned to the activity rubric.

When the evidence instead suggests that a **course-provided file, test,
template, CI workflow, or tool is defective**, separate that technical defect
from the student's grading outcome and report it through the course technical
path.

Examples that deserve technical review include a newly created untouched
personal repository failing contrary to the documented student CI lifecycle,
or several students receiving the same unexpected GitHub Actions
infrastructure failure.

Do not penalize a student for a confirmed course infrastructure defect without
applying the appropriate course/institutional process.

## AI and Academic Integrity

Use the current course, assignment, and SNHU academic-integrity/AI guidance in
Brightspace when evaluating student work.

Do not infer a separate GitHub-specific academic-integrity rule merely from
repository structure or Git history.

Public faculty support content should not include complete solutions to graded
IT 140 assignments or projects.

## Questions That Require Faculty Authority

Keep these with faculty rather than routing them to technical support:

* Does this submission meet the rubric?
* Which deliverable is required?
* How should an ambiguous requirement be interpreted?
* How does instructor feedback apply?
* What is the consequence of a late/missing submission?
* Is a particular source/use of AI acceptable under the current activity
  policy?

Return to the [Faculty Support Guide](README.md).
