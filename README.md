# Agont - An Anthropic Claude Tool Agent

Agont is a CLI tool agent that integrates with Anthropic's Claude AI model to provide file system manipulation capabilities through natural language interaction. It serves as a bridge between Claude's intelligence and your local file system, allowing you to perform operations like reading files, listing directories, and making file edits through conversation.

This README was entirely written by Agont (except this sentence)!

## Features

- Interactive CLI interface for natural language interaction with Claude
- File system operations through conversation:
  - Read file contents
  - List files and directories
  - Edit text files
  - Get current working directory
- Built on Claude 3 Sonnet (Latest version)
- Environment variable configuration support

## Prerequisites

- Go 1.24.2 or later
- An Anthropic API key

## Installation

1. Clone the repository:
```bash
git clone https://github.com/neerajsamtani/agontic.git
cd agont
```

2. Install dependencies:
```bash
go mod download
```

3. Create a `.env` file in the project root and add your Anthropic API key:
```
ANTHROPIC_API_KEY=your_api_key_here
```

## Usage

1. Build and run the program:
```bash
go run main.go
```

2. Interact with the agent using natural language. For example:
- "Show me what's in the current directory"
- "Read the contents of main.go"
- "Create a new file called example.txt with 'Hello World' as content"

To exit the program, use `ctrl+c`.

## Available Tools

The agent provides the following tools:

1. `read_file`: Read the contents of a given relative file path
2. `list_files`: List files and directories at a given path
3. `edit_file`: Make edits to a text file (replace text or create new files)
4. `get_current_dir`: Get the current working directory path

## Dependencies

- [anthropic-sdk-go](https://github.com/anthropics/anthropic-sdk-go) - Anthropic's official Go SDK
- [jsonschema](https://github.com/invopop/jsonschema) - JSON Schema generation
- [godotenv](https://github.com/joho/godotenv) - Environment variable loading
