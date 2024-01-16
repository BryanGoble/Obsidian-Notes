---
tags:
  - SQL_Injection
---
# SQL

**Structured query language (SQL)** is essential for working with relational databases and building dynamic websites. Even if you've never explicitly used SQL before, chances are you frequently interact with databases. Whether you're checking your bank account balance online, browsing through products on an e-commerce website, or posting a status on social media, you're indirectly querying and altering databases. SQL is one of the most popular languages that make this all possible.

Relational databases are structured data collections organised into tables, each consisting of various rows and columns. Within these collections, tables are interconnected with predefined relationships, facilitating efficient data organisation and retrieval. For example, an e-commerce relational database might include tables for "**customers**", "**orders**", and "**products**", with relationships defined to link customer information to their respective orders through the use of identifiers:

![A diagram illustrating three different tables within a relational database. Table 1 is titled Customers and contains the UUID column titled customer_id. This column is linked to the Customer column in the second table, titled Orders. A column in the Orders table is titled product_ordered, and links to the product_id column in the third table titled Products. Linking these three tables together illustrates how the unique ID from one table can be intrinsically linked to a relational column in another table. This is the foundation of how relational databases operate.](https://tryhackme-images.s3.amazonaws.com/user-uploads/6490641ea027b100564fe00a/room-content/9a00fbbf82f94bf2267da26f242576d8.svg)

SQL provides a rigid way to **query**, **insert**, **update**, and **delete** the data stored in these tables, allowing you to retrieve and alter databases as needed. A website or application that relies on a database must dynamically generate **SQL queries** and send them to the database engine to fetch or update the necessary data. The syntax of SQL queries is based on English and consists of structured commands using keywords like **SELECT**, **FROM**, **WHERE**, and **JOIN** to express operations in a natural, language-like way.

We'll leverage an example of a database table to represent the tracking and cataloguing of Christmas tree ornaments. The table and column structure might look something like this:

|ornament_id|elf_id|colour|category|material|date_created|price|
|---|---|---|---|---|---|---|
|1|124|Red|Ball|Glass|2023-12-04|5.99|
|2|116|Gold|Star|Metal|2023-12-04|7.99|
|3|102|Green|Tree|Wood|2023-12-05|3.99|
|4|102|Silver|Snowflake|Plastic|2023-12-07|2.49|

In the simple example above, we have defined a database table (`tbl_ornaments`) to store ornaments with various columns that provide characteristics or qualities related to each item.

We can run various SQL queries against this table to retrieve, update, or delete specific data. For example:

```sql
SELECT * FROM tbl_ornaments WHERE material = 'Wood';
```

This `SELECT` statement returns all columns for the ornaments where the material is specified as "**Wood**".

```sql
SELECT ornament_id, colour, category FROM tbl_ornaments WHERE elf_id = 102;
```

This `SELECT` statement will return all the ornaments created by the Elf with the ID **102**. Unlike the first statement, this query only returns the ornament's **ID**, **colour**, and **category**.

```sql
INSERT INTO tbl_ornaments (ornament_id, elf_id, colour, category, material, date_created, price) VALUES (5, 105, 'Blue', 'Star', 'Glass', '2023-12-10', 4.99);
```

This `INSERT` statement adds a new ornament to the table created by the Elf with the ID **105** and the specified values for each column.

# PHP

PHP is a popular general-purpose scripting language that plays a crucial role in web development. It enables developers to create dynamic and interactive websites by generating HTML content on the server and delivering it to the client's web browser. PHP's versatility and seamless integration with SQL databases make it a powerful tool for building feature-rich, dynamic web applications.

PHP is a **server-side** scripting language, meaning the code is executed on the web server before the final HTML is sent to the user's browser. Unlike client-side technologies like HTML, CSS, and JavaScript, PHP allows developers to perform various server-side tasks, such as connecting to a wide range of databases (such as MySQL, PostgreSQL, and Microsoft SQL Server), executing SQL queries, processing form data, and dynamically generating web content.

![A graphic illustration of a web server serving PHP files to produce a dynamic page on a web browser. As the web browser requests a PHP page on the web server, the server reaches out to a MySQL database server running internally. After obtaining the data from the database, the web server uses PHP to generate a dynamic page for users at runtime.](https://tryhackme-images.s3.amazonaws.com/user-uploads/6490641ea027b100564fe00a/room-content/a45d21ee811982eae4f18e361246efad.svg)

The most common way for PHP to connect to SQL databases is using the **PHP Data Objects (PDO)** extension or specific database server drivers like **mysqli** for **MySQL** or **sqlsrv** for **Microsoft SQL Server (MSSQL)**. The connection is typically established by providing parameters such as the host, username, password, and database name.

After establishing a database connection, we can execute SQL queries through PHP and dynamically generate HTML content based on the returned data to display information such as user profiles, product listings, or blog articles. Returning to our example, if we want our PHP script to fetch information regarding any green-coloured ornaments, we could introduce the following lines:

```php
// Execute an SQL query
$query = "SELECT * FROM tbl_ornaments WHERE colour = 'Green'";
$result = sqlsrv_query($conn, $query);
```

In the above snippet, we first save our SQL query into a variable named `$query`. This query instructs the database to retrieve all rows from the `tbl_ornaments` table where the "**colour**" column is set to "**Green**". We then use the `sqlsrv_query()` function to execute this query by passing it to a database connection object (`$conn`).

You can think of the `$result` variable as a container that holds the outcome of the SQL query, allowing you to iterate through the rows and access the data within those rows. Later in the script, you can use this result object to fetch and display data, making it a crucial part of the process when working with databases in PHP.

# User Input

While the ability to execute SQL queries in PHP allows us to interact with our database, the real power of database-driven web applications lies in making these queries **dynamic**. In our previous example, we hardcoded the query to fetch green ornaments. However, real-world applications often require users to interact with the data. For instance, let's imagine we want to provide users with the ability to search for ornaments of their choice. In this case, we need to create dynamic queries that can be adjusted based on user input.

One common way to take in user-supplied data in web applications is through **GET parameters**. These parameters are typically appended to the URL and can be accessed by PHP. They allow users to specify their search criteria or input, making it a valuable tool for interactive web applications.

We could create a simple search form with an input field for users to specify the colour of ornaments they want. Upon submitting the form, the website makes a **GET request** to the search results page, including the user's search parameters within the URL. PHP can access the user's input as a **GET parameter** and dynamically generate a query based on that input.

```php
// Retrieve the GET parameter and save it as a variable
$colour = $_GET['colour'];

// Execute an SQL query with the user-supplied variable
$query = "SELECT * FROM tbl_ornaments WHERE colour = '$colour'";
$result = sqlsrv_query($conn, $query);
```

The above snippet sets the `$colour` variable to the retrieved value of the "**colour**" URL parameter. That variable then gets passed into the `$query` string.

Now, users can dynamically control the query being executed by the database simply by modifying the URL parameter they include in their request. For example:

http://example.thm/ornament_search.php?colour=Green

![A graphic illustration of how the colour URL parameter can be retrieved and used to run queries. It depicts a web browser, with the URL http://example.thm/ornament_search.php?colour=Green. Below it, the PHP code $colour = $_GET['colour']; extracts the value. Finally, this value is passed to the SQL query, retrieving all of the green ornaments in the database.](https://tryhackme-images.s3.amazonaws.com/user-uploads/6490641ea027b100564fe00a/room-content/c9065f990eb616c297ec9aaf90aec23c.svg)

This simple example shows how powerful PHP and SQL can be in creating rich, dynamic websites.

# SQL Injection (SQLi)

Taking in user-supplied input gives us powerful ways to create dynamic content, but failing to secure this input correctly can expose a critical vulnerability known as **SQL injection (SQLi)**. SQL injection is an attack technique that exploits how web applications handle user input, particularly in SQL queries. Instead of providing legitimate input (like the ornament colour in the example above), the attacker injects malicious SQL statements into a web application's input fields or parameters. The application's database server then executes this rogue SQL query.

SQL injection vulnerabilities pose a considerable risk to web applications as they can lead to unauthorised access, data theft, data manipulation, or even the complete compromise of a web application and its underlying database through remote code execution. If an attacker can control which queries the database executes, they can control the database functions performed and the data returned. As such, the impact can be catastrophic, ranging from exposing sensitive user information to causing significant data breaches.

SQL injection vulnerabilities continue to be highly pervasive despite numerous advancements to mitigate them. This type of vulnerability is featured prominently in the [OWASP Top 10](https://owasp.org/www-project-top-ten/) list of critical web application security risks (**A03:2021-Injection**).

When a web application incorporates user input into SQL queries without proper validation and sanitisation, it opens the door to SQL injection. For example, consider our previous PHP code for fetching user input to search for ornament colours:

```php
// Retrieve the GET parameter and save it as a variable
$colour = $_GET['colour'];

// Execute an SQL query with the user-supplied variable
$query = "SELECT * FROM tbl_ornaments WHERE colour = '$colour'";
$result = sqlsrv_query($conn, $query);
```

Without adequate security measures, an attacker could manipulate the "**colour**" parameter to execute malicious SQL queries. For instance, instead of searching for a benign colour, they might input `' OR 1=1 --` as the input parameter, which would transform the query into:

```sql
SELECT * FROM tbl_ornaments WHERE colour = '' OR 1=1 --'
```

As the query above shows, the attacker **injected** the malicious payload into the dynamic query. Let's take a look at the payload in more detail:

- `' OR` is part of the injected code, where **OR** is a logical operator in SQL that allows for multiple conditions. In this case, the injected code appends a secondary **WHERE** condition in the query.
- `1=1` is the condition following the **OR** operator. This condition is always true because, in SQL, **1=1** is a simple equality check where the left and right sides are equal. Since 1 always equals 1, this condition always evaluates to true.
- The `--` at the end of the input is a comment in SQL. It tells the database server to ignore everything that comes after it. Ending with a comment is crucial for the attacker because it nullifies the rest of the query and ensures that any additional conditions or syntax in the original query are effectively ignored.
- The condition `colour = ''` is empty, and the `OR 1=1` condition is always true, effectively making the entire **WHERE** condition true for every row in the table.

![A graphic illustration of how the colour URL parameter can be exploited to retrieve all of the results in the database by injecting ' OR 1=1 --. After the PHP code extracts the value, it is passed to the query. This malicious query breaks out of the original intended statement and injects the second condition to return true. As a result, all ornaments, regardless of their colour, are returned to the user.](https://tryhackme-images.s3.amazonaws.com/user-uploads/6490641ea027b100564fe00a/room-content/ee1a94590a1fa55af578b565a4a4fc23.svg)

As a result, this SQL injection successfully manipulates the query to return **all rows** from the `tbl_ornaments` table, regardless of the actual ornament colour values. This is a classic example of an SQL injection payload, where the attacker leverages the **OR 1=1** condition to bypass any intended conditions or logic in the query and retrieve data they are not supposed to access.

# A Caution Around OR 1=1

It's crucial to emphasise the potential risks of using the `OR 1=1` payload. While commonly used for illustration, injecting it without caution can lead to unintended havoc on a database. When injecting `OR 1=1` into a query, the intention is typically to bypass authentication or to return all items in a table by making the condition always true. However, the risks lie in that you might not be aware of the context and scope of the query you're injecting into. Additionally, applications may sometimes use values from an initial request in multiple SQL queries. SQL injection payloads that return all rows can lead to unintended consequences when injected into different types of statements, such as `UPDATE` or `DELETE`.

Imagine injecting it into a query that **updates** a specific user's information. An `OR 1=1` payload would make the condition true for every row, leading to a mass update affecting all records (users) in the table. This lack of specificity in the payload makes it a risky choice for penetration testers who might inadvertently cause significant data loss or alterations. A safer example would be a more targeted condition based on a known attribute identifying the record you want to manipulate. For instance, `bob' AND 1=1--` would update Bob's record, while `bob' AND 1=2--` would not. This still demonstrates the SQL injection vulnerability without putting the entire table's records at risk.

For a practical example, check out the [Lesson Learned?](https://tryhackme.com/room/lessonlearned) room.

Fortunately, the development team behind the Best Festival website has confirmed that the website does not run any unpredictable queries and has permitted us to use this payload to demonstrate the vulnerability.

# Stacked Queries

SQL injection attacks can come in various forms. A technique that often gives an attacker a lot of control is known as a "**stacked query**". Stacked queries enable attackers to terminate the original (intended) query and execute additional SQL statements in a single injection, potentially leading to more severe consequences such as data modification and calls to stored procedures or functions.

In SQL, the semicolon typically signifies one statement's conclusion and another's commencement. This feature facilitates the execution of multiple SQL statements within a single interaction with the database server. It's important to note that certain web application technologies and database management systems (DBMS) may demand different syntax or lack support for stacked queries. Consequently, enumeration is essential for precision when conducting injection attacks.

Suppose our attacker in the previous example wants to go beyond just retrieving all rows and intends to **insert** some malicious data into the database. They can modify the previous injection payload to this:

```sql
' ; INSERT INTO tbl_ornaments (elf_id, colour, category, material, price) VALUES (109, 'Evil Red', 'Broken Candy Cane', 'Coal', 99.99); --
```

When the web application processes this input, here's the resulting query the database would execute:

```sql
SELECT * FROM tbl_ornaments WHERE colour = '' ; INSERT INTO tbl_ornaments (elf_id, colour, category, material, price) VALUES (109, 'Evil Red', 'Broken Candy Cane', 'Coal', 99.99); --'
```

As a result, the attacker successfully ends the original query using a semicolon and introduces an additional SQL statement to insert malicious data into the `tbl_ornaments` table. This showcases the potential impact of stacked queries, allowing attackers to not only manipulate the retrieved data but also perform permanent data modification.