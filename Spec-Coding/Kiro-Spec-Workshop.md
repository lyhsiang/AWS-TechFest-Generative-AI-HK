# 🚀 Kiro Spec Workshop: Hands-On Exercises

## Introduction

In this section, you will learn how to use Kiro in a spec-driven development style. Unlike vibe coding where you give high-level instructions and let Kiro figure everything out, spec coding involves creating detailed specifications that break down complex features into manageable, well-defined tasks. This approach provides better control, documentation, and iterative development for complex projects.

Kiro's Spec feature allows you to formalize the design and implementation process by iterating on requirements, design, and implementation tasks with structured documentation before letting the agent work through the implementation.

This is a fully hands-on workshop. Through a series of exercises, you will design, develop, and deploy the same webshooting game as the vibe coding workshop, but using a more structured, specification-driven approach. By the end, you'll have a fully functional chatbot with text, image, and voice capabilities, secured with user authentication.

### Setup
Create a folder named `MyShootingGame` and open it in Kiro. Instead of starting with vibe coding, we'll create a comprehensive specification first.

In the Let's build page, select **Spec** instead of Vibe. This will open the spec creation interface.

## 📋 Prerequisites

- AWS account with full permissions
- Configured AWS CLI

## 🚀 Step-by-Step Guide

### 📋 Prerequisites

- Installed and running Kiro IDE
- AWS account with S3 and CloudFront access permissions
- Configured AWS CLI (for deployment)

### Step 1: Create Project Folder

- On your computer, create a folder named `MyShootingGame`
- This will become the project workspace for your shooting game application

### Step 2: Open Project in Kiro

- Launch Kiro IDE
- Click the "Open a project" button
- Select the `MyShootingGame` folder you just created
- Kiro will initialize the project workspace

<img width="472" height="360" alt="image" src="https://github.com/user-attachments/assets/98371ca9-9c91-48ab-a978-b7ed09e6080c" />

### Step 3: Access Let's Build Feature

- In Kiro, navigate to the "Let's build" page
- You will see two available options:
  - **Vibe** - Chat first, build later. Explore ideas and iterate as you discover requirements
  - **Spec** - Plan first, build later. Create requirements and design before starting to code
- For this practice, choose "Vibe" mode
- Set the model to "Claude Sonnet 4" (or latest available version)
- Ensure Autopilot is enabled

<img width="472" height="360" alt="image" src="https://github.com/user-attachments/assets/7a6f1648-f717-4e44-a29a-189d096a70d3" />


### Step 4: Create Basic Shooting Game

In Kiro's chat area, enter the following prompt:

```
Please help me to build a web-base shooting game and deploy to local.
```

**Prompt Description:**
- Create a web-based shooting game
- Include basic shooting mechanics and enemy systems

##  🚀 Exercise 1 - Generate Steering document in Kiro 

Steering gives Kiro persistent knowledge about your project through markdown files in .kiro/steering/. Instead of explaining your conventions in every chat, steering files ensure Kiro consistently follows your established patterns, libraries, and standards.

### Step 1: Click Generate Steering Docs

<img width="966" height="661" alt="image" src="https://github.com/user-attachments/assets/6a4647ee-9a60-4f14-b1f7-f1e837ad0e1a" />


### 1.1 Requirements Specification

Start by asking Kiro to help you create a detailed requirements specification:

```
Create a comprehensive requirements specification for a serverless chatbot application with the following high-level requirements:

- Frontend: CloudFront distribution serving a static website
- Backend: API Gateway + Lambda functions  
- AI: Integration with Amazon Bedrock for chat responses
- Security: Enterprise-grade security considerations
- Scalability: Serverless architecture for automatic scaling

Please break this down into detailed functional and non-functional requirements.
```

**Expected Outcome**
Kiro will generate a detailed requirements document that includes:

**Functional Requirements:**
- User interface for chat interactions
- Message handling and display
- API endpoints for communication
- Integration with Bedrock models
- Error handling and recovery

**Non-Functional Requirements:**
- Performance metrics (response times, throughput)
- Security requirements (authentication, encryption)
- Scalability considerations
- Reliability targets
- Compliance requirements

### 1.2 Architecture Design

Once you have the requirements, ask Kiro to create an architecture design:

```
Based on the requirements specification, create a detailed system architecture design including:

- Component diagram showing all AWS services and their interactions
- Data flow diagrams for request/response cycles
- Security architecture with authentication and authorization flows
- Deployment architecture with CI/CD considerations
```

**Expected Outcome**
Kiro will generate a comprehensive architecture document with diagrams and explanations of:
- System components and their relationships
- Data flows between components
- Security mechanisms
- Deployment strategies

### 1.3 Implementation Plan

Finally, create a detailed implementation plan:

```
Create a step-by-step implementation plan that breaks down the development into phases:

Phase 1: Basic infrastructure setup
Phase 2: Frontend development and deployment
Phase 3: Backend API development
Phase 4: Bedrock integration
Phase 5: Security implementation
Phase 6: Testing and optimization

For each phase, provide specific tasks, deliverables, and acceptance criteria.
```

**Expected Outcome**
Kiro will generate a detailed implementation plan with:
- Phased approach to development
- Specific tasks for each phase
- Clear deliverables and milestones
- Acceptance criteria for quality assurance

### Review and Refinement
Review the generated spec document and refine it based on your specific needs. The spec should be comprehensive enough that any developer could understand what needs to be built.

---

##  🚀 Exercise 2 - Infrastructure Specification

### 2.1 AWS Resources Specification
```
Create a detailed specification for all AWS resources needed:

- S3 buckets (names, configurations, policies)
- CloudFront distribution (origins, behaviors, security headers)
- API Gateway (endpoints, methods, integration types)
- Lambda functions (runtime, memory, timeout, environment variables)
- IAM roles and policies (principle of least privilege)
- Bedrock model access and configurations

Include Infrastructure as Code (IaC) requirements using AWS CDK or CloudFormation.
```
**Expected Outcome**
Kiro will generate a detailed specification for all AWS resources needed for the chatbot application, including naming conventions, configurations, and policies.

### 2.2 Security Specification
```
Create a comprehensive security specification covering:

- CORS policies for cross-origin requests
- Content Security Policy (CSP) headers
- API authentication and authorization
- Input validation and sanitization
- Rate limiting and DDoS protection
- Encryption at rest and in transit
- Logging and monitoring requirements
```
**Expected Outcome**
Kiro will generate a detailed security specification that addresses all aspects of application security, from frontend to backend.

##  🚀 Exercise 3 - Frontend Specification

### 3.1 UI/UX Specification
```
Create a detailed frontend specification including:

- User interface mockups and wireframes
- Component architecture (if using a framework)
- Responsive design requirements
- Accessibility compliance (WCAG 2.1 AA)
- Browser compatibility requirements
- Performance requirements (loading times, bundle sizes)
```
**Expected Outcome**
Kiro will generate a detailed UI/UX specification with wireframes, component architecture, and design requirements.

### 3.2 Frontend Technical Specification
```
Specify the technical implementation details:

- Technology stack (HTML5, CSS3, JavaScript/TypeScript)
- Build process and bundling requirements
- Asset optimization strategies
- Progressive Web App (PWA) considerations
- Error handling and user feedback mechanisms
```

**Expected Outcome**
Kiro will generate a detailed technical specification for the frontend implementation, including technology choices, build processes, and optimization strategies.

##  🚀 Exercise 4 - Backend API Specification

### 4.1 API Specification
```
Create a detailed API specification including:

- OpenAPI/Swagger documentation for all endpoints
- Request/response schemas with validation rules
- Error response formats and HTTP status codes
- Rate limiting specifications
- Authentication/authorization requirements per endpoint
- Logging and monitoring specifications
```
**Expected Outcome**
Kiro will generate a comprehensive API specification in OpenAPI/Swagger format, detailing all endpoints, request/response schemas, and security requirements.

### 4.2 Lambda Function Specifications
```
Create detailed specifications for each Lambda function:

- Function purpose and responsibilities
- Input/output specifications
- Error handling strategies
- Performance requirements (cold start, execution time)
- Memory and timeout configurations
- Environment variable requirements
- Integration patterns with other AWS services
```

**Expected Outcome**
Kiro will generate detailed specifications for each Lambda function in the system, including their purpose, inputs/outputs, and configuration requirements.

## 🚀 Exercise 5 -  Implementation Phase 1 - Infrastructure

### 5.1 Infrastructure as Code
```
Based on our infrastructure specification, implement the AWS CDK stack that creates:

- S3 bucket for static website hosting
- CloudFront distribution with proper security headers
- API Gateway with CORS configuration
- Lambda function placeholders
- IAM roles with least privilege access
- All security policies as specified

Deploy this infrastructure and verify all resources are created correctly.
```
**Expected Outcome**
Kiro will generate and deploy the AWS CDK code that creates all the required infrastructure resources according to the specifications.

### 5.2 Validation and Testing
```
Create infrastructure validation tests to ensure:

- All AWS resources are created with correct configurations
- Security policies are properly applied
- Network connectivity works as expected
- Monitoring and logging are properly configured

```

**Expected Outcome**
Kiro will generate validation tests to verify that the infrastructure has been deployed correctly and meets all requirements.

##  🚀 Exercise 6 - Implementation Phase 2 - Frontend

### 6.1 Frontend Development
```
Based on our frontend specification, implement:

- Responsive chat interface with proper accessibility
- Real-time message display with proper error handling
- Input validation and sanitization
- Loading states and user feedback
- Progressive enhancement for better user experience
- Proper error boundaries and fallback UI

```
**Expected Outcome**
Kiro will generate the frontend code for the chatbot application, including HTML, CSS, and JavaScript/TypeScript files that implement the UI/UX specification

### 6.2 Frontend Testing
```
Implement comprehensive frontend testing:

- Unit tests for utility functions
- Integration tests for API communication
- End-to-end tests for user workflows
- Accessibility testing with automated tools
- Performance testing and optimization
```

**Expected Outcome**
Kiro will generate test files for the frontend components and utilities, ensuring that the application meets all requirements and works correctly.

##  🚀 Exercise 7 - Implementation Phase 3 - Backend API

### 7.1 API Implementation
```
Based on our API specification, implement:

- Lambda functions for chat endpoints
- Input validation middleware
- Error handling with proper HTTP status codes
- Request/response logging
- Rate limiting implementation
- Health check endpoints
```
**Expected Outcome**
Kiro will generate the backend Lambda functions that implement the API specification, including proper input validation, error handling, and logging. The implementation will follow RESTful API best practices and include all the endpoints defined in the API specification.

### 7.2 Bedrock Integration
```
Implement Bedrock integration with:

- Proper model selection and configuration
- Request/response transformation
- Error handling for Bedrock API calls
- Cost optimization strategies
- Response streaming if supported
```

**Expected Outcome**
Kiro will implement the integration with Amazon Bedrock, configuring the appropriate AI model and handling all the communication between your Lambda functions and the Bedrock service. The implementation will include error handling, retries, and optimizations to ensure reliable and cost-effective operation.


##  🚀 Exercise 8 - Security Implementation

### 8.1 Authentication and Authorization
```
Implement user authentication system:

- User registration and login functionality
- JWT token management
- Session handling and security
- Password security best practices
- Multi-factor authentication considerations

```

**Expected Outcome**
Kiro will implement a complete authentication system that allows users to register, login, and securely access the chatbot. The implementation will include secure password handling (hashing, salting), JWT token generation and validation, and proper session management. The system will follow security best practices to protect user credentials and prevent common authentication vulnerabilities.

### 8.2 Security Headers and Policies
```
Implement comprehensive security measures:

- Content Security Policy (CSP) headers
- CORS policies with proper origin validation
- Rate limiting with Redis or DynamoDB
- Input sanitization and validation
- SQL injection and XSS prevention
- Security monitoring and alerting
```

**Expected Outcome**
Kiro will implement various security measures to protect the application from common web vulnerabilities. This includes configuring security headers in CloudFront and API Gateway, implementing proper CORS policies, adding rate limiting to prevent abuse, and ensuring all user inputs are properly validated and sanitized. The implementation will also include monitoring and alerting for security-related events.After completing this exercise, your chatbot application will have enterprise-grade security features that protect both the infrastructure and the users. The security implementation will follow industry best practices and address the requirements specified in your security specification document.

## 🚀 Exercise 9 -  Cleanup and Resource Management

```
Create and execute cleanup procedures:

- Document all deployed AWS resources
- Create cleanup scripts for complete resource removal
- Verify all resources are properly deleted
- Document any persistent data that needs backup
- Create re-deployment procedures for future use
```

**Expected Outcome**
Kiro will generate a comprehensive inventory of all AWS resources deployed for your chatbot application, including S3 buckets, CloudFront distributions, API Gateway endpoints, Lambda functions, IAM roles, and any other resources. It will then create cleanup scripts (using AWS CDK, CloudFormation, or AWS CLI) to systematically remove these resources in the correct order to avoid dependency issues. The implementation will include verification steps to ensure all resources are properly deleted and documentation for any data that should be backed up before cleanup. Finally, Kiro will provide instructions for re-deploying the application in the future if needed.

After completing this exercise, you'll have successfully cleaned up all AWS resources used by your chatbot application, preventing any unexpected charges. You'll also have documentation and scripts that make it easy to redeploy the application in the future if desired.


## Comparing Spec vs Vibe Coding

After completing all exercises in this workshop, take some time to reflect on the differences between spec and vibe coding approaches:

### Advantages of Spec Coding:

* Better documentation and maintainability
* More predictable development process
* Easier to review and validate requirements
* Better suited for complex, enterprise applications
* Facilitates team collaboration and knowledge sharing

### When to Use Each Approach:

* Use Spec Coding for: Complex applications, team projects, enterprise software, long-term maintenance
* Use Vibe Coding for: Prototypes, simple applications, exploratory development, quick iterations

### Final Remarks
Spec coding with Kiro provides a more structured approach to AI-assisted development. While it requires more upfront planning, it results in better-documented, more maintainable, and more predictable software development processes.

The specifications you create become living documents that can be updated and refined as requirements change, making your development process more agile and responsive to changing needs. Consider using spec coding for your next complex project where documentation, maintainability, and team collaboration are important factors.
