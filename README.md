# Per-List Backup and Restore — GNU Mailman — GSoC 2026

**Report: https://naveeeya.github.io/Mailman-GSoC-26/**

Two commands for Mailman Core that write a mailing list's complete state to a JSON
file and rebuild the list from that file.

```
mailman backup  <listspec> [output_path]
mailman restore <backup_file> [--listname NAME] [--overwrite] [--yes]
```

Mailman 3 keeps list state in a relational database, and until now there was no
supported way to recover a list that had been deleted. A backup carries the list
config, every roster entry with its delivery preferences, content filters,
acceptable aliases, header match rules, list-scoped bans and archiver states. The
moderator password is deliberately excluded.

- **Merge request:** https://gitlab.com/mailman/mailman/-/merge_requests/1505
- **Branch:** https://gitlab.com/Naveeeya/mailman/-/tree/gsoc/per-list-backup-restore
- **Last GSoC commit:** `02660ea2`

33 commits, 11 files, 67 tests, 100% branch diff coverage. Pipeline green on SQLite,
PostgreSQL and MySQL across Python 3.9 to 3.13. The merge request is open for review
and not yet merged.

## Outstanding

REST endpoints in Core (`GET /3.1/lists/{listname}/backup`, `POST .../restore`), the
mailmanclient wrapper, and the Postorius buttons that sit on top of both. The report
describes their intended shapes.

## This repository

Holds the report only. All project code lives in the Mailman repository on the branch
above.

Author: Navya Khanna · [@Naveeeya](https://gitlab.com/Naveeeya)
