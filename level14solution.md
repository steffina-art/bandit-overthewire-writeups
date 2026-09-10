## Level 14 — Submitting a Password to a Local Port

The goal here was to get the level 15 password by sending the current password to a service listening on **port 30000** on localhost.

```bash
cat /etc/bandit_pass/bandit14
echo "<password>" | nc localhost 30000
```

`/etc/bandit_pass/bandit14` holds the current level's password (readable only because I was logged in as `bandit14`), and piping it into `nc` (netcat) is the same as connecting and typing it in by hand.
then connecting it to the localhost 30000 port. The service echoed back the next password.

