Here's a README based on the project details you provided:

---

# Hospital Management System

This project is a **Hospital Management System** developed as part of the **Database Systems** course. It is implemented using **C#** on **Visual Studio** with the **.NET framework**, utilizing an **Oracle database** for backend management. The system provides functionality for managing hospital staff, patients, appointments, and support tasks in an organized and efficient manner.

## Features

### 1. **User Management**
   - **Roles**: Admin, Employees (Doctors, Nurses), Patients.
   - **Registration**: Forms for registering new users (employees and patients).
   - **Login System**: Authentication based on roles, allowing access to different parts of the system depending on the user's role.

### 2. **Profile Management**
   - Admins can view and update user profiles.
   - Employee and patient profiles are linked to their user credentials and other hospital records.

### 3. **Appointments**
   - Admins and employees can view, schedule, and manage appointments.
   - Appointments are linked to both **patients** and **employees (doctors/nurses)** with details like scheduled time, purpose, and status.

### 4. **Employee Management**
   - Admins can manage employee details such as department, position, salary, and hire date.
   - New employees are registered into the system with automatic assignment of unique IDs using **sequences** in Oracle.
   - Deletion of employees cascades to the deletion of their profiles and user credentials.

### 5. **Patient Management**
   - Admins can manage patient information including medical history, and personal details.
   - A detailed medical history can be stored for each patient.

### 6. **Customer Support**
   - A ticketing system where patients and employees can submit support issues.
   - Support tickets track the issue description, submission date, and current resolution status.

### 7. **Prescriptions**
   - Doctors can issue prescriptions linked to patient profiles.
   - Details include the medication prescribed, dosage, and usage instructions.

### 8. **Reports**
   - Admins can generate reports such as **Salary Reports** for employees using the **iTextSharp** library to convert data into PDFs.
   
## Database Structure

The system uses an Oracle database with the following key tables:
- **Users Table**: Stores user credentials (UserID, Username, Password, RoleID).
- **Profiles Table**: Stores user profile information (ProfileID, FirstName, LastName, etc.).
- **Employees Table**: Stores employee-specific details like department, salary, and position.
- **Patients Table**: Stores patient-specific information like medical history.
- **Appointments Table**: Links employees and patients for scheduling purposes.
- **CustomerSupport Table**: Tracks support tickets submitted by users.
- **Prescriptions Table**: Records prescriptions issued by doctors.

### Database Sequences
- **USER_ID_SEQ, EMPLOYEE_ID_SEQ, PATIENT_SEQ**: Used for auto-generating primary keys for respective tables.

### Triggers
- Multiple triggers ensure the automatic generation of primary keys during insertions for tables like Users, Profiles, and Patients.

## Forms

### 1. **Login Form** (`Form1.cs`)
   - Allows users to log in with their credentials.
   - Directs users to the appropriate dashboard (Admin, Employee, Patient) based on their role.

### 2. **Registration Form** (`RegistrationForm.cs`)
   - Used for registering new patients and employees.
   - Submits data to the Oracle database.

### 3. **Admin Dashboard** (`Admin.cs`)
   - Admins can view and manage employees, patients, and hospital data.
   - Includes functionality for generating reports (e.g., salary reports) in PDF format.

### 4. **Manage Employees Form** (`ManageEmployee.cs`)
   - Allows admins to add, update, and delete employee records.
   - Includes a grid view for displaying current employee data and a department selection combo box.

### 5. **Appointments Management Form** (`Appointments.cs`)
   - Displays scheduled appointments and allows for adding, updating, and deleting appointments.
   - Linked to both patient and employee (doctor) records.

## Installation and Setup

1. Clone this repository.
2. Open the project in **Visual Studio**.
3. Make sure you have **Oracle database** set up and running.
4. Update the connection string in the `App.config` file with your Oracle database credentials.
5. Run the application in **Visual Studio**.

## Technologies Used
- **C# (.NET Framework)**
- **Oracle Database**
- **iTextSharp** (for PDF generation)
- **Visual Studio** (IDE)

## Contributors
- **Tayyab Khan** (22F-3440)
- **Muhammad Azam** (22F-8766)

## License
This project is for educational purposes as part of the Database Systems course.

---
