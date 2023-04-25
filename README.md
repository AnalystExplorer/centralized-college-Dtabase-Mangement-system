# centralized college Database management System
A centralized college database management system is a software application designed to manage and store information about students, faculty, courses, and other resources in a college or university. The system aims to streamline administrative tasks, improve communication between departments, and provide accurate and timely information to stakeholders.The system includes various modules such as student admission, course registration, attendance management, grading, fee collection, and reporting. It enables administrators to easily access and manipulate data related to academic performance, student demographics, financial transactions, and more.The system is typically designed with a user-friendly interface that allows authorized users to access the database securely and efficiently. The system can also be customized to meet the specific needs of the college or university, such as incorporating different data fields or integrating with other software applications.Overall, a centralized college database management system can help colleges and universities to improve their administrative efficiency, reduce errors, and enhance communication and collaboration among faculty, staff, and students.
#Entities:
1. College(Coll_ID, Coll_name, Coll_grade, Coll_location)
2. Department(Dept_ID, Dept_name)
3. Course(Course_ID,Course_name, Course_desc, Course_credit)
4. Assignment(Assignment_ID, Assignment_name, Assignment_desc, Assignment_deadline, no_of_assignment)
5. Student(Stu_ID,Stu_name, Stu_email, Stu_address, Stu_DOB, Stu_age, Stu_phnu)
6. Attendance(Auth_ID, Auth_pwd, Attendance_percent)
7. Faculty(Fac_ID, Fac_name, Fac_Phnu, Fac_email, Fac_add,Fac_salary,Fac_YOE, Fac_ Desg )
8. Library(Lib_ID, Lib_name, Book_ID, Book_name, Author_name, Issuing_Date, Return_Date, Rack_number)
9. Worker(worker_ID, worker_name, worker_email, Worker_address, Worker_Phnu, Worker_salary,Worker_DOB)
10. Cntene(Cant_ID, Cant_name, Menu_name(Veg_menu,Nonveg_menu),)
11. Campus Store(Store_ID, Store_name,Item_list,Item_name, Item_Price)

Creating Tables:

Create table College(
Coll_ID int not null,
coll_name varchar(250)not null,
coll_grade varchar(10) not null,
coll_location varchar(50) not null,
primary key(coll_ID));

Create table Department(
Dept_ID int not null,
Dept_name varchar(250)not null,
primary key(Dept_ID));

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
Fac_joining_Date Date


primary key(coll_ID));

Create table College(
Coll_ID int not null,
coll_name varchar(250)not null,
coll_grade varchar(10) not null,
coll_location varchar(50) not null,
primary key(coll_ID));

Create table College(
Coll_ID int not null,
coll_name varchar(250)not null,
coll_grade varchar(10) not null,
coll_location varchar(50) not null,
primary key(coll_ID));

Create table College(
Coll_ID int not null,
coll_name varchar(250)not null,
coll_grade varchar(10) not null,
coll_location varchar(50) not null,
primary key(coll_ID));

Create table College(
Coll_ID int not null,
coll_name varchar(250)not null,
coll_grade varchar(10) not null,
coll_location varchar(50) not null,
primary key(coll_ID));







 



 
