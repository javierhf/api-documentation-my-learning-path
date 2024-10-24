# Software Development Life Cycle    

## Overview        

**The Software Development Life Cycle (SDLC) is a framework that defines the stages involved in the development and maintenance of software applications**. Each phase produces specific outputs or documents, often guided or supplemented by technical writers. Below is a breakdown of each SDLC step, its process, and examples of associated technical writing documents.  

**The stages of the SDLC** are the following:  

1. Planning/Requirements Gathering  
2. System Design  
3. Implementation/Coding  
4. Testing  
5. Deployment  
6. Maintenance  
7. End-user Training and Documentation    

!!! info "Info"  

    Each SDLC phase requires its own set of documentation, and technical writers play an essential role in ensuring the clarity and accuracy of these documents, making it easier for teams to collaborate and for users to interact with the system.  


### SDLC Details 

The following table disclose each stage with more details:  

| Stage | Description | Technical Writer | Documents |  
|---------- | ------------ | ----------- |--------------- |  
| **Planning/Requirements Gathering** | In this phase, the project's goals, objectives, scope, and potential risks are identified. Stakeholders and teams gather functional and non-functional requirements for the system. | Technical writers collaborate with stakeholders, engineers, and product owners to document the business requirements, technical specifications, and scope of work. | *Requirements Specification Document (RSD)*: This outlines the system's functional and non-functional requirements.<br><br>Example: A Business Requirements Document (BRD) that details what the end-users expect from the system. |    
| **System Design** | Based on the requirements, architects and developers create high-level and detailed designs of the system. This includes the architecture, database design, and user interface mockups. | Writers document the design specifications and data models to ensure developers and stakeholders have clear guidance on implementation. |  *System Design Document (SDD)*: Describes system components, interfaces, data models, and architectural diagrams.<br><br>Example: A Data Flow Diagram (DFD) explaining how data moves within the system and a **System Architecture Document that describes server infrastructure and client-server communication. |   
| **Implementation/Coding** | The actual development of the software takes place. Developers write code, build features, and conduct initial unit testing. | Writers create developer-focused documentation, such as API references or code integration guides, and collaborate on in-line code comments. | *API Documentation*: Details how to use and integrate with the system’s APIs.<br><br>Example: A REST API Guide for integrating an external payment service with your system, detailing endpoints, request/response formats, and authentication. |   
| **Testing** | The system undergoes various forms of testing, such as unit, integration, system, and acceptance testing, to identify bugs and ensure all requirements are met. | Writers help create testing plans and document known issues or test results. | *Test Case Document*: Defines how to verify that each function or feature meets the requirements.<br><br>Example: A Test Plan for ensuring that the user authentication feature works correctly, detailing the different test cases, expected outcomes, and pass/fail criteria. |   
| **Deployment** | The software is delivered to the production environment, and it is made available to end-users. |  Writers assist in creating deployment guides and documenting configuration settings, upgrade paths, and rollback procedures. | *Deployment Guide*: Instructions on how to install, configure, and deploy the software to the production environment.<br><br>Example: A Cloud Deployment Manual for installing the application on AWS, covering steps for server setup, load balancing, and environment configuration. |  
| **Maintenance** |After deployment, the system is monitored, and any issues are addressed with patches or updates. New features may be added in future iterations. | Writers help with user guides, troubleshooting documentation, and release notes for future versions. | *Release Notes*: Summarize new features, bug fixes, and known issues for each new version.<br><br>Example: A Release Notes document for version 1.2.0, listing new features, fixed bugs, and deprecated functions. |  
| **End-User Training & Documentation** | As part of the rollout, end-users are trained on the new system through tutorials or training sessions. | Writers create user guides, FAQs, video tutorials, and other materials to facilitate learning. | *User Manual*: Guides users on how to operate the system.<br><br>Example: A Getting Started Guide for an e-commerce platform that explains how users can create accounts, browse products, and complete purchases. |  


## The API First Approach   

**The API First approach places the design and specification of an API at the forefront of the development process**. Instead of creating APIs as an afterthought to meet the needs of other parts of an application, the API is treated as a product from the beginning, guiding the entire software development lifecycle (SDLC). This ensures that the API is well-thought-out, meets the needs of its consumers, and evolves in a structured manner.   

By creating a clear and detailed OpenAPI specification early on, developers and stakeholders can work from a shared understanding, reducing misunderstandings and improving collaboration.

**The SDLC under the API First approach involves several key phases** as listed below:   

1. Planning - where business goals and API requirements are defined.  
2. Design - where the API is described using a formal OpenAPI spec.  
3. Contract finalization - where the API specification becomes a binding agreement between developers and consumers. Development proceeds based on this specification, ensuring that the implementation aligns with what has been agreed upon.  
4. Testing and quality assurance - Test are performed before the API is deployed and monitored in production.   
  
  
**The API is continuously improved post-release**, with an emphasis on maintaining documentation, monitoring performance, and supporting versioning as needed.  

### A Closer Look

The following table provides a summarized view of the "API First" development cycle:    

| Stage | Goal | Steps | Deliverables |  
|------ | ----- | ----- | ------------ |   
| **Planning and Ideation** | Identify business requirements and the purpose of the API. | <ol><li>Meet with stakeholders to define use cases and gather requirements.</li><li>Identify the target audience (internal teams, partners, or external developers).</li><li>Draft initial API requirements, focusing on core features.</li></ol> | <ul><li>High-level API requirements.</li><li>Use case definitions.</li><ol> |  
| **API Design (OpenAPI Specification)** | Design the API using the OpenAPI specification before any development starts. |<ol><li>Create an OpenAPI spec (YAML or JSON) to define endpoints, methods (e.g., `GET`, `POST`), request parameters, and response formats.</li><li>Collaborate with stakeholders to validate the API contract.</li><li>Iterate and refine the design based on feedback from consumers.</li><ol> | <ol><li>OpenAPI spec (v1.0) describing all endpoints, data models, and security requirements.</li><li>Mock server or documentation preview (e.g., using Swagger UI) for consumer feedback.</li></ol> |  
| **API Contract Finalization** | Establish the API contract as a binding agreement between the API provider and consumers. | <ol><li>Share the OpenAPI spec with consumers for early integration testing.</li><li>Freeze the API contract once feedback is incorporated.</li></ul> | <ul><li>Finalized API contract with stakeholder approval.</li><li>Mock server for developers to simulate interactions.</li><ul> |  
| **Development** |Implement the API backend following the agreed API contract. | <ol><li>Generate server-side code using OpenAPI tools (e.g., Swagger Codegen).</li><li>Implement business logic and integrate it with data sources.</li><li>Conduct unit tests to ensure individual components work as expected.</li><li>Use mock servers for early testing of API consumers.</li></ol> | <ul><li>Backend code implementation.</li><li>Unit test coverage.</li></ul> |  
| **Testing and Quality Assurance** | Ensure the API meets functional and non-functional requirements. | <ol><li>Perform contract testing to verify the API adheres to the OpenAPI spec.</li><li>Conduct integration tests with real data and external services.</li><li>Perform security testing, including authentication and authorization.</li>Conduct performance testing (load, stress, etc.) to verify scalability.</li><ol> | <ul><li>Test results (unit, integration, performance, and security).</li><li>Fixes and optimizations based on test outcomes.</li></ul> |   
| **Documentation and Developer Experience** | Provide comprehensive and user-friendly API documentation. |<ol><li>Auto-generate interactive documentation from the OpenAPI spec using tools like **Swagger UI** or **Redoc**.</li><li>Include examples, usage guides, and response formats.</li><li>Publish SDKs and client libraries if applicable.</li></ul> | <ul><li>Interactive API documentation.</li><li>API examples and usage guides.</li><li>Client SDKs (if applicable).</li></ul> |  
| **Deployment** | Release the API to a production environment. | <ol><li>Deploy the API to a staging environment for final acceptance testing.</li><li>Set up monitoring tools to track API performance and availability (e.g., Prometheus, Grafana).</li><li>Deploy the API to production, ensuring rollback strategies are in place.</li></ol> | <ul><li>Production-ready API.</li><li>Monitoring dashboards.</li></ul> |  
| **Post-Release Monitoring and Maintenance** | Continuously monitor and improve the API after release.  | <ol><li>Monitor API usage, performance, and errors in real-time.</li><li>Apply patches and fixes to address any issues.</li><li>Gather feedback from API consumers and prioritize future improvements.</li><li>Plan for versioning and deprecate old versions as needed.</li></ol> | <ul><li>Logs and performance metrics.</li><li>Bug fixes and feature enhancements.</li><li>API versioning strategy.</li></ul> |
