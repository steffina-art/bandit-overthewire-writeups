## Level 3 — A Hidden File

The password was somewhere inside a directory called `inhere`, but `ls` came up empty.

```bash
cd inhere
ls -a
```
`-a` shows dotfiles, which are hidden by default. There was a file called `.hidden` sitting there.

```bash
cat .hidden
```


