## Level 2 — Spaces in a Filename

The file this time was called `spaces in this filename`. Same idea as before — spaces break naive commands unless you handle them.

```bash
cat "spaces in this filename"
```

Quoting the whole name (or escaping each space with a backslash) keeps the shell from treating it as three separate arguments.

---
