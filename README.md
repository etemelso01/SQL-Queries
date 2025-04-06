<h1 align="center">SQL Assignment - CIS 310</h1>

<h2>Description</h2>
<p>This is an assignment I completed in CIS 310. In this task, I was asked to create a `LARGE_PROPERTY` table and perform multiple SQL operations, including inserting, updating, and deleting data based on certain conditions like square footage, monthly rent, and owner information. Below are the SQL queries and tasks completed for this assignment.</p>

<h2>SQL Query Example</h2>
<pre>
--1. Create a LARGE_PROPERTY table and insert properties where square footage is greater than 1,000.
CREATE TABLE LARGE_PROPERTY (
  OFFICE_NUM DECIMAL(2, 0) NOT NULL,
  ADDRESS CHAR(25) NOT NULL,
  BDRMS DECIMAL(2, 0),
  FLOORS DECIMAL(2, 0),
  MONTHLY_RENT DECIMAL(6, 2),
  OWNER_NUM CHAR(5)
);

INSERT INTO LARGE_PROPERTY (OFFICE_NUM, ADDRESS, BDRMS, FLOORS, MONTHLY_RENT, OWNER_NUM)
SELECT OFFICE_NUM, ADDRESS, BDRMS, FLOORS, MONTHLY_RENT, OWNER_NUM
FROM PROPERTY
WHERE SQR_FT > 1000;

--2. Increase the monthly rent of each large property by $50.
UPDATE LARGE_PROPERTY
  SET MONTHLY_RENT = (MONTHLY_RENT + 50);

--3. Decrease the rent of properties with monthly rent greater than $1750 by 3%.
UPDATE LARGE_PROPERTY
  SET MONTHLY_RENT = (MONTHLY_RENT) - ((3 * MONTHLY_RENT) / 100)
  WHERE MONTHLY_RENT > 1750;

--4. Insert a new property into the LARGE_PROPERTY table.
INSERT INTO LARGE_PROPERTY (OFFICE_NUM, ADDRESS, BDRMS, FLOORS, MONTHLY_RENT, OWNER_NUM)
VALUES (1, '2643 Lugsi Dr.', 3, 2, 775.00, 'MA111');

--5. Delete properties in LARGE_PROPERTY for the owner number 'BI109'.
DELETE FROM LARGE_PROPERTY
  WHERE OWNER_NUM = 'BI109';

--6. Set the monthly rent to NULL for the property at '891 Alton Dr.'.
UPDATE LARGE_PROPERTY
  SET MONTHLY_RENT = NULL
  WHERE ADDRESS = '891 Alton Dr.';

--7. Delete the LARGE_PROPERTY table.
DROP TABLE LARGE_PROPERTY;
</pre>

<h3>Checklist of SQL Elements Used</h3>
<ul>
  <li>☒ SELECT</li>
  <li>☒ FROM</li>
  <li>☒ WHERE</li>
  <li>☒ ORDER BY</li>
  <li>☒ AND</li>
  <li>☒ BETWEEN</li>
  <li>☒ IS NULL / IS NOT NULL</li>
  <li>☒ OR</li>
  <li>☒ Comparison Operators (&gt; &lt; = !)</li>
  <li>☒ ASC/DESC</li>
</ul>

<h2>Used to Create:</h2>
<ul>
  <li><b>SQL Server:</b></li>
</ul>

<p>These SQL queries demonstrate the process of managing large properties in a database, from creating tables to performing updates and deletions based on various conditions. This hands-on exercise has given me a deeper understanding of database management and SQL syntax.</p>


<h2>Used to create:</h2>

- <b>Sql Server</b>
- <img width="624" alt="image" src="https://github.com/user-attachments/assets/84dde83e-c7f0-49ec-b03c-9325279691c1" />
