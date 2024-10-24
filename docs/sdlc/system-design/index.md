# System Design  

## Overview   

B**ased on the requirements, architects and developers create high-level and detailed designs of the system**. This includes the architecture, database design, and user interface mockups. Technical Writers document the design specifications and data models to ensure developers and stakeholders have clear guidance on implementation.  


## Associated Documents: Deployment Guide  

System Design Document (SDD): Describes system components, interfaces, data models, and architectural diagrams.  

## Example  

A Data Flow Diagram (DFD) explaining how data moves within the system and a System Architecture Document that describes server infrastructure and client-server communication.  

### System Design Document (SDD) (Project Management System)  

!!! info ""  

    System Name: Project Nexus    
    Version: 1.0    
    Date: October 22, 2024    
    Author: Javier Martinez

### Overview  

Project Nexus is a cloud-based project management system designed to help teams organize, track, and manage project tasks. The system integrates task management, user collaboration, and reporting.

### System Architecture  

- Client Tier: A responsive web interface developed with React.js that interacts with the backend via RESTful APIs.
- Server Tier: Backend services developed with Node.js and Express.js, handling business logic and API requests.
- Database Tier: A relational database (MySQL) hosted on AWS RDS for storing project, task, and user data.

### Key Components  

1. User Authentication Module:  
> - OAuth 2.0 for user login and authorization.  
> - JWT-based token management for session handling.  
2. Task Management Module:  
> - Task creation, assignment, and tracking.  
> - Task dependencies with visual representation on Gantt charts.
3. Reporting Module:  
> - Real-time project status updates.  
> - Visual dashboards using Chart.js for performance tracking.  

### Data Flow  
_CONVERT INTO A DIAGRAM_  

- Client Request: The user sends a request (e.g., create task) from the React.js interface.
- Server Processing: The Node.js server processes the request and communicates with the database.
- Database Interaction: The MySQL database stores or retrieves the necessary data and responds to the server.
- Client Response: The processed data is returned to the client for rendering.



