## Level 1 — A File Named `-`

This one's a classic gotcha. There's a file literally named `-` in the home directory, and if you try `cat -`, the shell reads it as "read from standard input" instead of "open the file named dash."

The fix is to be explicit about the path:

```bash
cat ./-
```

Lesson learned: dashes at the start of arguments have special meaning, so `./` forces the shell to treat it as a relative path instead.

 
