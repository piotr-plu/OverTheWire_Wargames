# OverTheWire Bandit – Walkthrough

Dates indicate when each level was solved.  

---

## Level 0
**Date:** 18/08/2025  

```bash
ls
cat readme
````

---

## Level 1

**Date:** 18/08/2025

```bash
ls -la
cat ./-
```

---

## Level 2

**Date:** 18/08/2025

```bash
cat ./'--spaces in this filename--'
```

---

## Level 3

**Date:** 18/08/2025

```bash
ls -la
cat inhere/'...Hiding-From-You'
```

---

## Level 4

**Date:** 18/08/2025

```bash
cd /inhere
file ./*
cat ./-file07
```

---

## Level 5

**Date:** 18/08/2025

```bash
find inhere/ -type f ! -executable -size 1033c -exec cat {} \;
```

---

## Level 6

**Date:** 18/06/2025

```bash
find / -type f -user bandit7 -group bandit6 -size 33c -exec cat {} \; 2>/dev/null
```

---

## Level 7

**Date:** 18/08/2025

```bash
cat data.txt | grep millionth
```

---

## Level 8

**Date:** 18/08/2025

```bash
sort data.txt | uniq -u
```

---

## Level 9

**Date:** 18/08/2025

```bash
strings data.txt | grep ===
```

---

## Level 10

**Date:** 18/08/2025

```bash
base64 -d data.txt
```

---

## Level 11

**Date:** 18/08/2025

```bash
cat data.txt | tr 'A-Za-z' 'N-ZA-Mn-za-m'
```

---

## Level 12

**Date:** 18/08/2025

```bash
file zadanie12.bin
mv zadanie12.bin zadanie12.gz
gzip -d zadanie12.gz
mv zadanie12 zadanie12.bz2
bzip2 -d zadanie12.bz2
mv zadanie12 zadanie12.gz
gzip -d zadanie12.gz
mv zadanie12 zadanie12.tar
tar -x -f zadanie12.tar
file data5.bin
mv data5.bin data5.tar
tar -x -f data5.tar
mv data6.bin data6.bz2
bzip2 -d data6.bz2
mv data6 data6.tar
tar -x -f data6.tar
mv data8.bin data8.gz
gzip -d data8.gz
cat data8
```

---

## Level 13

**Date:** 19/08/2025

```bash
ssh -i sshkey.private -p 2220 bandit14@bandit.labs.overthewire.org
cat /etc/bandit_pass/bandit14
```

---

## Level 14

**Date:** 19/08/2025

```bash
nc localhost 30000
# send password for level 14
```

---

## Level 15

**Date:** 19/08/2025

```bash
openssl s_client -quiet -connect localhost:30001 -servername localhost
# send password for level 15
```

---

## Level 16

**Date:** 19/08/2025

```bash
nc -zv localhost 31000-32000 2>&1 | grep succeeded
nmap -v -p31046,31518,31691,31790,31960 -sV --open localhost
ncat --ssl localhost 31790
```

---

## Level 17

**Date:** 19/08/2025

```bash
grep -Fvxf passwords.old passwords.new
# OR
diff passwords.new passwords.old
```

---

## Level 18

**Date:** 19/08/2025

```bash
ssh -p 2220 bandit18@bandit.labs.overthewire.org 'cat readme'
```

---

## Level 19

**Date:** 19/08/2025

```bash
./bandit20-do cat /etc/bandit_pass/bandit20
```

---

## Level 20

**Date:** 19/08/2025

```bash
tmux new -s script
tmux new -s listener
```

**In `listener`:**

```bash
nc -lnvp 10000
```

**In `script`:**

```bash
./suconnect 10000
```

---

## Level 21

**Date:** 19/08/2025

```bash
cat /etc/cron.d/cronjob_bandit22
cat /usr/bin/cronjob_bandit22.sh
cat /tmp/t7O6lds9S0RqQh9aMcz6ShpAoZKF7fgv
```

---

## Level 22

**Date:** 19/08/2025

```bash
cat /etc/cron.d/cronjob_bandit23
cat /usr/bin/cronjob_bandit23.sh
cat /tmp/$(echo I am user bandit23 | md5sum | cut -d' ' -f1)
```

---

## Level 23

**Date:** 19/08/2025

```bash
cat /etc/cron.d/cronjob_bandit24
cat /usr/bin/cronjob_bandit24.sh
cat > /var/spool/bandit24/foo/passscript.sh << 'EOF'
#!/bin/bash
cat /etc/bandit_pass/bandit24 > /tmp/pass_bandit24_$(whoami).txt
EOF
chmod +x /var/spool/bandit24/foo/passscript.sh
cat /tmp/pass_bandit24_bandit24.txt
```

---

## Level 24

**Date:** 19/08/2025

```bash
#!/bin/bash
coproc nc localhost 30002
for i in $(seq 0 9999); do
  echo "gb8KRRCsshuZXI0tUuR6ypOFjiZbf3G8 $i" >&"${COPROC[1]}"
  read -r reply <&"${COPROC[0]}"
  if [[ ! $reply == *"Wrong"* ]]; then
    echo "$i : $reply"
  fi
done
```

---

## Level 25

**Date:** 19/08/2025

```bash
ssh -i bandit26.sshkey -p 2220 bandit26@localhost
cat /etc/passwd | grep bandit26
# resize terminal to very small
ssh -i bandit26.sshkey -p 2220 bandit26@localhost
# start v and use command :set shell=/bin/bash, :shell
cat /etc/bandit_pass/bandit26
```

---

## Level 26

**Date:** 19/08/2025

```bash
./bandit27-do cat /etc/bandit_pass/bandit27
```

---

## Level 27

**Date:** 19/08/2025

```bash
mktemp -d
git clone "ssh://bandit27-git@localhost:2220/home/bandit27-git/repo" /tmp/tmp.tipXfBx3GN
cat /tmp/tmp.tipXfBx3GN/README
```

---

## Level 28

**Date:** 19/08/2025

```bash
TMPDIR=$(mktemp -d)
git clone "ssh://bandit28-git@localhost:2220/home/bandit28-git/repo" $TMPDIR
git log
git show 68314e012fbaa192abfc9b78ac369c82b75fab8f
```

---

## Level 29

**Date:** 19/08/2025

```bash
TMPDIR=$(mktemp -d)
git clone "ssh://bandit29-git@localhost:2220/home/bandit29-git/repo" $TMPDIR
git branch -a
git show origin/dev:README.md
```

---

## Level 30

**Date:** 19/08/2025

```bash
TMPDIR=$(mktemp -d)
git clone "ssh://bandit30-git@localhost:2220/home/bandit30-git/repo" $TMPDIR
git tag
git show secret
```

---

## Level 31

**Date:** 20/08/2025

```bash
TMPDIR=$(mktemp -d)
git clone "ssh://bandit31-git@localhost:2220/home/bandit31-git/repo" $TMPDIR
cat README.md
echo "May I come in?" > key.txt
git add -f key.txt
git status
git commit -m "my force commit"
git push
```

---

## Level 32

**Date:** 20/08/2025

```bash
$SHELL
$0
/bin/bash
cat /etc/bandit_pass/bandit33
```