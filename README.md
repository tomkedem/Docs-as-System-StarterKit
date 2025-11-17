# Docs as System StarterKit

The Docs as System StarterKit is a CLI tool that creates a new project aligned with the Docs as System methodology.  
It prepares a clean project structure, initializes the documentation folder with ready to use templates, and sets up the environment for working with an AI agent inside the IDE.

The purpose is to begin every project with a consistent, organized, and fully documented baseline, without spending time creating folders and configuration files manually.

## Installation

### Using npx
npx docs-as-system-starterkit init my-project

### Global installation
npm install -g docs-as-system-starterkit
dass init my-project

## Available Commands

Create a new project
dass init project-name

This command creates a new project that includes:

• Starter project skeleton  
• Complete docs folder with templates  
  agent  
  planning  
  architecture  
  logs  
  automation  
  project  
• AGENT_CONFIG.yaml for project configuration  
• Git workflow scripts inside automation/git  
• Core configuration files  
  .gitignore  
  .editorconfig  
  .gitattributes  
• Basic README for the generated project  

## Project Structure

After the project is created, the folder will look like this:
```plaintext
📁 my-project/
📄 .editorconfig
📄 .gitattributes
📄 .gitignore
📄 README.md
📁 src/
    📁 automation/
        📁 git/
            📄 CREATE_BRANCH.sh
            📄 MERGE_AFTER_APPROVAL.sh
            📄 OPEN_PULL_REQUEST.sh
            📄 PUSH_BRANCH.sh
            📄 STAGE_AND_COMMIT.sh
            📄 README.md
📁 docs/
    📁 agent/
    📁 architecture/
    📁 planning/
    📁 automation/
    📁 project/
    📁 logs/
```
## What to Do After Creating a New Project

Open:
docs/IMPLEMENTATION_GUIDE.md

This guide explains the full Docs as System workflow:

• How to complete the planning documents  
• How to configure the AI agent and its permissions  
• How the logging system works  
• How to execute a full development cycle  
• What belongs to the human and what belongs to the agent  

## Why Docs as System

Docs as System connects documentation, code, workflows, and AI agents into a single living system.  
It is especially suited for environments where AI agents operate inside the IDE and must understand the intent and structure of the project.

## Contributors

The StarterKit was created with the help of several contributors.  
Every contribution is acknowledged to maintain transparency and professional appreciation.

Contributors to the Docs as System StarterKit

• Yuval Vanunu  
  Contributed to the early concept development and supported CLI design.

• Yehonatan Maman  
  Provided testing, deep review, and improvements to several templates.

Becoming a contributor

If you improved templates, fixed issues, contributed code, or otherwise helped shape the tool,  
you are welcome to open a Pull Request.  
Once approved, your name will be added to this section.

## License

MIT License  
Free to use, modify, and integrate into any project.

GitHub repository  
https://github.com/tomkedem/Docs-as-System-StarterKit

© 2025 Tomer Kedem  
Part of the official Docs as System template suite.
