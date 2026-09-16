# IT 140 Faculty Setup and Familiarization

Faculty do not need to reproduce every possible student environment. Faculty should, however, have enough familiarity with the **reference CVD** and the student setup workflow to recognize normal course behavior and route problems correctly.

## Faculty Module One Setup Instructions

Use the current faculty-specific setup guide:

[IT 140 Module One | Faculty Setup Instructions](https://github.com/GC-STEM/it140-m1-setup-tasks/blob/main/.faculty/README.md)

That guide is the authoritative location for the faculty-specific steps used to:

* prepare a GitHub account for course use;
* access the CVD through the faculty/instructor path;
* configure and verify the faculty CVD;
* review the student setup experience; and
* review or optionally configure a supported local course IDE.

Do not duplicate those step-by-step commands in this support repository.

## Faculty CVD Access Differs From Student Access

Faculty first reach the CVD through instructor-facing Codio navigation rather than exactly the same initial path students use.

Use the current faculty setup guide for the exact Brightspace/Codio navigation. The guide ultimately places faculty in the same student-facing CVD environment so they can understand what students see.

<!-- screenshot placeholder; show the Brightspace search results for Codio and the instructor-facing path used to reach the CVD, without exposing student information -->

<!-- screenshot placeholder; show the Codio instructor dashboard Overview page with the Preview/eye control used to open the faculty CVD landing page -->

> [!IMPORTANT]
> Codio is the development-environment platform for this course. Assignment submissions, grading, feedback, and normal student-management work remain in D2L Brightspace.

## Minimum Faculty Familiarization

Faculty should be able to recognize:

* the CVD desktop;
* VS Code;
* the integrated Terminal;
* the `~/Repos` workspace;
* the course Verify summary;
* the difference between a GC-STEM public course repository and a student's private repository; and
* where the activity README and Brightspace Guidelines and Rubric fit in the workflow.

For shared definitions, see:

* [Supported Environments](../shared/supported-environments.md)
* [Course Repository Architecture](../shared/course-repository-architecture.md)
* [GitHub Workflow](../shared/github-workflow.md)

## CVD First

The CVD is the course reference environment and the best faculty comparison point when a student reports that something is different or broken.

If a faculty CVD is already configured, the current Verify procedure can assess the course IDE without repairing it. Follow the current CVD instructions or the
[Service Desk Verification and Logs](../service-desk/verification-and-logs.md#cvd-verify) reference.

A successful Verify result is useful evidence that the reference environment is functioning.

## Local Faculty Setup

A supported local course IDE is optional for faculty, just as local setup is optional for students.

A local installation can be useful for:

* viewing assignments outside the CVD;
* testing the student local workflow;
* understanding platform-specific student questions; and
* comparing local behavior with the reference CVD.

Use the current [Module One Setup Tasks](https://github.com/GC-STEM/it140-m1-setup-tasks) platform guide rather than manually assembling the course toolset.

Do not bypass employer/device-management restrictions or security controls to create a local course environment.

## After a CVD Reset

A **RESET VM** returns the CVD to its original course image and removes the configured state.

If your faculty CVD was reset:

1. use the current faculty Module One setup instructions;
2. reconfigure the CVD;
3. verify the course IDE; and
4. restore any faculty working repositories from GitHub as needed.

A normal CVD restart is not the same as a reset.

## When Faculty Setup Fails

If your course environment fails to configure or Verify:

1. preserve the exact script summary and log path;
2. follow the script's documented remediation;
3. check [Course Status](https://github.com/GC-STEM/it140/wiki/Course-Status); and
4. use [Technical Issues and Escalation](technical-issues-and-escalation.md).

Faculty do not need to reverse-engineer course automation or manually repair managed course files.

Return to the [Faculty Support Guide](README.md).
