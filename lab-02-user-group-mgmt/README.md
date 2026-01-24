# Lab 2 — User and Group Management

## Lab Metadata
- **Category:** System Administration
- **Subdomain:** Linux Administration
- **Difficulty:** Beginner
- **Status:** Completed
- **Estimated Time:** 2–3 hours

---

## Objective
This lab focuses on managing Linux users and groups, implementing role-based access control, and enforcing least-privilege administration using `sudo`.

The goal is to demonstrate how administrative access is controlled through group membership and how misconfigurations can be identified and corrected.

---

## Environment
- **Host OS:** Windows 11
- **Hypervisor:** VirtualBox
- **Guest OS:** Ubuntu Server 22.04 LTS
- **Lab VM:** Same environment as Lab 01

---

## Tasks Performed

### Task 1 — Create Groups
Role-based groups were created to separate administrative and non-administrative users.

```bash
- sudo groupadd admins
- sudo groupadd developers
- getent group admins
- getent group developers
```
**Evidence:** 01-create-verify-groups.png


### Task 2 — Create Groups
Two users were created to represent different roles.
- jove-admin → administrative role
- jove-dev → standard (non-admin) role

```bash
- sudo useradd -m -s /bin/bash jove-admin
- sudo useradd -m -s /bin/bash jove-dev
- sudo passwd jove-admin
- sudo passwd jove-dev
```
**Evidence:** 02-create-users.png


### Task 3 — Assign Users to Groups
Users were assigned to their respective groups.

```bash
sudo usermod -aG admins jove-admin
sudo usermod -aG developers jove-dev
id jove-admin
id jove-dev
```
**Evidence:** 03-assign-users-to-groups.png


### Task 4 — Configure & Validate Sudo Access
Sudo access was granted only to the admins group using a dedicated sudoers file.

```bash
sudo visudo -f /etc/sudoers.d/admins
sudo chmod 440 /etc/sudoers.d/admins
sudo visudo -c
```
**Evidence:**
04-sudoers-admins-config.png
05-sudoers-validate-visudo.png

During validation, a misconfiguration was identified where the jove-dev user had unintentionally inherited administrative privileges through group membership.

The issue was corrected by removing the user from the privileged group:

```bash
sudo gpasswd -d jove-dev admins
```

- jove-admin has full sudo access
- jove-dev has no sudo privileges

**Evidence:** 06-remove-admin-access.png


### Task 5 - Pending

---

## Security Considerations

---

## Reflection




