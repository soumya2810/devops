# Day 2 - Linux Permissions

## Date
Thursday, May 14, 2026 (early morning, during night shift)

## What I did
- Reviewed Day 1: SSH'd into AWS EC2 server
- Created a practice folder ~/day2
- Decoded real permissions with ls -la (.bashrc, .ssh, day1.md)
- Changed permissions on secret.txt using chmod:
  - 600 (rw-------) -> private to owner
  - 777 (rwxrwxrwx) -> everyone can do anything (BAD)
  - 644 (rw-r--r--) -> normal file default
- Created hello.sh script
- Got "Permission denied" because file lacked execute (x)
- Used chmod 755 to add execute permission
- Successfully ran ./hello.sh -> printed "Hello from a script!"
- Hit a broken-quote bash trap, recovered with Ctrl+C

## What I learned
- Permissions are 3 groups (user/group/others) x 3 actions (rwx)
- r=4, w=2, x=1 (add them up for octal)
- 600 = private, 644 = normal file, 755 = executable script, 400 = SSH key
- 777 is almost always wrong (security code smell)
- Files need x permission to run, even if they contain valid commands
- .ssh is locked to 700 because it holds private keys, not because it's a folder
- chown changes ownership (vs chmod which changes permissions)
- Ctrl+C cancels a stuck/broken bash command

## How I felt
Concepts felt overwhelming at first - the numbers were confusing.
Worked through the octal math step by step until it clicked.
Got tripped up by an unclosed quote, recovered cleanly.
Real lesson: debugging IS the job.

## Next
Day 3 - Linux file system, links, find, grep
