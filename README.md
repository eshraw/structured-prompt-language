# structured-prompt-language README

This extension is a syntax highlighting and autocomplete extension for the Structured Prompt Language (SPL).

## Installation

- Open the Extensions view by clicking on the Extensions icon in the Activity Bar on the side of the window or by pressing `Ctrl+Shift+X`.
- Search for "Structured Prompt Language" in the search bar.
- Click on the "Install" button.

## Features

- Syntax highlighting for:
    - Tags
    - Variables
    - Strings
- Autocomplete
- Hover information

## About the Structured Prompt Language (SPL)

The Structured Prompt Language (SPL) is a declarative language that allows you to create prompts in a more readable and maintainable way as well as making the prompt more efficient. SPL is composed of 3 main components, tags, variables, and strings. The SPL syntax works within the n8n workflow editor but could be modified to work with other systems. This extension works with .spl files.

### Tags

Tags are used to define sections within the prompt. They are used to make the prompt more readable and maintainable. They help the user to organize the prompt into logical sections that are in turn more efficient to compute by the LLM model.
The following tags are available in SPL:

- `<AgentInstruction>`: Used to provide instructions to an AI agent. While this tag is not required, it is recommended to distinguish easily an Agent prompt from a non-Agent prompt
- `<Instructions>`: General purpose instruction tag to regroup multiple instructions
- `<Instruction>`: General purpose instruction tag
- `<Role>`: Defines the role or persona the AI should adopt
- `<Description>`: Provides detailed descriptions or context
- `<Example>`: Contains example content or usage patterns. Generally paired with the `<UserInput>` and any output tags.
- `<Query>`: Used for queries to be executed by the LLM model. Depending on the use case, this tag can be used for research queries, data retrieval, tool calls, etc.
- `<Goal>`: Defines objectives or desired outcomes, generally paired with the `<Primary>`, `<Secondary>`, and `<Tertiary>` tags.
- `<Primary>`: Indicates primary or main content
- `<Secondary>`: Indicates secondary or supporting content
- `<Tertiary>`: Indicates tertiary or additional content
- `<UserInput>`: Marks sections for user input
- `<AgentOutput>`: Designates expected agent output
- `<ChatbotInstruction>`: Specific instructions for chatbot behavior
- `<ChatbotOutput>`: Expected chatbot response content
- `<OutputLanguage>`: Designates the language of the output
- `<OutputFormat>`: Designates the format of the output
- `<Constraints>`: Defines constraints or limitations for the prompt
- `<Constraint>`: Defines a constraint for the prompt

### Variables

Variables are used to store values that can be fed to the LLM model and reused in the prompt. They are defined using the `$` symbol followed by the variable name constrained by `{}` such as `{$variable_name}`. This syntax works within the n8n workflow editor but could be modified to work with other systems.

### Strings

Strings are the core of the prompt. They carry the information that will be fed to the LLM model.

## Requirements

No requirements or dependencies needed to run this extension.

## Release Notes
### 1.0.0

Initial release of the Structured Prompt Language (SPL) syntax highlighting and autocomplete extension.

### 1.0.1
Update vscode supported version to 1.90

### 1.1.0
- Add support for the `<Instructions>` tag
- Add support for the `<Constraints>` tag
- Add support for the `<Constraint>` tag
- Add support for the `<OutputFormat>` tag
- Add support for the `Templates` prefilled prompt template