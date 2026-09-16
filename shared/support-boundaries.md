# IT 140 Support Boundaries

This page provides a common routing model for IT 140 support.

It helps F&S personnel distinguish among:

* technical environment problems;
* programming and learning-support needs;
* academic-skills and coaching needs;
* assignment, grading, and instructor questions; and
* academic-advising concerns.

> [!IMPORTANT]
> This page defines the support model used by the IT 140 support repository.
> Existing SNHU policies, departmental procedures, role definitions, privacy
> requirements, and escalation channels take precedence where they are more
> specific.

## Start by Classifying the Problem

A useful first question is:

> **What is preventing the student from making progress: the technical
> environment, understanding/solving the programming, understanding the graded
> requirement, managing the learning process, or a broader academic concern?**

Then refine the classification.

### Technical Environment or Access Problem

Examples:

* CVD will not launch;
* VS Code will not start;
* Python cannot run in the supported course IDE;
* GitHub authentication fails;
* GitHub CLI cannot access the student's account;
* the repository setup, clone, push, or pull command documented in the current
  activity README fails;
* Verify reports `NOT COMPLIANT`;
* a course lifecycle script fails; or
* a course-provided repository file or tool behaves differently from the
  documentation.

These problems primarily belong to a **technical support** path.

### Programming or Learning Problem

Examples:

* the Python program runs but gives the wrong result;
* the student does not understand a loop, branch, function, list, or
  dictionary;
* pseudocode does not match the student's intended logic;
* the student needs help reasoning through an error in their own code; or
* the student needs help learning how to test or debug.

These problems primarily belong to a **faculty and/or Academic Support
learning** path.

### Academic-Skills or Coaching Problem

Examples:

* the student waits until the weekend to begin most weekly work;
* the student does not know how to prioritize zyBooks, the current assignment,
  and the project;
* the student struggles to read and follow technical documentation;
* the student needs help organizing work across Brightspace, zyBooks, GitHub,
  and the course IDE;
* the student would benefit from academic strategies related to a diagnosed
  learning difference;
* the student needs to strengthen general academic habits; or
* the student needs a repeatable problem-solving process but not Python
  instruction.

These problems are appropriate for **Academic Coaching**. If the concern
expands into academic planning, program requirements, or broader persistence
decisions, an **Academic Advisor** may also be appropriate.

### Assignment or Grading Problem

Examples:

* what must be submitted;
* whether a file meets a rubric criterion;
* a grading decision;
* instructor feedback;
* a deadline;
* an accommodation/course decision within faculty responsibility; or
* a submission problem involving course requirements rather than the technical
  environment.

These questions primarily belong to **faculty/instructor** processes.

### Academic Planning or Referral Problem

Examples:

* whether the course fits a student's academic plan;
* course sequencing;
* broader program questions;
* help identifying the right support resource; or
* concerns that require advising rather than technical, instructional, or
  coaching support.

These primarily belong to **academic advising** processes.

## Primary Support Routing Matrix

| Problem | Primary Support Role/Service | Notes |
| --- | --- | --- |
| CVD access or launch problem | IT Service Desk | Escalate course-specific CVD behavior with evidence when normal access support does not resolve it |
| Supported local course IDE fails to install/configure | IT Service Desk | Use current setup instructions and logs; CVD can provide continuity |
| Verify reports `NOT COMPLIANT` or failures | IT Service Desk | Collect summary and log; escalate course-automation defects when appropriate |
| GitHub account/authentication or `gh` problem | IT Service Desk | Distinguish GitHub account access from a course-repository defect |
| Activity README repository setup/clone/push/pull command fails | IT Service Desk | Confirm account, repo owner, repo existence, local path, remote, and current README first |
| Student used Fork or Use this template instead of the activity README setup commands | IT Service Desk / repository workflow | Preserve work and identify the resulting repository state before changing anything |
| Public GC-STEM repository appears broken or inconsistent | Course technical maintainers | A GitHub Issue may be appropriate if the repository directs F&S there |
| Course-provided script, test, starter file, CI check, or documentation appears defective | Course technical maintainers | Preserve reproduction steps and distinguish from student edits or normal formative CI feedback |
| Student Python code has syntax or logic problems | Faculty or Academic Support | LSS/24/7 tutoring may provide learning support; Service Desk may isolate environment functionality |
| Student needs help understanding programming concepts | Faculty or Academic Support | Select LSS/live support or 24/7 tutoring based on need and availability |
| Student needs help with pseudocode or flowchart reasoning | Faculty or Academic Support | Maintain academic-integrity boundaries |
| Student needs time/task prioritization or organization | Academic Coaching | Particularly useful for spreading work across the week and managing multiple course systems |
| Student needs help reading/following technical documentation | Academic Coaching | Coach the reading/process skill; technical failures still go to Service Desk |
| Student needs learning strategies related to a diagnosed learning difference | Academic Coaching | Formal accommodations follow the appropriate university process |
| Student needs writing-development feedback | Written Feedback | Appropriate for writing quality; not programming/rubric validation |
| Student needs English-language learning support | Academic Support ELL/ESOL pathways | May span tutoring, LSS, coaching, and ARC resources |
| What the assignment requires or what to submit | Faculty / D2L Brightspace | Guidelines and Rubric are authoritative |
| Grading or instructor feedback | Faculty | Do not reinterpret a grading decision through another support path |
| Academic plan, course sequence, or broader program concern | Academic Advisor | Refer technical or instructional subquestions to the appropriate role |
| Student does not know where to ask for help | Any F&S supporter can triage | Use this page and [Academic Support for IT 140](../academic-support/README.md) as appropriate |

## IT Service Desk Boundary

The IT Service Desk should focus on whether the **supported technical
environment and access path** are functioning as documented.

Examples of appropriate Service Desk questions:

* Can the student access the system?
* Which environment is being used?
* Does the course IDE launch?
* Does Python run?
* Is GitHub CLI authenticated?
* Is the student working in the correct repository?
* Did the student follow the current activity README repository setup commands?
* What do `git status` and `git remote -v` show?
* What does Verify report?
* What does the lifecycle summary/log show?
* Can the issue be reproduced in the CVD reference environment?

The Service Desk does **not** need to determine whether a student's algorithm
is correct, whether a student's study plan is effective, or whether the
student's program deserves credit under a rubric.

A program that runs but produces the wrong answer is not automatically an
environment failure.

## Faculty Boundary

Faculty are the authoritative course contact for matters such as:

* interpreting the current assignment requirements;
* grading;
* rubric application;
* instructor feedback;
* assignment submission expectations;
* course-content questions appropriate for the instructor; and
* determining what assistance is appropriate for a graded activity.

Faculty may also help with programming learning and triage technical problems,
but technical infrastructure diagnosis can be routed to the Service Desk and
additional learning support can be routed through Academic Support.

## Academic Support Boundary

Academic Support includes several services that can support different parts of
an IT 140 student's learning process.

Use [Academic Support for IT 140](../academic-support/README.md) as the
canonical F&S-facing service-selection guide.

### Learning Support Specialists (LSS)

LSS help students build understanding and problem-solving skills through
IT 140-focused live support and related learning resources.

Appropriate LSS support may include:

* explaining course-level programming concepts;
* helping students interpret error messages;
* helping students reason through their own logic;
* teaching debugging and testing approaches;
* helping students use course development tools at a learning-support level;
  and
* helping students locate relevant course resources.

LSS support should help the student **discover and develop the solution**, not
replace the student's graded work with a completed solution.

See [LSS Support Guide](../lss/README.md).

### 24/7 Drop-In Tutoring

24/7 Drop-In Tutoring can support general Python concepts, programming problem
solving, and debugging.

Tutor.com tutors are not SNHU employees and should not be expected to know the
IT 140 course structure, current assignment wording, GitHub workflow, or
rubric.

F&S can improve the referral by helping the tutor/student locate current public
IT 140 context and by keeping rubric interpretation with faculty.

See [24/7 Drop-In Tutoring | IT 140 Context for F&S](../academic-support/tutoring.md).

### Academic Coaching

Academic Coaching is appropriate for academic-process needs such as:

* time and task prioritization;
* organization;
* reading and following technical documentation;
* strengthening academic skills;
* learning strategies;
* critical thinking and problem-solving process; and
* support strategies for diagnosed learning differences.

Coaches should not be expected to teach Python, troubleshoot Git/GitHub, or
interpret a graded rubric. They can help students establish a workable learning
process and recognize when another support route is needed.

See [Academic Coaching | IT 140 Guide for F&S](../academic-support/coaching.md).

### Written Feedback and English-Language Support

Written Feedback may support writing quality in IT 140's limited written
deliverables, such as the Module Two IDE Features Reflection and Project One
theme/storyline description. It should not be used to validate code,
pseudocode, flowcharts, or rubric compliance.

English-language learning support can span tutoring, LSS sessions, coaching,
and ARC ELL/ESOL resources.

See [Academic Support for IT 140](../academic-support/README.md).

## Academic Advisor Boundary

Academic advisors need enough technical and course context to:

* set reasonable course expectations;
* recognize when a student's concern is technical, instructional,
  coaching-related, or academic;
* help a student identify the correct support resource; and
* address academic-planning questions within the advisor role.

Advisors are not expected to troubleshoot Git, Python, VS Code, or course
automation.

## Course Technical Maintainer Boundary

Some problems are neither ordinary student-code questions nor routine desktop
support.

Examples include:

* a GC-STEM repository contains a broken link or incorrect starter file;
* a current course automation script fails reproducibly in the supported
  reference environment;
* the manifest/configuration defines an incorrect course component;
* course-provided tests fail against the intended starter state;
* a student CI workflow behaves differently from its documented lifecycle,
  especially for a fresh untouched personal repository;
* the same supported-environment or GitHub Actions failure affects multiple
  users; or
* documentation and automation disagree.

These should be escalated to the **course technical maintenance** path with a
reproducible evidence package.

See [Escalation Model](escalation-model.md).

## Academic Integrity Boundary

Support is expected to help students make progress without replacing the
student's graded work.

Supporters should not:

* post complete solutions to graded IT 140 assignments or projects in public
  support channels;
* provide a finished graded deliverable when the student's task is to create
  that deliverable;
* modify a student's program into a completed assignment while presenting the
  work as the student's own; or
* use a support channel to bypass course academic-integrity expectations.

Supporters may:

* explain concepts;
* ask diagnostic or coaching questions;
* point to relevant course resources;
* demonstrate a concept with a different or partial example;
* help a student interpret an error;
* help a student test their own work;
* help a student plan, organize, and read technical instructions; and
* help isolate whether a problem is environmental, learning-related,
  academic-skills-related, or in student-created code.

Role- and service-specific guides provide more detailed examples.

## Technical Versus Student-Code Test

When the distinction is unclear, ask:

1. **Can Python run a simple known-good command or course-provided example in
   the supported environment?**
2. **Does the course Verify process report an environment failure?**
3. **Does the same student program fail in the CVD reference environment?**
4. **Does only this student's code fail while the environment otherwise
   works?**

These questions do not prove the cause by themselves, but they help separate
environment failures from programming problems.

> [!CAUTION]
> Do not modify or delete the student's work merely to test the environment.
> Preserve student files and Git history.

## Shared Ownership Cases

Some issues cross role boundaries.

### Example: "My assignment won't run"

Possible routes:

* Python itself cannot run → technical support.
* VS Code is using the wrong interpreter → technical support / course IDE
  support.
* Python runs but the student's code has a syntax error → faculty or Academic
  Support learning support.
* The student does not know which file must be submitted → faculty /
  Brightspace.
* The student cannot organize enough time to make progress → Academic Coaching.
* The starter file itself is malformed for everyone → course technical
  maintainer.

### Example: "GitHub doesn't work"

Possible routes:

* cannot sign in to GitHub → account/technical support;
* `gh auth status` shows the wrong account → technical/repository workflow
  support;
* student's private repo already exists → repository workflow issue;
* student clicked **Fork** or **Use this template** instead of following the
  activity README → repository workflow issue;
* student is trying to clone the GC-STEM template directly → repository
  workflow issue;
* `git pull --ff-only` or `git push` fails after work on more than one device →
  stop changes and route to repository technical support;
* GitHub Actions gives normal formative feedback about student work → use the
  activity's CI guide and faculty/learning support as appropriate;
* several students see the same unexpected CI/infrastructure failure → course
  technical maintainer;
* GitHub works, but the student does not understand Git concepts → faculty/LSS
  learning support as appropriate; or
* the public course repository is missing or broken → course technical
  maintainer.

### Example: "I'm behind and I don't understand loops"

This likely contains more than one need:

* **time/task planning or organization** → Academic Coaching;
* **loop/programming understanding** → faculty, LSS, and/or 24/7 Drop-In
  Tutoring;
* **unclear assignment requirement** → faculty; and
* **broader academic-plan/persistence concern** → Academic Advisor when
  applicable.

Do not require the student to finish one independent support path before using
another.

## Public Versus Internal Support Channels

A public GitHub repository may be appropriate for:

* a reproducible defect in a public course repository;
* a broken public documentation link;
* a course-tool issue that does not require private information; or
* a general improvement request.

Do not place private student information, credentials, complete graded
solutions, or confidential SNHU operational information in public GitHub
areas.

This repository is public but **F&S-facing**. Student-specific coaching,
tutoring, advising, grading, and technical details should remain in approved
student-support systems.

Internal SNHU routing details should remain in the appropriate internal
system.

## When to Escalate or Refer

Refer or escalate when:

* the issue is outside the current role/service's responsibility;
* documented safe troubleshooting does not resolve a technical problem;
* the supported environment behaves differently from the current course
  documentation;
* a course-provided artifact appears defective;
* multiple users show the same failure;
* resolving the problem would require privileged or course-maintainer changes;
  or
* continuing would risk student work, privacy, credentials, or system
  stability.

Before a technical escalation, collect the evidence described in
[Escalation Model](escalation-model.md).

## Related Documentation

* [Academic Support for IT 140](../academic-support/README.md)
* [Course Overview](course-overview.md)
* [Course Repository Architecture](course-repository-architecture.md)
* [Course Glossary](glossary.md)
* [Supported Environments](supported-environments.md)
* [GitHub Workflow](github-workflow.md)
* [Escalation Model](escalation-model.md)

Return to the [Shared Documentation Index](README.md).
