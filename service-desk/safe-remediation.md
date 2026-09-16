# IT 140 Service Desk Safe Remediation

Use this page after the problem has been classified and evidence has been collected.

The governing rule is:

> **Prefer course-provided remediation over improvised repair.**

The IT 140 automation is designed to separate system installation, user configuration, verification, and maintenance. Random package repairs can make the environment harder to diagnose.

## Safe First-Line Actions

These actions are generally appropriate when they match the current course instructions or script remediation:

* close the current Terminal/PowerShell window and open a fresh one;
* rerun **Verify** after a documented remediation;
* rerun **Configure** when Verify explicitly identifies a current-user configuration problem;
* rerun **Update** when the CVD/other lifecycle summary explicitly directs it;
* rerun **Prepare** when the automation package or controlled assets are missing/stale and the script directs it;
* restart the computer/VM when the lifecycle summary says a restart is required;
* reauthenticate GitHub through the course's secure `gh`/Configure workflow;
* preserve/rename a damaged local repository before recloning the student's existing private GitHub repository; and
* move current work to the CVD when a local environment cannot be repaired promptly.

## Follow the Documented Lifecycle Stage

The canonical definitions of **Prepare, Install, Configure, Verify, and Update** are in
[Course Automation Terms](../shared/terminology.md#course-automation-terms).

For Service Desk remediation:

* follow the lifecycle stage named by the current README, script summary, **Next step**, or **Remediation** text;
* do not substitute a different lifecycle stage because it appears more powerful;
* use Verify as a read-only diagnostic where the current supported platform documents it; and
* stop rather than improvising manual package or configuration repairs when the course procedure does not authorize them.

For platform-specific privilege and support rules, use the current
[Supported Environments](../shared/supported-environments.md) guidance and the live platform setup README.

## Repository-Safe Remediation

Before repository recovery:

1. Identify the private GitHub repository.
2. Determine whether current work has been pushed.
3. Preserve any local-only work.
4. Verify the replacement clone before deleting backups.

Do not recreate a repository merely because the local folder is missing.

See [GitHub Workflow](../shared/github-workflow.md).

## Actions to Avoid

Unless current official course instructions or authorized course technical support specifically directs the action, do **not**:

* randomly reinstall Python, VS Code, Git, GitHub CLI, or VS Code extensions;
* manually edit the course manifest or schema;
* modify lifecycle scripts to bypass a check;
* run another platform's scripts;
* run Verify as root/Administrator when that platform expects a regular user;
* add `sudo` to macOS lifecycle commands;
* disable antivirus, endpoint protection, firewall, or other security controls;
* bypass Windows S Mode or organization-managed restrictions on the user's behalf;
* perform manual APT/Homebrew/package repairs after an automation failure without course direction;
* delete `~/it140` or the student's `~/Repos` contents as a first-line fix;
* delete a private GitHub repository before confirming the student's work is safely preserved;
* remove Git history to make a repository "clean"; or
* ask for credentials, tokens, or authentication codes.

## CVD Update Special Case

If a CVD Update appears to stop during package download, follow the documented 30-minute quiet-period procedure in
[Environment Troubleshooting](environment-troubleshooting.md#cvd-update-appears-frozen).

If the second documented Update attempt fails, stop rather than escalating manual package repair.

## Unsupported/Restricted Local Computers

Local setup is optional.

If the device is unsupported, lacks required permissions, or is managed in a way that blocks the course tools:

* do not bypass management controls;
* recommend the CVD for course work; and
* document the local limitation if further support is required.

## When to Stop Remediation

Stop and escalate when:

* the same failure remains after the script's documented remediation;
* the reference CVD reproduces the failure;
* a controlled course file appears defective;
* multiple users report the same supported-environment failure;
* the next step would risk student work or system stability;
* the next step would require bypassing a security/management control; or
* the issue is outside the Service Desk support boundary.

Continue with [Escalation](escalation.md).

Return to the [Service Desk Triage and Escalation Runbook](README.md).
