# Open Source Software Audit - Git

**Student Name:** Shourya Bharadwaj  
**Roll Number:** 24BAC10051
**Course Name:** Open Source Software  
**Chosen Software:** Git

## Project Overview

This project is an audit and exploration of **Git**, the world's most popular distributed version control system. It demonstrates a practical understanding of Git's open-source nature (licensed under GPL v2) and its footprint on a Linux environment. The repository includes a set of Bash shell scripts to audit the system, inspect FOSS packages, analyze logs, and dynamically generate an open-source manifesto.

## Directory Structure

```
oss-audit-24bac10051/
├── README.md                           # This file
├── script1\\\_system\\\_identity.sh          # Outputs basic Linux OS and user info
├── script2\\\_package\\\_inspector.sh        # Checks for Git and other FOSS software
├── script3\\\_disk\\\_auditor.sh             # Scans directory sizes and permissions
├── script4\\\_log\\\_analyzer.sh             # Simple parser for finding keywords in logs
├── script5\\\_manifesto\\\_generator.sh      # Interactive script to make a personalized manifesto
└── report\\\_notes/
    └── report\\\_support\\\_pack.md          # Notes, viva prep, and screenshots checklist for the PDF report
```

## Included Shell Scripts

### 1\. System Identity Report (`script1\\\_system\\\_identity.sh`)

Displays the current Linux distribution in use, kernel version, logged-in user details, and system uptime. It includes a brief note about Linux's GPL licensing.

### 2\. FOSS Package Inspector (`script2\\\_package\\\_inspector.sh`)

Checks if Git is installed on the system using `dpkg`/`apt` or `which`. It displays the installed version and gives a quick overview of Git's purpose and its primary license.

### 3\. Disk and Permission Auditor (`script3\\\_disk\\\_auditor.sh`)

Loops over crucial Linux directories (like `/etc`, `/var/log`, `/home`) to report their size and permissions. It also checks if the global Git config (`\\\~/.gitconfig`) exists.

### 4\. Log File Analyzer (`script4\\\_log\\\_analyzer.sh`)

A utility script that reads any log file line-by-line. Provide a log file and optionally a keyword (defaults to "error"). It returns the number of matches and the last few matching lines.

### 5\. Open Source Manifesto Generator (`script5\\\_manifesto\\\_generator.sh`)

An interactive script. It asks you a few simple questions about your tech interests and generates a customized text file (`manifesto\\\_<username>.txt`) detailing your personal open-source philosophy.

## How to Run the Scripts on Ubuntu/Linux

**Step 1: Make scripts executable**
Before running any script for the first time, you must give it execute permissions:

```bash
chmod +x script\\\*.sh
```

**Step 2: Execute the scripts**
Run each script using `./`:

```bash
./script1\\\_system\\\_identity.sh
./script2\\\_package\\\_inspector.sh
./script3\\\_disk\\\_auditor.sh
./script4\\\_log\\\_analyzer.sh /var/log/dpkg.log
./script5\\\_manifesto\\\_generator.sh
```

**Dependencies**

* A standard Linux environment (Ubuntu/Debian recommended)
* `Bash` shell
* Standard pre-installed utilities: `awk`, `du`, `grep`, `dpkg` (for Debian-based distros)

\---

*Created for the Open Source Software capstone assignment.*

