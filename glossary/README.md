# Glossary (All Labs)

This glossary defines common words and ideas used across my labs.

## Virtualisation
- **Host (Host OS):** Your real computer (e.g., Windows 11).
- **Guest (Guest OS):** The OS running inside the VM (e.g., Ubuntu Server).
- **Hypervisor:** Software that runs VMs (e.g., VirtualBox).
- **Snapshot:** A “save point” for a VM you can roll back to.
- **NAT (Network Address Translation):** A networking mode where the VM can access the internet, but inbound access is restricted by default.


## Authentication & Identity
- **whoami:** Displays the currently logged-in user.
- **Login shell:** The shell started when a user logs in (e.g., `/bin/bash`).
- **Environment:** User-specific settings loaded at login, such as PATH and profile files.


## Users and Groups
- **User:** An account that can log in and run commands.
- **Group:** A label you can assign to users. Used to control access to files and permissions.
- **Primary group:** The main group a user belongs to.
- **Supplementary group:** Extra groups a user is added to.
- **UID (User ID):** A unique number assigned to each user account.
- **GID (Group ID):** A unique number assigned to each group.
- **Role-based access control (RBAC):** Managing permissions based on group membership rather than individual users.


## Permissions
- **Owner / Group / Others:** The three permission “buckets” for a file/folder.
- **chmod:** Changes permissions.
- **chown:** Changes owner and/or group.
- **Least privilege:** Give only the minimum access needed.
- **setgid:** A special permission that causes new files in a directory to inherit the directory’s group.
- **2770:** A permission mode where owner and group have full access, others have none, and setgid is enabled.


## Sudo
- **sudo:** Run a command with admin rights (if you’re allowed).
- **sudoers:** The rules file(s) that decide who can use sudo.
- **visudo:** Safe editor/checker for sudo rules.


## Useful folders
- **/srv:** Common place to store data for services (shared folders, web content, etc.).
- **/etc:** System configuration files.
- **/home:** User home folders.


## Configuration Files
- **/etc/sudoers.d/:** A directory for modular sudo configuration files.
- **sudoers file:** A configuration file that defines who can run commands with sudo.


## Verification & Validation
- **Validation:** Checking that a configuration is correct before using it.
- **visudo -c:** A command that validates sudo configuration files for errors.


