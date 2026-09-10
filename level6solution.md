## Level 6 — Searching the Whole Filesystem

No more `inhere` folder to search — the password file could be *anywhere* on the system. But I had three clues:

- owned by user `bandit7`
- owned by group `bandit6`
- exactly 33 bytes

```bash
find / -user bandit7 -group bandit6 -size 33c 2>/dev/null
```
I redirected stderr to `/dev/null` because searching from `/` throws a ton of "Permission denied" noise for folders I can't access, and I only cared about the one result that actually worked.

Then this provides .password something then read that .passsword to get the password for bandit7.
