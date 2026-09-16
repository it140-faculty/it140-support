# Shared IT 140 Support Documentation

The `shared/` directory contains **canonical information that applies to more than one IT 140 support role or service**.

Faculty and staff are **not expected to read these pages in order before helping someone**. Role- and support-area guides should link directly to the shared page or section needed for a particular support task.

> [!IMPORTANT]
> **Shared facts are documented once. Role-specific responsibilities and procedures live under the role's directory.**
>
> When a shared fact changes, update it here and review the role-/service-specific pages that link to it. Do not copy the same fact into multiple guides unless the local context requires a brief restatement.

The [Academic Support Guide](../academic-support/README.md) similarly serves as the canonical F&S-facing overview of Academic Support services relevant to IT 140. Other role guides should link there instead of independently maintaining complete service lists when practical.

## Shared Resources

| Resource | Use It To Understand |
| --- | --- |
| [Course Overview](course-overview.md) | What IT 140 is, how students work, its workload context, and which systems provide which kinds of course information |
| [Course Repository Architecture](course-repository-architecture.md) | The purpose of each IT 140 repository and the difference between course templates, student GitHub repositories, and local clones |
| [Course Glossary](glossary.md) | Abbreviations and technical terms used anywhere in the IT 140 public repository and wiki ecosystem |
| [Supported Environments](supported-environments.md) | The CVD reference environment, supported local environments, course IDE components, and unsupported/best-effort configurations |
| [GitHub Workflow](github-workflow.md) | How students create, clone, work in, back up, recover, and reuse course repositories |
| [Support Boundaries](support-boundaries.md) | Which kinds of problems belong primarily to faculty, Academic Support/LSS, Academic Coaching, advisors, the IT Service Desk, or course technical maintainers |
| [Escalation Model](escalation-model.md) | What evidence to collect and preserve when a problem must move to another support level |

## How Role and Service Guides Should Use Shared Pages

A role- or service-specific page should:

1. Start with the task or decision the F&S member needs to make.
2. Include enough context to proceed without browsing `shared/` first.
3. Link to the exact shared page or section when a canonical fact is needed.
4. Keep role-specific actions, responsibilities, and escalation instructions in the appropriate role/service directory.
5. Avoid reproducing long explanations that already exist in `shared/`.
6. Use the [Academic Support Guide](../academic-support/README.md) as the canonical service-selection reference when the question is which Academic Support option best fits the student's need.

For example, a Service Desk procedure for a failed local setup should link to:

* [Supported Environments](supported-environments.md) for the supported-platform facts; and
* [Escalation Model](escalation-model.md) for the evidence package.

The Service Desk procedure should then contain the **Service Desk actions** for that scenario.

## Documentation Ownership

Shared pages should contain facts that remain true regardless of who is helping the student, such as:

* the distinction between D2L Brightspace and GitHub;
* the purpose of a course repository;
* the CVD's role as the course reference environment;
* supported course IDE components;
* course-wide terminology and abbreviations;
* course automation stages and result language;
* standard diagnostic log locations; and
* the common evidence needed for escalation.

Role-specific directories should contain information such as:

* what that role should do first;
* what that role may or may not change;
* how far that role should troubleshoot;
* what constitutes a successful resolution for that role; and
* where that role sends the problem next.

The `academic-support/` directory contains **F&S-facing service-selection and service-context guidance** that applies across Academic Support. Detailed LSS procedures remain in `lss/`.

## Keeping Shared Documentation Current

When course infrastructure changes:

1. Update the authoritative student-facing course or setup documentation first when appropriate.
2. Update the affected shared support page.
3. Search the role/service guides for links or short restatements that may need revision.
4. Update screenshots if the user interface or expected output changed.
5. Record material support-documentation changes in the repository `CHANGELOG.md`.

When an Academic Support service description, access path, or service-selection recommendation changes:

1. Update the official Academic Support source first where appropriate.
2. Update [Academic Support for IT 140](../academic-support/README.md).
3. Review faculty, LSS, advisor, and Service Desk links that depend on it.
4. Avoid copying a new service list independently into each role guide.

When a new abbreviation or technical term is introduced anywhere in the IT 140 public repository or wiki ecosystem, add it to the [Course Glossary](glossary.md) during the corresponding documentation review.

Avoid placing rapidly changing artifact versions in general shared pages unless the version itself is needed to explain a support decision. Supporters should use the current course repository and setup instructions when an exact current version matters.

## Screenshots

Screenshots for support documentation belong in:

```text
.github/images/
```

During drafting, use hidden placeholders such as:

```html
<!-- screenshot placeholder; show the relevant verification summary with Result, Failed, and Exit code visible -->
```

A screenshot should clarify a navigation step, expected state, error location, or decision point. Do not add screenshots only for decoration.

## Related Role and Support Guides

* [Faculty Support Guide](../faculty/README.md)
* [Academic Support for IT 140](../academic-support/README.md)
* [LSS Support Guide](../lss/README.md)
* [Advisor Support Guide](../advisors/README.md)
* [Service Desk Triage and Escalation Runbook](../service-desk/README.md)

Return to the [IT 140 Support home page](../README.md).
