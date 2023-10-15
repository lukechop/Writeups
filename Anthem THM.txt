#### Initial Reconnaissance

- Conducted an Nmap scan with scripting engine and service detection.

#### Web Enumeration

- Discovered a web server.
- Located a password in `/robots.txt`.
- Found Flag 2 in the page source code.

#### Directory Bruteforcing

- Executed gobuster.
- `/install` redirected to `/umbraco` (a login form).

#### Flag Discovery

- Flag 3 located in `/authors`.

#### User Enumeration

- Identified the administrator through clues in a blog post.
- Derived the administrator's email based on the corporate email format.

#### Gaining Initial Access

- Attempted to log in at `/umbraco`.
- Successful login using `sg` and a discovered password via xfreerdp (port 3389 open).
- User flag obtained from the desktop.

#### Privilege Escalation

- Searched for admin password, no immediate success.
- Used `dir .txt /s /b` to search system for .txt files.
- Located a backup directory.

#### Overcoming Permissions

- Added current user account for directory access.
- Obtained what appears to be an admin password.

#### Root Access

- Accessed the admin directory using the new password.
- Captured the root flag.