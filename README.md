# Cursor CLI: AI Coding Assistant

Cursor CLI is an interactive, agentic AI coding assistant for your terminal. It leverages multiple LLM (Large Language Model) API keys to answer coding questions, generate and edit code, run shell commands, and interact with your file system - all in a structured, conversational way.

## Setup

1. **Clone the repository:**
   ```sh
   git clone https://github.com/dhruvagrawal1080/Cursor-CLI.git
   cd cursor
   ```

3. **Set up your environment variables:**
   - Create a `.env` file in the project root with your LLM API keys:
     ```env
     GOOGLE_API_KEY1=your_api_key
     ```

4. **Run the assistant:**
   ```sh
   python cursor.py
   ```

## Usage
- Type your coding question or command at the prompt (`>`).
- The assistant will respond in a structured, step-by-step format.
- You can:
  - Ask for code generation or editing
  - Request file reads/writes
  - Run shell commands (e.g., list files, create folders)
  - Get explanations or debugging help

### Example Interactions
```
> Create a Python script that prints Hello, World!
🤖: The file hello_world.py has been created in the project folder.

> Show me all files in the current directory
🤖: Here is the list of files in the current directory.

> Read the contents of hello_world.py
🤖: Here is the content of hello_world.py.
```

## Customization
- **System Prompt:** Edit the `systemPrompt` variable in `cursor.py` to change the assistant's behavior, code style, or rules.
- **Tools:** Add or modify tool functions in `cursor.py` to extend capabilities.

## Safety & Best Practices
- The assistant will never perform destructive actions (like deleting files) without checking first.
- All file changes are made using safe Python functions, not shell commands.
- New projects are always created in their own folders for organization.