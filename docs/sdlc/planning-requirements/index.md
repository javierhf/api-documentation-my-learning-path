# Planning and Requirements  

## Overview    

**In this phase, the project's goals, objectives, scope, and potential risks are identified**. Stakeholders and teams gather functional and non-functional requirements for the system. Technical writers collaborate with stakeholders, engineers, and product owners to document the business requirements, technical specifications, and scope of work.  


## Associated Documents: Requirements Specification Document  

Requirements Specification Document (RSD): This outlines the system's functional and non-functional requirements.    

## Example  

A Requirements Specification Document for an E-commerce Platform.  

### Requirements Specification Document for an E-commerce Platform    

#### Overview    

!!! info ""  

    Project Name: ShopMaster  
    Version: 1.0  
    Author: Javier Martinez  
    Date: October 22, 2024



ShopMaster is an e-commerce platform that allows users to browse products, add items to the cart, and complete purchases. The system will support online payments, user accounts, and order tracking.  

#### Functional Requirements    

| Requirement | Description |  
|---------------- | --------------- |    
| **User Registration** | <ul><li>The system must allow users to create an account with an email and password.</li><li>A confirmation email should be sent to the user upon registration.</li></ul> |  
| **Product Browsing** | <ul><li>Users should be able to browse products by category and search by name or SKU.</li><li>The system must display product details including name, description, price, and stock availability.</li><ul> |  
| **Shopping Cart** |  <ul><li>Users can add and remove products from the cart.</li><li>The system will update the total price as items are added or removed.</li></ul> |  
| **Checkout** | <ul><li>The system will guide the user through the checkout process.</li><li>Payment integration with Stripe or PayPal must be supported.</li><ul> |  
| **Order Management** | Users should be able to view their past orders and track current orders through the system. |

#### Non-Functional Requirements    

|Requirement | Description |  
| ------------- | ------------ |  
| **Performance** | The system must handle up to 10,000 concurrent users without performance degradation. |  
| **Security** |  User passwords must be stored using bcrypt hashing, and sensitive information (e.g., payment details) must be encrypted. |


