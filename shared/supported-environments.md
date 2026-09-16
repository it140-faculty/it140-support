# IT 140 Supported Environments

This page describes the IT 140 course development environments and the support implications of using the CVD, a supported local computer, or an unsupported/best-effort configuration.

For exact setup commands, always use the current [`GC-STEM/it140-m1-setup-tasks`](https://github.com/GC-STEM/it140-m1-setup-tasks) instructions rather than copying commands from this support page.

## Course Environment Model

IT 140 uses the same core course IDE capabilities across supported environments, but the installation and maintenance procedures differ by platform.

The **Codio Virtual Desktop (CVD)** is the course **reference environment**.

Students may also use a supported local:

* Windows computer;
* Apple-silicon Mac; or
* Ubuntu computer with GNOME Desktop.

Local setup is optional. A working local installation is not required to complete the course when the student can use the CVD.

## Current Supported-Environment Summary

| Environment | Current Course Role | Key Support Notes |
| --- | --- | --- |
| **Codio Virtual Desktop (CVD)** | Reference environment | Recommended baseline for course work, screenshots, demonstrations, troubleshooting reproduction, and course continuity |
| **Windows 10 22H2 or Windows 11** | Supported local environment | Requires a supported Windows installation and the ability to authorize required software installation |
| **macOS 14 Sonoma, macOS 15 Sequoia, or macOS 26 Tahoe on Apple silicon** | Supported local environment | Requires an Apple-silicon Mac and an Administrator account; Intel Macs are not supported by the current automation |
| **Ubuntu with GNOME Desktop** | Supported local Linux environment | Use the current Linux/Ubuntu setup guidance; other Linux configurations are not equivalent to the supported automated profile |
| **Other/manual configurations** | Best-effort alternative | Not a fully supported IT 140 configuration; CVD is the recommended fallback |

> [!IMPORTANT]
> An instructor or experienced student may choose a different development toolset, but that choice does not make the toolset a course-supported environment. The user should first configure and verify the CVD as the reference and fallback environment. See [Alternative Local Development Tools](https://github.com/GC-STEM/it140/wiki/Alternative-Local-Development-Tools) for compatibility requirements and support expectations.

> [!NOTE]
> Supported platform status can change as the course automation is tested and released. Check the current Module One Setup Tasks and main course repository before making a platform-support determination.

## Codio Virtual Desktop (CVD)

The CVD is a cloud-based Linux desktop accessed through a web browser.

The reference CVD uses:

* Ubuntu 24.04 LTS;
* the Xfce desktop environment; and
* an x86_64 processor architecture.

The CVD begins from a course-managed system image. That makes its starting configuration more consistent than a personal computer.

The CVD is used as the course baseline for:

* screenshots;
* instructional demonstrations;
* troubleshooting reproduction;
* primary acceptance testing; and
* a continuity environment when a local installation is unavailable or being repaired.

<!-- screenshot placeholder; show the CVD desktop with VS Code, Terminal, and the Repos workspace/shortcut identifiable without exposing account information -->

### CVD Setup Persistence

A configured CVD normally remains configured across ordinary sessions and VM restarts.

If the CVD is **reset**, it returns to its original course image and the user must repeat the current CVD setup/configuration process.

### CVD and Local-Computer Problems

When a supported local Windows, macOS, or Linux setup is not working, the student can continue course work in the CVD while the local problem is investigated.

This is an important support principle:

> **A local setup problem should not automatically become a course-progress blocker when the CVD is available and working.**

## Supported Windows Environment

The current supported Windows setup path covers:

* **Windows 10 22H2**, or
* **Windows 11**.

The automated Windows local setup assumes the student:

* can run supported command-line tools;
* has access to an account that can authorize administrator-level installation when required; and
* is not prevented by device-management or security policy from installing the course tools.

Some lifecycle steps must be run as a regular user, while installation requires administrator privileges. Supporters should follow the exact current Windows README rather than running every course command from an Administrator PowerShell window.

A computer managed by an employer, school, family member, or other organization may impose restrictions that make local installation unsuitable.

Do not instruct a student to bypass those controls.

## Supported macOS Environment

The current automated macOS setup supports:

* Apple-silicon Macs; and
* macOS 14 Sonoma, macOS 15 Sequoia, or macOS 26 Tahoe.

Apple silicon includes Apple M-series processors such as M1, M2, M3, M4, and later supported Apple-silicon processors.

The current automation does **not** support Intel-based Macs.

The macOS account used for the automated setup must be able to authorize software installation. The automation is started from the regular user account and requests elevated authorization only when required; students should not add `sudo` to course lifecycle commands unless current course instructions explicitly say to do so.

## Supported Linux Environment

The supported local Linux path is based on **Ubuntu with GNOME Desktop**.

The course automation design uses an Ubuntu Desktop profile and APT-based software management.

Other Linux distributions, desktop environments, and package-management configurations may be technically capable of running the course tools, but they are not automatically equivalent to the supported Ubuntu/GNOME course profile.

When a student uses another Linux configuration, treat it as a best-effort/manual environment unless current course documentation explicitly identifies it as supported.

## Unsupported or Best-Effort Environments

Examples that should normally use the CVD include:

* Chromebooks;
* tablets;
* Intel-based Macs under the current macOS automation;
* operating-system versions outside the current supported guides;
* computers on which required command-line or installation capabilities are blocked; and
* devices whose management policy does not permit the course software.

The Module One local setup documentation also provides a manual setup path for advanced or unsupported configurations.

That manual path is **best effort** and is not the same as a fully supported automated configuration.

Do not disable security software, bypass administrator restrictions, or make major system changes merely to force an unsupported local environment to work.

## Course IDE Components

The supported IT 140 course IDE is designed around a common core toolset.

### Primary Tools

| Tool | Course Purpose |
| --- | --- |
| **Python 3.12** | Run and develop Python programs |
| **Visual Studio Code (VS Code)** | Edit, run, test, debug, and organize course work |
| **Git** | Track repository changes and history |
| **GitHub CLI (`gh`)** | Authenticate and interact with GitHub from the command line when directed |
| **pytest** | Run course-provided automated tests |
| **pytest-cov** | Measure test coverage where used |
| **Ruff** | Python code-quality and formatting support |

### VS Code Extensions

The current course IDE includes support such as:

| Extension / Feature | Purpose |
| --- | --- |
| Python | Python language support |
| Ruff | Python formatting and code-quality feedback |
| Draw.io Integration | Flowcharts and diagrams |
| I2P Pseudocode | Pseudocode files and syntax support |
| Code Spell Checker | Spelling assistance in code and documentation |
| Office Viewer | Viewing supported document files in VS Code |

Exact extension versions and managed settings may change. Use current course verification rather than comparing a student's environment to an old screenshot or copied version list.

## Automation Lifecycle by Environment

The common lifecycle is:

> **Prepare → Install → Configure → Verify → Update**

The actual first-time sequence depends on the environment.

### Typical Local Setup

A supported local environment normally follows:

> **Prepare → Install → Configure → Verify**

### Typical CVD Setup

Because the CVD starts from a course-managed system image, its initial sequence normally uses:

> **Prepare → Update → Configure → Verify**

Do not choose or reorder lifecycle stages based only on memory. Follow the current environment README and the final **Next step** printed by the script.

## Verification

The Verify stage is designed to check the current environment without repairing or changing the course IDE.

A successful verification reports:

* `Result: COMPLIANT`;
* `Failed: 0`; and
* exit code `0`.

A warning does not automatically make the environment noncompliant.

If Verify reports `NOT COMPLIANT`, one or more failures, a nonzero exit code, or remediation instructions:

1. read the complete final summary;
2. preserve the exact log path;
3. follow the remediation instructions; and
4. rerun Verify when directed.

<!-- screenshot placeholder; show a successful IT 140 Verification Summary with Result COMPLIANT, Failed 0, Exit code 0, and the log path visible -->

See [Escalation Model](escalation-model.md) before escalating a technical environment problem.

## Course Automation Logs

Lifecycle scripts create timestamped logs/transcripts in the user's IT 140 log folder.

Standard locations are:

```text
Windows:
%USERPROFILE%\it140\logs\

CVD, macOS, Linux:
~/it140/logs/
```

Logs can identify:

* the script and version;
* platform;
* actions performed;
* warnings or failures; and
* where the failure occurred.

Review logs for private information before sharing them outside an authorized support channel.

## Beta and Development Status

The IT 140 setup and automation environment may be under active testing or development.

That has two support implications:

1. Do not assume that a procedure copied from an earlier term or earlier repository revision is still current.
2. When exact support status matters, use the live course and setup repositories as the source of truth.

Use:

* [`GC-STEM/it140`](https://github.com/GC-STEM/it140) for course-wide technical status and repository availability; and
* [`GC-STEM/it140-m1-setup-tasks`](https://github.com/GC-STEM/it140-m1-setup-tasks) for current environment setup instructions.

## Safe Support Principles

When troubleshooting environments:

* identify the platform first;
* use the instructions for that platform;
* do not run another platform's scripts because the filenames look similar;
* do not randomly reinstall Python, VS Code, Git, or course extensions;
* do not edit course-managed scripts, manifests, or schemas;
* do not bypass system-management or security restrictions;
* preserve student repositories and Git history;
* prefer Verify for read-only environment assessment when appropriate; and
* use the CVD to maintain course continuity during a local-environment problem.

## Related Shared Documentation

* [Course Overview](course-overview.md)
* [Course Repository Architecture](course-repository-architecture.md)
* [Terminology](terminology.md)
* [GitHub Workflow](github-workflow.md)
* [Support Boundaries](support-boundaries.md)
* [Escalation Model](escalation-model.md)

Return to the [Shared Documentation Index](README.md).
