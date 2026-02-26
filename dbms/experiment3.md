### 3. EXP2 – Basic `SELECT` with Conditions

- **Q1. List distinct jobs from `EMPLOYEE`**

  ```sql
  SELECT DISTINCT JOB
  FROM EMPLOYEE;
  ```

- **Q2. List employees in department 30**

  ```sql
  SELECT *
  FROM EMPLOYEE
  WHERE DEPTNO = 30;
  ```

- **Q3. List distinct department numbers greater than 20**

  ```sql
  SELECT DISTINCT DEPTNO
  FROM EMPLOYEE
  WHERE DEPTNO > 20;
  ```

- **Q4. List employees in department 30 who are MANAGER or CLERK**

  ```sql
  SELECT *
  FROM EMPLOYEE
  WHERE DEPTNO = 30
  AND JOB IN ('MANAGER', 'CLERK');
  ```

- **Q5. List all clerks with EMPNO and DEPTNO**

  ```sql
  SELECT ENAME, EMPNO, DEPTNO
  FROM EMPLOYEE
  WHERE JOB = 'CLERK';
  ```

- **Q6. List managers not in department 30**

  ```sql
  SELECT *
  FROM EMPLOYEE
  WHERE JOB = 'MANAGER'
  AND DEPTNO <> 30;
  ```

- **Q7. List employees in department 10 whose job is not MANAGER or CLERK**

  ```sql
  SELECT *
  FROM EMPLOYEE
  WHERE DEPTNO = 10
  AND JOB NOT IN ('MANAGER', 'CLERK');
  ```

- **Q8. List employees whose salary is between 1200 and 1400**

  ```sql
  SELECT ENAME, JOB
  FROM EMPLOYEE
  WHERE SAL BETWEEN 1200 AND 1400;
  ```

- **Q9. List employees whose job is CLERK, ANALYST or SALESMAN**

  ```sql
  SELECT ENAME, DEPTNO
  FROM EMPLOYEE
  WHERE JOB IN ('CLERK', 'ANALYST', 'SALESMAN');
  ```

- **Q10. List employees whose name starts with 'M'**

  ```sql
  SELECT ENAME, DEPTNO
  FROM EMPLOYEE
  WHERE ENAME LIKE 'M%';
  ```

---