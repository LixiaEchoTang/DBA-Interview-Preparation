`**Date:** March 13, 2025`

# 1. Database Storage Overview

## 1.1 Database Storage Overview

### Top 5 Interview Questions
- What are the main storage structures in an Oracle database?
- How does Oracle manage storage at logical and physical levels?
- What is the difference between tablespaces, segments, extents, and blocks?
- How do datafiles relate to tablespaces?
- What is the purpose of SYSTEM and SYSAUX tablespaces?

### Core Concepts
- **Logical storage structures:** Tablespaces, Segments, Extents, Blocks
- **Physical storage structures:** Datafiles, Control files, Redo logs
- SYSTEM and SYSAUX tablespaces

### Tools & Commands
- Views: `DBA_TABLESPACES`, `DBA_DATA_FILES`, `DBA_SEGMENTS`
- Example Command: `SELECT * FROM DBA_TABLESPACES;`

### Demos/Practices
- Viewing tablespace structures
- Checking storage allocation

## 1.2 Purpose of the Default Tablespaces

### Top 5 Interview Questions
- What are the default tablespaces in Oracle?
- How does the TEMP tablespace work?
- What is the purpose of the UNDO tablespace?
- How do default tablespaces impact storage?
- How do you change a user's default tablespace?

### Core Concepts
- Default tablespaces: SYSTEM, SYSAUX, TEMP, UNDO
- Temporary tablespaces and sorting
- Assigning default tablespaces to users

### Tools & Commands
- Views: `DBA_TABLESPACES`, `DBA_USERS`
- Example Command: `ALTER DATABASE DEFAULT TABLESPACE users;`

### Demos/Practices
- Viewing tablespace usage
- Changing default tablespace for a user

## 1.3 Storage of Data in Blocks

### Top 5 Interview Questions
- What is the structure of an Oracle data block?
- How does Oracle manage free space in blocks?
- What is row chaining and row migration?
- What are PCTFREE and PCTUSED?
- How does block size affect performance?

### Core Concepts
- **Data block structure:** Header, Row Data, Free Space
- **Storage parameters:** PCTFREE, PCTUSED
- Row chaining & migration

### Tools & Commands
- Views: `DBA_EXTENTS`, `DBA_SEGMENTS`
- Example Command: `SELECT * FROM DBA_SEGMENTS WHERE SEGMENT_NAME='TABLE_NAME';`

### Demos/Practices
- Viewing block usage
- Checking free space in tablespaces

## 1.4 Advantage of Deferred Segment Creation

### Top 5 Interview Questions
- What is deferred segment creation?
- How does it improve storage efficiency?
- How do you disable deferred segment creation?
- What happens when data is inserted?
- What are the trade-offs of deferred segment creation?

### Core Concepts
- Deferred vs. Immediate segment allocation
- Storage optimization

### Tools & Commands
- Views: `DBA_SEGMENTS`, `DBA_TABLES`
- Example Command: `ALTER SYSTEM SET DEFERRED_SEGMENT_CREATION = FALSE;`

### Demos/Practices
- Testing deferred segment creation
- Checking segment allocation

# 2. Creating and Managing Tablespaces

## 2.1 Creating and Managing Tablespaces

### Top 5 Interview Questions
- How do you create a new tablespace in Oracle?
- What is the difference between permanent, temporary, and undo tablespaces?
- How do you resize a tablespace?
- What is a bigfile tablespace?
- How do you drop a tablespace?

### Core Concepts
- Tablespace types: Permanent, Temporary, Undo
- Autoextend and resizing

### Tools & Commands
- Commands: `CREATE TABLESPACE`, `ALTER DATABASE`
- Example Command: `ALTER DATABASE DATAFILE 'filename.dbf' RESIZE 500M;`

### Demos/Practices
- Creating and resizing tablespaces

## 2.2 Viewing Tablespace Information

### Top 5 Interview Questions
- How can you check tablespace usage?
- How do you monitor free space?
- What views provide tablespace details?
- How do you find fragmented tablespaces?
- How do you prevent tablespace overuse?

### Core Concepts
- Monitoring tablespace usage
- Tablespace fragmentation

### Tools & Commands
- Views: `DBA_FREE_SPACE`, `DBA_TABLESPACES`
- Example Command: `SELECT * FROM DBA_TABLESPACES;`

### Demos/Practices
- Running SQL queries to check usage

# 3. Improving Space Usage

## 3.1 Space Management Features

### Top 5 Interview Questions
- What is ASSM and MSSM?
- How does Oracle reclaim space?
- What is tablespace fragmentation?
- What is locally managed vs. dictionary-managed tablespaces?
- How do you prevent space allocation issues?

### Core Concepts
- Automatic segment space management
- Reclaiming unused space

### Tools & Commands
- Views: `DBA_SEGMENTS`, `DBA_FREE_SPACE`
- Example Command: `ALTER TABLESPACE COALESCE;`

### Demos/Practices
- Monitoring fragmentation
- Running tablespace coalescing

## 3.2 Creating Global Temporary Tables

### Top 5 Interview Questions
- What are global temporary tables?
- How does Oracle manage session-specific data?
- What is the difference between temporary and permanent tables?
- How do you ensure data isolation?
- When should you use temporary tables?

### Core Concepts
- Global Temporary Tables (GTTs)
- Session vs. Transaction scope

### Tools & Commands
- Command: `CREATE GLOBAL TEMPORARY TABLE`
- View: `DBA_TEMP_TABLES`

### Demos/Practices
- Creating and using temporary tables

## 3.3 Using Compression

### Top 5 Interview Questions
- What types of compression does Oracle support?
- How does compression impact performance?
- What is Hybrid Columnar Compression (HCC)?
- When should you use OLTP vs. Archive compression?
- How does compression affect redo logs?

### Core Concepts
- Table, Index, and Tablespace compression
- Performance considerations

### Tools & Commands
- Command: `ALTER TABLE ... COMPRESS;`
- View: `DBA_TABLES`

### Demos/Practices
- Enabling compression

# 4. Managing Undo Data

## 4.1 Managing the Undo

### Top 5 Interview Questions
- What is the purpose of the undo tablespace in Oracle?
- What is the difference between undo and redo?
- How do you monitor undo tablespace usage?
- How do you configure automatic undo management?
- What happens if the undo tablespace runs out of space?

### Core Concepts
- Undo vs. Redo
- Undo retention policies
- Automatic Undo Management (AUM)

### Tools & Commands
- Views: `DBA_UNDO_EXTENTS`, `V$UNDOSTAT`
- Example Command: `ALTER DATABASE SET UNDO TABLESPACE undo_ts;`

### Demos/Practices
- Viewing undo segment usage
- Configuring undo tablespaces

## 4.2 Enabling Temporary Undo

### Top 5 Interview Questions
- What is temporary undo in Oracle?
- How does temporary undo help with performance?
- How do you enable temporary undo for a PDB?
- What is the impact of using temporary undo?
- How do you monitor temporary undo usage?

### Core Concepts
- Temporary Undo for PDBs
- Undo tablespace efficiency

### Tools & Commands
- Views: `DBA_TEMP_FREE_SPACE`, `V$TEMPSEG_USAGE`
- Example Command: `ALTER DATABASE SET TEMP_UNDO_ENABLED = TRUE;`

### Demos/Practices
- Enabling and testing temporary undo

# 5. Creating and Managing User Accounts

## 5.1 Creating and Managing User Accounts

### Top 5 Interview Questions
- How do you create a user in Oracle?
- What is the difference between a common user and a local user in a CDB?
- How do you manage user authentication?
- How do you drop a user safely?
- How do you assign a default tablespace to a user?

### Core Concepts
- User authentication methods (password, OS, external)
- User privileges and roles

### Tools & Commands
- Commands: `CREATE USER`, `ALTER USER`
- View: `DBA_USERS`

### Demos/Practices
- Creating users
- Assigning tablespaces

## 5.2 Assigning Quotas

### Top 5 Interview Questions
- What is a quota in Oracle?
- How do you limit user storage in a tablespace?
- How do you view user quotas?
- How do quotas impact space management?
- Can you set quotas for SYSTEM tablespaces?

### Core Concepts
- Quotas in user management
- Preventing overuse of storage

### Tools & Commands
- View: `DBA_TS_QUOTAS`
- Example Command: `ALTER USER username QUOTA 500M ON users;`

### Demos/Practices
- Setting and verifying quotas

# 6. Configuring Privileges and Roles Authorization

## 6.1 Configuring Privileges and Roles

### Top 5 Interview Questions
- What is the difference between system and object privileges?
- How do roles help in user management?
- How do you create and grant a role?
- How do you revoke privileges from a user?
- What is the minimum privilege required to create a session?

### Core Concepts
- System vs. Object privileges
- Role-based access control

### Tools & Commands
- Commands: `GRANT`, `REVOKE`
- Views: `DBA_SYS_PRIVS`, `DBA_ROLE_PRIVS`

### Demos/Practices
- Creating roles
- Assigning privileges

# 7. Configuring User Resource Limits

## 7.1 Configuring User Resource Limits

### Top 5 Interview Questions
- How do you limit the number of sessions per user?
- What is a profile in Oracle?
- How do you enforce password complexity?
- How do you check the current resource limits?
- What happens if a user exceeds their resource limits?

### Core Concepts
- Profiles and resource limits
- Password policies

### Tools & Commands
- View: `DBA_PROFILES`
- Example Command: `ALTER PROFILE my_profile LIMIT PASSWORD_LIFE_TIME 30;`
- Command: `CREATE PROFILE my_profile LIMIT PASSWORD_LIFE_TIME 30;`

### Demos/Practices
- Creating and assigning profiles

# 8. Implementing Oracle Database Auditing

## 8.1 Implementing Auditing

### Top 5 Interview Questions
- What is unified auditing?
- How do you enable and configure auditing?
- How do you view audit logs?
- What are common use cases for database auditing?
- How do you audit specific user actions?

### Core Concepts
- Unified Auditing
- Enabling standard auditing

### Tools & Commands
- Commands: `AUDIT`
- View: `DBA_AUDIT_TRAIL`
- Example Command: `ALTER SYSTEM SET AUDIT_TRAIL = DB;`

### Demos/Practices
- Enabling and checking audit logs

# 9. Loading and Transporting Data

## 9.1 Loading Data

### Top 5 Interview Questions
- What are the different methods to load data into Oracle?
- What is the difference between SQL*Loader and Data Pump?
- How do you load data from an external file?
- What are external tables?
- How do you monitor data load performance?

### Core Concepts
- SQL*Loader vs. Data Pump
- External Tables

### Tools & Commands
- Tools: SQL*Loader, `DBMS_DATAPUMP`
- Example Command: `CREATE DIRECTORY ext_dir AS '/datafiles';`

### Demos/Practices
- Loading data using SQL*Loader
- Creating an external table

# 10. Transporting Data

## 10.1 Transporting Tablespaces

### Top 5 Interview Questions
- What is a transportable tablespace?
- How do you export and import a transportable tablespace?
- What are the benefits of transportable tablespaces?
- What are the limitations of transportable tablespaces?
- How do you handle cross-platform tablespace transport?

### Core Concepts
- Transportable Tablespaces (TTS)
- Cross-platform data migration

### Tools & Commands
- Tools: `EXPDP`, `IMPDP`
- View: `DBA_TABLESPACES`

### Demos/Practices
- Exporting and importing a tablespace

# 11. Using External Tables

## 11.1 Using External Tables for Data Transport

### Top 5 Interview Questions
- What is an external table?
- How do external tables differ from regular tables?
- What are the performance considerations for external tables?
- How do you create an external table?
- How do you query and unload data using external tables?

### Core Concepts
- External tables as a data transfer mechanism
- Querying data without loading it into the database

### Tools & Commands
- Command: `CREATE EXTERNAL TABLE`
- Tool: `DBMS_EXTERNAL`

### Demos/Practices
- Creating an external table
- Querying external data
