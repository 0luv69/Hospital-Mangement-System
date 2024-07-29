# Hospital Management

**1. Project Overview**
===================

### 1.1 Introduction

The Hospital Management System is a web application designed to manage hospital operations efficiently. The system is built using Django for the back-end and HTML, CSS, and JavaScript for the front-end. The application provides distinct functionalites for three types of users: Hospital Admin, Doctor, and Patient.

### 1.2 Objectives

* Provide an intuitive platform for hospital administration, allowing for streamlined processes.
* Create a system where doctors can apply for positions and manage their patient appointments effectively.
* Enable patients to book appointments and manage their hospital interactions seamlessly.
* Automate billing and invoicing for discharged patients.

### 1.3 Features and Functionalities

### A. Admin

* **Doctor Management**: Register, view, approve, reject, or delete doctors applying for positions within the hospital.
* **Patient Management**: Admit, view, approve, reject, and discharge patients (discharge patients when treatment is completed).
* **Invoice Management**: Generate and download PDF invoices based on medicine costs, room charges, doctor fees, and additional expenses.
* **Appointment Management**: View, book, and approve patient appointments (approve appointments requested by patients).

### B. Doctor

* **Job Application**: Apply for a job within the hospital and log in only after approval from the hospital admin.
* **Patient Management**: View details of patients assigned by the admin, including symptoms, names, and mobile numbers. Access a list of patients who have been discharged (by admin).
* **Appointment Management**: View appointments booked by the admin. Delete appointments after attending to the patient.

### C. Patient

* **Account Management**: Create an account to seek admission to the hospital and log in only after approval from the hospital admin.
* **Doctor Information**: View assigned doctor’s details, including specialization, mobile number, and address.
* **Appointment Management**: Check the status of booked appointments (pending/confirmed by admin). Book appointments (approval required from admin).
* **Invoice Management**: View and download PDF invoices only after being discharged by the admin.

---

**User Manual**
===========

### How to Install

#### 1. Clone the Repository

* Open your terminal or command prompt.
* Navigate to the directory where you want to clone the repository.
* Run the following command:

```bash
git clone <repository-url>
```

Replace `<repository-url>` with the actual URL of your GitHub repository.

#### 2. Navigate to the Project Directory

* Change your directory to the newly cloned project:

```bash
cd hospital-management-system
```

#### 3. Create and Activate a Virtual Environment

* Create a virtual environment:

```bash
python -m venv env
```

* Activate the virtual environment:
  + On Windows:

```bash
.\env\Scripts\activate
```

  + On macOS/Linux:

```bash
source env/bin/activate
```

#### 4. Install Required Packages

* Install the required Python packages:

```bash
pip install -r requirements.txt
```

#### 5. Migrate the Database

* Run the following commands to apply the database migrations:

```bash
python manage.py makemigrations
python manage.py migrate
```

#### 6. Create a Superuser

* Create an admin account to access the admin panel:

```bash
python manage.py createsuperuser
```

#### 7. Run the Development Server

* Start the Django development server:

```bash
python manage.py runserver
```

* Open your web browser and navigate to `http://127.0.0.1:8000` to access the application.

---

### How to Use

#### Admin User

* **Signup/Login**:
  + Navigate to the admin signup page to create an admin account.
  + Use the admin login page to log in with the created admin account.
* **Dashboard**:
  + Manage doctors, patients, and appointments.
  + Approve or reject doctor and patient requests.
  + Discharge patients and generate invoices.
  + Approve or reject appointment requests.

#### Doctor User

* **Signup/Login**:
  + Navigate to the doctor signup page to apply for a job.
  + Use the doctor login page to log in after approval by the admin.
* **Dashboard**:
  + View assigned patients and their details.
  + Manage appointments.
  + View discharged patients.

#### Patient User

* **Signup/Login**:
  + Navigate to the patient signup page to create an account.
  + Use the patient login page to log in after approval by the admin.
* **Dashboard**:
  + View assigned doctor details.
  + Book and manage appointments.
  + View and download invoices after discharge.

---

## Drawbacks/LoopHoles

- Any one can be Admin. There is no Approval required for admin account. So you can disable admin signup process and use any logic like creating superuser.
- There should be at least one doctor in hospital before admitting patient. So first add doctor.
- On update page of doctor/patient you must have to update password.

---

## Disclaimer

This project is developed for demo purpose and it's not supposed to be used in real application.
