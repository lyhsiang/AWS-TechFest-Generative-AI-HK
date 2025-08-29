# Kiro Spec Workshop: Hands-On Exercises

> **Master specification-driven development** through practical exercises that demonstrate real-world scenarios and build your expertise with Kiro Specs.

## Workshop Overview

This workshop provides four progressive exercises designed to teach you different aspects of Kiro Spec mode:

1. **Serverless Chatbot** - Learn the basics of spec creation
2. **E-commerce API** - Practice API-focused specifications  
3. **Mobile Messaging** - Handle real-time systems and mobile considerations
4. **Legacy Migration** - Tackle complex system analysis and migration planning

Each exercise follows the complete Kiro Spec workflow: Requirements → Design → Implementation Planning → Execution.

---

## Exercise 1 - Creating Your First Spec

**Scenario:** Build a comprehensive specification for a serverless chatbot application before writing any code.

### Setup
Create a folder named `MyCoolChatbotSpec` and open it in Kiro. Instead of starting with vibe coding, we'll create a comprehensive specification first.

In the Let's build page, select **Spec** instead of Vibe. This will open the spec creation interface.

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

**Learning Goals:**
- Master the basic Kiro Spec workflow
- Practice EARS notation for requirements
- Understand serverless architecture documentation
- Learn phased implementation planning

---

## Exercise 2 - E-commerce API Specification

**Scenario:** You need to build a RESTful API for an e-commerce platform with product catalog, shopping cart, and order management.

### 2.1 Setup
Create a new spec called `EcommerceAPISpec`

### 2.2 Requirements Phase
```
Create requirements for an e-commerce API with the following capabilities:
- Product catalog management (CRUD operations)
- Shopping cart functionality
- Order processing and tracking
- User authentication and authorization
- Payment integration
- Inventory management

Use EARS notation for all functional requirements and include comprehensive non-functional requirements for performance, security, and scalability.
```

### 2.3 Design Phase
```
Design a RESTful API architecture including:
- OpenAPI specification for all endpoints
- Database schema design
- Authentication and authorization flows
- Error handling strategies
- Rate limiting and caching strategies
- Integration patterns for payment providers
```

### 2.4 Implementation Planning
```
Create an implementation plan that includes:
- Database setup and migrations
- API endpoint development priority
- Testing strategy (unit, integration, load testing)
- Security implementation checklist
- Deployment and monitoring setup
```

**Learning Goals:**
- Practice with API-focused specifications
- Understand database design in specs
- Learn security considerations for APIs
- Experience with external integration planning

---

## Exercise 3 - Mobile App Feature Specification

**Scenario:** Add a real-time messaging feature to an existing mobile application.

### 3.1 Setup
Create a new spec called `MobileMessagingFeature`

### 3.2 Requirements Development
```
Specify requirements for a real-time messaging feature including:
- One-on-one and group messaging
- Message delivery status (sent, delivered, read)
- File and media sharing
- Push notifications
- Offline message sync
- Message encryption

Focus on mobile-specific considerations like battery life, network connectivity, and user experience.
```

### 3.3 Technical Design
```
Design the messaging architecture considering:
- Real-time communication protocols (WebSocket, Server-Sent Events)
- Message queuing and delivery guarantees
- Data synchronization strategies
- Push notification architecture
- Local storage and caching
- Cross-platform compatibility (iOS/Android)
```

### 3.4 Implementation Strategy
```
Plan the implementation with focus on:
- Incremental rollout strategy
- A/B testing for UX features
- Performance monitoring and optimization
- Backward compatibility considerations
- App store deployment process
```

**Learning Goals:**
- Mobile-specific requirement considerations
- Real-time system design
- Cross-platform development planning
- Performance and UX optimization

---

## Exercise 4 - Legacy System Migration

**Scenario:** Migrate a monolithic application to microservices architecture.

### 4.1 Setup
Create a new spec called `LegacyMigrationSpec`

### 4.2 Current State Analysis
```
Document the current monolithic system including:
- Existing functionality and business logic
- Current architecture and dependencies
- Performance bottlenecks and pain points
- Data models and database structure
- Integration points with external systems

Then specify requirements for the target microservices architecture.
```

### 4.3 Migration Architecture
```
Design the migration strategy including:
- Service decomposition strategy
- Data migration and synchronization
- API gateway and service mesh architecture
- Monitoring and observability setup
- Rollback and disaster recovery plans
```

### 4.4 Phased Migration Plan
```
Create a detailed migration plan with:
- Service extraction priority and dependencies
- Data migration strategies
- Testing approaches for each phase
- Risk mitigation strategies
- Success metrics and monitoring
```

**Learning Goals:**
- Complex system analysis and documentation
- Migration strategy planning
- Risk assessment and mitigation
- Microservices architecture design

---

## Workshop Tips

### Getting the Most from Each Exercise
- **Start Simple:** Begin with basic requirements, then add complexity
- **Iterate Frequently:** Use the decision points in the workflow to refine your specs
- **Ask Questions:** Use Kiro to clarify requirements and explore alternatives
- **Think End-to-End:** Consider the full user journey and system lifecycle

### Common Patterns to Practice
- **EARS Notation:** Master the "WHEN...THE SYSTEM SHALL..." format
- **Architecture Diagrams:** Practice describing system components and interactions
- **Task Breakdown:** Learn to create actionable, measurable tasks
- **File References:** Use `#[[file:...]]` to link related documentation

### Troubleshooting Your Specs
- **Vague Requirements:** Ask Kiro to help make them more specific and testable
- **Missing Edge Cases:** Review each requirement for error conditions and exceptions
- **Unclear Tasks:** Ensure each task has clear acceptance criteria
- **Architecture Gaps:** Verify all components and integrations are documented

### Advanced Techniques
- **Reference External Files:** Use `#[[file:api/openapi.yaml]]` to link specifications
- **Iterative Refinement:** Use the workflow decision points to improve your specs
- **Stakeholder Reviews:** Share specs with team members for feedback
- **Living Documentation:** Keep specs updated as implementation progresses

---

## Next Steps

After completing these exercises, you'll have hands-on experience with:
- Creating comprehensive requirements using EARS notation
- Designing system architectures for different domains
- Planning implementation with trackable tasks
- Managing complex projects through specifications

**Continue Learning:**
- Apply Kiro Specs to your real projects
- Experiment with file references and external documentation
- Practice collaborative spec development with your team
- Explore advanced architectural patterns in your designs

*Ready to transform your development process? Start with Exercise 1 and work your way through each scenario.* 🚀
