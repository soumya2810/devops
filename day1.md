# Day 1 - Linux Foundations

## Date
Friday, May 8, 2026 (early morning, during night shift)

## What I did
- SSH'd into my AWS EC2 server (Ubuntu 26.04, ap-south-1 Mumbai)
- Ran my first 8 Linux commands: whoami, pwd, ls, ls -la, mkdir, cd, touch, echo, cat
- Created a folder called day1 and a file called hello.txt
- Wrote text to the file using echo and redirection (>)
- Read the file back using cat
- Explored the Linux filesystem: /, /etc, /home, /root
- Tried to break things: hit "Permission denied" on /root and /etc/passwd
- Learned that sudo lets me run commands as admin
- Checked system info: hostname, date, uptime, df -h, free -h, nproc

## What I learned
- Linux has one root directory (/) and everything lives under it
- ~ is shorthand for my home folder
- .. means parent folder
- Permission denied errors are Linux protecting the system, not bugs
- Silence after a command usually means it worked
- echo "text" > file.txt writes text into a file
- cat prints file contents to the screen

## How I felt
Day 1 was harder emotionally than technically. Almost gave up on Wednesday night. 
Came back Friday 2 AM and did it. Feeling proud.

## Next
Day 2 — Linux file permissions (chmod, chown, octal notation)
