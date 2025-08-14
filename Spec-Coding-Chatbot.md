Web Shooting Game with AWS Deployment

> **Welcome to Kiro!** In this hands-on lab, you'll learn how to use Kiro's AI capabilities to build applications quickly and efficiently.

## What You'll Build

A fully functional web shooting game featuring:
- **Enemy health bars** and visual feedback
- **Power-up systems** (Triple Shot, Rapid Fire, Shield)
- **Boss stages** that trigger at score milestones
- **AWS serverless deployment** with CloudFront distribution

---

## 🎯 Learning Goals

By the end of this lab, you'll know how to:
- ✅ Build complex interactive web games with Kiro
- ✅ Deploy to AWS serverless architecture
- ✅ Manage and clean up AWS resources properly

## 📋 What You Need

Before starting, make sure you have:
- **AWS Account** with full permissions
- **AWS CLI** configured on your machine
- **Kiro IDE** installed and running

---

## � Let'rs Get Started

### Step 1: Set Up Your Project

1. **Create a new folder** called `MyShootingGame` on your computer
2. **Open Kiro IDE** and click "Open a project"
3. **Select your folder** - Kiro will initialize the workspace

### Step 2: Choose Your Build Mode

1. Navigate to **"Let's build"** in Kiro
2. Choose **"Vibe"** mode (chat first, build later)
3. Set model to **"Claude Sonnet 4"** 
4. **Enable Autopilot** for autonomous file modifications

> **Why Vibe mode?** It's perfect for iterative development where you explore ideas as you build.

## 🎮 Building Your Game (Step by Step)

### Step 3: Create the Basic Game

**Copy and paste this prompt into Kiro:**

```
Please help me to build a web-base shooting game.
```

**What you'll get:** A basic web game with shooting mechanics and enemy systems.

---

### Step 4: Improve Controls

**Your next prompt:**

```
Use keyboard to control spaceship is hard to target the enemies. Please help me to add the cursor mode. Also, please follow below rules:
- With cursor mode, please do not add Y axis direction movement, and the bullet on can shoot straight forward.
- Do not add auto-aim function.
- With cursor mode, please add a aim dot to represent cursor position.
```

**What this adds:**
- 🎯 **Dual control modes:** WASD + spacebar OR mouse/touch controls
- 🎯 **Aiming dot** for better targeting
- 🎯 **No auto-aim** - skill-based gameplay

---

### Step 5: Add Visual Feedback

**Your next prompt:**

```
Please help me add a health bar on enemies to understand how many time left to take down it. Meanwhile, please add the how-to-play on the page
```

**What this adds:**
- ❤️ **Enemy health bars** - see damage progress
- 📖 **How-to-play instructions** - built into the page

---

### Step 6: Create Start Screen

**Your next prompt:**

```
Create a start game page.
```

**What this adds:**
- 🏁 **Professional start screen**
- ⚙️ **Control method selection**

---

### Step 7: Power-Up System

**Your next prompt:**

```
I would like to add some random dropped items to temporarily power up myself. Such as shooting more fast, or shooting more wide.
```

**What this adds:**
- 🚀 **Triple Shot** - spread fire
- ⚡ **Rapid Fire** - faster shooting
- 🛡️ **Shield** - temporary protection
- 🎲 **Random drops** from defeated enemies

---

### Step 8: Boss Battles

**Your next prompt:**

```
When the score reach specific points, I would like to have a boss stage. Once the boss is eliminated, return to normal stage to get more points and wait next boss stage.
```

**What this adds:**
- 👹 **Boss appears every 200 points**
- 🔥 **Escalating difficulty**
- 🏆 **Epic boss battle mechanics**

---

### Step 9: Deploy to AWS

**Your deployment prompt:**

```
Please help me deploy to my AWS Account with serverless architecture, make sure the S3 bucket not public read and can only go through Cloudfront. Please deploy
```

**What this does:**
- ☁️ **Serverless architecture** (S3 + CloudFront)
- 🔒 **Secure setup** - no public S3 access
- 🚀 **Automated deployment**

> **Important:** All AWS CLI commands will include `--no-paginate` and `--no-cli-pager` flags

---

### Step 10: Clean Up Resources

**When you're done testing:**

```
Please help me to terminate the related resources from my AWS account.
```

**Why this matters:** Prevents unexpected AWS charges!

---

## 📁 What You'll End Up With

Your final project structure:

```
MyShootingGame/
├── 🎮 src/
│   ├── index.html          # Main game
│   ├── game.js             # Game logic  
│   ├── styles.css          # Styling
│   └── instructions.html   # How to play
├── ☁️ infrastructure/
│   ├── serverless.yml      # AWS config
│   └── deploy.sh           # Deploy script
└── 📖 README.md            # Documentation
```

## 🏗️ Your AWS Setup

**What gets deployed:**
- 📦 **S3 Bucket** - hosts your game files (private)
- 🌐 **CloudFront** - serves your game globally
- 🔒 **Secure access** - only through CloudFront URL

## ✅ Testing Your Deployment

After deployment, check that:
- ✅ Game loads from CloudFront URL
- ✅ All features work (shooting, power-ups, bosses)
- ✅ No direct S3 access (security check)
- ✅ Costs stay reasonable

---

## 💡 Pro Tips

### Working with Kiro
- 🔄 **Build incrementally** - one feature at a time
- 🧪 **Test before moving on** - make sure each step works
- 📝 **Be specific** - describe exactly what you want
- 🔁 **Iterate freely** - use Kiro's strengths to refine your game

### Game Development
- ⚡ **Keep it smooth** - optimize your game loop
- 👀 **Visual feedback** - players need to see what's happening  
- 📈 **Balanced difficulty** - not too easy, not impossible
- � **rMulti-device support** - works on desktop and mobile

---

## 🐛 If Something Goes Wrong

### Game Issues
| Problem | Solution |
|---------|----------|
| 🐌 Game stutters | Check game loop efficiency |
| 🎮 Controls don't work | Review input handling code |
| 💊 Power-ups broken | Check state management |

### AWS Issues  
| Problem | Solution |
|---------|----------|
| 🚫 Deployment fails | Verify AWS permissions |
| 🌐 Game won't load | Check S3/CloudFront config |
| 💰 Unexpected charges | Review all AWS services |

### Get Help from Kiro
Ask Kiro: *"Please help me check if there are any missed AWS resources"*

---

## 🏆 You're Done When...

✅ **Game works perfectly** - shooting, enemies, power-ups, bosses  
✅ **Controls feel great** - both keyboard and mouse/touch  
✅ **Instructions are clear** - players know how to play  
✅ **Boss battles trigger** - every 200 points  
✅ **AWS deployment successful** - accessible via CloudFront  
✅ **Resources cleaned up** - no surprise bills  

## 🎯 See It In Action

**Live example:** https://dvru9fepx5b2b.cloudfront.net

---

*Ready to build something awesome? Let's go! 🚀*
