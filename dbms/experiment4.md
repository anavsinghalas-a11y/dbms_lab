
- **Q4. List employees whose name contains 'S'**

  ```sql
  SELECT *
  FROM EMPLOYEE
  WHERE ENAME LIKE '%S%';
  ```

- **Q5. List employees whose name ends with 'S'**

  ```sql
  SELECT *
  FROM EMPLOYEE
  WHERE ENAME LIKE '%S';
  ```

- **Q6. List employees who are in department 10, 20, or 30 OR whose job is CLERK, SALESMAN, or ANALYST**

  ```sql
  SELECT ENAME, JOB, DEPTNO
  FROM EMPLOYEE
  WHERE DEPTNO IN (10,20,30)
  OR JOB IN ('CLERK', 'SALESMAN', 'ANALYST');
  ```

- **Q7. List employees having non-null commission**

  ```sql
  SELECT ENAME
  FROM EMPLOYEE
  WHERE COMM IS NOT NULL;
  ```

- **Q8. Find total salary (salary + commission) for each employee**

  ```sql
  SELECT EMPNO,
         SUM(SAL + IFNULL(COMM, 0)) AS TOTAL_SALARY
  FROM EMPLOYEE
  GROUP BY EMPNO;
  ```

- **Q9. Display department number and annual salary (SAL*12) for each employee**

  ```sql
  SELECT DEPTNO, SAL * 12 AS ANNUAL_SALARY
  FROM EMPLOYEE
  GROUP BY EMPNO;
  ```

- **Q10. List clerks whose salary is greater than 3000**

  ```sql
  SELECT ENAME
  FROM EMPLOYEE
  WHERE JOB IN ('CLERK') AND SAL > 3000;
  ```

- **Q11. List employees whose job is CLERK, SALESMAN, or ANALYST and salary is greater than 3000**

  ```sql
  SELECT ENAME
  FROM EMPLOYEE
  WHERE JOB IN ('CLERK', 'SALESMAN', 'ANALYST') AND SAL > 3000;
  ```

---