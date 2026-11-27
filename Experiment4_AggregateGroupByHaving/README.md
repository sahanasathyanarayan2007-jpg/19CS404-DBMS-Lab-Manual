# Experiment 4: Aggregate Functions, Group By and Having Clause

## AIM
To study and implement aggregate functions, GROUP BY, and HAVING clause with suitable examples.

## THEORY

### Aggregate Functions
These perform calculations on a set of values and return a single value.

- **MIN()** – Smallest value  
- **MAX()** – Largest value  
- **COUNT()** – Number of rows  
- **SUM()** – Total of values  
- **AVG()** – Average of values

**Syntax:**
```sql
SELECT AGG_FUNC(column_name) FROM table_name WHERE condition;
```
### GROUP BY
Groups records with the same values in specified columns.
**Syntax:**
```sql
SELECT column_name, AGG_FUNC(column_name)
FROM table_name
GROUP BY column_name;
```
### HAVING
Filters the grouped records based on aggregate conditions.
**Syntax:**
```sql
SELECT column_name, AGG_FUNC(column_name)
FROM table_name
GROUP BY column_name
HAVING condition;
```

**Question 1**
--
```
How many patients are there in each city?

Sample table: Patients Table



For example:

Result
Address     TotalPatients
----------  -------------
Berlin      3
Chicago     4
Mexico      3
```

**Output:**
```
select Address,count(*) as TotalPatients from Patients group by Address;
```
<img width="640" height="397" alt="image" src="https://github.com/user-attachments/assets/988a0d13-035e-482a-9607-84ac8fb0cfae" />



**Question 2**
---
```
What is the average dosage prescribed for each medication?

Sample tablePrescriptions Table



For example:

Result
Medication     AvgDosage
-------------  ----------
Ciprofloxacin  500.0
Doxorubicin    60.0
Ibuprofen      400.0
Levothyroxine  50.0
Lisinopril     10.0
MMR            0.5
Pending        0.0
Prenatal vita  1.0
Sertraline     50.0
Topiramate     25.0
```

**Output:**
```
select Medication,avg(Dosage) as AvgDosage from Prescriptions group by Medication;
```
<img width="586" height="682" alt="image" src="https://github.com/user-attachments/assets/7607e8a7-de21-4186-b85d-87e3cfd982a3" />

**Question 3**
---
```
How many patients are covered by each insurance company?

Sample table:Insurance Table

name               type
-----------------  ----------
InsuranceID        INTEGER
PatientID          INTEGER
InsuranceCompany   TEXT
PolicyNumber       TEXT
PolicyHolder       TEXT
ValidityPeriod     TEXT
For example:

Result
InsuranceCompany   TotalPatients
-----------------  -------------
DEF Insurance      1
GHI Insurance      1
GLM Insurance      2
JKL Insurance      1
MNO Insurance      3
PQR Insurance      1
YZA Insurance      1
```

**Output:**

```
select InsuranceCompany ,count (*) as TotalPatients from Insurance group by InsuranceCompany;
```
<img width="702" height="602" alt="image" src="https://github.com/user-attachments/assets/4537fc68-a3be-4415-9f83-027b94c60287" />

**Question 4**
---
```
Write a SQL query to find Who has the highest income among employee living in California?

Table: employee

name        type
----------  ----------
id          INTEGER
name        TEXT
age         INTEGER
city        TEXT
income      INTEGER
For example:

Result
name        max(income)
----------  -----------
Adam        5000000

```

**Output:**

```
select name, max(income) from employee where city='California';
```
<img width="591" height="255" alt="image" src="https://github.com/user-attachments/assets/e875d179-af73-451e-863b-d6279f5855f4" />

**Question 5**
---
```
Write a SQL query to return the total number of rows in the 'customer' table where the city is not Noida.

Sample table: customer



 

For example:

Result
COUNT
----------
9

```

**Output:**

```
select count(*) as COUNT from customer where city !='Noida';
```
<img width="350" height="250" alt="image" src="https://github.com/user-attachments/assets/063cd6ce-a8ec-418a-a98f-5598b3401e5a" />

**Question 6**
---
```
Write a SQL query to Calculate the average income of the employees with names starting with 'A': 

Table: employee

name        type
----------  ----------
id          INTEGER
name        TEXT
age         INTEGER
city        TEXT
income      INTEGER
For example:

Result
avg_income
----------
5000000.0
```

**Output:**

```
select avg(income) as avg_income from employee where name like 'A%';
```
<img width="312" height="225" alt="image" src="https://github.com/user-attachments/assets/44bb0e51-305f-4a73-a4eb-c90f87eed2f8" />

**Question 7**
---
```
Write a SQL query to calculate the average purchase amount of all orders. Return average purchase amount.

Sample table: orders

ord_no      purch_amt   ord_date    customer_id  salesman_id

----------  ----------  ----------  -----------  -----------

70001       150.5       2012-10-05  3005         5002

70009       270.65      2012-09-10  3001         5005

70002       65.26       2012-10-05  3002         5001

 

For example:

Result
AVERAGE
----------
1461.765
```

**Output:**

```
select avg(purch_amt) as AVERAGE from orders;
```
<img width="330" height="232" alt="image" src="https://github.com/user-attachments/assets/dd418035-cbad-4609-9152-2cafa01d7758" />

**Question 8**
---
```
Write the SQL query that achieves the grouping of data by age, calculates the minimum income for each age group, and includes only those age groups where the minimum income is less than 1,000,000.

Sample table: employee



For example:

Result
age         Income
----------  ----------
32          200000
40          350000
45          450000
```

**Output:**

```
select age,min(Income) as Income from employee group by age having min(Income) <1000000;
```
<img width="535" height="367" alt="image" src="https://github.com/user-attachments/assets/7ea0a624-5b43-4b90-8121-6c638c0f8805" />

**Question 9**
---
```
Write a SQL query to identify the cities (addresses) where the average salary is greater than Rs. 5000, as per the "customer1" table.

Sample table: customer1



For example:

Result
address     AVG(salary)
----------  -----------
Bhopal      8500.0
Indore      10000.0
Mumbai      6500.0
```

**Output:**

```
select address, AVG(salary) from customer1 group by address having avg(salary) > 5000;
```
<img width="562" height="362" alt="image" src="https://github.com/user-attachments/assets/ec4472fe-0a36-4f9b-96a6-1a14f91830f1" />

**Question 10**
---
```
Write the SQL query that achieves the grouping of data by city, calculates the total income for each city, and includes only those cities where the total income sum is greater than 200,000.

Sample table: employee



For example:

Result
city        Income
----------  ----------
Alaska      450000
Arizona     1000000
California  5300000
Florida     5350000
Georgia     250000
```

**Output:**

```
select city,sum(Income) as Income from employee group by city having sum(Income) > 200000;
```
<img width="542" height="467" alt="image" src="https://github.com/user-attachments/assets/99e1f18e-227b-4bfe-a726-5d5e122eb3f3" />


## RESULT
Thus, the SQL queries to implement aggregate functions, GROUP BY, and HAVING clause have been executed successfully.
