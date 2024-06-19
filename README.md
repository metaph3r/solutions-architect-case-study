# Case Study

## Design objectives

### Scope

Develop a learning platform application for students and instructors.

The application should have the ability to log in as different users with different roles. Users are able to see courses they are applicable for.

Students can view the course lectures and ask questions to the instructor.

Instructors on the other hand can manage their courses and answer questions.

### Key audiance

Students - People who want to learn a new skill for their career or private endeavours.

Instructor - People who host their courses on the platform and provide feedback to the students.

### Use cases

![Use cases](/doc/plantuml/out/use-cases/use-cases.png)

### Activities

#### Students

![Student activities](/doc/plantuml/out/student-activities/student-activities.png)

#### Instructors

![Instructor activities](/doc/plantuml/out/instructor-activities/instuctor-activities.png)

### Constraints

#### Technical

1. Lectures need to load within 1 second

    Use high-performance cloud service.
    
2. Downtimes have to be avoided

    Use geo-reduntant high-availability cloud service.
    
3. Millions of users to be expected

    Use scalable cloud environment with distributed content delivery network.

## Architecture overview

### Kind of application

This will be a web application with views for desktop, mobile phones and tablets in mind.

### Technology stack

#### Frontend

The frontend will be implemented using Javascript with Angular framework.

#### Backend

The backend application server will be implemented with the Java Spring framework. Front end and backend will communicate via REST protocol.