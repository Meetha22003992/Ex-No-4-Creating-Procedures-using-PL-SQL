# Ex. No: 4 Creating Procedures using PL/SQL

## DATE: 25.09.2023

### AIM: To create a procedure using PL/SQL.

### Steps:
1. Create employee table with following attributes (empid NUMBER, empname VARCHAR(10), dept VARCHAR(10),salary NUMBER);
2. Create a procedure named as insert_employee data.
3. Inside the procdure block, write the query for inserting the values into the employee table.
4. End the procedure.
5. Call the insert_employee data procedure to insert the values into the employee table.
6. Display the employee table

### Program:

CREATE TABLE employee ( empid INT, empname VARCHAR(10),dept VARCHAR(10),salary FLOAT );

CREATE PROCEDURE insert_employee_data (
         p_empid INT,
         p_empname VARCHAR(10),
         p_dept VARCHAR(10),
         p_salary DECIMAL(10, 2)
     )
     BEGIN
         INSERT INTO employee (empid, empname, dept, salary)
         VALUES (p_empid, p_empname, p_dept, p_salary);
     END //

DELIMITER ;
mysql> CALL insert_employee_data(1, 'John', 'HR', 50000.00);
mysql> CALL insert_employee_data(2, 'Alice', 'Finance', 60000.00);
mysql> CALL insert_employee_data(3, 'Bob', 'IT', 55000.00);

mysql> SELECT * FROM employee;


### Output:
![image](https://github.com/Meetha22003992/Ex-No-4-Creating-Procedures-using-PL-SQL/assets/119401038/acbff79e-8c9a-41ea-975c-40f16f600593)

![image](https://github.com/Meetha22003992/Ex-No-4-Creating-Procedures-using-PL-SQL/assets/119401038/73138b13-1518-4c62-b3f6-37fdf7289cde)

### Result:
Thus the procedure has been successfully created in mysql
