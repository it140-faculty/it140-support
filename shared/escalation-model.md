# IT 140 Escalation Model

This page defines the **common evidence and handoff model** for IT 140 support escalations.

It does not define SNHU's internal ticket queues, service-level agreements, staff contact lists, or restricted administrative procedures. Those belong in the appropriate internal systems or role-specific guides.

## Goal of an Escalation

A useful escalation allows the next support person to continue the investigation **without starting over**.

A good handoff answers:

* What was the user trying to do?
* Where were they doing it?
* What should have happened?
* What actually happened?
* What evidence was collected?
* What safe troubleshooting has already been attempted?
* What is the current impact?
* Can the student continue working through the CVD or another supported path?

## First: Protect Course Continuity and Student Work

Before escalating:

1. Preserve the student's files and repositories.
2. Do not delete or overwrite the only known copy of student work.
3. If a local environment is failing, determine whether the student can continue in the CVD reference environment.
4. Do not make broad system changes merely to produce a different result.
5. Do not bypass security controls or management restrictions.

A workaround that keeps coursework moving does not eliminate the need to investigate a reproducible course defect, but it can reduce immediate student impact.

## Classify the Problem Before Escalating

Use [Support Boundaries](support-boundaries.md) to determine whether the primary issue is:

* technical access/environment;
* Git/GitHub/repository workflow;
* student code or programming concepts;
* assignment/grading;
* academic advising; or
* a course-provided technical artifact.

An escalation should go to the role that can act on the actual problem, not merely the role that first received the question.

## Minimum Evidence Package

Collect as much of the following as applies.

### User and Course Context

* User role: student, faculty, LSS, advisor, or other
* IT 140 module/activity
* Relevant repository name
* Whether the issue blocks current course work
* Whether a working CVD path is available

Do not place protected student information in public GitHub content.

### Environment

* CVD, Windows, macOS, or Linux
* Operating-system version for local computers
* Whether the device is personally controlled or managed/restricted
* Whether the configuration is a supported automated environment or a best-effort/manual environment

### Location in the Procedure

* README or guide being followed
* Section or numbered step
* Script or application name
* Exact action being attempted

### Expected and Actual Result

Record:

* what the instructions said should happen;
* what actually happened; and
* whether the problem is repeatable.

Avoid summaries such as "it doesn't work" when more specific information is available.

### Commands and Messages

When applicable, preserve:

* the exact command entered;
* the complete error message;
* the final script summary; and
* the script's displayed Next step or remediation message.

Copy text directly when practical rather than retyping it from memory.

## Automation-Specific Evidence

IT 140 lifecycle scripts are designed to produce support evidence.

For an automation problem, collect:

* lifecycle stage: Prepare, Install, Configure, Verify, or Update;
* platform;
* final result such as `PASS`, `FAIL`, `PARTIAL`, `COMPLIANT`, or `NOT COMPLIANT`;
* warning and failure counts when shown;
* exit code;
* exact log/transcript path; and
* the relevant log file.

A normal successful verification reports:

```text
Result: COMPLIANT
Failed: 0
Exit code: 0
```

A `FAIL`, `PARTIAL`, `NOT COMPLIANT`, nonzero exit code, or remediation message should be treated as information to preserve and interpret—not as a reason to improvise a repair.

<!-- screenshot placeholder; show an example failed or NOT COMPLIANT Verification Summary with Result, warning/failure counts, Exit code, Remediation/Next step, and log path visible -->

## Standard Log Locations

Lifecycle logs are stored in:

```text
Windows:
%USERPROFILE%\it140\logs\

CVD, macOS, Linux:
~/it140/logs/
```

Each run creates a timestamped text log or transcript.

The log can help identify:

* script version;
* platform;
* actions performed;
* completed stages; and
* the point of failure.

When a script identifies a specific log path, use that path instead of guessing which file is relevant.

## Repository-Specific Evidence

For a repository or Git/GitHub problem, collect:

```text
GitHub username:
Repository name:
Repository owner:
Repository visibility:
GitHub repository URL:
Local repository path:
```

From the local repository root, these commands are commonly useful:

```bash
git status
git remote -v
```

For GitHub CLI authentication problems:

```bash
gh auth status
```

The output can help determine whether:

* the student is using the intended GitHub account;
* the local clone is connected to the student's private repository;
* the repository already exists;
* the user opened the wrong local folder; or
* the local and GitHub copies have diverged.

Review command output before sharing it publicly.

## Screenshots

A screenshot is useful when the problem depends on a graphical state that text does not capture well.

Examples:

* the wrong GitHub repository owner is visible;
* VS Code has the wrong top-level folder open;
* an authentication page displays an unexpected state;
* a CVD or noVNC control is missing;
* a graphical installer or OS dialog reports an error.

A good support screenshot should:

* include enough surrounding context to identify the application and problem;
* show the complete relevant message when possible;
* avoid unnecessary desktop or browser content; and
* be reviewed for private information before sharing.

Do not use a screenshot as a substitute for copyable terminal text or logs when the text is available.

## Troubleshooting Already Attempted

Record only actions that were actually performed.

Examples:

```text
Troubleshooting already attempted:
* Reopened a new regular PowerShell window.
* Ran Verify again.
* Confirmed gh auth status shows the intended account.
* Confirmed the same local problem does not occur in the CVD.
```

This prevents the next supporter from repeating the same steps without reason.

## Actions to Avoid Before Escalation

Unless current course instructions or an authorized support procedure directs otherwise, do not:

* randomly reinstall Python, VS Code, Git, or GitHub CLI;
* delete the student's assignment/project repository;
* delete Git history;
* edit course automation scripts, manifests, or schemas;
* run another platform's lifecycle scripts;
* disable security controls;
* bypass device-management restrictions;
* run broad manual package repairs after a course script failure;
* recreate a student's repository without first identifying and preserving existing work; or
* expose private credentials or student work in a public issue.

## Privacy and Security Review

Before sending screenshots, logs, terminal output, or repository information, check for:

* passwords;
* authentication or verification codes;
* personal access tokens;
* recovery codes;
* private contact information;
* student identification numbers;
* other credentials or secrets;
* confidential SNHU information; and
* complete solutions to graded assignments.

Remove or use an authorized private support channel for information that should not be public.

> [!WARNING]
> Never ask a student to send a password, authentication code, recovery code, passkey, or access token as troubleshooting evidence.

## Public GitHub Issue Versus Internal Escalation

A **public GitHub Issue** may be appropriate when the problem is a reproducible defect in public course content and can be described safely without private information.

Examples:

* broken public link;
* incorrect README command;
* missing public starter file;
* reproducible course automation failure that can be described without credentials or protected data.

An **internal support channel** is more appropriate when the case includes:

* protected student information;
* account-specific information;
* internal SNHU routing;
* privileged infrastructure details;
* security-sensitive data; or
* information that should not be publicly searchable.

Role-specific guides should identify the correct internal destination.

## Suggested Escalation Handoff Format

Use a concise structure such as:

```text
IT 140 escalation

User role:
Module/activity:
Issue category:

Environment:
Operating system/version:
Supported or manual configuration:

Repository:
GitHub owner:
Local path:

Guide/step:
Action attempted:
Expected result:
Actual result:

Exact error/final summary:
Exit code:
Log path:

Troubleshooting already attempted:
CVD continuity available: Yes / No / Not applicable

Attachments:
* Relevant log
* Screenshot, if useful

Private/security information removed or sent through an authorized channel: Yes
```

Not every field applies to every problem. Omit fields that are irrelevant rather than filling them with guesses.

## Reproduction in the CVD

For a course-environment or course-provided artifact problem, the CVD can be a useful reference point because it is the standard course environment.

If the same problem can be reproduced in a clean/current CVD configuration, record that fact.

If the problem occurs only on a local computer and the CVD works, record that too.

This distinction can help isolate:

* a course-wide defect;
* a platform-specific automation problem;
* a local-machine configuration problem; or
* a student-code issue.

Do not copy private student code into public reproduction steps.

## After Escalation

The receiving support role should be able to determine:

* what has already been checked;
* whether the student has a continuity path;
* what evidence is authoritative;
* what remains unknown; and
* what action is needed next.

If the investigation identifies an error in shared support documentation, update the canonical shared page rather than adding competing instructions to multiple role guides.

If the investigation identifies a role-specific procedure change, update that role's guide and keep the shared facts unchanged unless the underlying course behavior also changed.

## Related Shared Documentation

* [Course Overview](course-overview.md)
* [Course Repository Architecture](course-repository-architecture.md)
* [Terminology](terminology.md)
* [Supported Environments](supported-environments.md)
* [GitHub Workflow](github-workflow.md)
* [Support Boundaries](support-boundaries.md)

Return to the [Shared Documentation Index](README.md).
