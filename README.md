# centralized college Database management System
A centralized college database management system is a software application designed to manage and store information about students, faculty, courses, and other resources in a college or university. The system aims to streamline administrative tasks, improve communication between departments, and provide accurate and timely information to stakeholders.The system includes various modules such as student admission, course registration, attendance management, grading, fee collection, and reporting. It enables administrators to easily access and manipulate data related to academic performance, student demographics, financial transactions, and more.The system is typically designed with a user-friendly interface that allows authorized users to access the database securely and efficiently. The system can also be customized to meet the specific needs of the college or university, such as incorporating different data fields or integrating with other software applications.Overall, a centralized college database management system can help colleges and universities to improve their administrative efficiency, reduce errors, and enhance communication and collaboration among faculty, staff, and students.

## Entities and Attributes:
1. College(Coll_ID, Coll_name, Coll_grade, Coll_location)
2. Department(Dept_ID, Dept_name)
3. Course(Course_ID,Course_name, Course_desc, Course_credit)
4. Assignment(Assignment_ID, Assignment_name, Assignment_desc, Assignment_deadline, no_of_assignment)
5. Student(Stu_ID,Stu_name, Stu_email, Stu_address, Stu_DOB, Stu_age, Stu_phnu)
6. Attendance(Auth_ID, Auth_pwd, Attendance_percent)
7. Faculty(Fac_ID, Fac_name, Fac_Phnu, Fac_email, Fac_add,Fac_salary,Fac_YOE, Fac_ Desg )
8. Library(Lib_ID, Lib_name, Book_ID, Book_name, Author_name, Issuing_Date, Return_Date, Rack_number)
9. Worker(worker_ID, worker_name, worker_email, Worker_address, Worker_Phnu, Worker_salary,Worker_DOB)
10. Cantene(Cant_ID, Cant_name, Menu_name(Veg_menu,Nonveg_menu),)
11. Campus Store(Store_ID, Store_name,Item_list,Item_name, Item_Price)

![ER unknown-Page-3 drawio (2)](https://user-images.githubusercontent.com/125997064/234306996-8a87abb3-22de-411f-b5a5-e0b15cce8840.png)

## Creating Tables:

Create table College(
Coll_ID int not null,
coll_name varchar(250)not null,
coll_grade varchar(10) not null,
coll_location varchar(50) not null,
primary key(coll_ID));

Create table Department(
Dept_ID int not null,
Dept_name varchar(250)not null,
primary key(Dept_ID),foreign key(coll_ID));

Create table Course(
Course_ID int not null,
Course_name varchar(250)not null,
Course_desc varchar(250)not null,
Course_credit varchar(250)not null,
primary key(Dept_ID), 
foreign key(Dept_ID));

Create table Assignment(
Assignment_ID int not null,
Assignment_name varchar(250)not null,
Assignment_desc varchar(10) not null,
Assignment_deadline varchar(50) not null,
no_of_assignment int not null,
primary key(Assignment_ID), 
foreign key(Course_ID), 
foreign key(Course_name));

Create table Student(
Stu_ID int not null,
Stu_name varchar(250) not null,
Stu_email varchar(10) not null,
Stu_address varchar(50) not null,
Stu_DOB Date,
Stu_age int not null
Stu_phnu int not null
primary key(Stu_ID), );

Create table Attendance(
Auth_ID int not null,
Auth_pwd varchar(250)not null,
Attendance_percent int not null );

Create table Faculty(
Fac_ID int not null,
Fac_name varchar(250)not null,
Fac_Phnu int not null,
Fac_email varchar(50) not null,
Fac_address varchar(250) not null,
Fac_salary int not null,
Fac_YOE int not null,
Fac_ Desg varchar(100) not null,
Fac_joining_Date Date,
primary key(coll_ID));

Create table Library( 
Lib_ID int not null,
Lib_name varchar(50)not null,
Book_ID int not null,
Book_name varchar(10) not null,
Author_name varchar(50) not null,
Issuing_Date Date,
Return_Date Date,
Rack_number int not null,
primary key(Lib_ID),
Foreign key(coll_ID),foreign key(Dept_ID), Foreign key(Stud_ID));

Create table Worker(
worker_ID int not null,
worker_name varchar(250)not null,
worker_email varchar(10) not null,
Worker_address varchar(50) not null,
Worker_Phnu int not null,
Worker_salary int not null,
Worker_DOB Date,
primary key(worker_ID), 
Foreign key(coll_ID));

Create table Cantene(
Cant_ID int not null,
Cant_name varchar(250)not null,
Menu_name varchar(10) not null,
Veg_menu varchar(50) not null,
Nonveg_menu varchar(50) not null,
primary key(coll_ID), );

Create table Campus Store(
Store_ID int not null,
Store_name varchar(250)not null,
Item_list varchar(250) not null,
Item_name varchar(150) not null,
Item_Price int not null,
primary key(coll_ID), Foreign key(Dept_ID), Foreign key(coll_ID));

##### **Inserting value into Table **
**College_Table**

| coll_ID       | Coll_name     | coll_Grade | Coll_location |
| ------------- | ------------- | ---------- | -------------- |
| 101  | Christ university  | B | Bangalore |
| 102  | VTU                | B | Bangalore |
| 103 | SJCIT  | B | Bangalore |
| 104 | MIT | A | Pune |
| 105 | MITID | A | Pune |

**Department_Table**

| Dept_ID       | Dept_name     | compltn_time |
| ------------- | ------------- | ------------ |
| 1010  | Engineering  |  4 yrs(8 sem)|
| 1020  | BBA               | 3 yrs(6 sem) |
| 1030 | MBA  |   2 yrs(6 trisem) |
| 1040 | Diploma | 2 yrs(4 sem) |
| 1050 | Design | 4 yrs(8 sem) |

**Course_Table**

| Course_ID       | Course_name     | Course_desc | Course_credit |
| ------------- | ------------- | ----------- | ------------ |
| 11  | IT  | computer science engineering | 5 |
| 12  | Finace                | Finance analytics | 5 |
| 13 | BA  | Business analytics | 5 |
| 14 | civil | civil engineering  | 5 |
| 15 | product design | design specification | 5 |

**Assignment_table**

| Assignment_ID        | Assignment_name     | Assignment_desc | Assignment_deadline | no_of_assignment |
| -------------------- | ------------------- | --------------- | ------------------- | -------------------- | 
| 110  | Python  | Basics to pro | 7 days | 5 |
| 120  | Sql | Basics to pro | 7 days | 5|
| 130 | Case study | critical thinking | 10 days | 1 |
| 140 | communication | Basics to pro  | 3 days | 5 |
| 150 | presentation | Basics to pro | 7 days |10 |

**Student_table**

| Stu_ID       | Stu_name     | Stu_email | Stu_address | Stu_DOB | Stu_age |Stu_phnu | 
| -------------------- | ------------------- | --------------- | ------------------- | -------------------- | ----------| ---------|
| 2110  | Swati  | swati@gmail.com | Bihar | 29-05-1945 | 23 | 9353787654 |
| 2120  | Anshu | Anshu@gmail.com | Bihar | 02-08-1946 | 22 | 9353787645 |
| 2130 | Tejasvi | TJ@gmail.com | Bangalore | 01-09-1948 | 21 | 9353786754 |
| 2140 | Aakriti | Aakriti@gmail.com  | Bhopal | 02-10-1949 | 22 | 9335787654 |
| 2150 | Riya| Riya@gmail.com | Bihar | 03-11-1950 | 21 | 9343787654 |

**Attendance_Table**


| Auth_ID      | Auth_pwd     | Attendance_percent |
| ------------- | ------------- | ------------ |
| 1010  | user  |  90% |
| 1020  | user              | 95%  |
| 1030 | user  |   85% |
| 1040 | user | 70% |
| 1050 | user| 92% |

 **Faculty**
 | Fac_ID      | Fac_name     | Fac_Phnu | Fac_email | Fac_add | Fac_salary |Fac_YOE | Fac_ Desg  |
| -------------------- | ------------------- | --------------- | ------------------- | -------------------- | ----------| ---------| ------------|
| 21413 | Anshul saxena | 93537876855 | Anshulsaxena@gmail.com | MP | 10,00,000 |02-08-2006 | HOS |
| 21414| Danesh Hussain | 6523456892| DaneshHussain@gmail.com | Bangalore | 11,00,000 | 01-09-2007 | HOS  |
| 21415 | Jerin Jose | 2354896524 | JerinJose@gmail.com  | Bangalore | 12,00,000 | 02-10-2012 | facluty |
| 21416| Beky Thomas | 9845762143| BekyThomas@gmail.com | pune | 15,00,000 | 03-11-2018 | HOD  |

 **Library**
| Lib_ID      | Lib_name     | Book_ID | Book_name | Author_name | Issuing_Date |Return_Date | Rack_number|
| -------------------- | ------------------- | -------------- | ------------------- | -------------------- | ----------| ---------| ------------|
| 562110  | central  | 85623 |Rich dad poor dad| sawti | 29-05-2022 |01-06-2022 | 3 | 
| 652120  | MBA | 95462 |Business intelligence | Anshu | 02-08-2022 |29-08-2022 | 2 | 
| 872130 | central| 75423 |case studys | Tejasvi | 01-09-2022 |22-09-2022 | 1 | 
| 782140 | central | 97561 | R laguage  | Aakriti | 02-10-2022 |20-10-2022 | 2 | 
| 952150 | MBA| 95687 |Big Data Management |  Riya | 03-11-2022 |25-11-2022 | 7 |

**Worker**
| worker_ID      | worker_name     | worker_email | Worker_address | Worker_Phnu | Worker_salary | Worker_DOB | 
| -------------------- | ------------------- | --------------- | ------------------- | -------------------- | ----------| ---------|
| 211550  | Rahul  | rahul@gmail.com | pune|7854693215 | 50000 | 27-05-1945 |  
| 233120  | manish | manish@gmail.com | lavasa | 6987452134 | 45000 |07-08-1946 | 
| 214530 | sonu | sonu@gmail.com | pirangut| 7894125864 | 50000 |11-09-1948 | 
| 218840 | Rashmi | rashmi@gmail.com  | lavasa | 9999745699 | 55000 |12-10-1949 |  
| 215990 | rekha| rekha@gmail.com | pune | 8795641829 | 50000 |23-11-1950 |

**Cantene**
| Cant_ID     | Cant_name    | Menu_name(Veg_menu,Nonveg_menu) | 
| -------------------- | ------------------- | ---------------------------- |
| 21210  | lutos  | Veg_menu |
| 23120  | cafe valley | Veg_menu,Nonveg_menu |
| 23130 | conserto | Veg_menu | 
| 24140 | sreamimng mugs| Veg_menu,Nonveg_menu  | 
| 22150 | cafrtaria| Veg_menu,Nonveg_menu | 

**Campus Store**
| Store_ID      | Store_name     | Item_list | Item_name | Item_Price | 
| -------------------- | ------------------- | -------------- | ------------------ | ---------------|
| 1234 | cen_trinity  |  1 | classmate notebook |175 | 
| 5678  | Mba_Trinity | 2 | uniball pen | 80 |
| 9012 | cafe coffe day | 3 | cappechino | 55 |























 



 
