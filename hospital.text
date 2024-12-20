CREATE TABLE Doctors (
    DoctorId BIGINT(50) UNSIGNED NOT NULL AUTO_INCREMENT PRIMARY KEY,
    Name VARCHAR(50) NOT NULL,
    Specialization VARCHAR (50) NOT NULL,
    Phone VARCHAR (50) NOT NULL,
    DepartmentID BIGINT UNSIGNED NOT NULL,
    FOREIGN KEY (`DepartmentID`) REFERENCES `Departments`(`DepartmentID`) ON DELETE RESTRICT ON UPDATE CASCADE

);

CREATE TABLE Departments (
    DepartmentID BIGINT UNSIGNED NOT NULL AUTO_INCREMENT PRIMARY KEY,
    Name VARCHAR(50) NOT NULL,
    Location VARCHAR (50) NOT NULL
    
);

CREATE TABLE Patients (
    PatientId BIGINT(50) UNSIGNED NOT NULL AUTO_INCREMENT PRIMARY KEY,
    Name VARCHAR(50) NOT NULL,
    Age VARCHAR(50) NOT NULL,
    Gender VARCHAR (50) NOT NULL,
    Phone VARCHAR (50) NOT NULL
);


CREATE TABLE Appointments (
    AppointmentId BIGINT(50) UNSIGNED NOT NULL AUTO_INCREMENT PRIMARY KEY,
    Date DATETIME NOT NULL,
    Time DATETIME  NOT NULL,
    Status VARCHAR (50) NOT NULL,
    PatientID BIGINT UNSIGNED NOT NULL,
    DoctorID BIGINT UNSIGNED NOT NULL,
    FOREIGN KEY (`PatientID`) REFERENCES `Patients`(`PatientID`) ON DELETE RESTRICT ON UPDATE CASCADE,
    FOREIGN KEY (`DoctorID`) REFERENCES `Doctors`(`DoctorID`) ON DELETE RESTRICT ON UPDATE CASCADE

);


CREATE TABLE Doctor_Patient (
    PatientID BIGINT UNSIGNED NOT NULL,
    DoctorID BIGINT UNSIGNED NOT NULL,
    PRIMARY KEY (PatientID, DoctorID),
    FOREIGN KEY (`PatientID`) REFERENCES `Patients`(`PatientID`) ON DELETE RESTRICT ON UPDATE CASCADE,
    FOREIGN KEY (`DoctorID`) REFERENCES `Doctors`(`DoctorID`) ON DELETE RESTRICT ON UPDATE CASCADE

);

INSERT INTO `departments`(`DepartmentID`, `Name`, `Location`) 
VALUES 
('1', 'Cardiology', 'Building A'),
('2', 'Neurology', 'Building B'),
('3', 'Orthopedics', 'Building C'),
('4', 'Pediatrics', 'Building D'),
('5', 'General Medicine', 'Building E');

INSERT INTO `doctors`(`DoctorId`, `Name`, `Specialization`, `Phone`, `DepartmentID`) 
VALUES 
('1', 'Dr. Alice', 'Cardiology', '123-456-7890', '1'),
('2', 'Dr. Bob', 'Neurology', '987-654-3210', '2'),
('3', 'Dr. Carol', 'Orthopedics', '555-555-5555', '3'),
('4', 'Dr. David', 'Pediatrics', '444-444-4444', '4'),
('5', 'Dr. Eve', 'General Medicine', '333-333-3333', '5');



INSERT INTO `patients`(`PatientId`, `Name`, `Age`, `Gender`, `Phone`) 
VALUES 
('1', 'John Doe', '45', 'Male', '123-111-1234'),
('2', 'Jane Smith', '30', 'Female', '234-222-2345'),
('3', 'Sam Wilson', '60', 'Male', '345-333-3456'),
('4', 'Emily Davis', '25', 'Female', '456-444-4567'),
('5', 'Michael Brown', '50', 'Male', '567-555-5678');


INSERT INTO `appointments`(`AppointmentId`, `Date`, `Time`, `Status`, `PatientID`, `DoctorID`) 
VALUES 
('1', '2024-12-20', '10:00:00', 'Scheduled', '1', '1'),
('2', '2024-12-21', '11:30:00', 'Scheduled', '2', '2'),
('3', '2024-12-22', '09:00:00', 'Completed', '3', '3'),
('4', '2024-12-23', '14:00:00', 'Canceled', '1', '2'),
('5', '2024-12-24', '16:00:00', 'Scheduled', '2', '3');



INSERT INTO `doctor_patient`(`PatientID`, `DoctorID`) 
VALUES 
('1', '1'), 
('2', '2'),
('3', '3'), 
('4', '4'), 
('5', '5');