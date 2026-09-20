# Oracle Pluggable Databases (PDB) Management - Assignment II

## Overview of Tasks
This repository contains the practical completion and technical documentation for INSY 8311 Assignment II.

- **Task 1:** Created a new Pluggable Database (`se_pdb_20251SEN137`), opened it in `READ WRITE` mode, and created a dedicated PDB user (`senga_plsqlauca_20251SEN137`)[cite: 1, 3].
- **Task 2:** Created a temporary Pluggable Database (`se_to_delete_pdb_20251SEN137`) and completely dropped it including its datafiles[cite: 1, 3].
- **Task 3:** Accessed and verified the environment status via Oracle Enterprise Manager (OEM) Express Dashboard.

---

## Oracle Environment Used
- **Database Version:** Oracle Database 21c Enterprise Edition (Release 21.3.0.0.0)[cite: 4, 6]
- **Operating System:** Microsoft Windows x86 64-bit[cite: 4, 6]
- **Architecture:** Multitenant Container Database (CDB)[cite: 4, 6]

---

## Technical Tasks & Evidence

### Task 1: Create a New Pluggable Database & User
1. Created PDB `se_pdb_20251SEN137` from `PDBSEED`[cite: 1, 3].
2. Opened `se_pdb_20251SEN137` in `READ WRITE` mode[cite: 1, 3].
3. Created user `senga_plsqlauca_20251SEN137` inside the PDB and granted necessary privileges[cite: 1, 3].

#### Evidence:
![PDB Creation & User Setup](screenshots/pdb_creation/task1_create_pdb.png)

---

### Task 2: Create and Delete a Temporary PDB
1. Created temporary PDB `se_to_delete_pdb_20251SEN137`[cite: 1, 3].
2. Dropped `se_to_delete_pdb_20251SEN137` including datafiles[cite: 1, 3].
3. Verified remaining PDBs using `SHOW PDBS;`[cite: 1, 3].

#### Evidence:
![PDB Deletion Verification](screenshots/pdb_deletion/task2_drop_temp_pdb.png)

---

### Task 3: Oracle Enterprise Manager (OEM) Setup
Accessed the OEM Express interface at `https://localhost:5500/em` to verify system status and active PDB containers[cite: 3, 4].

#### Evidence:
![OEM Dashboard](screenshots/oem_dashboard/oem_dashboard.png)

---

## Challenges Faced & Solutions
- **ORA-65005 (Missing/Invalid File Name Pattern):** Encountered during PDB creation on Windows[cite: 1]. Solved by explicitly specifying Windows absolute file paths[cite: 1].
- **ORA-01920 (User Name Conflict):** Resolved by ensuring clean execution environment before user privilege assignments[cite: 1].

---

## Academic Integrity Statement
I declare that this assignment represents my own individual work. All commands, screenshots, and repository setup were performed independently without unauthorized collaboration or prohibited tool usage.

---

## Submission Details
- **Repository Link:** https://github.com/aphroseng/oracle_pdb_ass_II_20251SEN137_senga[cite: 3, 9]
- **PDB Name Created:** se_pdb_20251SEN137[cite: 1, 3]
- **Issues Encountered:** Yes (Windows path conversion ORA-65005, resolved via exact Windows file path strings)[cite: 1, 3]
