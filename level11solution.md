## Level 11 — ROT13

This one was scrambled with ROT13 (each letter shifted 13 places through the alphabet — which conveniently means applying it twice gets you back to the original).

```bash
cat data.txt | tr 'A-Za-z' 'N-ZA-Mn-za-m'
```

`tr` here maps each letter onto the one 13 places ahead, which is exactly what ROT13 does.
 
