# Command Notes (My Toddler Notes)

These notes explain the commands I use across labs in very simple terms.
They act as a personal reference and will be updated as I learn and use more commands.

---

## Users & Groups

| Command | Explain like I'm 5 |
|-------|--------------------|
| `whoami` | “Who am I right now?” |
| `useradd -m -s /bin/bash <username>` | “Make a new person and give them their own room.” |
| `usermod -l <new> <old>` | “Change the person’s name, but keep everything else the same.” |
| `usermod -aG <group> <user>` | “Put this person into a team without removing them from other teams.” |
| `id <username>` | “Show me this person’s ID card and what teams they belong to.” |
| `groupadd <group>` | “Make a new team.” |
| `groupmod -n <new> <old>` | “Change the team’s name without deleting it.” |
| `gpasswd -d <user> <group>` | “Take this person out of the team.” |
| `getent group <group>` | “Show me this team and who’s in it.” |
| `getent passwd <user>` | “Show me this person’s account details.” |

---

## Navigation & Identity

| Command | Explain like I'm 5 |
|-------|--------------------|
| `su - <username>` | “Pretend you logged in as this person properly, with their settings.” |
| `ls -ld /home/<username>` | “Who owns this room, and who is allowed inside?” |

---

## Sudo & Permissions

| Command | Explain like I'm 5 |
|-------|--------------------|
| `visudo -f /etc/sudoers.d/admins` | “Carefully write the rules for who is allowed to be the boss.” |
| `chmod 440 /etc/sudoers.d/admins` | “Only the system can read these rules, nobody can mess with them.” |
| `visudo -c` | “Double-check the rules before using them.” |
| `sudo -l` | “What boss-level commands am I allowed to run?” |

---

## Files & Directories

| Command | Explain like I'm 5 |
|-------|--------------------|
| `mkdir <directory>` | “Make a new folder.” |
| `mkdir <dir1> <dir2> <dir3>` | “Make lots of folders in one go.” |
| `mkdir -p <path>` | “Make the folder and any folders above it if they don’t exist.” |
| `chown <owner>:<group> <dir>` | “Decide who owns it and which team it belongs to.” |
| `chmod 2770 <dir>` | “Only the team can use this folder, and everything inside stays part of the team.” |
| `chmod 2775 <dir>` | “The team can fully use it, others can look but not change anything.” |
| `ls` | “What’s here?” |
| `ls -l` | “Show me who can do what with these files.” |
| `ls -d */` | “Show me just the folders.” |
| `ls -ld */` | “Show me who owns each folder and who can use it.” |

---

## Permissions Library (Quick Reference)

| Mode | Explain like I'm 5 |
|-----|--------------------|
| `2770` | “Owner and team can read, write, and enter. Others are blocked. New files stay with the team.” |
| `2775` | “Owner and team can fully use it. Others can look and enter, but not change anything.” |
| `111` | “You can enter or run it, but you can’t see or change anything inside.” |
| `555` | “Everyone can look and enter, but nobody can change anything.” |

---

## Misc Commands

| Command | Explain like I'm 5 |
|-------|--------------------|
| `sudo shutdown now` | “Turn the computer off right now.” |
| `clear` / `Ctrl + L` | “Clean the screen so it’s easier to see.” |

---
