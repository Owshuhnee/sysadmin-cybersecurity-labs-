# Command Notes (My Toddler notes)

These notes explain the commands I use across labs in simple terms.

## Users & Groups

| Command | What it does | Explain like I'm 5 |
|-------|--------------|--------------------|
| `groupadd admins` | Creates a new group called `admins`. | “Make a new team called admins.” |
| `useradd -m -s /bin/bash jove-dev` | Creates a user with a home folder and Bash shell. | “Make a new person and give them their own room.” |
| `usermod -aG admins jove-admin` | Adds a user to the admins group without removing other groups. | “Put this person in the admins team without removing them from other teams.” |
| `id jove-dev` | Shows a user’s ID and group memberships. | “Show me this person’s ID card.” |
| `gpasswd -d jove-dev admins` | Removes a user from a group. | “Take this person out of the admins team.” |
| `whoami` | Displays the current logged-in user. | “Who am I right now?” |
| `getent group` | Displays group information from the system database. | “Show me this team and who’s in it.” |
| `sudo groupadd <group>` | Creates a new group. | “Make a new team.” |
| `sudo groupmod -n new old` | Renames an existing group. | “Change the team’s name without deleting it.” |



## Sudo & Permissions

| Command | What it does | Explain like I'm 5 |
|-------|--------------|--------------------|
| `visudo -f /etc/sudoers.d/admins` | Safely creates or edits sudo rules for the admins group. | “Carefully write the rules for who is allowed to be the boss.” |
| `chmod 440 /etc/sudoers.d/admins` | Sets strict permissions on sudo rules. | “Only the system is allowed to read these rules.” |
| `visudo -c` | Checks sudo configuration for errors. | “Double-check the rules before using them.” |



## Files & Directories

| Command | What it does | Explain like I'm 5 |
|-------|--------------|--------------------|
| `mkdir -p /srv/devshare` | Creates a folder and any missing parent folders. Does not error if the folder already exists. | “Make this folder, and make any bigger folders first if they don’t exist.” |
| `chown root:developers /srv/devshare` | Sets the owner to `root` and the group to `developers`. | “Root owns it, and the developers team is allowed to use it.” |
| `chmod 2770 /srv/devshare` | Sets read/write/execute for owner and group, none for others. Enables setgid so new files inherit the group. | “Only the team can use this folder, and anything created inside stays part of the team.” |
