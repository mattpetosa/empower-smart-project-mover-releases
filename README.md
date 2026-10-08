<p align="center"><img src="assets/app-logo-256.png" width="112" alt="Empower Smart Project Mover"></p>

# Empower Smart Project Mover — Downloads

This repository hosts **downloads and issue tracking** for Empower Smart Project Mover, part of
the Empower Smart Tools family alongside
[Empower Smart Deploy](https://github.com/mattpetosa/empower-smart-deploy-releases),
[Empower Smart Recovery](https://github.com/mattpetosa/empower-smart-recovery-releases) and
[Empower Smart License Audit](https://github.com/mattpetosa/empower-smart-license-audit-releases):
a Windows app that backs up, restores and moves Waters **Empower 3** projects, checking every
step as it goes.

**[⬇ Download the latest release](https://github.com/mattpetosa/empower-smart-project-mover-releases/releases)** — or get it from
[empower.mhpwebserver.com](https://empower.mhpwebserver.com/downloads/espm) (the app updates itself).

## What it does

- **Check System** — reads the Empower version, databases and disk space, and can test a sign-in.
  Changes nothing.
- **Back Up Projects** — backs up the projects you pick, optionally locking each one read-only
  while it is copied, then checks every file of the backup against the live project.
- **Restore Projects** — verifies each backup before restoring it, then checks the restored
  project against the backup. **Preview only** shows the plan without restoring anything.
- **Move Projects** — backs up, verifies, restores into another database or under another parent,
  and verifies again. The source projects are never changed or deleted.
- **Verify Backups** — re-checks existing backups anywhere, with no Empower needed.
- **Clean Up Backups** — removes old backup runs made by this app, keeping each database's newest.

Every run writes an HTML and CSV report of each project's checks.

## Requirements

- Windows 10/11 or Windows Server 2016–2025, run as Administrator, on a computer with
  Empower 3 installed.
- An Empower account with the privileges to back up and restore projects.
- A license key from [empower.mhpwebserver.com](https://empower.mhpwebserver.com/license.html)
  (Check System works without one).

## Issues

Found a problem? [Open an issue](https://github.com/mattpetosa/empower-smart-project-mover-releases/issues).
