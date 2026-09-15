# Linux / DevOps Cheat Sheet

## File & Directory Management

| Command | Usage |
|---|---|
| `pwd` | Show the current working directory. |
| `ls` | List files and directories. |
| `ls -la` | List all files, including hidden files, with details. |
| `cd <dir>` | Change to a directory. |
| `mkdir <dir>` | Create a directory. |
| `touch <file>` | Create an empty file or update its timestamp. |
| `cp <src> <dest>` | Copy files or directories. |
| `mv <src> <dest>` | Move or rename files/directories. |
| `rm <file>` | Delete a file. |
| `rm -rf <dir>` | Recursively delete a directory and its contents. |
| `find <path> -name <pattern>` | Search for files/directories by name. |

## Viewing & Editing

| Command | Usage |
|---|---|
| `cat <file>` | Print an entire file to the terminal. |
| `less <file>` | View a file page-by-page. |
| `head <file>` | Show the first 10 lines of a file. |
| `tail <file>` | Show the last 10 lines of a file. |
| `tail -f <file>` | Continuously follow new lines added to a file/log. |
| `grep <pattern> <file>` | Search a file for matching text. |
| `grep -r <pattern> <dir>` | Recursively search files for matching text. |
| `sort <file>` | Sort lines of text. |
| `wc -l <file>` | Count the number of lines. |

## Permissions & Users

| Command | Usage |
|---|---|
| `whoami` | Show the current user. |
| `id` | Show the user's UID, GID, and group memberships. |
| `chmod 755 <file>` | Change file permissions. |
| `chown <user>:<group> <file>` | Change file owner and group. |
| `sudo <command>` | Run a command with elevated privileges. |

## Processes & System

| Command | Usage |
|---|---|
| `ps aux` | List running processes. |
| `top` | Display live CPU/memory/process information. |
| `kill <PID>` | Send a signal to a process. |
| `df -h` | Show filesystem disk usage in human-readable units. |
| `du -sh <dir>` | Show the total size of a directory. |
| `free -h` | Show RAM and swap usage. |
| `uname -a` | Display kernel/system information. |

## Services & Logs

| Command | Usage |
|---|---|
| `systemctl status <service>` | Check the status of a systemd service. |
| `systemctl start <service>` | Start a service. |
| `systemctl stop <service>` | Stop a service. |
| `systemctl restart <service>` | Restart a service. |
| `journalctl -u <service>` | View logs for a systemd service. |
| `journalctl -f` | Follow system logs in real time. |

## Networking

| Command | Usage |
|---|---|
| `ping <host>` | Test basic network reachability and latency. |
| `ip addr` | Display network interfaces and their IP addresses. |
| `dig <domain>` | Query DNS records and troubleshoot DNS resolution. |
| `curl <url>` | Make HTTP requests and inspect responses. |
| `ss -tulpn` | Show listening TCP/UDP ports and associated processes. |
| `traceroute <host>` | Show the network path toward a destination. |

## Packages & Archives

| Command | Usage |
|---|---|
| `apt update` | Refresh package repository metadata on Debian/Ubuntu. |
| `apt install <package>` | Install a package on Debian/Ubuntu. |
| `tar -czf archive.tar.gz <dir>` | Create a gzip-compressed tar archive. |
| `tar -xzf archive.tar.gz` | Extract a gzip-compressed tar archive. |

## DevOps Priority Commands


- `cd`
- `ls -la`
- `find`
- `grep`
- `tail -f`
- `chmod`
- `sudo`
- `ps`
- `kill`
- `df`
- `du`
- `systemctl`
- `journalctl`
- `ip addr`
- `ss`
- `dig`
- `curl`

These are especially useful for troubleshooting Linux services, containers, networking, DNS, logs, and production systems.