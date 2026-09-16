# IT 140 Service Desk Escalation

Use this page when first-line technical troubleshooting does not resolve the
problem or the issue belongs to another support path.

The shared [Escalation Model](../shared/escalation-model.md) defines the common
evidence package. This page applies that model to the IT Service Desk role.

## Before Escalating

Confirm that you have:

* classified the problem;
* protected the student's work;
* checked whether the student can continue in the CVD;
* followed the current course/script remediation where appropriate;
* collected the relevant summary/log/support artifact; and
* removed or protected private/security-sensitive information.

## Build the Evidence Package

Use the canonical
[IT 140 Escalation Model](../shared/escalation-model.md#minimum-evidence-package)
for the common handoff fields and evidence rules.

For a **Service Desk** escalation, make sure the handoff also makes these
points easy to identify:

| Service Desk Addition | What to Record |
| --- | --- |
| Course continuity | Whether the student can continue in the CVD |
| Technical layer | Access, environment, lifecycle automation, GitHub/repository, or another technical layer |
| Current procedure | The exact README/guide section and action being followed |
| Automation evidence | Final result, exit code, remediation/next-step text, and exact log/support-artifact path when applicable |
| Work already attempted | Only the documented actions that were actually performed |
| Requested action | What the receiving support role is being asked to do |

Do not duplicate large log excerpts in the ticket when an authorized
attachment or sanitized support artifact is sufficient.

<!-- screenshot placeholder; show a model Service Desk ticket with the IT 140
environment, failed step, exact summary, exit code, CVD continuity, and attached
sanitized support artifact fields visible -->

## Route to Faculty

Route to faculty when the technical environment works and the primary question
is about:

* assignment requirements;
* what must be submitted;
* grading or rubric application;
* instructor feedback;
* course deadlines or instructor-controlled processes; or
* other instructional matters that require faculty authority.

Do not interpret or override the D2L Brightspace Guidelines and Rubric from a
Service Desk ticket.

## Route to LSS

Route or refer to Learning Support Specialists (LSS) when the environment works
and the student needs learning support with:

* programming concepts;
* understanding syntax/errors in student-created code;
* debugging strategy;
* pseudocode/flowchart reasoning; or
* development of the student's own solution.

Do not provide a complete graded solution through the technical support process.

## Course Technical Maintenance Escalation

Escalate to the course technical maintenance path when evidence indicates a
defect in course-managed technical content rather than an individual user's
normal environment.

Examples:

* current public README command fails as written;
* a course lifecycle script fails reproducibly in the supported environment;
* a controlled manifest/schema or course asset is invalid;
* a public starter file/test is missing or malformed;
* a student CI workflow behaves differently from its documented lifecycle;
* course automation and documentation disagree;
* the same supported-environment or GitHub Actions failure affects multiple
  users; or
* the reference CVD reproduces the course-tool failure.

Before escalation:

1. Check [Course Status](https://github.com/GC-STEM/it140/wiki/Course-Status).
2. Capture exact reproduction steps.
3. Include script version/Version DTG when shown.
4. Include the final summary and exit code.
5. Attach the relevant sanitized support artifact or reviewed log when
   appropriate.
6. State whether the problem reproduces in the CVD.

A public GitHub Issue can be appropriate for a reproducible defect in public
course content **only when the report contains no protected/private information
or graded student solution**.

* [Main IT 140 Issues](https://github.com/GC-STEM/it140/issues) — course-wide
  automation or repository issue
* [Module One Setup Tasks Issues](https://github.com/GC-STEM/it140-m1-setup-tasks/issues)
  — setup instructions or platform-specific setup behavior

When a public issue is not appropriate, use the current approved internal
Service Desk/course-maintenance path. Queue, category, assignment-group, and
contact details should be maintained in the appropriate SNHU internal support
system rather than this public repository.

## University-System or Account Escalation

For SNHU account, Brightspace, Codio access, device-management, or other
university-system problems, use the approved internal Service Desk escalation
path for that system.

Do not move an account-specific case into a public GitHub Issue merely because
IT 140 uses GitHub or Codio.

ServiceNow categories, assignment groups, contacts, and other restricted
routing details should be maintained in the approved internal support system
rather than this public repository.

## GitHub Account/Service Escalation

Separate these two cases:

### Account/Authentication Problem

Examples:

* user cannot access the intended GitHub account;
* GitHub requires account recovery;
* authentication is blocked outside the IT 140 scripts.

Use the appropriate account/service support path. Do not request credentials or
recovery secrets.

### Course Workflow/Repository Problem

Examples:

* the current activity README repository-setup command fails;
* the documented clone/push/pull workflow fails unexpectedly;
* a GC-STEM repository is missing or malformed;
* course documentation creates an incorrect remote/repository state; or
* a fresh untouched personal repository receives an unexpected CI failure that
  contradicts the activity's documented student CI lifecycle.

Use the course technical maintenance path when the problem is reproducible and
course-provided.

If a student's histories have diverged after working on more than one device,
preserve the affected copies and avoid merge/reset/rebase/force-push commands
until the repository state is understood. This may be an individual repository
recovery case rather than a public course defect.

## Public Versus Internal Evidence

Follow the shared
[Public GitHub Issue Versus Internal Escalation](../shared/escalation-model.md#public-github-issue-versus-internal-escalation)
and
[Privacy and Security Review](../shared/escalation-model.md#privacy-and-security-review)
rules.

For the Service Desk specifically:

* account-specific, student-specific, managed-device, and university-system
  cases stay in authorized internal channels;
* a public GitHub Issue is only for a reproducible defect in public course
  content that can be reported safely without protected information or graded
  student work; and
* when in doubt, keep the case internal and escalate through the approved
  Service Desk path.

## Escalation Completion Criteria

A handoff is ready when the receiving role can determine:

* the failing layer;
* the environment and exact procedure;
* what has already been tried;
* the authoritative evidence;
* whether the student has a course-continuity path; and
* what action is requested from the receiving role.

Return to the [Service Desk Triage and Escalation Runbook](README.md).
