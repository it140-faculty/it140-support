# IT 140 LSS | Referrals and Escalation

LSS should keep the student moving toward the right kind of help without taking ownership of problems outside the learning-support role.

Use [Support Boundaries](../shared/support-boundaries.md) as the canonical routing model and [Academic Support for IT 140](../academic-support/README.md) when deciding whether another Academic Support service is a better fit.

## Refer Within Academic Support

Not every student who reaches an LSS needs the same type of learning support.

| Need | Academic Support Option |
| --- | --- |
| Quick on-demand general Python help | [24/7 Drop-In Tutoring](../academic-support/tutoring.md) |
| Time/task prioritization or organization | [Academic Coaching](../academic-support/coaching.md) |
| Reading and following technical documentation | [Academic Coaching](../academic-support/coaching.md#reading-comprehension-and-technical-documentation) |
| Academic-skill development or critical-thinking/problem-solving process | [Academic Coaching](../academic-support/coaching.md) |
| Learning strategies related to a diagnosed learning difference | [Academic Coaching](../academic-support/coaching.md#support-for-learning-differences) |
| Writing-development feedback on the IDE Features reflection or game-theme writing | Written Feedback; see [Academic Support for IT 140](../academic-support/README.md#written-feedback) |
| English-language learning support | Use the ELL/ESOL pathways in [Academic Support for IT 140](../academic-support/README.md#english-language-learning-support) |

These services can complement each other. A student may use LSS for programming learning and Academic Coaching for time/organization in parallel.

## Refer to Faculty

Refer the student to faculty for:

* interpretation of assignment requirements;
* what must be submitted;
* whether work meets a rubric criterion;
* grades;
* instructor feedback;
* deadlines or late-work questions;
* accommodations/course decisions within faculty responsibility; and
* questions about whether a particular approach is acceptable for a graded activity.

LSS may help the student understand concepts related to the work, but faculty remains authoritative for the graded requirement.

## Refer to the IT Service Desk

Route technical failures such as:

* CVD access or launch problems;
* supported local course IDE installation/configuration failures;
* Python itself cannot run;
* VS Code will not launch;
* GitHub authentication problems;
* GitHub CLI (`gh`) failures;
* repository creation or cloning failures;
* risky Git/repository recovery;
* Verify failures; or
* another supported environment problem.

When practical, preserve:

* the environment;
* exact task/step;
* exact error message;
* Verify final summary/exit code when applicable; and
* whether the student can continue in the CVD.

See [Service Desk Triage and Escalation Runbook](../service-desk/README.md).

## Refer to an Academic Advisor

Refer academic-planning questions such as:

* course sequencing;
* program planning;
* broader academic-path questions; and
* concerns that require advising rather than technical, instructional, or coaching support.

## Course-Provided Content Appears Defective

Examples include:

* a public course README command is incorrect;
* a public course link is broken;
* a starter file or test appears defective;
* documentation and automation disagree; or
* multiple students encounter the same supported-environment failure.

Before escalating:

1. check [IT 140 Course Status](https://github.com/GC-STEM/it140/wiki/Course-Status);
2. confirm the current live repository/resource;
3. preserve the exact URL and issue;
4. avoid including private student work; and
5. use the appropriate public GitHub Issue or approved internal course path.

The common evidence model is in [Escalation Model](../shared/escalation-model.md).

## Academic Resource Center Issue

If the problem is in an LSS/Academic Support learning resource:

* preserve the Academic Resource Center URL;
* identify the specific incorrect/outdated section;
* compare it with current IT 140 materials;
* distinguish a general programming error from an IT 140-specific mismatch; and
* use the current Academic Support resource-maintenance process.

Do not report an Academic Resource Center content correction as an IT 140 course-repository defect unless the underlying course source is also incorrect.

## Group-Session Privacy

Do not route private student information through a public GitHub Issue or expose it in a group session.

Public GitHub reporting is appropriate only for a reproducible defect in public course content that can be reported safely.

See:

* [Public Versus Internal Support Channels](../shared/support-boundaries.md#public-versus-internal-support-channels)
* [Privacy and Security Review](../shared/escalation-model.md#privacy-and-security-review)

## Escalation Handoff

A concise LSS handoff should explain:

* what the student is trying to do;
* whether the issue is programming learning, academic-skills/coaching, assignment, technical, advising, or course-resource related;
* exact error/behavior when applicable;
* what LSS support was already attempted;
* where the student was referred; and
* any evidence that will prevent the next supporter from starting over.

Avoid diagnosing beyond the evidence.

Return to the [LSS Support Guide](README.md).
