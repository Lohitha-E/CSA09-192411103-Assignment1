# CSA09 – Programming in Java
## Assignment 5 – CO5: Data Persistence Engineering – Files and Databases
### Student Details
- **Student Name:** E. LOHITHA
- **Register Number:** 192411103
- **Course / Section:** CSA09 – JAVA PROGRAMMING
- **JDK Version:** OpenJDK 21
- **MySQL Version:** MySQL 8.0.42
- **GitHub Repository:** [CSA09-192411103-Assignment1](https://github.com/Lohitha-E/CSA09-192411103-Assignment1)

## Project Overview

This project demonstrates Java persistence techniques using files and relational databases. It covers binary file formats, buffered I/O, the DAO pattern, object serialization, transactions, file-backed storage, SQL injection prevention, JDBC batching and migration from legacy files.

## Requirements

- OpenJDK 21
- MySQL Server 8.0.42
- MySQL Connector/J compatible with the installed JDK and server
- A terminal or Java IDE with `java` and `javac`
- MySQL Workbench or the MySQL command-line client (recommended)

## Project Structure

```text
CSA09-Assignment5/
├── Task01_FileFormat/       # Binary and text file formats
├── Task02_BufferedIO/       # Buffered/unbuffered file processing
├── Task03_DAO/              # DAO and CRUD operations
├── Task04_Serialization/    # Java object serialization
├── Task05_Transactions/     # Commit and rollback
├── Task06_FileStore/        # File-backed record storage
├── Task07_Security/         # SQL security and PreparedStatement
├── Task08_JDBC_Batch/       # JDBC batch operations and schema.sql
├── Task09_Migration/        # Legacy-file migration
├── Evidence/                # Screenshots, benchmark data and notes
└── README.md
```

The exact filenames may vary in the final project. Keep each task's source code, input files and notes in its corresponding folder.

## Compile and Run Java Tasks

Check the installed JDK version:

```bash
java -version
javac -version
```

Open a terminal in the required task folder, compile the Java source files and run the class containing the `main` method.

Example:

```bash
javac *.java
java BinaryPassFormat
```

Replace `BinaryPassFormat` with the actual main class for that task. If the code uses Java packages, compile and run it from the project root using its package-qualified class name.

## MySQL and JDBC Setup

### Step 1: Start MySQL Server

Start your MySQL Server and connect using MySQL Workbench or the MySQL command-line client.

### Step 2: Create the Database

```sql
CREATE DATABASE csa09_assignment5;
```

Select the database:

```sql
USE csa09_assignment5;
```

### Step 3: Execute the SQL Schema

Execute the supplied schema file, adjusting the path if necessary:

```bash
mysql -u YOUR_USERNAME -p csa09_assignment5 < Task08_JDBC_Batch/schema.sql
```

Alternatively, open the SQL file in MySQL Workbench and execute it.

### Step 4: Configure JDBC

- Add the MySQL Connector/J JAR to the Java classpath.
- Configure the JDBC URL, username and password locally.
- Do not upload real database credentials to GitHub.
- Run the JDBC programs and verify their results using SQL `SELECT` queries.

Example JDBC classpath:

```bash
javac -cp ".:mysql-connector-j-<version>.jar" *.java
java -cp ".:mysql-connector-j-<version>.jar" YourMainClass
```

On Windows, use `;` instead of `:` as the classpath separator.

## Assignment Task Guide

| Task | Topic | Verification |
|---|---|---|
| A1 / Task01 | Binary and text file formats | Write and read a record; inspect version and encoded fields. |
| A2 / Task02 | Buffered I/O | Confirm line counts and compare timings at multiple file sizes. |
| A3 / Task03 | DAO pattern | Insert, find, update and delete records. |
| A4 / Task04 | Serialization | Serialize and restore an object; inspect transient fields. |
| A5 / Task05 | Transactions | Verify commit and forced-failure rollback. |
| B1 / Task06 | File store | Test valid, missing, malformed and route-filtered records. |
| B2 / Task07 | SQL security | Compare unsafe SQL with PreparedStatement using a disposable database. |
| B3 / Task08 | JDBC and batching | Verify rows, metadata, batch behavior, rollback and timings. |
| B4 / Task09 | Migration | Reconcile source, loaded and rejected records; inspect metadata. |

## Evidence and Screenshots

The project report includes screenshots demonstrating task outputs.

**Important:** Some report screenshots may be genuine local Java execution captures, while database-task images marked **SIMULATED** are illustrative examples only. They are not proof of execution against a live MySQL server.

Before submission:

- Run the DAO, transaction, security, JDBC batch and migration tasks against your own MySQL test database.
- Replace simulated images with screenshots captured from those actual runs if live evidence is required.
- Record real benchmark timings. Do not present sample values as actual measurements.
- Use synthetic test data and keep passwords and other secrets out of screenshots.

## Benchmarking Guidance

For reliable performance comparisons:

1. Use the same machine, schema, indexes, generated data, transaction settings and database instance.
2. Warm up the JVM before measuring.
3. Run each test at least three times.
4. Report the median execution time.
5. Record the JDK, operating system, CPU/RAM, MySQL version and Connector/J version.

Performance results depend on the execution environment.

## GitHub Repository

Initialize Git and upload the project using the following commands:

```bash
git init
git add .
git commit -m "Add Assignment 5 persistence tasks"
```

Make meaningful commits as tasks are completed.

Confirm that the final repository contains:

- Java source files
- SQL schema files
- README.md
- Evidence and screenshots
- Assignment report
- Required project files

Do not commit database credentials, private keys or unnecessary compiled `.class` files.

**GitHub Repository:**  
[https://github.com/Lohitha-E/CSA09-192411103-Assignment1](https://github.com/Lohitha-E/CSA09-192411103-Assignment1)

## Final Submission Checklist

- [ ] Student details and GitHub repository URL are completed.
- [ ] Java source files compile and run using OpenJDK 21.
- [ ] MySQL 8.0.42 database is configured.
- [ ] MySQL schema and JDBC connection are configured.
- [ ] Database tasks have been run and verified.
- [ ] Simulated screenshots are replaced with genuine evidence where required.
- [ ] Benchmark values are actual measurements.
- [ ] No credentials or private information are committed.
- [ ] Report, source folders, README and ZIP package are consistent.

## Academic Integrity Note

Only claim tests, screenshots, database operations or performance measurements that you have actually executed and verified.

---

**Course:** CSA09 – Programming in Java  
**Assignment:** Assignment 5 – CO5  
**Student:** E. LOHITHA  
**Register Number:** 192411103
