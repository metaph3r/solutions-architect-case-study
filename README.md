# Case Study

## Design objectives

### Scope

Develop an learning platform application for students and instructors.

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
2. Downtimes have to be avoided
3. Millions of users to be expected

## Architecture overview

### Kind of application

This will be a web application with views for desktop, mobile phones and tablets in mind.

### Technology stack

#### Frontend

The frontend will be implemented using Javascript with Angular framework.

#### Backend

The backend application server will be implemented with the Java Spring framework. Front end and backend will communicate via REST protocol.