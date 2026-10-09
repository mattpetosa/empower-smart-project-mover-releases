# Release history

Newest first. Downloads are on the [Releases](https://github.com/mattpetosa/empower-smart-project-mover-releases/releases) page.

## v3.10.0.1-0.6.0 (2026-10-09)

### Changed
- **The run's progress bar shows the whole job, with an ETA.** The setup steps (check, sign in, choose) take a short stretch at the start of the bar; the long stretch is the projects themselves, filling as their data is backed up, checksummed, restored or verified — a big project counts for more than a small one. Under the bar: how many projects there are, how many are queued and running, how many completed, completed with warnings or failed — and about how long is left, with the time it should be done.
- **Projects are listed in a compact table while they run.** One line per project: its number, name, what it is doing right now, its own progress bar, how long it has taken, and its result on the right. The list follows the project that is running. Click a project to see its checks, messages and live log.
- **Each project's bar runs from start to finish.** It no longer starts again for each stage (backing up, checksumming, comparing the raw data); every stage has its share of the bar by how long it should take, and the bar never goes backwards.

### Improved
- **The estimates learn from your runs.** Each backup records its real size and how fast this computer backed up, restored and checksummed, so the next run's bars and time left are closer to the truth. The first run uses Empower's size figures and cautious speeds.

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
