# EduConsultPro - Salesforce CRM for Educational Institutions

![Salesforce](https://img.shields.io/badge/Salesforce-00A1E0?style=for-the-badge&logo=Salesforce&logoColor=white)

## Overview

EduConsultPro is a comprehensive Salesforce CRM solution tailored for educational institutions. It streamlines the entire student lifecycle, from initial inquiry and enrollment to ongoing support. This centralized platform manages courses, consultants, student data, appointments, and communication effectively.


## Demonstration

[![EduConsultPro Demo](http://img.youtube.com/vi/tdC1aOKQyfY/0.jpg)](https://www.youtube.com/watch?v=tdC1aOKQyfY "EduConsultPro Demonstration Video")


Watch the video above for a complete demonstration of EduConsultPro's features and functionality.
## Key Features

* **Student Admission Management:**
    * Automated application process
    * Course selection and registration
    * Automated email notifications
    * Comprehensive student data management

* **Appointment Scheduling:**
    * Consultant booking system
    * Automated approval process
    * Timely email notifications
    * Integrated calendar management

* **Case Management:**
    * Immigration support
    * Visa application tracking
    * Student support ticketing system

* **Course Management:**
    * Comprehensive course catalog
    * Registration tracking
    * Student enrollment management


## Technical Architecture

### Custom Objects

* `Student`
* `Course`
* `Consultant`
* `Appointment`
* `Registration`

### Object Relationships

* `Appointment` → `Student` (Lookup)
* `Appointment` → `Consultant` (Lookup)
* `Registration` → `Student` (Lookup)
* `Registration` → `Course` (Lookup)
* `Student` → `Case` (Lookup)


### Automation

* **Flows:**
    * **Student Admission Flow:**  Handles student information collection, course selection, registration, and email notifications.
    * **Appointment Booking Flow:** Manages student verification, consultant selection, appointment scheduling, and approval initiation.
    * **Combined Master Flow:**  Provides a unified interface, routing new/existing students and directing them to the appropriate process.

* **Approval Processes:**  Appointment approval workflow with manager-based routing and email notifications for submissions, approvals, and rejections.


* **Apex Triggers:**
    * **`StudentTrigger`:**  This trigger automatically creates a welcome case when a new student record is inserted.  The case is used to track the student's onboarding process.
    * **`AppointmentTrigger`:** This trigger performs the following actions:
        * **Before Insert/Update:** Validates that appointments are scheduled during business hours (9 AM to 5 PM) and that the chosen consultant is available at the requested time.
        * **After Insert:** Sends email notifications to both the student and the consultant confirming the newly scheduled appointment.
### User Interface

* **Lightning Components:**
    * Custom Lightning App: "EduConsultPro"
    * Custom Home Page for optimized user experience
    * Streamlined navigation with essential tabs


## Setup Instructions

1. **Object Creation:**
    * Import `Course` object and data.
    * Import `Consultant` object and data.
    * Import `Student` object and data.
    * Create necessary relationship fields between objects.

2. **User Configuration:**
    * Create users with the "Standard Platform User" profile.
    * Configure user hierarchies for approval processes.

3. **Flow Deployment:**
    * Deploy the `Student Admission Flow`.
    * Deploy the `Appointment Booking Flow`.
    * Deploy the `Combined Master Flow`.

4. **Lightning App Setup:**
    * Deploy the `EduConsultPro` Lightning App.
    * Configure home page layouts for optimal user experience.
    * Assign user permissions for app access.


## Custom Settings

### Case Object Configuration

* **Type Field Values:**  `Immigration`, `Visa Application`
* **Status Field Values:** `Open`, `In-Progress`, `Closed`



## Features in Detail

### Student Admission Process

1. Student completes the admission form.
2. Student selects desired courses.
3. System automatically creates the registration record.
4. Confirmation email is sent to the student.
5. Student record is created in Salesforce.

### Appointment Management

1. System verifies student information.
2. Consultant availability is checked.
3. Appointment is scheduled based on availability.
4. Appointment is submitted for manager approval.
5. Email notifications are sent throughout the process.


## System Requirements

* Salesforce Enterprise Edition or higher
* System Administrator profile for initial setup
* Standard Platform User license for end users


## Author

**MOKA MANOJ KUMAR**<br>
Gayatri Vidya Parishad College of Engineering(A), Visakhapatnam<br>
Roll Number: 21131A05C3<br>
Email: 21131a05c3@gvpce.ac.in


## License

This project is licensed under the MIT License - see the [LICENSE.md](LICENSE.md) file for details.

## Acknowledgments

* Gayatri Vidya Parishad College of Engineering
* Salesforce Development Team
* Project Mentors and Guides


---

*Note: This README is part of an academic project demonstrating Salesforce CRM implementation for educational institutions.*
