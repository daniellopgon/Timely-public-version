# TIMELY

## Description
Timely is a clean architecture-based web platform for HR management. It allows employees to log their work hours and breaks, request vacations or permissions, and submit entry/exit modifications using modern software development practices.

It features a role-based system:

- **Employees:** Register attendance, request vacations or modifications.  
- **Managers:** Approve/reject requests, view employee stats.  
- **Admin:** Manage companies and employees for security purposes.

---

## Tech Stack
- Java 17  
- Spring Boot 3.4.3 (REST API, Security, JPA)  
- MariaDB  
- Maven  
- Lombok, OpenCSV  
- JUnit & Mockito (Testing)  
- Clean Architecture & Domain-Driven Design  

---

## Key Features
- HR Management Actions (attendance, vacations, permissions)  
- Reports & Statistics for managers  
- Secure Authentication (Spring Security & JWT)  
- Clean Architecture implementation  
- Responsive Web Design  

---

## Architecture & Project Structure

### Clean Architecture Structure
```text
src/main/java/com/comerziotech/timely/
├── domain/ # Business Logic Layer
│ ├── model/ # Domain Entities
│ ├── repository/ # Repository Interfaces
│ ├── service/ # Domain Services
│ └── exception/ # Domain Exceptions
├── application/ # Use Cases Layer
│ ├── port/
│ │ ├── in/ # Input Ports (Use Cases)
│ │ └── out/ # Output Ports
│ ├── service/ # Application Services
│ └── dto/ # Data Transfer Objects
└── infrastructure/ # Framework Layer
├── controller/ # REST Controllers
├── persistence/ # Data Persistence
├── config/ # Configuration
└── web/ # Web Configuration
```

### Architecture Benefits
- **Separation of Concerns:** Clear boundaries between business logic and infrastructure  
- **Testability:** Easy unit testing of domain logic  
- **Maintainability:** Changes in one layer don't affect others  
- **Scalability:** Easy to add new features and technologies  

---

## Domain Models
- **Employee:** User management with role-based access  
- **Checkin:** Attendance tracking with timestamps  
- **Enterprise:** Company organization structure  
- **Schedule:** Work schedule management  
- **Holidays:** Vacation and time-off management  
- **Permits:** Permission request workflow  

---

## Frontend Structure
```text
src/main/resources/
├── static/
│ ├── css/
│ │ ├── base/ # Base styles & variables
│ │ ├── components/ # Reusable components
│ │ └── pages/ # Page-specific styles
│ ├── js/
│ │ ├── services/ # API communication
│ │ ├── components/ # UI components
│ │ ├── utils/ # Utility functions
│ │ └── pages/ # Page-specific logic
│ └── images/ # Assets & icons
└── templates/
├── fragments/ # Reusable HTML fragments
├── components/ # UI components
└── pages/ # Main application pages
```

---

## Recruiter Access
This is a private repository.  
If you'd like to review the code, please contact me via LinkedIn or email at **daniel.lopgon.4@gmail.com** and I will grant temporary access.

---

## Screenshots

### Login Screen  
On this screen, you need to log in. Depending on your role, you will be redirected to the corresponding home screen.

![Login Screen](login-screen.png)

---

### Employees Screen  
Here you can register your check-in, check-out, and breaks. Your assigned work schedule is also displayed.  
This screen is designed to be simple and user-friendly to minimize errors.

![Employees Screen](employees-screen.png)

---

### Dynamic Buttons  
The check-in and check-out buttons are dynamic:

- After checking in, the buttons change to allow starting or ending breaks.  
- Once a break is finished, you can either start another break or check out.  

This design ensures simplicity and a clean UI.

![Dynamic Buttons](dynamic-buttons.png)

---

### Vacation Request Page  
Displays a history of vacation requests with start and end dates.  
Approved requests are shown in green, while pending ones appear in blue.  
Requests are sent to managers, who can approve or reject them.  
Includes a calendar view where granted or pending vacations are visually displayed.

To request a vacation, simply select the start and end date directly on the calendar.

![Vacation Page](vacation-page.png)

---

### Permission Request Page  
Similar to the vacation request page but includes an additional field for the reason for the request.  
In the future, it could differentiate between paid and unpaid permissions.

![Permission Page](permission-page.png)

---

### Check-in Modification Page  
Here, employees can:

- Edit their check-in or check-out times.  
- Adjust break times.  
- Add missing entries if they forgot to check in.

![Check-in Modification](checkin-modification.png)

---

### Manager Interface  
The Manager Interface provides a comprehensive platform for employee management.  
From this page, you can:

- Search for employees by name or email.  
- Approve or reject vacation requests, permissions, and check-in/check-out modifications.  
- View aggregated reports of your employees' activity and export them in CSV format for further analysis.

**Employee Selection**  
![Employee Selection](employee-selection.png)

**Dashboard Overview**  
![Dashboard Overview](dashboard-overview.png)

**Approve or Reject Requests**  
![Approve or Reject Requests](approve-or-reject-requests.png)

---

## Getting Started

### Prerequisites
- Java 17  
- Maven 3.6+  
- MariaDB  

### Installation
1. Configure database connection in `application.yml`  
2. Run:
   ```bash
   mvn spring-boot:run
Access the application at http://localhost:8080

Build
bash
Copiar código
mvn clean install
License
This project is developed for educational purposes as part of academic coursework.

Author
Daniel López
Email: daniel.lopgon.4@gmail.com
LinkedIn: Daniel López

This project demonstrates modern software development practices including Clean Architecture, Domain-Driven Design, and responsive web development.
