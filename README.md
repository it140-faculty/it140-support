# IT 140 Support

This repository is the central **faculty-and-staff support resource** for Southern New Hampshire University (SNHU) personnel who support students and faculty in **IT 140 - Introduction to Scripting**.

The repository is public so faculty and staff can reach it easily, but its guidance is written for **SNHU faculty and staff (F&S)** rather than for students. Student-facing directions should remain in D2L Brightspace, the student-facing IT 140 repositories and wikis, and official Academic Support resources.

The repository provides guidance for:

* [Faculty](faculty/README.md)
* [Academic Support](academic-support/README.md)
* [Learning Support Specialists (LSS)](lss/README.md)
* [Academic Advisors](advisors/README.md)
* [IT Service Desk personnel](service-desk/README.md)

> [!IMPORTANT]
> Start with the guide for **your role or support area**. You are not expected to read the shared documentation first.
>
> Role- and support-area guides link directly to the course information needed to complete each support task.

---

* **Course**: IT 140 - *Introduction to Scripting*
* **Repository Purpose**: 
* **Repository Version**: 1.0.4
* **Repository Version DTG**: 2026-09-07-14-30a

---

## Documentation Model

This repository follows one central documentation rule:

> **Shared facts are documented once. Role-specific responsibilities and procedures live under the role's directory.**

Shared documentation provides canonical information about the course, supported environments, course glossary, GitHub workflow, support boundaries, and escalation model.

The [Academic Support Guide](academic-support/README.md) is the canonical F&S-facing overview of Academic Support options that may help IT 140 students. Detailed LSS operational guidance remains in the existing [`lss/`](lss/) directory.

Role- and support-area documentation:

* explains what the faculty or staff member should do;
* links directly to the relevant shared information at the point it is needed;
* avoids requiring supporters to discover or read the `shared/` directory before beginning;
* avoids duplicating shared facts that could become inconsistent over time; and
* links to the canonical Academic Support overview rather than maintaining separate lists of services wherever practical.

## Choose Your Starting Point

| Role or Support Area | Start Here | Primary Focus |
| --- | --- | --- |
| Faculty | [Faculty Support Guide](faculty/README.md) | Teaching, student support, course workflow, assignment support, and escalation |
| Academic Support | [Academic Support for IT 140](academic-support/README.md) | Selecting among tutoring, LSS workshops/office hours, coaching, written feedback, and English-language support |
| Learning Support Specialists (LSS) | [LSS Support Guide](lss/README.md) | IT 140-focused learning support, workshops, office hours, course tools, resource development, and escalation |
| Academic Advisors | [Advisor Support Guide](advisors/README.md) | Course expectations, preparation and planning, common student concerns, technology context, and referrals |
| IT Service Desk | [Service Desk Triage and Escalation Runbook](service-desk/README.md) | Technical triage, diagnostics, safe remediation, evidence collection, and escalation |

## Scope

This repository supports the **IT 140 course environment and F&S support workflows**. It is not the authoritative source for graded activity requirements and is not intended to replace student-facing course or Academic Support instructions.

For graded assignments and projects:

* **D2L Brightspace** remains the authoritative source for activity requirements, submissions, grading, deadlines, and instructor feedback.
* Student-facing GitHub repositories provide course tooling, templates, instructions, and supporting resources.
* Academic Support's official student-facing systems provide current service access and scheduling.
* Support personnel should not provide or publish complete solutions to graded assignments.

## IT 140 Course Repositories

| Purpose | Repository |
| --- | --- |
| Main course hub and course IDE automation | [GC-STEM/it140](https://github.com/GC-STEM/it140) |
| Module One setup tasks | [GC-STEM/it140-m1-setup-tasks](https://github.com/GC-STEM/it140-m1-setup-tasks) |
| Module Two assignment | [GC-STEM/it140-m2-assignment](https://github.com/GC-STEM/it140-m2-assignment) |
| Module Three assignment | [GC-STEM/it140-m3-assignment](https://github.com/GC-STEM/it140-m3-assignment) |
| Module Four assignment | [GC-STEM/it140-m4-assignment](https://github.com/GC-STEM/it140-m4-assignment) |
| Projects One and Two and Module Six Milestone | [GC-STEM/it140-projects](https://github.com/GC-STEM/it140-projects) |

## Repository Structure

```text
it140-support/
├── README.md
├── .github/
│   ├── CHANGELOG.md
│   └── images/
├── shared/
│   ├── README.md
│   ├── course-overview.md
│   ├── course-repository-architecture.md
│   ├── glossary.md
│   ├── terminology.md
│   ├── supported-environments.md
│   ├── github-workflow.md
│   ├── support-boundaries.md
│   └── escalation-model.md
├── academic-support/
│   ├── README.md
│   ├── tutoring.md
│   └── coaching.md
├── faculty/
│   ├── README.md
│   ├── start-of-term.md
│   ├── setup-and-familiarization.md
│   ├── supporting-students.md
│   ├── assignments-and-grading.md
│   ├── github-and-repositories.md
│   ├── technical-issues-and-escalation.md
│   └── common-scenarios.md
├── lss/
│   ├── README.md
│   ├── orientation-and-familiarization.md
│   ├── workshops-and-office-hours.md
│   ├── learning-support-and-integrity.md
│   ├── github-and-course-tools.md
│   ├── resource-development.md
│   ├── referrals-and-escalation.md
│   └── common-scenarios.md
├── advisors/
│   ├── README.md
│   ├── course-expectations.md
│   ├── course-planning-and-preparation.md
│   ├── technology-context.md
│   ├── student-concerns.md
│   ├── referrals-and-routing.md
│   └── common-scenarios.md
└── service-desk/
    ├── README.md
    ├── triage.md
    ├── environment-troubleshooting.md
    ├── github-repository-troubleshooting.md
    ├── verification-and-logs.md
    ├── safe-remediation.md
    └── escalation.md
```

Role- and support-area sections intentionally differ in size. A Service Desk runbook requires more technical procedures than an advisor guide; Academic Coaching needs different course context than an LSS workshop guide. The repository does not force artificial symmetry across roles or services.

## Shared Documentation

The `shared/` directory contains information that applies to more than one support role.

| Shared Resource | Purpose |
| --- | --- |
| [Shared Documentation Index](shared/README.md) | Index of canonical shared information |
| [Course Overview](shared/course-overview.md) | Course purpose, instructional context, workload context, and major technologies |
| [Course Repository Architecture](shared/course-repository-architecture.md) | Purpose and relationship of the IT 140 GitHub repositories |
| [Course Glossary](shared/glossary.md) | Canonical glossary for abbreviations and technical terms used across the IT 140 repository ecosystem |
| [Supported Environments](shared/supported-environments.md) | Supported course IDE environments and platform expectations |
| [GitHub Workflow](shared/github-workflow.md) | Common GitHub and repository workflow used in IT 140 |
| [Support Boundaries](shared/support-boundaries.md) | Distinguishes technical support, learning support, academic-skills support, instructional responsibilities, and advising |
| [Escalation Model](shared/escalation-model.md) | Common escalation principles and evidence expectations |

> [!NOTE]
> These pages are reference sources, not prerequisites. Role-specific documents should link to the exact shared page needed for a procedure.

## Support Principles

Support guidance in this repository should follow these principles:

1. **Start from the supporter's role or service.** Do not require F&S personnel to learn the repository structure before they can help someone.
2. **Use the supported course workflow.** Avoid generic troubleshooting steps that could move a student farther from the expected IT 140 environment.
3. **Preserve support boundaries.** Technical troubleshooting, programming learning support, academic coaching, advising, and grading responsibilities are related but not interchangeable.
4. **Collect evidence before escalation.** Escalations should contain enough information for the next support level to continue without restarting the investigation.
5. **Prefer links over duplication.** When a fact or service description is shared across roles, link to the canonical page.
6. **Keep instructions current.** Update the canonical source when the course environment or workflow changes.
7. **Protect student privacy and academic integrity.** Do not place sensitive information or complete graded-assignment solutions in public GitHub content.
8. **Keep student-facing instructions in student-facing channels.** This public support repository may be visible to students, but it should speak to the F&S personnel who support them.

## Screenshots and Images

Screenshots and other support images should be stored in:

```text
.github/images/
```

Hidden screenshot placeholders may be retained where a future sanitized screenshot would materially improve a procedure. The surrounding text should remain usable without the image, so a placeholder is a maintenance cue rather than a publication blocker.

Example:

```html
<!-- screenshot placeholder; show the IT 140 verification summary with the status and exit code visible -->
```

Do not add screenshots merely for decoration. Screenshots should clarify navigation, expected output, a decision point, or information that a supporter must identify.

## Updating This Repository

Because the IT 140 course environment and support procedures may change rapidly, this repository is intended to be maintained through normal GitHub version-control practices.

When updating documentation:

* change the canonical shared page when a shared fact changes;
* change the Academic Support overview when an Academic Support service description or routing recommendation changes;
* review role-specific pages that link to changed information;
* avoid copying revised facts or service lists into multiple role guides;
* update procedures when the supported course workflow changes;
* use pull requests for review when practical; and
* record material documentation changes in [CHANGELOG.md](./.github/CHANGELOG.md).

## Security, Privacy, and Academic Integrity

Do not post any of the following in public GitHub areas:

* passwords;
* authentication or multi-factor authentication codes;
* GitHub personal access tokens or other access tokens;
* private identifying information;
* confidential SNHU operational information;
* student submissions containing protected information; or
* complete solutions to graded IT 140 assignments or projects.

Internal escalation routing, restricted administrative procedures, student-specific information, or security-sensitive information should remain in the appropriate SNHU internal system.

## Development Status

The core support architecture includes:

* shared canonical support documentation;
* IT Service Desk triage and escalation runbook;
* faculty support guide;
* LSS support guide;
* Academic Advisor support guide; and
* Academic Support service-selection guidance, including IT 140-specific references for 24/7 Drop-In Tutoring and Academic Coaching.

Ongoing maintenance should focus on:

* validating Academic Support descriptions and links against current official Academic Support resources;
* adding sanitized screenshots only where they materially improve a support procedure;
* keeping restricted routing, queue, contact, and workflow details in the appropriate SNHU internal systems rather than this public repository; and
* updating canonical course facts and linked role procedures as the IT 140 environment evolves.

## Repository Metadata

* **Course**: IT 140 - *Introduction to Scripting*
* **Repository Name**: IT 140 Support
* **Primary Audience**: SNHU faculty and staff who support IT 140, including faculty, Academic Support personnel, LSS, academic advisors, and IT Service Desk personnel
* **Repository Purpose**: Provide canonical shared course-support information and role-/service-specific support procedures for IT 140
* **Development Status**: Operational Documentation / Ongoing Maintenance
