## Level 5 — Digging Through Subdirectories

This level upped the difficulty: the password file was buried somewhere inside `inhere`, which had a bunch of nested subdirectories. The goal gave three clues — the file had to be:

- human-readable
- exactly 1033 bytes
- **not** executable

`find` with the right flags did all the filtering for me:

```bash
find inhere -type f -size 1033c ! -executable
```
type f refers to human-readable format
size 1033c refers no of bytes required to search
! executable refers to the file that isn't in executable format

That narrowed a haystack of files down to exactly one match.

---

