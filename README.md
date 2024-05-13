# Library Database System Project

## Project Overview

This task demonstrates the creation of a comprehensive database system based on a client brief for a library. The objective is to design and implement a database system that manages member information, library catalog, loan history, and overdue fine repayments.

## Client Brief

### Client Requirements

1. **Member Information**:
   - Full name, address, date of birth, username, and password are required.
   - Optional information: email address and telephone number.
   - Track total overdue fines, repaid amounts, and outstanding balances.
   - Retain information of former members for marketing, including the date membership ended.
   - Members can sign up and log in online.

2. **Overdue Fines Repayment**:
   - Record repayment details: date/time, amount, and method (cash or card).

3. **Library Catalogue**:
   - Item details: title, type (Book, Journal, DVD, Other Media), author, publication year, date added, current status (On Loan, Overdue, Available, Lost/Removed).
   - Record ISBN for books.
   - Record the date when an item is identified as lost or removed.

4. **Loan History**:
   - Record each loan with member, item, loan date, due date, and return date (NULL if not returned).
   - Calculate overdue fees at a rate of 10p per day.
   - Ensure data integrity and avoid data loss.

## Task Details

### Database Design and Implementation

1. **Normalization**:
   - Design and normalize the database to 3NF.
   - Provide T-SQL statements for creating tables and views.
   - Highlight primary and foreign keys.
   - Justify data types and constraints.
   - Include a database diagram.
   - Document any additional assumptions.

2. **Stored Procedures and Functions**:
   - Search the catalog by title, sorted by the most recent publication date.
   - List items on loan due in less than five days.
   - Insert new member records.
   - Update existing member details.

3. **Views**:
   - Create a view to display loan history, including borrowed items, borrow dates, due dates, and associated fines.

4. **Triggers**:
   - Automatically update item status to Available when returned.

5. **Queries**:
   - Provide a function, view, or query to identify the total number of loans on a specified date.

6. **Data Insertion**:
   - Insert test records to validate the functionality of the database, including SELECT queries, functions, procedures, and triggers.

7. **Additional Objects**:
   - Provide additional relevant views, procedures, functions, or triggers with explanations of their functionality for higher marks.

### Client Guidance

1. **Data Integrity and Concurrency**:
   - Ensure accurate and consistent data across the database.
   - Manage simultaneous data access without conflicts.

2. **Database Security**:
   - Implement measures to protect data from unauthorized access and breaches.

3. **Database Backup and Recovery**:
   - Develop strategies for data backup and recovery to prevent data loss.

### Required Elements for Higher Marks

- Use views, stored procedures, system functions, user-defined functions, triggers, and SELECT queries with joins and sub-queries.

## Conclusion

This project outlines the development of a robust library database system that meets the specified requirements, ensuring data integrity, security, and efficient management of library operations. The detailed T-SQL implementation, supported by a comprehensive report, demonstrates the ability to transform client needs into a functional database system.
