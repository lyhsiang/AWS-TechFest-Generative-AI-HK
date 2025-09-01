# Kiro Hands-on Practice

Welcome to the Kiro hands-on experience! In this lab, you will learn how to use Kiro's AI capabilities to build applications quickly and efficiently.

## Practice : Build a Web Shooting Game and Deploy to AWS

In this practice, you will use Kiro to create a fully functional web shooting game with advanced features including enemy health bars, power-up systems, Boss stages, and deploy it to AWS serverless architecture.

## 🎯 Learning Objectives

- Use Kiro to build complex interactive web games
- Implement AWS serverless architecture deployment
- Master AWS resource management and cleanup

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
Please help me to build a web-base shooting game.
```

**Prompt Description:**
- Create a web-based shooting game
- Include basic shooting mechanics and enemy systems

### Step 5: Improve Game Controls

After the basic game is created, use the following prompt to improve the control experience:

```
Use keyboard to control spaceship is hard to target the enemies. Please help me to add the cursor mode. Also, please follow below rules:
- The bullet can only be shoot straight forward. 
- Do not add auto-aim function. 
- With cursor mode, please add a aim dot to represent cursor position.
- Allow customer could switch between cursor and keyboard control mode.
```

**Improvement highlights:**
- Optimize aiming mechanics
- Dual control support:
  - **Keyboard control**: WASD movement, spacebar to shoot
  - **Mouse/Touch control**: Move cursor/finger to move, click/touch to shoot
- Add auxiliary aiming functionality

### Step 6: Add Enemy Health Bars and Game Instructions

Continue using the following prompt to enhance game functionality:

```
Please help me add a health bar on enemies to understand how many time left to take down it.
```

**New features:**
- Enemy health bar display
- Visual health indicators

### Step 7: Add Start Screen

Continue using the following prompt to enhance game functionality:

```
Create a start game page and control instruction page.
```

**New features:**
- Game start screen
- Game instruction page

### Step 8: Implement Power-up System

Use the following prompt to add power-up mechanics:

```
Add some random dropped items to temporarily power up myself. Such as shooting more fast, or shooting more wide.At the same time, please explain what the functions of these power items are.
```

**Power-up system includes:**
- Randomly dropped enhancement items
- Triple Shot: Triple shooting ability
- Rapid Fire: Fast shooting mode
- Shield: Protective shield
- Temporary enhancement effects

### Step 9: Add Boss Stage System

Use the following prompt to implement advanced stage mechanics:

```
When the score reach specific points, I would like to have a boss stage. Once the boss is eliminated, return to normal stage to get more points and wait next boss stage.
```

**Boss system features:**
- Boss stage appears every 200 points
- Gradually increasing game difficulty
- Special Boss battle mechanics

### Step 10: Deploy to AWS Serverless Architecture

Use the following prompt for AWS deployment:

```
Please help me deploy to my AWS Account with serverless architecture, make sure the S3 bucket not public read and can only go through Cloudfront. Please deploy
```

**Deployment requirements:**
- Use AWS serverless architecture
- All AWS CLI commands must include `--no-paginate` and `--no-cli-pager` parameters
- Automated deployment process

### Step 11: Resource Cleanup

After completing testing, use the following prompt to clean up AWS resources:

```
Please help me to terminate the related resources from my AWS account.
```

## 📁 Expected Project Structure

After completion, your project may include:

```
MyShootingGame/
├── src/
│   ├── index.html              # Main game page
│   ├── game.js                 # Game logic
│   ├── styles.css              # Game styles
│   ├── assets/                 # Game assets
│   │   ├── sprites/            # Sprite images
│   │   └── sounds/             # Sound files
│   └── instructions.html       # Game instruction page
├── infrastructure/
│   ├── serverless.yml          # Serverless configuration
│   ├── cloudformation.yaml     # AWS infrastructure
│   └── deploy.sh               # Deployment script
├── scripts/
│   ├── deploy.sh               # Deployment script
│   └── cleanup.sh              # Resource cleanup script
└── README.md                   # Project documentation
```

## 🎮 Expected Game Features

After completion, your shooting game should look like this:
- Game main screen
<img width="1056" height="770" alt="image" src="https://github.com/user-attachments/assets/73d51eb4-7109-4d88-8c34-586c4f5d0da8" />

- Game instruction page
<img width="1134" height="832" alt="image" src="https://github.com/user-attachments/assets/68981c67-260b-4cae-a7ee-8ff18182143b" />


## 🏗️ AWS Architecture

**Serverless components:**
- **S3**: Static website hosting
- **CloudFront**: Global content distribution
- **Lambda**: Backend logic processing (if needed)
- **API Gateway**: API management (if needed)
- **DynamoDB**: Score recording (if needed)

## 🔧 Deployment Verification

After deployment is complete, verify the following items:
- Game can be accessed normally through CloudFront URL
- All game functions work properly
- AWS resources are created correctly
- Cost control within reasonable range

## 💡 Development Tips

**When interacting with Kiro:**
- Build features step by step, don't request too much at once
- Test each feature before continuing to the next step
- Specifically describe the game experience you want
- Utilize Kiro's iterative capabilities to optimize the game

**Game development best practices:**
- Maintain smooth game loop flow
- Appropriate visual feedback
- Balanced game difficulty curve
- Responsive design supporting multiple devices

## 🐛 Troubleshooting

**Game development issues:**
- **If game stutters**: Check game loop and rendering efficiency
- **If controls are unresponsive**: Adjust input handling and collision detection
- **If power-ups don't work**: Check state management and timers

**AWS deployment issues:**
- **If deployment fails**: Check AWS permissions and quotas
- **If game won't load**: Check S3 and CloudFront configuration
- **If CLI commands fail**: Ensure `--no-paginate` and `--no-cli-pager` are added

**Resource cleanup issues:**
- **If cleanup is incomplete**: Manually check AWS console
- **If there are residual charges**: Check all related services
- **Use Kiro for assistance**: "Please help me check if there are any missed AWS resources"

## ✅ Success Criteria

The practice is complete when you have accomplished the following:
- Basic shooting game works properly (similar game screen as shown in screenshots)
- Improved control system provides good experience (supports keyboard and mouse controls)
- Enemy health bars and game instructions implemented (includes complete How to Play page)
- Boss stage system works properly (score milestones trigger)
- Successfully deployed to AWS serverless architecture
- Able to completely clean up AWS resources

## ✅ Success Example

https://dvru9fepx5b2b.cloudfront.net
