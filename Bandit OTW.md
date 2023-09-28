[[Common Linux Commands]]
[[Linux Privilege Escalation]]
[[Linux Fundamentals]]

#### 0 -> 1
NH2SXQwcBdpmTEzi3bvBHMM9H66vVXjL

#### 1 -> 2
- Dashed filename
- Had to cat the whole directory
- rRGizSaX8Mk1RTb1CNQoXTcYZWU6lgzi
#### 2 -> 3
- Spaces were in filename, just tabbed it
- aBZ0W5EmUfAf7kHTQeOwd8bauFJ2lAiG
#### 3 -> 4
- Hidden file
- Had to use ls -la then cat .hidden
- 2EW7BBsr6aMMoJ2HjW067dm8EgX26xNe
#### 4 -> 5
- easy
- lrIWWI6bB37kxfiCQZqUdOIYfr6eEeqR
#### 5 -> 6
- Had to find file that was 1033 bytes
- used find -size 1033c
- P4L4vucdmLnm8I7Vl7jG1ApGSfjYKqJU
#### 6 -> 7
- had to find specific file that was owned by specific user and group
- used find / with the -user and -group flag
- trashed junk with 2>/dev/null
- z7WtoNQU2XfjmMtWA8u5rN4vzqu4v99S
#### 7 -> 8
- easy grep
- TESKZC0XvTetK0S9xNwm25STk5iWrBvP
### 8 -> 9
- had to show line that didn't repeat
- `cat data.txt | sort | uniq -u`
- EN632PlfYiZbn3PhVK3XOGSlNInNE00t
### 9 -> 10
- strings
- G7w8LIi6J3kTb8A7j9LgrywtEUlyyp6s
### 10 -> 11
- base64
- 6zPeziLdR2RKNdNYFNb6nVCKzphlXHBM
### 11 -> 12
- rot13
- JVNBBFSmZwKKOP0XbFXOoW8chDz5yVRv
### 12 -> 13
- a **hex dump** is a hexadecimal view of computer data from memory of a computer file. Hex dumps are commonly organized into rows of 8 or 16 bytes, sometimes separated by whitespaces.
- `xxd -r data.txt <data2`
- had to use `mv` to change the extensions to whatever `file` had it at
- `gzip -d data2.gzip`
- `tar -xvf data2.tar`
- wbWdlBxEir4CaE8LaPhauuOo6pwRmrDw
### 13 -> 14
- used ssh with a certificate to log in
- `ssh -i sshkey.private bandit14@bandit.labs.overthewire.org -p 222`
### 14 -> 15
- had to write to a port
- used `echo "text" | nc localhost 30000`
- jN2kgmIXJ6fShzhT2avhotn4Zcka6tnt
### 15 -> 16
- Connected using openssl
- `echo "jN2kgmIXJ6fShzhT2avhotn4Zcka6tnt" | openssl s_client -ign_eof -connect localhost:30001` 

- JQttfApK4SeyHwDlI9SXGR50qclOAil1
### 16 -> 17
- if bad permissions, `chmod 600 (filename)`
- had to get private key by scanning network for open machines and testing to machines to see which had openssl
- by getting into machine and giving password for last level, got private key
- had to rename private key `id_rsa` 
### 17 -> 18
- `dif` (file1) (file2) - shows the difference
- hga5tuuCLF6fFzUpnagiMN8ssu9LFrdg
### 18 -> 19
- had to run `cat readme` right after sshing
- awhqfNnAbc1naukrpqDYcF95h7HoMTrC
### 19 -> 20
- `readelf` 
- had to use the executable to read into /etc/bandit
- VxCazJaVykI6W36BkBU0mJTCM8rR95XT
### 20 -> 21
- unix job control: 
- **&**: Run a command in the background by appending an ampersand (`&`) at the end, like `command &`.
- **CTRL-Z**: Pauses the current foreground job. Use this to halt a job if you need terminal access.
- **bg**: Resume a paused job in the background. Type `bg` followed by job number, like `bg %1`.
- **fg**: Bring a background job to the foreground. Usage is similar to `bg`: `fg %1`.
- **jobs**: Lists all current background jobs. Shows you job numbers, which can be used with `bg` and `fg`. 
- to create a port and write to it: `nc -l -p (port)` then write to it after
- NvEJF7oVjkddltPSrdKEFOllh9V1IBcq
### 21 -> 22
- Cron
- all * means running every minute
- WdDozAdTM2z9DiFEQ2mGlwngMfj4EZff
### 22 -> 23






