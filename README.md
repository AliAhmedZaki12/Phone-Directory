# Phone Directory Project

This project is a simple phone directory application developed using a graphical user interface (GUI) in Java, with SQL Server as the primary database. The application allows users to easily input contact information, execute queries, and manage data using SQL.

## My Role in the Project

- I was primarily responsible for developing and creating SQL database queries, including designing tables, writing SQL code, and optimizing performance.
- Additionally, I contributed to other tasks, such as designing the user interface and integrating the application with the database, but my main focus was working with SQL.

## Features

- Input user data (first name, last name, phone number, address, email) into an SQL Server database.
- Validate email addresses to ensure correct formatting.
- Design a graphical user interface (GUI) to simplify user interaction.

## Table Structure

The following script creates the required `Users` table in the database:

```sql
CREATE TABLE Users (
    UserID INT IDENTITY(1,1) PRIMARY KEY,
    FirstName NVARCHAR(50) NOT NULL,
    LastName NVARCHAR(50) NOT NULL,
    PhoneNumber NVARCHAR(15) NOT NULL,
    Address NVARCHAR(255) NOT NULL,
    Email NVARCHAR(255) NOT NULL
);
```

## Setting Up the Project

1. Clone the repository or download the source code.
2. Update the following details in the `InsertUserData.java` file:
   - `dbURL`: Database connection string (e.g., `jdbc:sqlserver://your_server_name:1433;databaseName=your_database_name`).
   - `username`: Database username.
   - `password`: Database password.
3. Ensure the SQL Server JDBC driver is added to the project's classpath.

## How to Run the Application

1. Compile the Java file:
   ```bash
   javac InsertUserData.java
   ```
2. Run the program:
   ```bash
   java InsertUserData
   ```
3. Follow the on-screen instructions to input user details. The program will validate email addresses and insert the data into the `Users` table.
