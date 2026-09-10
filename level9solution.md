## Level 9 — Filtering Readable Text Out of Binary Data

`data.txt` this time was mostly binary garbage, with the actual password buried inside, preceded by a run of `=` characters.

```bash
strings data.txt | grep '='
```

`strings` pulls out anything that looks like printable text from a binary file, and I filtered further for lines starting with `=` since that's what the clue mentioned.
