# Linux File Permissions Management

##  Project Overview

This project demonstrates how to **inspect, understand, and modify file and directory permissions in Linux** using commands such as `ls -la` and `chmod`. The goal is to ensure that files and directories have the **correct level of authorization** to improve system security.

The scenario is based on a research organization that needed to **audit and fix insecure permissions** inside a `projects` directory.

## Skills Demonstrated

* Using `ls -la` to inspect file and directory permissions
* Understanding Linux permission strings (`rwxrwxrwx`)
* Modifying permissions using `chmod`
* Managing permissions for:

  * Regular files
  * Hidden files
  * Directories
* Applying **principle of least privilege** for security

## What Was Done

### 1. Checked File and Directory Permissions

Used:

```bash
ls -la
```

To display all files (including hidden ones) and inspect their permission strings.

### 2. Interpreted Permission Strings

Example:

```bash
-rw-rw-r--
```

Explained:

* File type
* User permissions
* Group permissions
* Other permissions

---

### 3. Modified File Permissions

* Removed write access from **others** on certain files:

```bash
chmod o-w project_k.txt
```

---

### 4. Secured a Hidden File

* Removed write access from user and group
* Ensured only read access remained:

```bash
chmod u-w,g-w,g+r .project_x.txt
```

---

### 5. Secured a Directory

* Removed execute permissions from the group so **only one user** can access it:

```bash
chmod g-x drafts
```

---

##  Why This Matters

Incorrect file permissions can:

* Allow unauthorized file modification
* Expose sensitive data
* Create serious security risks

This project shows how to **lock down a Linux system properly** using correct permission management.

##  Tools Used

* Linux Terminal
* `ls`
* `chmod`

## Outcome

All files and directories now follow the organization’s **security policy** and only authorized users can access or modify sensitive data.
