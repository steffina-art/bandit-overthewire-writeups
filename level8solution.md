## Level 8 — Finding the Line That's Not a Duplicate

`data.txt` again, but this time the password was on the **one line that appears exactly once** — everything else repeats.

```bash
sort data.txt | uniq -u
```

`sort` groups identical lines next to each other, and `uniq -u` prints only the lines that have no duplicates.
cause without uniq the list will provide set of duplicated values

