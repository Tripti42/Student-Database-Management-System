# Student-Database-Management-System

This project is a Student Information Management System designed to help educational institutes and colleges maintain student records easily. The system provides a user-friendly interface for managing all kinds of student details, academic reports, and related information.


![image](https://github.com/user-attachments/assets/0091f800-ca92-4d50-b655-b436402d53f1)



Purpose of project is to maintain details of the students such as storing information about

1.Student id

2.Student Name

3.Roll no

4.DOB

5.Mail

6.Phone No

7.Address

8.Gender

9.Division

10.Semester

11.Year

12.Course

13.Department

14.Teacher


##**Technologies Used**

Python: The programming language for the project

MySQL: The database for storing student information and records.

Tkinter: For creating a simple graphical user interface (GUI).




**Prerequisites**

Python 3.x installed on your machine.
MySQL database server running.

Install required Python libraries using:
    pip install mysql-connector-python tkinter

    
**Database Setup**

**Create a new database in MySQL:
**

   CREATE DATABASE student_management;
    USE student_management;
    
   ** Create necessary tables:**


CREATE TABLE Students (

    student_id INT PRIMARY KEY AUTO_INCREMENT,
    name VARCHAR(255),
    address VARCHAR(255),
    phone_number VARCHAR(15),
    email VARCHAR(255),
    course VARCHAR(100),
    semester INT,
    attendance_percentage DECIMAL(5, 2)
);

CREATE TABLE Attendance (

    attendance_id INT PRIMARY KEY AUTO_INCREMENT,
    student_id INT,
    date DATE,
    status VARCHAR(10),
    FOREIGN KEY (student_id) REFERENCES Students(student_id)
);

CREATE TABLE Results (

    result_id INT PRIMARY KEY AUTO_INCREMENT,
    student_id INT,
    subject VARCHAR(100),
    marks INT,
    FOREIGN KEY (student_id) REFERENCES Students(student_id)
);



**Connecting the database**

def connect_to_db():

    return mysql.connector.connect(
        host="localhost",
        user="root",  # Your MySQL username
        password="mysql123",  # Your MySQL password
        database="student_management"
    )




**How the System Works**

**Add Data in Database**

**Update the Data**

**Delete data from Database**

**Reset Database**

**Search the details of the Student**


















