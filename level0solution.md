I've been working through [OverTheWire's Bandit wargame](https://overthewire.org/wargames/bandit/) to get more comfortable with the Linux command line, and figured I'd keep notes on how I cracked each level. Nothing fancy here — just what I ran and why it worked, mostly so future-me remembers the logic instead of just the commands. And these are the commands I used in Windows PowerShell.
A quick note before diving in: I'm leaving the actual passwords out of this writeup and using placeholders like `<password>` instead. Anyone doing the game should find their own — that's kind of the point, So that will make them more interested rather than spoonfeed.
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
