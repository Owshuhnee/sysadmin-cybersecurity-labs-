# Lab 2R — Linux User & Group Management (Independent Practice)

## Lab Metadata
- **Category:** System Administration
- **Subdomain:** Linux Administration
- **Difficulty:** Beginner
- **Mode:** Independent (no AI assistance), Scenario was AI generated
- **Status:** In Progress
- **Estimated Time:** (pending)

---

## Scenario Overview

You are acting as a **junior Linux system administrator** in a small organization.  
A new internal application project is starting, and you are responsible for:

- Onboarding users
- Managing group-based access
- Enforcing least privilege
- Troubleshooting permission issues
- Offboarding users cleanly

All access must be controlled through **groups and permissions**, not per-user exceptions.

---

## Environment
- **Host OS:** Windows 11
- **Hypervisor:** VirtualBox
- **Guest OS:** Ubuntu Server 22.04 LTS
- **Lab VM:** Keep Lab 2 users/groups and create new ones for this scenario

---

## Roles & Access Model

| Role | Purpose | Access Summary |
|-----|--------|----------------|
| sysadmin | Full system administration | Full sudo |
| devs | Application deployment | Write to app directory, limited sudo |
| qa | Testing and verification | Read-only access to logs |
| interns | Training only | Restricted training directory |

---

## Task 1 — Create Role-Based Groups (Complete)
### Completion Date/Time - 27/01/26 12:23 AM

### User Story
As an administrator, I want role-based groups so permissions are managed consistently and securely.

### Tasks Performed / Reflection
Existing role-based groups (admins and developers) were already present from the initial Lab 2 setup, so these were reused and modified.

I used getent group to review all groups on the system. This returned a large list which got me confused. This just means that Linux also includes many pre-existing system groups in addition to administrator-defined groups. I noticed that custom user and role groups typically begin at GID 1000 and above, while system groups use lower IDs. I dont have information yet as of why but will park it for research.

To align with clearer role naming and least-privilege principles, I made the following changes:

- Renamed admins to sysadmins
- Renamed developers to devs
- Created new role groups: qas and interns

New groups were added using the groupadd command. Existing groups updated using groupmod command.

### Acceptance Criteria
- [x] Groups exist and are visible in the system
- [x] Group IDs and memberships can be verified
- [x] No users have unnecessary privileges

### Commands used for this task
```bash
getent group
sudo groupadd [groupname]
sudo groupmod -n [new-group-name] [old-group-name]
```

### Evidence
- [Check existing group](./screenshots/01-getent-group.png)
- [Add a group](./screenshots/02-group-add.png)
- [Modify Group](./screenshots/03-group-mod.png)
- [Verify updates](./screenshots/05-verify-group-update.png)

![Add a group](./screenshots/02-group-add.png)
![Modify Group](./screenshots/03-group-mod.png)
![Verify updates](./screenshots/05-verify-group-update.png)

---

## Task 2 — Onboard New Users (pending)
### Completion Date/Time - 

### User Story
As an administrator, I want new staff accounts created with correct group membership and secure defaults.

### Users
- **SuperAdmin** jove
- **Sysadmins** jove-admin modify to mark-admin (to avoid confusion)
- **Developers** alex-dev
- **QA** mika-qa
- **Interns** sam-intern

### Tasks Performed
- Add users to the system (List above) and verify that users exits
- Ensure that it Primary group is correct
- Create home directory and verify it exists
- Check and make sure users for sudo access (by user, by group)

### Acceptance Criteria
- [ ] Users exist and can log in
- [ ] Correct primary and secondary groups assigned
- [ ] Home directories exist with correct ownership
- [ ] No administrative access granted unintentionally

### Evidence
- Screenshot(s):
- Command output(s):

---

## Task 3 — Configure Shared Directories & Permissions (pending)

### User Story
As a team, we need shared directories where access is granted only to the appropriate roles.

### Directories
- **Application directory:**  
- **Log directory:**  
- **Training directory:**  

### Tasks Performed
- 
- 
- 

### Acceptance Criteria
- [ ] Dev users can write to the application directory
- [ ] QA users can read logs but cannot modify them
- [ ] Interns can only access the training directory
- [ ] Unauthorized access attempts fail

### Evidence
- Screenshot(s):
- Command output(s):

---

## Task 4 — Implement Least-Privilege Sudo Access (pending)

### User Story
As an administrator, I want developers to run limited administrative commands without granting full sudo access.

### Scope of Elevated Access
- **Allowed:**  
- **Not allowed:**  

### Tasks Performed
- 
- 
- 

### Acceptance Criteria
- [ ] `sudo -l` shows only approved commands
- [ ] Privilege escalation beyond scope is denied
- [ ] System integrity remains intact

### Evidence
- Screenshot(s):
- Command output(s):

---

## Task 5 — Incident Response: Permission Denied (pending)

### Incident Description
A developer reports receiving **“Permission denied”** while working in the application directory.

### Investigation
- **Observations:**  
- **Root cause identified:**  

### Resolution
- 
- 
- 

### Acceptance Criteria
- [ ] Root cause clearly identified
- [ ] Issue resolved without weakening security
- [ ] Least privilege preserved
- [ ] Access restored only where appropriate

### Evidence
- **Before:**  
- **After:**  

---

## Task 6 — User Offboarding & Audit (pending)

### User Story
As an administrator, I want to remove access cleanly when a staff member leaves.

### Offboarded User
- **Username:**  
- **Role:**  

### Tasks Performed
- 
- 
- 

### Acceptance Criteria
- [ ] User can no longer log in
- [ ] Group memberships updated
- [ ] No orphaned permissions remain
- [ ] Audit snapshot captured

### Evidence
- Screenshot(s):
- Command output(s):

---


## Next Steps

- 
- 
- 

---

### Notes
This lab was completed **without AI assistance**, using:
- Personal notes
- System documentation (`man`)
- Trial-and-error testing
- Research and Video tutorials
