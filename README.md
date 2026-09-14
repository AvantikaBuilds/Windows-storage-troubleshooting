# Windows-C-Drive-Storage-Optimization-Troubleshooting
Investigated critically low free space on the Windows C: drive and performed a structured cleanup while protecting Windows system files, hardware drivers, development environments, database software, and application dependencies.

*Self-directed troubleshooting project — Windows administration, storage analysis, dependency-aware system cleanup*

## The problem
My C: drive was down to **17.8 GB free out of 220 GB**. Instead of mass-uninstalling apps or deleting folders blindly, I treated it as a real troubleshooting task: diagnose by category, tell apart what's safe to remove vs. what's a dependency, verify before touching anything tied to active software.

## Before → After
| | Before | After |
|---|---|---|
| Free space | 17.8 GB | *(fill in)* |
| Used space | 202 GB | *(fill in)* |

## What I did
- Broke down disk usage by category using Windows Storage settings
- Cleared temp files; manually reviewed each file in Downloads than blind-deleting
- Audited installed apps individually — not a mass uninstall
- Verified which SQL Server version was active before removing an older install
- Separated real bloat from disguised dependencies (drivers, runtimes, ODBC/OLE DB, OEM utilities)
- Removed obsolete software, kept everything actively used

## Skills demonstrated
`Windows Storage Management` `Dependency Auditing` `Safe Uninstall Practices` `SQL Server` `Root-Cause Troubleshooting`

📄 **[Full troubleshooting log →](troubleshooting-log.md)** — every decision, and the reasoning behind it

## Screenshots
![before](s)
![after](screenshots/after-storage.png)
