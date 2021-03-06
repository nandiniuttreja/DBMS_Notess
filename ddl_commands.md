# DDL commands:  

## 1. To create a table named "chitkara_students"
### create table command 

```sql
create table chitkara_students (
    roll_no int,
    std_name varchar(20),
    course_name varchar(15),
    marks float
); 
```
-   From here, the table is created, but it isn't visible yet. 

## 2. To describe a table 
### desc <tablename> command

```sql
desc chitkara_students;
```
-   The table is now being displayed.

## 3. To drop a table 
### drop table <tablename> command

```sql
drop table chitkara_students; 
```
-   The table is now dropped i.e. deleted. Use desc <tablename> command to verify.

## 4. To add a new column in a table
### alter table <tablename> add <columnname> <datatype> command

```sql
alter table chitkara_students add hostel_name varchar(20); 
```
-   Describe the table and you can now see the new added column.

## 5. To drop a column in a table
### alter table <tablename> drop <columnname> command

```sql
alter table chitkara_students drop column hostel_name; 
```
-   Describe the table and you can now see that the column is now dropped.

## 6. To modify datatype of a column
### alter table <tablename> modify <columnname> datatype command

```sql
alter table chitkara_students modify marks int;
```
-   The datatype has been changed from float to int.

## 7. To modify the length of a datatype of a column
### alter table <tablename> modify <columnname> datatype(length) command

```sql
alter table chitkara_students std_name varchar2(25);
```
-   The length of datatype has been changed from 20 to 25.

## 8. To rename the tablename
### alter table <tableOLDname> rename to <tableNEWname> command

```sql
alter table chitkara_students rename to chitkara_ke_bache;
```
-   The name of the table has been changed.

## The complete program :

```sql
    create table chitkara_students (
        roll_no int,
        std_name varchar2(20),
        course_name varchar2(15)
    ); 
    desc chitkara_students;
    -- drop table chitkara_students; 
    -- desc chitkara_students;
    alter table chitkara_students add hostel_name varchar(20); 
    desc chitkara_students;
    alter table chitkara_students drop column hostel_name; 
    desc chitkara_students;
    truncate table chitkara_students; 
    alter table chitkara_students modify marks int;
    alter table chitkara_students modify std_name varchar2(25);
    alter table chitkara_students rename to chitkara_ke_bache;
    desc chitkara_ke_bache;
```