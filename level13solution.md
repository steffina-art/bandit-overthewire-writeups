## Level 13 — Logging In With an SSH Private Key

Instead of a password, this level handed me an SSH **private key** (`sshkey.private`) and said it would let me log into `bandit14` directly — no password needed. And in terminal I used ls command and it provided me with HINT sshkey.private and so reading it I exited then again
```bash
ls
##a hint will be provided and read that hint
cat HINT
##then exit
exit
```
then this process will help you to login inside bandit14 
```bash
scp -P 2220 bandit13@bandit.labs.overthewire.org:sshkey.private
 dir
ssh -i .\sshkey.private bandit14@bandit.labs.overthewire.org -p 2220
##you will be logged into bandit14
cat /etc/bandit_pass/bandit14
```

in this command we are copying the contents outside the bandit and login using password once again then reading it. LATER
The `-i` flag tells `ssh` to authenticate using that key file instead of a password. Since I was already on the Bandit server, I connected to `bandit14`. Then reading the password for 14.
 
