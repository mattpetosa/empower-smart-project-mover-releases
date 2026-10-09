# Release history

Newest first. Downloads are on the [Releases](https://github.com/mattpetosa/empower-smart-project-mover-releases/releases) page.

## v3.10.0.1-0.5.5 (2026-10-09)

### Changed
- **More room for project names in the Back Up list.** Each project now shows its full name with its backup check mark lined up on the right. Hover over a project to see the date of its last backup — the name shortens to make room while the mouse is over it. The tooltip shows the full project name and the whole backup story, including when a failed project was last backed up successfully.

## v3.10.0.1-0.5.4 (2026-10-09)

### Added
- **The Back Up project list shows how each project's last backup went.** A green check means it backed up fine, a green check in a yellow ring means it backed up with warnings, and a red cross means the last attempt failed. The date shows under the name — and a failed project also shows when it was last backed up successfully. Handy when you back up a database over several runs: you can see at a glance what is done and what needs another go. Projects that were left out (in use, or couldn't be locked) and backups you cancelled don't count. The history is kept per database on the computer that ran the backups.

## v3.10.0.1-0.5.3 (2026-10-08)

### Fixed
- **The ring on the running step turns.** Since 0.5.0 it stood still on many computers while a step ran. It now turns once a second for as long as the step runs.
- **The window stays responsive while a step runs.** Each step does its work in the background, so the window can be moved and Cancel answers straight away while a step is busy.
