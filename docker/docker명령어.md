
```linux
    docker run -d -e MYSQL_ROOT_PASSWORD=cnu --name=mysql1 mysql:5.7
```
>> 명령어로 docker에 container를 실행시켜 줍니다.
>> 그 후 

```linux
    docker exec -it mysql1 bash
```
>> 접속 

```linux
# apt update
# apt install nano
# apt install wget
# apt install bzip2
# wget https://launchpad.net/test-db/employees-db-1/1.0.6/+download/employees_db-full-1.0.6.tar.bz2
# bzip2 -d em~~.bz2
# tar xvf ~~.tar
# cd em...db
# mysql -uroot -p
# source empl~~~.sql

# show databases;
# use employees;
# show tables;
# select count(*) from employees;
# select * from employees limit 10;
# show create table department;
# select * from employees join dept_emp on employees.emp_no = dept_emp.emp_no;
# select * from employees join dept_emp on employees.emp_no = dept_emp.emp_no join departments on dept_emp.dept_no = departments.dept_no where employees.emp_no = 10001\G;
# select avg(salaries.salary) from employees join dept_emp on employees.emp_no = dept_emp.emp_no join departments on dept_emp.dept_no = departments.dept_no join salaries on employees.emp_no = salaries.emp_no where departments.dept_name = 'Development';
# desc dept_emp;
# create index sample_index on employees(first_name,last_name);
# select * from employees where first_name like 'Geo%';
# select * from employees where first_name like 'geo___';
// 복합 인덱스 생성

mysql> commit;
Query OK, 0 rows affected (0.00 sec)

mysql> select * from departments;
+---------+--------------------+
| dept_no | dept_name          |
+---------+--------------------+
| 100     | CNU                |
| d009    | Customer Service   |
| d005    | Development        |
| d002    | Finance            |
| d003    | Human Resources    |
| d001    | Marketing          |
| d004    | Production         |
| d006    | Quality Management |
| d008    | Research           |
| d007    | Sales              |
+---------+--------------------+
10 rows in set (0.00 sec)

mysql> rollback;
Query OK, 0 rows affected (0.00 sec)

// 간단한 트랜잭션에 대한 실습

```

>> 결과는 맞게 나와도 쿼리를 실행하는데 2.5초?





