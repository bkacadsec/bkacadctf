# Bandit 1
ssh bandit0@bandit.labs.overthewire.org -p 2220

```sh
bandit0@bandit:~$ cat readme 
boJ9jbbUNNfktd78OOpsqOltutMc3MY1
```

# Bandit 2

```sh
bandit1@bandit:/home$ cat /home/bandit1/-
CV1DtqXWVFXTvM2F0k09SHz0YwRINYA9
bandit1@bandit:/home$ 
```

# Bandit 3

```sh
bandit2@bandit:~$ cat /home/bandit2/spaces\ in\ this\ filename 
UmHadQclWmgdLOKQ3YNgjWxGoRMb5luK
bandit2@bandit:~$ 
```

# Bandit 4

```sh
bandit3@bandit:~$ ls -l
total 4
drwxr-xr-x 2 root root 4096 May  7 20:14 inhere
bandit3@bandit:~$ cat inhere/.hidden 
pIwrPrtPN36QITSp3EQaw936yaFoFgAB
bandit3@bandit:~$ 
```

# Bandit 5

```sh
bandit4@bandit:~/inhere$ find . -readable -size 33c
./-file01
./-file00
./-file06
./-file03
./-file05
./-file08
./-file04
./-file07
./-file02
./-file09

bandit4@bandit:~/inhere$ cat ./*
�/`2ғ}�%��rL~5�g��� �����p,k�;��r*��	�.!��C��J	�dx,�e�)�#��5����p�?��r�l$�?h�9('���!y�e�#�O��=��ly���~��A�f����-E�{���m�����ܗMkoReBOKuIDDepwhWk7jZC0RTdopnAYKh
�T�?�i��j���îP�F�l�n��J����{��@�e�0$�in=��_b�5FA�P7sz��g
```

koReBOKuIDDepwhWk7jZC0RTdopnAYKh

# Bandit 6

```sh
bandit5@bandit:~$ ls
inhere
bandit5@bandit:~$ cd inhere/
bandit5@bandit:~/inhere$ find . -size 1033c -readable 
./maybehere07/.file2
bandit5@bandit:~/inhere$ cat ./maybehere07/.file2
DXjZPULLxYr17uwoI01bNLQbtFemEgo7

```

# Bandit 7

```sh
bandit6@bandit:~$ find / -size 33c -group bandit6 -user bandit7
find: ‘/root’: Permission denied
find: ‘/home/bandit28-git’: Permission denied
find: ‘/home/bandit30-git’: Permission denied
find: ‘/home/bandit5/inhere’: Permission denied
find: ‘/home/bandit27-git’: Permission denied
find: ‘/home/bandit29-git’: Permission denied
find: ‘/home/bandit31-git’: Permission denied
find: ‘/lost+found’: Permission denied
find: ‘/etc/ssl/private’: Permission denied
find: ‘/etc/polkit-1/localauthority’: Permission denied
find: ‘/etc/lvm/archive’: Permission denied
find: ‘/etc/lvm/backup’: Permission denied
find: ‘/sys/fs/pstore’: Permission denied
find: ‘/proc/tty/driver’: Permission denied
find: ‘/proc/26230/task/26230/fd/6’: No such file or directory
find: ‘/proc/26230/task/26230/fdinfo/6’: No such file or directory
find: ‘/proc/26230/fd/5’: No such file or directory
find: ‘/proc/26230/fdinfo/5’: No such file or directory
find: ‘/cgroup2/csessions’: Permission denied
find: ‘/boot/lost+found’: Permission denied
find: ‘/tmp’: Permission denied
find: ‘/run/lvm’: Permission denied
find: ‘/run/screen/S-bandit26’: Permission denied
find: ‘/run/screen/S-bandit18’: Permission denied
find: ‘/run/screen/S-bandit13’: Permission denied
find: ‘/run/screen/S-bandit16’: Permission denied
find: ‘/run/screen/S-bandit31’: Permission denied
find: ‘/run/screen/S-bandit8’: Permission denied
find: ‘/run/screen/S-bandit14’: Permission denied
find: ‘/run/screen/S-bandit19’: Permission denied
find: ‘/run/screen/S-bandit21’: Permission denied
find: ‘/run/screen/S-bandit12’: Permission denied
find: ‘/run/screen/S-bandit5’: Permission denied
find: ‘/run/screen/S-bandit22’: Permission denied
find: ‘/run/screen/S-bandit24’: Permission denied
find: ‘/run/screen/S-bandit25’: Permission denied
find: ‘/run/screen/S-bandit0’: Permission denied
find: ‘/run/screen/S-bandit20’: Permission denied
find: ‘/run/screen/S-bandit23’: Permission denied
find: ‘/run/shm’: Permission denied
find: ‘/run/lock/lvm’: Permission denied
find: ‘/var/spool/bandit24’: Permission denied
find: ‘/var/spool/cron/crontabs’: Permission denied
find: ‘/var/spool/rsyslog’: Permission denied
find: ‘/var/tmp’: Permission denied
find: ‘/var/lib/apt/lists/partial’: Permission denied
find: ‘/var/lib/polkit-1’: Permission denied
/var/lib/dpkg/info/bandit7.password
find: ‘/var/log’: Permission denied
find: ‘/var/cache/apt/archives/partial’: Permission denied
find: ‘/var/cache/ldconfig’: Permission denied
bandit6@bandit:~$ cat /var/lib/dpkg/info/bandit7.password
HKBPTKQnIay4Fw76bEy8PVxKEDQRKTzs
bandit6@bandit:~$ 

```

# Bandit 8

```sh
bandit7@bandit:~$ ls
data.txt
bandit7@bandit:~$ wc data.txt 
  98567  197133 4184396 data.txt
bandit7@bandit:~$ cat data.txt | grep "millionth"
millionth	cvX2JJa4CFALtqS87jk27qwqGhBM9plV
bandit7@bandit:~$ 

```

# Bandit 9

```sh
bandit8@bandit:~$ cat data.txt | sort | uniq -cu
      1 UsvVyFSfZZWbi6wgC7dAFyFuR6jQQUhR

```

# Bandit 10

```sh
bandit9@bandit:~$ strings data.txt 
...
&========== truKLdjsbJ5g7yyJ2X2R0o3a5HQJFuLk
...
```

# Bandit 11

```sh
bandit10@bandit:~$ ls
data.txt
bandit10@bandit:~$ wc data.txt 
 1  1 69 data.txt
bandit10@bandit:~$ cat data.txt 
VGhlIHBhc3N3b3JkIGlzIElGdWt3S0dzRlc4TU9xM0lSRnFyeEUxaHhUTkViVVBSCg==
bandit10@bandit:~$ cat data.txt | base64 -d
The password is IFukwKGsFW8MOq3IRFqrxE1hxTNEbUPR
bandit10@bandit:~$ 
```

# Bandit 12

```sh
bandit11@bandit:~$ wc data.txt 
 1  4 49 data.txt
bandit11@bandit:~$ cat data.txt 
Gur cnffjbeq vf 5Gr8L4qetPEsPk8htqjhRK8XSP6x2RHh
bandit11@bandit:~$ cat data.txt | tr 'N-ZA-Mn-za-m' 'A-Za-z'
The password is 5Te8Y4drgCRfCx8ugdwuEX8KFC6k2EUu
bandit11@bandit:~$ 

```
