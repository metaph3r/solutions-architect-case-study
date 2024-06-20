# Case Study

This is the homework for the Udemy course [How To Become An Outstanding Solution Architect](https://www.udemy.com/share/101WJS3@lUbCm1Nf2kvKUyZW4_4gQLIjK0Ku1H1n9vr16CT0y-wiyy3vg1xoszHW5Ntz7JnJ/).

## Design objectives

### Scope

Develop a learning platform application for students and instructors.

The application should have the ability to log in as different users with different roles. Users are able to see courses they are applicable for.

Students can view the course lectures and ask questions to the instructor.

Instructors on the other hand can manage their courses and answer questions.

### Key audiance

Students - People who want to learn a new skill for their career or private endeavors.

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

    Use geo-redundant high-availability cloud service.
    
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

### Components

![Architectural Components](/doc/plantuml/out/components/components.png)

### Design considerations

The frontend will be implemented as Angular-Application running in the user browser. It will connect to the Backend services via a content delivery network.

The CDN will primarily cache the media data, especially the training videos, to provide fast access for the students.

In order to address the performance and availability requirements the backend will be split into different services. User and course management contain the business logic and the metadata and media service provide access to the business data.

The different services can be scaled independently to provide necessary performance and availability.

The main purpose of the API Gateway is to provide secure access to the underlying services.

### Business Entities

![Business Entities](/doc/plantuml/out/business-entities/business-entities.png)