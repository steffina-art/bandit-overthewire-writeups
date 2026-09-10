## Level 4 — Finding the Only Human-Readable File
Level 4's `inhere` folder had a bunch of files named `-file00` through `-file09`, and only one of them was actual readable text — the rest were junk/binary data meant to throw me off. And it's tiring to read all the files one by one.
I used the `file` command to check each one's type instead of guessing:

```bash
cd inhere
file ./-file*
```

That immediately flagged which file was `ASCII text` versus `data`. Then:

```bash
cat ./-fileXX
```
(swap `XX` for whichever number came back as ASCII text).
Find the file number by yourself so that you will gain experience!

