# Oracle DBA "What If" Scenarios Interview Questions & Insights

## Types of “What If” Scenarios

- [**Top Oracle Error Codes** that Oracle DBA often encounter (‘ORA-’)](#top-oracle-error-codes-that-oracle-dba-often-encounter-ora-)
- **Performance and Resource Management Scenarios:** Slow running queries, memory or CPU bottlenecks, high redo log or I/O activity.
- **Availability and Recovery Scenarios:** Data file corruption or loss, unexpected database shutdown or crash, backup and restore failures.
- **Security and Access Control Scenarios:** Unauthorized access or data breach, SQL injection or vulnerability exploits.
- **Configuration and Infrastructure Changes Scenarios:** Database upgrade or patch failure, migration to new hardware or cloud environment.
- **Operational Anomalies and Maintenance Scenarios:** Locking and concurrency issues, “Snapshot Too Old” errors.

---

## How to Approach These Scenarios

For each “what if” scenario, your interview response should ideally:

- **Identify the Symptom:** Clearly state what the error or issue is.
- **Outline a Diagnostic Plan:** Mention the tools or logs you would use (e.g., AWR, alert logs, SQL Trace).
- **Propose a Resolution:** Explain step-by-step how you would resolve the issue and prevent it from reoccurring.
- **Discuss Preventive Measures:** Address how regular monitoring, capacity planning, or best practices in configuration can mitigate these issues.

---

## Top Oracle Error Codes That Oracle DBA Often Encounter (‘ORA-’)
<!-- Anchor: top-oracle-error-codes-that-oracle-dba-often-encounter-ora- -->

### Connection & Authentication Errors
- **ORA-01017:** Invalid username/password; logon denied.
- **ORA-27101:** Shared memory realm does not exist – typically occurs when attempting to connect to an instance that is not started.
- **ORA-01031:** Insufficient privileges (raised when a user lacks the necessary permissions to perform an operation).
- **ORA-01034:** Oracle not available.
- **ORA-12154:** TNS: could not resolve the connect identifier specified.
- **ORA-12541:** TNS: no listener.
- **ORA-12514:** TNS: listener does not currently know of service requested.
- **ORA-12505:** TNS: listener does not currently know of SID given in connect descriptor.
- **ORA-12519:** TNS: no appropriate service handler found.
- **ORA-12560:** TNS: protocol adapter error (often related to issues with Oracle services or network configuration).

### SQL & Syntax Errors
- **ORA-00904:** Invalid identifier.
- **ORA-01008:** Not all variables bound.
- **ORA-01830:** Date format picture ends before converting entire input string.
- **ORA-00907:** Missing right parenthesis.
- **ORA-00911:** Invalid character – usually caused by an unsupported or extra character in a SQL statement.
- **ORA-00932:** Inconsistent datatypes (occurs when there is a mismatch in expected data types in SQL operations).
- **ORA-00933:** SQL command not properly ended.
- **ORA-00936:** Missing expression.
- **ORA-00984:** Column not allowed here.
- **ORA-00918:** Column ambiguously defined.
- **ORA-01461:** Cannot bind a LONG value.
- **ORA-02010:** Specified argument is not supported.
- **ORA-01722:** Invalid number (typically occurs when a conversion from character to number fails in SQL).

### Resource & Performance Errors
- **ORA-01555:** Snapshot too old (often occurs during long-running queries with undo issues).
- **ORA-04030:** Out of process memory (indicates memory allocation issues, often related to resource constraints).
- **ORA-00054:** Resource busy and acquire with NOWAIT specified or timeout expired.
- **ORA-00257:** Archiver error – indicates that the archive log destination is full or unavailable, halting database operations.
- **ORA-04031:** Unable to allocate memory in the shared pool (indicates memory allocation issues).
- **ORA-01652:** Unable to extend temp segment (indicates issues with temporary tablespace space).
- **ORA-01000:** Maximum open cursors exceeded.

### Communication & Process Errors
- **ORA-03113:** End-of-file on communication channel.
- **ORA-03114:** Not connected to Oracle.
- **ORA-12537:** TNS: connection closed.
- **ORA-03135:** Connection lost contact.

### PL/SQL & Trigger Errors
- **ORA-01403:** No data found – often encountered in PL/SQL when a SELECT INTO statement returns no rows.
- **ORA-06508:** PL/SQL: could not find program unit being called.
- **ORA-04063:** Package has been changed (indicates that a PL/SQL package or related object is invalid and may need recompilation).
- **ORA-20001:** User-defined error (commonly raised via RAISE_APPLICATION_ERROR).
- **ORA-01422:** Exact fetch returns more than the requested number of rows (often encountered in PL/SQL SELECT INTO statements).
- **ORA-20000:** User-defined error (commonly raised in PL/SQL code using RAISE_APPLICATION_ERROR).
- **ORA-04098:** Trigger is invalid and failed re-validation.
- **ORA-06512:** Indicates the line number in PL/SQL code where the error occurred.

### Constraint & Data Integrity Errors
- **ORA-00001:** Unique constraint violated.

### Other / Internal Errors
- **ORA-00600:** Internal error code (this is a generic error indicating an internal problem within the Oracle database engine).
- **ORA-00604:** Error occurred at recursive SQL level (an internal error that often propagates from a lower-level issue).
- **ORA-01110:** Error on file (provides file-specific details for further diagnosis).
