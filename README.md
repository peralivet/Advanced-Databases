# Library Database System Project

## Project Overview

This task demonstrates the creation of a comprehensive database system based on a client brief for a library. The objective is to design and implement a database system that manages member information, library catalog, loan history, and overdue fine repayments.

### Project Brief

Imagine you are employed as a database developer consultant for a library. They are currently in the process of developing a new database system which they require for storing information on their members, their library catalogue, loan history, and overdue fine repayments. In your initial consultation with the library, you have gathered the information below. Please read the below carefully and continue to the task description.

### Client Requirements

1. **Member Information**:
   - When a member joins the library, they need to provide their full name, address, date of birth, and they must create a username and password to allow them to sign into the member portal.
   - Optionally, they can also provide an email address and telephone number.
   - Members are charged a fine if they have overdue books and the library has to keep track of the total overdue fines owed by an individual, how much they have repaid, and the outstanding balance.
   - When a member leaves, the library wants to retain their information on the system so they can continue marketing to them, but they should keep a record of the date the membership ended.
   - Members can sign up and login online.

2. **Overdue Fines Repayment**:
   - When a member has overdue fines, they can repay some or all the overdue fines. Each repayment needs to be recorded, along with the date/time of the repayment, the amount repaid, and the repayment method (cash or card).

3. **Library Catalogue**:
   - The library has a catalogue of items. For each they have an item title, item type (which is classified as either a Book, Journal, DVD, or Other Media), author, year of publication, date the item was added to the collection, and current status (which is either On Loan, Overdue, Available, or Lost/Removed).
   - If the item is identified as being lost or removed from the collection, the library will record the date this was identified.
   - If the item is a book, they will also record the ISBN.

4. **Loan History**:
   - The library wants to also keep a record of all current and past loans. Each loan should specify the member, the item, the date the item was taken out, the date the item is due back, and the date the item was actually returned (this will be NULL if the item is still out).
   - If the item is overdue, an overdue fee needs to be calculated at a rate of 10p per day.
   - The library processes hundreds of loans a day and details of the items on loan are business critical for them, so they need to avoid data loss if their systems go down. However, if their systems are down for a couple of hours, they think this isn’t too much of an issue for them.

### Task Details

As the database consultant, you are required to design the database system based on the information provided above, along with a number of associated database objects, such as stored procedures, user-defined functions, views, and triggers. Your submission will take the form of working T-SQL statements required for the steps outlined below, a backup of the database created, and a report explaining and justifying your design decisions, and the process you followed to complete the tasks. You should include screenshots and the T-SQL statements within the report itself.

1. **Database Design and Normalization**:
   - You should design and normalise your proposed database into 3NF, fully explaining and justifying your database design decisions and documenting the process you have gone through to implement this design using T-SQL statements in Microsoft SQL Server Management Studio, using screenshots to support your explanation.
   - All tables and views must be created using T-SQL statements, which should be included in your report.
   - Clearly highlight which column(s) are primary keys or foreign keys.
   - Explain the data type used for each column and justify the reason for choosing this.
   - Consider using constraints when creating your database to help ensure data integrity.
   - Include a database diagram as part of your submission.
   - If you have made any additional assumptions aside from the information above when designing your database, you should clearly state these.

2. **Stored Procedures and User-Defined Functions**:
   - The library also requires stored procedures or user-defined functions to do the following things:
     - a) Search the catalogue for matching character strings by title. Results should be sorted with most recent publication date first. This will allow them to query the catalogue looking for a specific item.
     - b) Return a full list of all items currently on loan which have a due date of less than five days from the current date (i.e., the system date when the query is run).
     - c) Insert a new member into the database.
     - d) Update the details for an existing member.

3. **Views**:
   - The library wants to be able to view the loan history, showing all previous and current loans, and including details of the item borrowed, borrowed date, due date, and any associated fines for each loan. You should create a view containing all the required information.

4. **Triggers**:
   - Create a trigger so that the current status of an item automatically updates to Available when the book is returned.

5. **Queries**:
   - You should provide a function, view, or SELECT query which allows the library to identify the total number of loans made on a specified date.

6. **Data Insertion**:
   - So that you can demonstrate the database to the client you should insert some records into each of the tables (you only need to add a small number of rows to each, however, you should also ensure the data you input allows you to adequately test that all SELECT queries, user-defined functions, stored procedures, and triggers are working as you expect).

7. **Additional Database Objects**:
   - If there are any other database objects such as views, stored procedures, user-defined functions, or triggers which you think would be relevant to the library given the brief above, you will obtain higher marks for providing these along with an explanation of their functionality.

### Report Guidelines

Within your report, you will also need to provide your client with advice and guidance on:
- Data integrity and concurrency
- Database security
- Database backup and recovery

Generic information on these topics, which is not applied to the given scenario, is likely to score poorly.

To get more than a satisfactory mark, you must use all of the below at least once in your database:
- Views
- Stored procedures
- System functions and user-defined functions
- Triggers
- SELECT queries which make use of joins and sub-queries


## Conclusion

This project outlines the development of a robust library database system that meets the specified requirements, ensuring data integrity, security, and efficient management of library operations. The detailed T-SQL implementation, supported by a comprehensive report, demonstrates the ability to transform client needs into a functional database system.

The database report file contains the report for this project while the Peter-Adepoju_sql.sql file contains the SQL codes
