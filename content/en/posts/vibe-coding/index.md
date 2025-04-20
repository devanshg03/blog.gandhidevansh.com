---
title: Vibe Coding Guide
date: 2025-04-19
author: Devansh Gandhi
description: Everything you need to start vibe-coding—setting up your development environment and understanding our tech stack.
isStarred: true
---

By [Devansh Gandhi](https://x.com/itzdgofficial)

## Introduction

This is my personal workflow for vibe-coding at Decisions Lab. We use this workflow to quickly protoype, and iterate on our product features, and I also use this to code my own projects for fun. We use a combination of AI tools, particularly Cursor, and v0, but the same workflow and principles can be applied to any tool such as Copilot, Replit, Lovable, Bolt and more.

## Our Vibe Coding Stack

Here are the key technologies we build our product on top of, these are not just easy to use, but are extremely scalable in the long-term. Next.js is used by companies such as OpenAI, Claude, Spotify and [more](https://nextjs.org/showcase).

Framework and hosting:

- **[Next.js](https://nextjs.org/)** — Our programming framework.
- **[Vercel](https://vercel.com/)** — Our host for the web app.

Database and authentication:

- **[Supabase](https://supabase.com/)** — Where our stuff is stored.
- **[Stackauth](https://stack-auth.com/)** — Our login provider and handler.

AI Tools:

- **[Cursor](https://www.cursor.com/)** — Our 100x engineer that codes the project.
- **[v0](https://v0.dev/)** — Our 10x engineer that prototypes our UI.

## Building Blocks of the Internet

Although this guide is on vibe-coding, and letting the LLM take charge, it is still important to understand the building blocks of the internet, so that you will have a much better time debugging and understanding the code when things inevitably go wrong. You can think og the internet as a LEGO set, with HTML, CSS and JavaScript as the items included in the set.

- **HTML** — The structure, like the bricks you use to build castles.

  - Learn the basics with [MDN's HTML Basics](https://developer.mozilla.org/en-US/docs/Learn/Getting_started_with_the_web/HTML_basics), or use this prompt with your favorite AI model:

  ```
  "I am a complete beginner to web development. I want to learn HTML. Can you explain the basics of HTML in a way that is easy to understand? Focus only on the basics I need to know to build an MVP for my project."
  ```

- **CSS** — Styles your structure, making the bricks colorful and visually appealing.

  - We will use a slightly different version of CSS, called Tailwind CSS, which is a utility-first CSS framework that can be used to build complex designs with the least amount of code, you can use this prompt with your favorite AI model to learn more about it:

  ```
  "I am a complete beginner to web development. I want to learn Tailwind CSS. Can you explain the basics of Tailwind CSS in a way that is easy to understand? Focus only on the basics I need to know to build an MVP for my project."
  ```

- **JavaScript** — Brings interactivity and life, just like motors and sensors in a LEGO robot.

  - Begin with [JavaScript.info](https://javascript.info/) or use this prompt with your favorite AI model:

  ```
  "I am a complete beginner to web development. I want to learn JavaScript. Can you explain the basics of JavaScript in a way that is easy to understand? Focus only on the basics I need to know to build an MVP for my project."
  ```

## Version Control and Security

- **Version Control**:

  - Git and GitHub help you keep track of your changes and collaborate seamlessly.
  - Learn Git basics with [GitHub's Git Handbook](https://guides.github.com/introduction/git-handbook/) or use this prompt with your favorite AI model:

  ```
  "I am a complete beginner to web development. I want to learn Git. Can you explain the basics of Git in a way that is easy to understand? Focus only on the basics I need to know to build an MVP for my project."
  ```

- **Security**:

  - Keep your credentials and sensitive data secure—if something feels off, it probably is, especially be careful with your API keys and secrets. Use this prompt with your favorite AI model to learn more about security:

  ```
  "I am a complete beginner to web development. I want to learn about security. Can you explain the basics of security in a way that is easy to understand? What are API Keys and .env files? How can I make sure my credentials and sensitive data are secure? Focus only on the basics I need to know to build an MVP for my project."
  ```

## Development Environment Setup (macOS)

One of the ticky parts of programming is making sure your development environment is setup correctly. Follow these steps to ensure you have a smooth experience.

### 1. Create a GitHub Account

Visit [GitHub Signup](https://github.com/signup) and follow the prompts to create an account. GitHub is essential for version control and collaboration with other developers.

### 2. Install Cursor IDE

Visit [Cursor](https://cursor.com), download the installer for your OS, and follow the prompts to install the IDE. You can sign in with your GitHub account.

### 3. Install Homebrew

Homebrew is a package manager for macOS that allows you to install software easily, this can include Node.js, Git, Python, and more. Follow the [official Homebrew installation guide](https://brew.sh) or use open your terminal and paste the following command:

```bash
/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"
```

### 4. Install Node.js

Node.js is a runtime environment that allows you to run JavaScript code outside of the browser. It is used to build web applications and APIs. You can install it via Homebrew:

```bash
brew install node
```

### 5. Install Git

Git is a version control system that allows you to track changes to your code. It is used to collaborate with other developers and to keep track of your code history. You can install it via Homebrew:

```bash
brew install git
```

### 6. Create a folder for your projects

Create a folder in your preferred location to store your coding projects. You can create this directly using finder. Then, you can open this folder in Cursor by opening Cursor, clicking 'open folder' and selecting the folder.

### 7. Now, you are ready to vibe-code, and can start coding your project.

## Vibe-Coding Your App

The magic of vibe-coding happens when you partner with AI to go from idea to implementation. Here's how to vibe-code an app:

### 1. Plan with AI

Start by creating a Product Requirements Document (PRD) with Cursor, by asking the following prompt, set the chat mode to 'chat' or by pressing "Cmd + L".

```
"You are an expert product manager. I want to build [your app idea]. Help me create a Product Requirements Document. We will be using Next.js, Supabase and Stackauth for this project.

Do NOT code yet. Instead, ask me follow-up questions to clarify on my idea, and then organize this into a structured PRD with sections for Overview, User Personas, Core Requirements, Technical Stack, and Implementation.

One we are done, help save the PRD as docs/requirements.md in my project."
```

### 2. Step-by-Step Implementation

Now ask Cursor to work on your app step by step by asking the following prompt, set the chat mode to 'agent' or by pressing "Cmd + I".

```
"Let's implement the app described in @docs/requirements.md step by step:

Please give me explicit instructions on setting up our database, and what tables we need to create. We are using Next.js, Supabase and Stackauth for this project, alongwith Shadcn UI components and Tailwind CSS.

1. First, help me set up the project structure and initial files
2. Then, let's build the core components one by one
3. Next, we'll implement the main functionality
4. Finally, we'll add styling and polish
"
```

Follow Cursor's guidance and build your app iteratively, asking for help at each step.

## AI Models Review (April 2025)

As of April 20th, 2025, here's my breakdown of which AI models excel at different tasks (note that this might change anytime as models evolve):

### Best for Code Generation & UI Elements

- **Anthropic Claude 3.7-Sonnet / Claude 3.5 Sonnet**
  - Excels at generating clean, well-structured code
  - Particularly strong with UI component design
  - The "thinking" feature provides detailed reasoning about implementation choices
  - Other Anthropic models in this family also perform well for code tasks

### Best for Large Codebases & Complex Tasks

- **Google Gemini 2.5 Pro**
  - Excellent at understanding and navigating complex codebases
  - Can maintain context across thousands of files
  - Particularly good at refactoring and optimizing existing code
  - Handles multi-file projects better than most alternatives

### Best for Complex Algorithms

- **OpenAI o3 / o4-mini**
  - Specializes in optimization problems and algorithm design
  - Excellent at explaining complex mathematical concepts
  - Can generate efficient implementations of data structures
  - The mini version offers good performance at lower cost

### Best for Simple Changes & Speed

- **OpenAI GPT-4.1 / GPT-4.1-mini**
  - Fastest response time for quick edits and simple tasks
  - Great for routine coding tasks like formatting or small fixes
  - Efficient when you need immediate assistance
  - Mini version maintains most capabilities at lower latency

Remember, these recommendations reflect the state of AI as of April 2025 and may change rapidly as models evolve.
