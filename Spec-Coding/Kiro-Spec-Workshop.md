# 🚀 Kiro Spec Workshop: Hands-On Exercises

## Introduction

In this section, you will learn how to use Kiro in a spec-driven development style. Unlike vibe coding where you give high-level instructions and let Kiro figure everything out, spec coding involves creating detailed specifications that break down complex features into manageable, well-defined tasks. This approach provides better control, documentation, and iterative development for complex projects.

Kiro's Spec feature allows you to formalize the design and implementation process by iterating on requirements, design, and implementation tasks with structured documentation before letting the agent work through the implementation.

This is a fully hands-on workshop. Through a series of exercises, you will design, develop, and deploy the same webshooting game as the vibe coding workshop, but using a more structured, specification-driven approach. By the end, you'll have a fully functional chatbot with text, image, and voice capabilities, secured with user authentication.

### Setup
Create a folder named `MyShootingGame` and open it in Kiro. Instead of starting with vibe coding, we'll create a comprehensive specification first.

### 📋 Prerequisites

- Installed and running Kiro IDE ( https://kiro.dev/downloads )
- AWS account with S3 and CloudFront access permissions
- Configured AWS CLI (for deployment)
- Install uv from Astral ( https://docs.astral.sh/uv/getting-started/installation )

**Login to Kiro**

- Start URL ( https://d-9066223a3e.awsapps.com/start/ )
- Enter the username / password provide onsite

<img width="200" height="300" alt="Screenshot 2025-09-03 at 8 53 09 AM" src="https://github.com/user-attachments/assets/6b66ab52-e5ac-48e4-940f-e550e72aee10" />


**Logout Kiro** 
*(please logout after the event)*
- Click account information from the left down corner 
<img width="351" height="169" alt="Screenshot 2025-09-03 at 9 04 27 AM" src="https://github.com/user-attachments/assets/a004b61d-efcf-4159-bd1f-3d578db137e4" />





### Setup 1: Create Project Folder

- On your computer, create a folder named `MyShootingGame`
- This will become the project workspace for your shooting game application

### Setup 2: Open Project in Kiro

- Launch Kiro IDE
- Click the "Open a project" button
- Select the `MyShootingGame` folder you just created
- Kiro will initialize the project workspace

<img width="472" height="360" alt="image" src="https://github.com/user-attachments/assets/98371ca9-9c91-48ab-a978-b7ed09e6080c" />

### Setup 3: Access Let's Build Feature

- In Kiro, navigate to the "Let's build" page
- You will see two available options:
  - **Vibe** - Chat first, build later. Explore ideas and iterate as you discover requirements
  - **Spec** - Plan first, build later. Create requirements and design before starting to code
- Set the model to "Claude Sonnet 4" (or latest available version)
- Ensure Autopilot is enabled

<img width="472" height="360" alt="image" src="https://github.com/user-attachments/assets/7a6f1648-f717-4e44-a29a-189d096a70d3" />

##  🚀 Exercise 1 - Use Vibe Coding to create a simple Web base shooting game  

```

Please help me to build a web-base shooting game and deploy to local

```

##  🚀 Exercise 2 - Generate Steering document in Kiro 

Steering gives Kiro persistent knowledge about your project through markdown files in .kiro/steering/. Instead of explaining your conventions in every chat, steering files ensure Kiro consistently follows your established patterns, libraries, and standards.

#### 2.1 Click Generate Steering Docs

<img width="966" height="661" alt="image" src="https://github.com/user-attachments/assets/6a4647ee-9a60-4f14-b1f7-f1e837ad0e1a" />

#### 2.2 Review the outputs markdown file from Agent Steering to make update if need

- Product Overview (product.md): Defines your product's purpose, target users, and business objectives

- Technology Stack (tech.md): Documents frameworks, libraries, and technical constraints

- Project Structure (structure.md): Outlines file organization, naming conventions, and architectural decisions

<img width="908" height="669" alt="image" src="https://github.com/user-attachments/assets/1ab7adb6-1f59-4a2d-ba03-fef8ea563160" />


##  🚀 Exercise 3 - Use Specs coding for more comprehensive implementation 

```

Create a more comprehensive modern web-based shooting application with following high-level requirements:

1) A clear introduction page about how to play the game
2) A healthy bar or status of enemies for user to understand how many time left to take it down 
3) Allow user to select different themes and character, let's make 3 different themes and 3 different spaceship please refer to  Masked Rider themes 2) ultraman 3) Godzilla.
4) Implement a power-up system , add some random items temporarily power up the spaceship. Such as shooting more fast, or shooting more wide, please create 6 different items, the more special the better, also include explanation of the power up items

```

#### 3.1 Review the Requirements ( requirements.md ) provide by Kiro 

<img width="731" height="630" alt="image" src="https://github.com/user-attachments/assets/b024f8a0-5387-44a3-a9d8-b55adbf6362d" />

#### 3.2 Move to Design phase and review design ( design.md )
<img width="635" height="434" alt="image" src="https://github.com/user-attachments/assets/87efa607-f6d5-4113-9102-037855d1dc6b" />


#### 3.3 Start implementation plan , review the Tasklist ( tasks.md )
<img width="611" height="418" alt="image" src="https://github.com/user-attachments/assets/e2446220-7e17-4e67-a53c-f182cf0f11aa" />


#### 3.4 Start Task by click the :zap:

<img width="568" height="332" alt="image" src="https://github.com/user-attachments/assets/3a3f912d-fe8d-4e63-b7d1-5ff21de23e4e" />


##  🚀 Exercise 4 - Add MCP server in Kiro 

Model Context Protocol (MCP) extends Kiro's capabilities by connecting to specialized servers that provide additional tools and context. This guide helps you set up, configure, and use MCP servers with Kiro.

> :warning:
> Before you start this exercise, please make sure you have install the uv command in your environment. To check the uv command whether has been installed, you could use following commnad:

```
$ uv self version
```
> If you didn't install it yet, please check [Astral](https://docs.astral.sh/uv/getting-started/installation) to install uv command.

#### 4.1 Click Enable MCP

<img width="368" height="268" alt="image" src="https://github.com/user-attachments/assets/0906b563-d0bf-4102-a0f8-332c7d277f97" />


#### 4.2 Modify the mcp.json file to add the MCP server

In this workshop, we will add: 
- **AWS Documentation MCP Server**: This MCP server provides tools to access AWS documentation, search for content, and get recommendations.
- **AWS Diagram MCP Server**: This MCP server that seamlessly creates diagrams using the Python diagrams package DSL. This server allows you to generate AWS diagrams, sequence diagrams, flow diagrams, and class diagrams using Python code.
- **AWS CDK MCP Server**: MCP server for AWS Cloud Development Kit (CDK) best practices, infrastructure as code patterns, and security compliance with CDK Nag.

For more AWS provided MCP, please refer this [document](https://awslabs.github.io/mcp/).

```
{
  "mcpServers": {
    "awslabs.aws-documentation-mcp-server": {
      "command": "uvx",
      "args": ["awslabs.aws-documentation-mcp-server@latest"],
      "env": {
        "FASTMCP_LOG_LEVEL": "ERROR",
        "AWS_DOCUMENTATION_PARTITION": "aws"
      },
      "disabled": false,
      "autoApprove": []
    },
    "awslabs.cdk-mcp-server": {
      "command": "uvx",
      "args": [
        "awslabs.cdk-mcp-server@latest"
      ],
      "env": {
        "FASTMCP_LOG_LEVEL": "ERROR"
      },
      "disabled": false,
      "autoApprove": [
        "GetAwsSolutionsConstructPattern"
      ]
    },
    "awslabs.aws-diagram-mcp-server": {
      "command": "uvx",
      "args": [
        "awslabs.aws-diagram-mcp-server"
      ],
      "env": {
        "FASTMCP_LOG_LEVEL": "ERROR"
      },
      "disabled": false,
      "autoApprove": [
        "list_icons",
        "list_icons",
        "generate_diagram",
        "get_diagram_examples",
        "list_icons"
      ]
    }
  }
}

```

##  🚀 Exercise 5 - Add Hooks in Kiro 

Agent Hooks are powerful automation tools that streamline your development workflow by automatically executing predefined agent actions when specific events occur in your IDE. With hooks, you eliminate the need to manually request routine tasks and ensure consistency across your codebase.

#### 4.1 Click "+" on AGENT HOOKS to add new hooks


<img width="393" height="731" alt="image" src="https://github.com/user-attachments/assets/22af98c2-f7e8-470c-9cf6-ec695a711f30" />


#### 4.2 Describe the hook using natural language

We want agent hooks to help us monitoring the CDK resource files change, and keep generating the AWS service diagram by using AWS Diagram MCP Server.

```
Analyze the modified CDK files and generate or update AWS service architecture diagrams using the PPython diagrams package DSL. Parse the CDK code to identify AWS services, their relationships, and data flow. If the previous diagram not exist, create a visual representation showing the infrastructure components, connections, and dependencies. Include proper grouping for VPCs, subnets, and logical service boundaries. Otherwise, delete the previous diagram before create new one. Output the Python diagrams code that can be executed to generate the architecture diagram.
```

After the hook create complete and CDK resource files have change, you should see the similiar diagram as following example:

<img width="1620" height="2106" alt="image" src="https://github.com/user-attachments/assets/0d9e81dc-0ffd-4837-b768-7a852290538c" />


##  🚀 Exercise 5 - Create a new Spec for AWS enviroment deployment 

```
I have a web-based shooting application need to deploy to AWS Cloud. Create a comprehensive AWS architecture with following high-level requirements:
1) Must use AWS serverless services, such as Cloudfront, S3, etc..
2) Follow each service's configuration best practice
3) Prefer to use Infrasturce as Code solution to deploy, such as AWS CDK.
4) Since we are in demo, please do not add any new feature for the game.
```

## 🚀 Exercise 6 -  Cleanup and Resource Management

```
Create and execute cleanup procedures:

- Document all deployed AWS resources
- Create cleanup scripts for complete resource removal
- Verify all resources are properly deleted
- Document any persistent data that needs backup
- Create re-deployment procedures for future use
```

**Expected Outcome**
Kiro will generate will create cleanup scripts (using AWS CDK, CloudFormation, or AWS CLI) to systematically remove these resources in the correct order to avoid dependency issues. The implementation will include verification steps to ensure all resources are properly deleted and documentation for any data that should be backed up before cleanup. Finally, Kiro will provide instructions for re-deploying the application in the future if needed.

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

### Survey 


