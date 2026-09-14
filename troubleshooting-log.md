# Troubleshooting Log — Windows C: Drive Cleanup

This is the detailed reasoning behind the clean up. Each row is a decision I can explain the "why" behind.

## Initial diagnosis
| Category | Size |
|---|---|
| Installed applications | ~80.1 GB |
| Desktop | ~43.9 GB |
| Pictures | ~12.5 GB |
| Temporary files | ~12.5 GB |
| Other | ~12 GB |

## Decisions

| Found | Investigation | Decision |
|---|---|---|
| C: drive nearly full | Windows Storage breakdown by category | Investigated top categories before acting, didn't guess |
| ~12.5 GB temp files | Windows Storage → Temporary files | Removed — safe, regenerable |
| Downloads folder large | Needed manual review of contents file by file | Separated files still needed from ones no longer useful; removed the unneeded ones rather than blind-deleting or leaving the whole folder untouched |
| Old SQL Server alongside SQL Server 2025 | Ran a query to confirm which instance was active | Kept 2025 (active); uninstalled the old one via the proper SQL Server uninstaller, not manual folder deletion |
| Multiple ODBC / OLE DB drivers | Identified as DB connectivity dependencies, not standalone apps | Retained |
| Multiple .NET / Visual C++ Redistributable versions | Recognized as shared runtime dependencies used by other software | Retained |
| Several Dell utilities | Separated update/recovery/support tools from bundled bloatware | Kept required support tools, removed the rest |
| Exam/secure browsers | Rarely used, easy to reinstall when needed | Removed |
| Hardware drivers (Intel / Realtek / Dell) | Confirmed active use, high risk if removed incorrectly | Left untouched |

## Why this mattered
The easy version of this task is "delete anything you don't recognize" — that's also the version that breaks a system. The actual skill here was pausing at each unfamiliar item and asking: *is this an application, or is this something else depending on it?* That distinction is the same one that matters in a support role — before touching a user's machine, you verify what a component does before removing it.
