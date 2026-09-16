# Changelog

All notable documentation and structural changes to the IT 140 Support repository should be recorded in this file.

## Unreleased

### Added

* Initial `it140-support` repository architecture.
* Top-level repository purpose, scope, support principles, and role-based navigation.
* Shared-documentation directory and initial outlines.
* Role-specific directories for faculty, Learning Support Specialists (LSS), academic advisors, and IT Service Desk personnel.
* `.github/images/` directory for screenshots and other support images.
* Documentation convention requiring role-specific guides to link directly to relevant shared information.
* Hidden screenshot-placeholder convention for documentation under development.
* Developed the IT Service Desk triage and escalation runbook with role-specific procedures for triage, supported environments, GitHub/repositories, verification/logs, safe remediation, and escalation.
* Developed the faculty support guide with start-of-term reorientation, faculty setup/familiarization, student support, assignment/grading, repository, escalation, and common-scenario guidance for adjunct faculty.
* Developed the LSS support guide with role orientation, Python Workshop and IT Basic Office Hours guidance, learning-support and academic-integrity practices, course-tool/repository guidance, Academic Resource Center development, referral/escalation, and common-scenario guidance.
* Developed the Academic Advisor support guide with course expectations, advisor-level technology context, student-conversation guidance, cross-role referrals, and common scenarios for both STEM and non-STEM advising contexts.
* Added `shared/glossary.md` as the canonical scaffold for abbreviations and technical terms used across the public IT 140 repository and wiki ecosystem.
* Added `advisors/course-planning-and-preparation.md` for workload planning, pre-term preparation, preview-period orientation, concurrent-course considerations, and optional preparatory guidance.
* Added advisor early-warning guidance based on reported advising patterns, including early-course difficulty, zyBooks progress, weekly pacing, and timely use of support resources.
* Added the course-progression visual explaining how IT 140 programming and problem-solving skills support later technical work.
* Added `academic-support/README.md` as the canonical F&S-facing guide for selecting among IT 140-relevant Academic Support services, including LSS live support, 24/7 Drop-In Tutoring, Academic Coaching, Written Feedback, and ELL/ESOL pathways.
* Added `academic-support/tutoring.md` to give F&S personnel IT 140 context for Tutor.com referrals, including public course sources, course progression, academic-integrity boundaries, and routing limits.
* Added `academic-support/coaching.md` to give Academic Coaches IT 140-specific course context and coaching strategies for time/task prioritization, technical reading, academic skills, learning differences, critical thinking/problem solving, and organization.

### Changed

* Refactored `shared/course-repository-architecture.md` so repository recovery and repeat-student procedures are canonical in `shared/github-workflow.md` rather than duplicated in the architecture page.
* Refined Service Desk remediation and escalation pages so lifecycle definitions, platform facts, and the common evidence schema remain canonical in `shared/`, while Service Desk pages retain role-specific actions.
* Added explicit return-to-runbook navigation to Service Desk procedure pages.
* Updated the top-level repository structure and development status after completion of all four role-specific support sections.
* Moved repository-maintenance artifacts under `.github/`, including `CHANGELOG.md` and the support-image directory.
* Corrected the top-level repository tree and screenshot path to use `.github/images/`.
* Completed a cache-busted rendered integration review of the shared and role-specific documentation after the August 17, 2026 GitHub service incident.
* Replaced public internal-routing/workflow placeholders with durable guidance to use the current approved SNHU internal systems for restricted operational details.
* Clarified that hidden screenshot placeholders are maintenance cues for future sanitized images and do not make the surrounding text incomplete.
* Expanded advisor course-expectation guidance to state the official planning expectation of about 16 hours per week on average for an eight-week, three-credit course and to distinguish "introductory" from "low workload."
* Added zyBooks workload planning context: approximately 4–5 hours per week in earlier weeks and 2–3 hours per week in later weeks, while preserving Brightspace/zyBooks as the source for exact weekly activities.
* Clarified that optional pre-term preparation is appropriate but advisors should not recommend beginning required IT 140 course work before the official term start.
* Added Academic Support options to advisor guidance: 24/7 Drop-In Tutoring with Python support, `IT 140 - Intro to Python Workshop`, and `IT Basics Office Hours`, with a link to the current-term group-session schedule.
* Normalized older live-session labels in LSS/advisor documentation to `IT 140 - Intro to Python Workshop` and `IT Basics Office Hours`.
* Added advisor-level zyBooks access/setup routing and clarified that screenshots may supplement, but are not a universal requirement for, requests for programming help.
* Replaced direct advisor/LSS references to the former terminology page with the new Course Glossary; retained `shared/terminology.md` as a compatibility pointer.
* Clarified throughout the repository that the public IT 140 Support repository is **F&S-facing**, while student-facing directions belong in D2L Brightspace, student-facing course repositories/wikis, and official Academic Support resources.
* Expanded the support model from LSS-only learning-support references to the broader Academic Support ecosystem while preserving the existing `lss/` directory for detailed LSS operational guidance.
* Refactored tutoring guidance so F&S can provide or locate current IT 140 context for Tutor.com tutors instead of placing student-facing "Help the tutor help you" instructions in this support repository.
* Expanded Academic Coaching guidance around a practical weekly pattern of starting early and working approximately 2–2.5 hours per day, with a general priority of current zyBooks Participation/Lab Activities, then the current module assignment/milestone, then active Text-Adventure Game project work when planned time remains.
* Added coaching guidance for reading and following technical documentation, strengthening academic skills, learning-difference strategies, critical thinking/problem solving through the IT 140 SDLC, and organization across Brightspace, zyBooks, GitHub, and the course IDE.
* Updated faculty, LSS, advisor, shared-boundary, and Service Desk routing language so programming-learning needs, coaching needs, assignment/grading questions, technical failures, and advising concerns are more clearly distinguished.
* Replaced duplicated Academic Support service lists in key referral pages with links to the canonical `academic-support/README.md` where practical.
* Synchronized support documentation with assignment/project repository version 1.0.4 workflow changes, including the distinction between the documented `gh repo create --template ...` command and the GitHub **Fork**/**Use this template** browser controls.
* Standardized support guidance around opening activity repositories with `cd ~/Repos/<repository-name>` followed by `code .` and added VS Code Restricted Mode/Workspace Trust guidance for the course `~/Repos` folder.
* Added the canonical multi-device workflow: commit/push before switching devices, run `git pull --ff-only` before editing on the next existing clone, and stop changes when pull/push cannot fast-forward rather than attempting merge/reset/rebase/force-push recovery.
* Added faculty and support interpretation of the version 1.0.4 student CI lifecycle: fresh personal repositories are neutral, CI is formative rather than grading/submission, optional M3/M4 Python practice remains outside student CI requirements, Projects CI is progressive, and Projects Ruff feedback is advisory.
* Updated Service Desk and LSS routing terminology from generic "template creation" failures to the current activity README repository-setup workflow and added explicit triage for students who used Fork/Use this template or created divergent multi-device histories.
