## Level 15 — Same Idea, but Over SSL

This level was basically Level 14 again, except the service on **port 30001** expected an SSL/TLS-encrypted connection, so plain `nc` wouldn't work.

```bash
cat /etc/bandit_pass/bandit15
openssl s_client -connect localhost:30001 -quiet
```

Once connected, I pasted in the password and hit enter, same as before — `openssl s_client` just wraps the connection in TLS first, which is what the service required.
