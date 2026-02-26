CREATE DATABASE COMPLAINT_MANAGMENT;
USE COMPLAINT_MANAGMENT;
CREATE TABLE Category (
    Category_ID INT PRIMARY KEY,
    Category_Name VARCHAR(100),
    Department VARCHAR(100),
    Priority_Level VARCHAR(50),
    SLA_Days INT
);
CREATE TABLE User (
    User_ID INT PRIMARY KEY,
    Name VARCHAR(100),
    Email VARCHAR(100) UNIQUE,
    Phone_No VARCHAR(20),
    Address TEXT
);
CREATE TABLE Admin (
    Admin_ID INT PRIMARY KEY,
    Name VARCHAR(100),
    Email VARCHAR(100) UNIQUE,
    Role VARCHAR(50),
    Work_Shift VARCHAR(50)
);
CREATE TABLE Complaint (
    Complaint_ID INT PRIMARY KEY,
    Title VARCHAR(255),
    Description TEXT,
    Date_Filed DATE,
    Status VARCHAR(50),
    User_ID INT,
    Category_ID INT,
    Admin_ID INT,
    FOREIGN KEY (User_ID) REFERENCES User(User_ID),
    FOREIGN KEY (Category_ID) REFERENCES Category(Category_ID),
    FOREIGN KEY (Admin_ID) REFERENCES Admin(Admin_ID)
);
CREATE TABLE Resolution (
    Resolution_ID INT PRIMARY KEY,
    Solution_Type VARCHAR(100),
    Feedback TEXT,
    Date_Resolved DATE,
    Remarks TEXT,
    Complaint_ID INT UNIQUE,
    Admin_ID INT,
    FOREIGN KEY (Complaint_ID) REFERENCES Complaint(Complaint_ID),
    FOREIGN KEY (Admin_ID) REFERENCES Admin(Admin_ID)
);
INSERT INTO Category VALUES (1, 'Technical', 'IT', 'High', 2), (2, 'Billing', 'Finance', 'Medium', 5);
INSERT INTO User VALUES (101, 'Alice Smith', 'alice@email.com', '555-0101', '123 Maple St');
INSERT INTO Admin VALUES (501, 'Charlie Brown', 'charlie@company.com', 'Senior Lead', 'Morning');
INSERT INTO Complaint VALUES (1001, 'Internet Outage', 'Connection lost.', '2026-02-20', 'Resolved', 101, 1, 501);
INSERT INTO Resolution VALUES (9001, 'On-site Repair', 'Fixed fiber.', '2026-02-21', 'Verified.', 1001, 501);
SELECT * FROM COMPLAINT;


SHOW TABLES;
SELECT*FROM COMPLAINT;



