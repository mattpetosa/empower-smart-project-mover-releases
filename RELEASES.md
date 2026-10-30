# Release history

Newest first. Downloads are on the [Releases](https://github.com/mattpetosa/empower-smart-project-migration-releases/releases) page.

## v3.10.0.1-0.8.0 (2026-10-30)

### Changed
- **Empower Smart Project Mover is now Empower Smart Project Migration.** Same app and same backups; license keys still start with ESPM-. The first time the renamed app opens, it moves its reports, logs and settings — including any projects it still has locked — from the old "Empower Smart Project Mover" folders into folders with the new name. Request a new Project Migration license key and activate once; keys made for Project Mover no longer activate. A copy that updates itself picks up the new name automatically.

## v3.10.0.1-0.7.0 (2026-10-23)

### Changed
- **License keys now name their app.** New keys from the license page start with ESPM-, are shorter, and use only capital letters and digits in groups of five; when you enter one, case, spaces, line breaks and dashes don't matter. Keys issued before keep working, and a computer that is already activated needs nothing new.
- **A refused license key says why:** a character looks mistyped, the key is for another Smart Tools app (the message names it), or the text isn't a license key at all.

### Fixed
- **A license key pasted from an email where it wraps onto a second line is no longer cut off** at the line break.
- **"Leave each project locked" now applies only to a good backup.** With *Unlock each project after its backup* unticked, a backup that failed its checks, was stopped by an Empower error or was cancelled used to leave the project read-only too. Such a project is now unlocked again, and the report says why. A move leaves its source locked only once the copy has been restored and verified.
- **Closing the window during a run stops the run first.** The app asks, stops the run the way Cancel does, unlocks what the run locked, then closes. Closing used to end the app at once, leaving projects locked until the next sign-in.
- **A second message no longer hides the first.** When a question appeared while another was open (for example the Cancel confirmation and a question from a running backup), the first one disappeared and the run could stop waiting for an answer that could no longer be given.
- **Activation works behind a proxy that blocks the license site.** A proxy's "blocked" or "sign in to the proxy" page was taken as the license server refusing the key, so the key couldn't be activated at all. The app now activates offline in that case, as it does when there is no network.
- **The license works on computers set to a non-Gregorian calendar** (for example Persian or Thai). The key's issue date was read in the computer's calendar, which could report "System clock error" for a valid key.
- **Backup run folders are always dated in the Gregorian calendar,** so Clean Up reads their age correctly on every computer.
- **Updates no longer get stuck downloading.** A download that stops part-way now ends after a minute instead of waiting forever (which left the update button greyed out).
- **Self-update works from folders with brackets or typographic apostrophes in their names** (for example `Tools [v2]` or `Matt’s Tools`). In such folders the app could fail to restart after an update, or fail to open at all.
- **A license no longer works on a copied (cloned) computer.** Project Mover now uses the same license checks as the other Smart Tools. A computer made as a copy of an activated one (a cloned virtual machine or disk image) has to be activated online once before it can be used. Existing activations keep working. Replacing a computer's motherboard, or moving a virtual machine to another host, also counts as a new computer: activate it online once.
- **A project is never locked when the app can't record the lock.** If the app's list of locks can't be read or written, the project is backed up without a lock (and flagged in the report) rather than locked without a record; the list is never overwritten by an empty one.

## v3.10.0.1-0.6.1 (2026-10-14)

### Changed
- **The header's license chip just says "Licensed".** The full text (who it's licensed to and when it expires) was long enough to crowd the header's other buttons. Click **Licensed** to see who the license is for, when it expires, its license ID and when this computer last checked in, with a button to enter a different key.

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
