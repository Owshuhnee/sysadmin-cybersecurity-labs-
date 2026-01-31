# Command Notes (My Toddler Notes)

These notes explain the commands I use across labs in simple, in easy toddler terms.  
They act as a personal reference and will be updated as I learn and use more commands.

---

## Users & Groups

| Command | What it does | Explain like I'm 5 |
|-------|--------------|--------------------|
| `whoami` | Displays the currently logged-in user. | “Who am I right now?” |
| `useradd -m -s /bin/bash <username>` | Creates a user with a home folder and Bash shell. | “Make a new person and give them their own room.” |
| `usermod -l <new> <old>` | Renames an existing user account. | “Change the person’s name, but keep everything else.” |
| `usermod -aG <group> <user>` | Adds a user to a group without removing other group memberships. | “Put this person into a team without kicking them out of other teams.” |
| `id <username>` | Shows a user’s UID, GID, and group memberships. | “Show me this person’s ID card.” |
| `groupadd <group>` | Creates a new group. | “Make a new team.” |
| `groupmod -n <new> <old>` | Renames an existing group. | “Change the team’s name without deleting it.” |
| `gpasswd -d <user> <group>` | Removes a user from a group. | “Take this person out of the team.” |
| `getent group <group>` | Displays group details from the system database. | “Show me this team and who’s in it.” |
| `getent passwd <user>` | Displays user account information. | “Show me this person’s account details.” |

---

## Navigation & Identity

| Command | What it does | Explain like I'm 5 |
|-------|--------------|--------------------|
| `su - <username>` | Switches to another user and loads their full environment. | “Pretend you logged in as this person properly.” |
| `ls -ld /home/<username>` | Shows ownership and permissions of a user’s home directory. | “Who owns this room, and who can enter it?” |

---

## Sudo & Permissions

| Command | What it does | Explain like I'm 5 |
|-------|--------------|--------------------|
| `visudo -f /etc/sudoers.d/admins` | Safely creates or edits sudo rules for a group. | “Carefully write the rules for who can be the boss.” |
| `chmod 440 /etc/sudoers.d/admins` | Sets strict permissions on sudo rules. | “Only the system is allowed to read these rules.” |
| `visudo -c` | Validates sudo configuration for errors. | “Double-check the rules before using them.” |
| `sudo -l` | Shows what sudo commands the current user is allowed to run. | “What am I allowed to do as the boss?” |

---

## Files & Directories

| Command | What it does | Explain like I'm 5 |
|-------|--------------|--------------------|
| `mkdir <directory>` | Creates a new directory. | “Make a new folder.” |
| `mkdir <dir1> <dir2> <dir3>` | Creates multiple directories at once. | “Make lots of folders in one go.” |
| `mkdir -p <path>` | Creates directories and missing parent directories. | “Make the folder and any folders above it if needed.” |
| `chown <owner>:<group> <dir>` | Changes ownership and group of a file or directory. | “Decide who owns it and which team it belongs to.” |
| `chmod 2770 <dir>` | Sets permissions and enables setgid so group ownership is inherited. | “Only the team can use this folder, and everything inside stays part of the team.” |
| `chmod 2775 <dir>` | Sets permissions and enables setgid so group ownership is inherited while allowing read/execute access for others. | “The team can fully use this folder, and others can view it but not change anything.” |
| `ls -l` | Lists files with permissions and ownership. | “Show me who can do what with these files.” |

---

Pending: need to create Permissions library here
2770
2775
111
555

sudo shutdown now
clear or ctrl + l
 

