

# Book Management System
BOOK MANAGEMENT SYSTEM
       - DRAFT VERSION 1.0
         - KARTHIKEYAN
##  Objective : 
Build an e-Books Collection Management Solutions

## Problem Statement:
The current challenge is to create a system that enables seamless management of books in a repository. This includes fundamental CRUD (Create,
Read, Update, Delete) operations while ensuring a user-friendly interface and robust backend support. The solution must also be deployable in modern,
scalable environments, catering to the needs of developers, users, and administrators
         
## Architecure Diagram :
 
![Example Image](https://github.com/karthikemssuppmail/bookMgmtSystem/blob/main/architecture.png)

## Cloud Native Architecture 
![Example Image](https://github.com/karthikemssuppmail/bookMgmtSystem/blob/main/cloud-native-solutions.png)

## Container Architecture
![Example Image](https://github.com/karthikemssuppmail/bookMgmtSystem/blob/main/ContainerArchitecture.jpg)


# High-Level Architecture:

### Frontend (ReactJS):
UI Layer: Users interact with the frontend built using ReactJS. It communicates with the backend (NodeJS) via API requests.
React Router: Manages routing for different pages such as book listings, adding books, editing details, etc.
Axios/Fetch: Used for making HTTP requests to the backend APIs.
Backend (NodeJS):

### API Layer: 
The NodeJS backend serves RESTful APIs for various CRUD operations, such as adding books, updating book information, and deleting records.
Express.js: The framework used to handle the API routing and requests.
Authentication & Authorization: JWT-based authentication or any other method is used for securing user access and managing roles (admin/user).
Database (AWS RDS):

### RDS Instance: 
AWS RDS (Relational Database Service) hosts the database (MySQL/PostgreSQL).
Data Layer: Stores the book details, user information, and other metadata.
Scalable and Fault-tolerant: The database should be scalable based on user traffic.

### Container Platform (AWS ECS/Fargate):
AWS ECS (Elastic Container Service) or AWS Fargate manages the backend services (NodeJS) in containers.
Containerization: Backend API services are containerized using Docker and deployed on ECS/Fargate for scalability, fault tolerance, and high availability.

### CI/CD Pipeline: 
Continuous Integration/Continuous Deployment via services like AWS CodePipeline or GitHub Actions to automate deployments.

### AWS Load Balancer:

Distributes incoming HTTP/HTTPS requests to different instances of the containerized backend (NodeJS) to ensure high availability and fault tolerance.
Cloud Infrastructure:

###  VPC (Virtual Private Cloud):
A secure network where all components (ReactJS, NodeJS, RDS, and ECS) communicate.
Security Groups: Controls access and limits traffic to and from the services.
IAM (Identity Access Management): Manages roles and permissions for different AWS services.
S3 Bucket (Optional):

If you plan to store and serve book covers or other media files, you can use AWS S3 to handle file storage.

# PROPOSED SOLUTIONS..
### 1. Front-End (User Interface)
The front-end of the system will be developed using ReactJS, allowing for a dynamic and responsive user interface.
React is a best choice for building modern web applications due to its speed, scalability, and ease of integration with
backend services.

### 2. Backend (Node.js Microservices)
The backend will be built using Node.js with a microservices architecture. Microservices will help maintain modularity,
making it easier to scale and manage specific functionalities as the system grows

### 3. Database & Data Management
The database layer will be managed using a combination of relational databases (SQL) and NoSQL databases.
A SQL database like PostgreSQL or MySQL will store structured data, including users, books, and transactions.
NoSQL DBs - MongoDB or DynamoDB (for cloud-native) could be used for semi-structured data such as logs, user
activity, and perhaps some non-critical metadata. NoSQL allows greater flexibility and can scale horizontally.

### 4. Search Functionality
To support fast, full-text searches for books, an Elasticsearch instance will be integrated into the system.
                              
### 5. Scalability and Cloud-Native Deployment

The system will be designed to run on cloud-native infrastructure using services like AWS, Google Cloud, or
Microsoft Azure. The key principles will include scalability, high availability, and fault tolerance.
Containerization: The backend services will be containerized using Docker, ensuring that they are portable and can
run in any environment (local, staging, or production).

Kubernetes will be used for container orchestration, enabling the system to scale horizontally based on demand and
ensuring that the services remain highly available.

### AWS Cloud Services:
   • Elastic Load Balancer (ELB): Manages incoming traffic and distributes it across multiple service instances.
   • CloudFront (CDN): Used to deliver static content such as images, book covers, and JavaScript files to users
      globally with low latency.
   • WAF (Web Application Firewall): Protects the system from common web exploits like SQL injection and cross-
      site scripting (XSS).
   • CloudWatch: Monitors the system's performance and generates logs and metrics that can be used for
      proactive monitoring and reporting.
                             
### 6. Security & Compliance
Security will be a core aspect of the system, ensuring that user data is safe and protected. We will implement the
following:

 • Authentication & Authorization:
   Use OAuth 2.0 and JWT tokens for user authentication and secure access control across the system
   
 • Data Encryption:All sensitive user data will be encrypted both in transit (using HTTPS) and at rest (using
   database-level encryption).
   
 • Web Application Firewall (WAF):A WAF will be deployed to prevent unauthorized access and attacks like
   cross-site scripting (XSS), SQL injection, and other malicious attacks.

### 7. Reporting & Analytics
The Reporting Service will integrate with AWS CloudWatch and other analytics tools to provide detailed insights into
user activity, transaction logs, and book status.
Real-Time Monitoring: Using CloudWatch, you can monitor system metrics, track errors, and identify bottlenecks in
real-time.


## DIFFERENCE BETWEEN CLIENT-SIDE RENDERING AND SERVER-SIDE RENDERING
 
Client-Side Rendering (CSR) means that the web page's content is loaded by the browser after the JavaScript
code is downloaded. Initially, the browser loads a basic page and then fetches data (like books or users) and
dynamically displays it. This leads to fast transitions between pages but can result in slower initial page load
times. CSR is commonly used in modern web apps like social media platforms because it allows for smooth
interactivity after the page loads.

Server-Side Rendering (SSR), on the other hand, means the server generates the full HTML of the page and
sends it to the browser. The browser simply renders the page right away, which makes the initial load faster and
better for SEO since search engines can easily read the content. However, every time you navigate to a new
page, the browser has to request the full HTML again from the server, which can be slower for interactions after
the page loads.
In simple terms, CSR is like building the page in the browser using JavaScript after the initial load, while SSR is
like getting a complete page from the server right away.

## JUSTIFICATION OF TECHNOLOGY STACK
 
The stack is carefully chosen to build a scalable, maintainable, and secure system. React and Node.js provide
a consistent JavaScript development experience, enabling faster development and easier integration. Material-
UI and React Router help streamline UI development and routing. Redux helps manage complex application
state, while Passport.js handles secure user authentication. The cloud-native approach with Docker and
Kubernetes ensures that the app is highly scalable and easy to deploy. All of this makes for an efficient and
flexible system that can scale as your Book Management System grows.


 ## SAMPLE USECASE DIAGRAM
 ![Example Image](https://github.com/karthikemssuppmail/bookMgmtSystem/blob/main/usecase.png)

