# 🤖 What is Kiro?

"An agentic IDE that helps you do your best work." — Official Kiro Tagline

## 🏢 Kiro's Official Positioning

Kiro is designed as an "Agentic IDE," which means it doesn't just passively respond to developer commands, but can:

🎯 **Proactively Understand Goals**: Understand developers' ultimate objectives, not just individual commands  
🤔 **Make Smart Decisions**: Make optimal technical decisions during development  
🔄 **Execute Autonomously**: Independently complete complex development task sequences  
📈 **Continuously Improve**: Learn from each interaction to provide increasingly precise assistance

## 🌟 Kiro's Revolutionary Features

### 💬 Natural Language Programming

Kiro supports a truly conversational development experience:
- Describe the features you want to build using everyday conversation
- Kiro understands complex business logic and technical requirements
- No need to memorize complex syntax or API documentation
- Supports mixed Chinese and English development conversations
- Can understand vague requirements and ask clarifying questions

### 🧠 Intelligent Context Understanding

Based on advanced AI models, Kiro has deep understanding capabilities:
- Deep understanding of project structure and code relationships
- Automatically infer optimal technology choices and architectural patterns
- Remember your development preferences and team standards
- Provide consistent code that matches project style
- Cross-file intelligent refactoring and dependency management

### 🚀 End-to-End Development Process

Kiro covers the complete software development lifecycle:

🎨 **Design Phase**: Assist with requirements analysis and architectural design  
⚡ **Development Phase**: Automatically generate high-quality code  
🧪 **Testing Phase**: Generate test cases and debugging assistance  
🚀 **Deployment Phase**: Automated CI/CD and cloud deployment  
🔧 **Maintenance Phase**: Code refactoring and performance optimization

### ☁️ Deep AWS Integration

As an AWS strategic partner, Kiro provides:
- Native support for all major AWS services
- Automatically generate architectures compliant with AWS Well-Architected Framework
- Intelligent cost optimization recommendations and resource allocation
- Automatic implementation of security best practices
- Real-time AWS service status and quota monitoring

## ✨ Kiro's Core Capabilities

### 🎯 Vibe Mode vs Spec Mode

Kiro offers two different development modes for different development scenarios:

**🌊 Vibe Mode - Exploratory Development**
- Suitable for rapid prototyping and creative exploration
- Build while chatting, flexibly adjust direction
- Suitable for early development with unclear requirements
- Supports rapid iteration and experimentation

**📋 Spec Mode - Structured Development**
- Suitable for large projects and team collaboration
- Plan first, then implement, ensuring complete architecture
- Automatically generate detailed technical specification documents
- Support complex project management and tracking

A detail comparison of two approaches :

<img width="716" height="377" alt="image" src="https://github.com/user-attachments/assets/f689340f-5d72-4f04-bca4-491c8df6fb02" />


## 🌟 Why Choose Kiro? Unique Features That Set Us Apart

Kiro isn't just another AI coding assistant. We've built unique features that transform how you develop software, making your workflow more intelligent, automated, and collaborative.

### 🎯 Steering: Your Team's Knowledge, Always Available

**What is Steering?**
Steering gives Kiro persistent knowledge about your project through markdown files in `.kiro/steering/`. Instead of explaining your conventions in every chat, steering files ensure Kiro consistently follows your established patterns, libraries, and standards.

**Key Benefits:**
- **Consistent Code Generation**: Every component, API endpoint, or test follows your team's established patterns and conventions
- **Reduced Repetition**: No need to explain project standards in each conversation. Kiro remembers your preferences
- **Team Alignment**: All developers work with the same standards, whether they're new to the project or seasoned contributors
- **Scalable Project Knowledge**: Documentation that grows with your codebase, capturing decisions and patterns as your project evolves

**Flexible Inclusion Modes:**
- **Always Included**: Core standards loaded into every interaction (default for foundational files)
- **Conditional Inclusion**: Automatically included when working with specific file patterns (e.g., `*.tsx` for React components)
- **Manual Inclusion**: Available on-demand by referencing `#steering-file-name` in chat

**Foundation Files Kiro Can Generate:**
- **Product Overview** (`product.md`): Defines your product's purpose, target users, and business objectives
- **Technology Stack** (`tech.md`): Documents frameworks, libraries, and technical constraints
- **Project Structure** (`structure.md`): Outlines file organization, naming conventions, and architectural decisions

**Real-World Example:**
```markdown
# .kiro/steering/api-standards.md
---
inclusion: conditional
fileMatchPattern: "app/api/**/*"
---

Always use our REST API conventions:
- Use kebab-case for endpoints
- Include proper error handling with our standard error format
- Reference our OpenAPI spec: #[[file:api/openapi.yaml]]
- Follow our authentication patterns using JWT tokens
```

### 🔗 Agent Hooks: Automation That Thinks

**What are Agent Hooks?**
Agent Hooks are powerful automation tools that streamline your development workflow by automatically executing predefined agent actions when specific events occur in your IDE. With hooks, you eliminate the need to manually request routine tasks and ensure consistency across your codebase.

**How Agent Hooks Work:**
1. **Event Detection**: The system monitors for specific events in your IDE (saving files, creating files, deleting files)
2. **Prompt Execution**: When an event occurs, a predefined prompt is sent to the agent
3. **Automated Action**: The agent processes the prompt and performs the requested actions

**Key Benefits:**
- **Maintain Consistent Code Quality**: Automatically enforce standards across your codebase
- **Prevent Security Vulnerabilities**: Automated security checks and fixes
- **Reduce Manual Overhead**: Eliminate repetitive tasks from your workflow
- **Standardize Team Processes**: Ensure all team members follow the same automated workflows
- **Create Faster Development Cycles**: Focus on building while hooks handle routine maintenance

**Setting Up Hooks:**
- **Explorer View**: Navigate to Agent Hooks section in Kiro panel, click + to create new hooks
- **Command Palette**: Use `Cmd + Shift + P` → "Kiro: Open Kiro Hook UI"
- **Natural Language**: Define hook workflows using simple, natural language descriptions

**Real-World Automation Examples:**
- **Code Quality**: Automatically format code, update imports, and fix linting issues on file save
- **Test Maintenance**: Update unit tests when functions change, ensure test coverage remains complete
- **Documentation Sync**: Keep API docs, README files, and code comments synchronized automatically
- **Security Compliance**: Scan for vulnerabilities, update dependencies, validate input sanitization

### 🔌 MCP (Model Context Protocol): Extend Kiro's Capabilities

**What is MCP?**
Model Context Protocol (MCP) extends Kiro's capabilities by connecting to specialized servers that provide additional tools and context. MCP is a protocol that allows Kiro to communicate with external servers to access specialized tools and information.

**What MCP Enables:**
- **Access Specialized Knowledge Bases**: Connect to documentation systems, wikis, and knowledge repositories
- **Integrate with External Services**: Work with APIs, databases, cloud services, and third-party tools
- **Extend with Domain-Specific Tools**: Add capabilities tailored to your specific industry or workflow
- **Create Custom Tools**: Build MCP servers for your organization's unique requirements

**Easy Setup and Management:**
- **Configuration**: Simple JSON configuration files (workspace or user-level)
- **MCP Servers Tab**: Visual interface in Kiro panel showing all configured servers and connection status
- **Tool Discovery**: Click any tool name to insert placeholder prompts in chat
- **Auto-Approval**: Configure trusted tools to run without manual approval

**Popular MCP Server Examples:**
- **AWS Documentation**: Search and access AWS documentation directly within Kiro
- **Database Connectors**: Query databases, update schemas, generate migrations
- **File System Tools**: Advanced file operations, search, and manipulation
- **Web Browsing**: Fetch web content, search the internet, access documentation sites
- **API Integration**: Connect to REST APIs, GraphQL endpoints, and web services

**Configuration Example:**
```json
{
  "mcpServers": {
    "aws-docs": {
      "command": "uvx",
      "args": ["awslabs.aws-documentation-mcp-server@latest"],
      "disabled": false,
      "autoApprove": ["search_aws_docs"]
    }
  }
}
```

**Troubleshooting Support:**
- **MCP Logs**: Dedicated log output in Kiro panel for debugging connection issues
- **Connection Status**: Visual indicators showing server health and availability
- **Error Handling**: Clear error messages and solutions for common configuration problems

### 🚀 The Kiro Advantage: Putting It All Together

**Intelligent Context Awareness**
Unlike other AI assistants that work in isolation, Kiro understands your entire development ecosystem through steering, hooks, and MCP integrations.

**Team-Centric Development**
Kiro scales your team's expertise, ensuring everyone benefits from your collective knowledge and maintains consistency across projects.

**Proactive Development**
Instead of just responding to requests, Kiro anticipates needs and automates routine tasks, letting you focus on creative problem-solving.

**Extensible Architecture**
As your needs evolve, Kiro grows with you through customizable steering rules, intelligent hooks, and expandable MCP connections.

---
### 🚀 Other Core Capabilities

🧠 **Intelligent Conversational Development**: Describe requirements in natural language, Kiro understands and implements your ideas  
🏗️ **End-to-End Project Construction**: Complete application development process from concept to deployment  
☁️ **AWS Native Integration**: Deep integration with AWS services, automated cloud deployment and management  
🔄 **Iterative Improvement**: Continuously learn your preferences, provide personalized development experience  
📚 **Best Practice Guidance**: Built-in industry standards and security best practices  
🎯 **Multimodal Development**: Support text, image, voice and other input methods  
🔒 **Enterprise-Grade Security**: Code privacy protection and compliance support  
🤖 **Autopilot Mode**: Automatically execute complex development task sequences


## 🚀 Experiment Overview

This repository contains demonstration materials and experimental exercises showing how Kiro integrates with AWS services to simplify cloud development workflows. Participants will learn how to use AI assistance to build, deploy, and manage applications on AWS.

Through this experiment, you will experience firsthand how Kiro makes complex cloud development tasks simple and intuitive, and understand why developers worldwide are choosing Kiro as their AI development partner.

## 📋 Pre-Experiment Preparation

- AWS account with appropriate permissions
- Basic cloud computing concepts
- Basic command line interface operations
- Git installed locally
- Kiro IDE installed (provided at experiment venue)

## 🛠️ Experiment Content

### Experiment 1: Kiro Getting Started Experience - Intelligent Chatbot

Experience Kiro's basic AI development capabilities by building an AWS Bedrock chatbot:

🎯 **Experiment Focus**:
- **Conversational Development**: Learn how to communicate with Kiro in natural language
- **Rapid Prototyping**: Build a complete chatbot UI in 30 minutes
- **AWS Integration**: Automatically generate S3 + CloudFront deployment architecture
- **Security Best Practices**: Implement AWS security configuration and permission management

🚀 **You Will Build**:
- Modern chat interface with Chinese and English support
- Secure AWS cloud hosting environment
- Responsive design supporting multiple devices
- Architecture design reserved for future API integration

### Experiment 2: Advanced Application Development - Web Shooting Game

Challenge Kiro's advanced development capabilities by building a fully functional interactive game:

🎯 **Experiment Focus**:
- **Complex Logic Implementation**: Game engine, collision detection, state management
- **Iterative Development**: Gradually add features, experience agile development process
- **Performance Optimization**: AI-assisted code optimization and best practices
- **Serverless Deployment**: Complete AWS serverless architecture implementation

🎮 **You Will Build**:
- Complete space shooting game (like Space Invaders)
- Enemy health bar system and power-up mechanics
- Boss levels and progressive difficulty system
- Professional game instructions and user interface
- High-performance AWS serverless deployment architecture

## 🏗️ Kiro Development Architecture

```
┌─────────────────┐    ┌─────────────────┐    ┌─────────────────┐
│   Developer     │    │      Kiro       │    │   AWS Services  │
│   Natural Lang  │◄──►│   AI Assistant  │◄──►│   (S3, Lambda,  │
│   Iterative     │    │   Code Gen      │    │   CloudFront)   │
│   Feedback      │    │                 │    │                 │
└─────────────────┘    └─────────────────┘    └─────────────────┘
```

## 🔄 Kiro Workflow

1. **Requirements Understanding**: Developer describes requirements in natural language
2. **Intelligent Analysis**: Kiro analyzes requirements and proposes implementation solutions
3. **Code Generation**: Automatically generate high-quality code and infrastructure
4. **AWS Integration**: Seamlessly integrate AWS services and best practices
5. **Iterative Optimization**: Continuously improve and optimize based on feedback
