All levels are reached the same basic way:

```bash
ssh banditN@bandit.labs.overthewire.org -p 2220
```

where `N` is the level number, and the password is whatever I dug up from the previous level.

---

## Level 0 — Getting In

This one's just to make sure I could actually connect. OverTheWire gives you the password for level 0 upfront.

```bash
ssh bandit0@bandit.labs.overthewire.org -p 2220
```

Once I was in, the goal said the level 1 password was sitting in a file called `readme` in the home directory.

```bash
cat readme
```

And there it was.
<password>
---
