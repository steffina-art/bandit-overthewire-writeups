## Level 12 — Repeatedly Compressed / Hex-Dumped File

This was the most involved one so far. `data.txt` was a **hexdump** of a file that had been compressed multiple times, using different tools stacked on top of each other.

Rough process:

```bash
mkdir /tmp/mywork12
cp data.txt /tmp/mywork12
cd /tmp/mywork12

# Turn the hexdump back into actual binary data
xxd -r data.txt > data.bin

# From here it's a loop of "check the file type, then decompress accordingly"
file data.bin
```

Then, depending on what `file` reported each round, I ran the matching command — usually one of:

```bash
mv data.bin data.gz  && gunzip data.gz
mv data.bin data.bz2 && bunzip2 data.bz2
mv data.bin data.tar && tar -xf data.tar
```
...renaming the output and re-running `file` after every step, until it finally came back as plain ASCII text — which was the password.

It's tedious and hard, but it's really just "check type → decompress → repeat" until the layers run out.
 
