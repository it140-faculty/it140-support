# IT 140 Verification and Logs

Use this page to assess a configured course environment and collect technical evidence.

## Why Verify Comes First

IT 140 Verify scripts are designed to assess the current course environment **without repairing it**.

This makes Verify the preferred first diagnostic for an already configured:

* Codio Virtual Desktop (CVD);
* supported Windows local environment; or
* supported macOS local environment.

Verify checks course capabilities such as required software, Python, Git/GitHub configuration, VS Code settings/extensions, and the course repository workspace.

> [!IMPORTANT]
> The current Linux local guide does not document the same lifecycle Verify workflow. For Linux, follow [Environment Troubleshooting: Linux](environment-troubleshooting.md#linux).

## CVD Verify

Open a **new CVD Terminal** as the normal CVD user and run:

```bash
verify_it140.sh
```

A successful CVD verification reports:

```text
Result          : COMPLIANT
Failed          : 0
Exit code       : 0
```

Warnings may still be present with exit code `0`; review their recommended actions.

CVD Verify is read-only except for its transcript and an explicitly requested sanitized support directory.

![CVD Verify Success](../shared/images/verify_it140_fail.png)

## Windows Verify

Run Windows Verify from a **regular, non-elevated Windows PowerShell** window:

```powershell
cd "$env:USERPROFILE\it140\scripts\win"
Set-ExecutionPolicy -Scope Process -ExecutionPolicy Bypass -Force
.\verify_it140.ps1
```

The current Windows verifier reports pass/warning/failure counts, the log path, remediation/follow-up, and an exit code. A successful run has:

* no required `FAIL` checks;
* `Failed` equal to `0`; and
* exit code `0`.

If the verifier was run as Administrator on a regular Windows computer, close that PowerShell window and rerun Verify from a regular PowerShell window.

<!-- screenshot placeholder; show a successful Windows VERIFICATION SUMMARY with Failed 0, Log file, success notice, and Exit code 0 visible -->

## macOS Verify

Open a **new Terminal** window as the normal macOS course user and run:

```zsh
"$HOME/it140/scripts/mac/verify_it140.zsh"
```

Do not add `sudo`.

A successful macOS verification reports:

```text
Result          : COMPLIANT
Failed          : 0
Exit code       : 0
```

Warnings should be reviewed but do not by themselves make the environment noncompliant.

## Interpreting Verify Exit Codes

Do not assume every lifecycle script on every platform uses the same set of exit codes.

For the **current CVD and Windows Verify scripts**, the documented meanings are:

| Exit Code | Verify Meaning |
| --- | --- |
| `0` | All required checks passed; warnings may be present |
| `1` | One or more required checks failed |
| `2` | Unsupported execution/platform context |
| `5` | Controlled manifest/schema/managed-asset validation failure |

The current macOS Verify script returns `0` when compliant and `1` when required checks fail.

Always read the **summary and remediation** in addition to the numeric exit code.

## Read the Final Summary Before the Log

The final summary is the fastest first diagnostic.

Record:

* script/platform;
* result or success/failure state;
* passed/warning/failed counts;
* exit code;
* remediation/follow-up text; and
* exact log path.

A single earlier red/error-looking line can be misleading if the script later handles the condition. Use the final summary to determine the lifecycle result.

## Standard Log Locations

IT 140 lifecycle logs are stored under the user's home folder:

```text
Windows:
%USERPROFILE%\it140\logs\

CVD and macOS:
~/it140/logs/
```

Each run creates a timestamped log/transcript. Use the exact path printed by the failed run when available.

For the current manual Linux setup guide, the setup command writes:

```text
~/Desktop/it140_setup_log.txt
```

## What to Look for in a Log

Use the log to answer:

* Which script/version ran?
* Which platform/profile was detected?
* Which checks passed?
* Which check first failed?
* What remediation did the script recommend?
* Did the script finish normally and print a summary?

Avoid turning log review into manual reverse engineering of course-managed scripts. If the failure points to a controlled manifest/script defect, collect the evidence and escalate.

## Windows Sanitized Support Bundle

The current Windows Verify script can create an explicitly requested sanitized support ZIP.

From a **regular PowerShell** window:

```powershell
cd "$env:USERPROFILE\it140\scripts\win"
Set-ExecutionPolicy -Scope Process -ExecutionPolicy Bypass -Force
.\verify_it140.ps1 -SupportBundle
```

The script asks for explicit confirmation and creates a ZIP under the IT 140 log folder.

The bundle is designed to include sanitized verification evidence and exclude student source files, repository contents/Git history, credentials, and browser data.

Prefer this support artifact when it is sufficient for the case.

## CVD Sanitized Support Directory

The current CVD Verify script can create an explicitly requested sanitized support directory:

```bash
verify_it140.sh --support-bundle
```

Confirm creation when prompted.

The resulting directory is created under:

```text
~/it140/logs/
```

It includes a sanitized support summary and verification log and does not include student repository contents or Git history.

## macOS Support Evidence

The current macOS Verify script creates its normal transcript log but does not currently expose the same optional sanitized support-bundle feature as the CVD and Windows verifier.

Use the exact log identified by Verify and review it for private information before sharing.

## Privacy Review Before Sharing

Before attaching logs, screenshots, or terminal output, check for:

* passwords;
* authentication/device codes;
* access tokens;
* recovery codes;
* private email/contact information;
* student identification information;
* confidential SNHU information; and
* complete graded-assignment solutions.

Never request authentication secrets as evidence.

## After Verify

* **Compliant / required checks pass:** the environment is likely not the failing layer; return to [Triage](triage.md) and inspect the repository or student-code layer.
* **Failure with documented remediation:** follow [Safe Remediation](safe-remediation.md), then rerun Verify.
* **Repeatable failure after documented remediation:** follow [Escalation](escalation.md).

Return to the [Service Desk Triage and Escalation Runbook](README.md).
