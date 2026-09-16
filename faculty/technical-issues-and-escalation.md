# IT 140 Faculty | Technical Issues and Escalation

Faculty should be able to recognize and route technical problems without becoming the final technical escalation point.

## First Decide What Is Failing

Use this distinction:

| Evidence | Likely Path |
| --- | --- |
| Student cannot access a required system or launch the environment | IT Service Desk |
| Supported course IDE cannot configure or Verify | IT Service Desk |
| GitHub authentication/template/clone workflow fails | IT Service Desk |
| Python runs but the student's code fails | Faculty / Academic Support learning path |
| Student needs time/task, organization, technical-reading, or learning strategies | Academic Coaching |
| Current public GC-STEM instructions or course-managed artifact fails reproducibly | Course technical maintenance |
| Grading/assignment interpretation question | Faculty |

See [Support Boundaries](../shared/support-boundaries.md) and [Academic Support for IT 140](../academic-support/README.md).

## Keep the Student Moving

When a student's local course IDE is the problem, encourage use of the CVD while the local issue is investigated.

The CVD is the reference environment and a working local installation is optional.

Do not spend instructional time attempting increasingly invasive local-system repairs when the issue belongs to technical support.

## What to Preserve Before Referring a Technical Problem

When practical, ask the student to preserve:

* environment: CVD, Windows, macOS, Linux, or unsupported;
* exact task/step;
* exact error message;
* Verify final summary and exit code when applicable;
* exact log/support-artifact path when applicable; and
* whether the student can continue in the CVD.

The full common evidence model is in [Escalation Model](../shared/escalation-model.md).

Faculty do not need to collect every field before a normal Service Desk referral if doing so would delay support; preserve the evidence already available.

## Course-Provided Content Appears Defective

Examples include:

* public README command fails as written;
* course-provided starter file is missing or malformed;
* current public link is broken;
* course-provided test appears invalid;
* course documentation and automation disagree; or
* the same supported-environment failure affects multiple users.

Before reporting:

1. check [IT 140 Course Status](https://github.com/GC-STEM/it140/wiki/Course-Status);
2. confirm that you are using the current live repository;
3. reproduce the problem in the reference CVD when reasonable;
4. remove student-specific/private data; and
5. report the reproducible course defect through the appropriate course GitHub Issue or approved internal path.

### Public GitHub Issues

A public GitHub Issue can be appropriate for a defect in public course content when the report contains no protected information or graded student solution.

Common locations include:

* [Main IT 140 Issues](https://github.com/GC-STEM/it140/issues) — course-wide automation or central repository problems
* [Module One Setup Tasks Issues](https://github.com/GC-STEM/it140-m1-setup-tasks/issues) — setup instructions or setup automation
* The Issues tab of the affected assignment/project repository — activity-specific public repository defect

<!-- screenshot placeholder; show an IT 140 repository Issues tab and the new-issue entry point without displaying any private student information -->

## Faculty-Only Questions or Concerns

Do not post faculty-sensitive questions, student-specific matters, grading concerns, or internal SNHU operational information in public GitHub Discussions or Issues.

Use the current approved faculty-only SNHU communication/escalation channel.

Specific channel names, contacts, or restricted routing details should be maintained in the appropriate SNHU internal system rather than this public repository.

## When to Use the IT Service Desk

Refer technical problems involving:

* university account/system access;
* Brightspace/Codio access;
* supported local computer restrictions;
* CVD launch/configuration;
* supported course IDE failures;
* GitHub authentication;
* GitHub CLI;
* repository creation/cloning/recovery; or
* another individual technical environment issue.

The [Service Desk Triage and Escalation Runbook](../service-desk/README.md) documents the technical support path.

## When the Problem Is Not Technical

If Python and the course environment work:

* programming concepts/student-code debugging → faculty or an appropriate [Academic Support](../academic-support/README.md) learning service;
* time/task, organization, technical-reading, or learning-strategy need → [Academic Coaching](../academic-support/coaching.md);
* assignment/rubric/grade question → faculty; or
* academic planning → advisor.

Do not send these problems through the Service Desk merely because the student is working in VS Code.

## What Not to Do

Do not:

* disable security controls;
* bypass device-management restrictions;
* randomly reinstall course tools after an automation failure;
* edit course lifecycle scripts/manifests to force success;
* delete a student's repository as a first troubleshooting step;
* ask for authentication secrets; or
* post private student work in a public issue.

## After a Confirmed Course Defect

If a course technical defect affected student work:

* preserve the issue/reference;
* communicate any approved workaround consistently;
* apply grading/course remedies through the appropriate faculty process; and
* use the corrected live course documentation rather than continuing to distribute the workaround after the source is fixed.

Return to the [Faculty Support Guide](README.md).
