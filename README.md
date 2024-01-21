# Project Title: AI-Enhanced Code Automation Suite

## Description

This project presents a comprehensive suite of Python tools designed to automate various aspects of software
development, leveraging the power of AI. It integrates the `langchain-core` and `langchain-openai` libraries to generate
code-related outputs, including documentation, refactoring, security analysis, and more. Each tool is an agent focusing
on a specific area, such as data mesh principles, code refactoring, security assessments, test case generation, and
agile feature suggestions.

The agents operate on provided code snippets, analyzing and transforming them based on the guidelines embedded within
their prompts. These prompts incorporate principles from clean coding, security, data mesh, and other development
practices, translating these into actionable insights and modifications to the code.

The system is designed to work continuously, detecting changes in a designated input file and updating the outputs
accordingly. This dynamic approach makes it particularly useful for ongoing projects where code evolves over time.

## Installation

To use this project, follow these steps:

### Prerequisites

- Python >= 3.10
- Git (for cloning the repository)
- An OpenAI API key (for AI-driven functionalities)

### Setup

1. **Clone the Repository**:
   ```bash
   git clone https://github.com/BenLinnik/helferlein
   cd helferlein
   ```

2. **Environment Setup**:
    - Copy the `.env.template` file to a new file named `.env`.
    - Replace `"sr-<your_open_ai_api_key_here>"` in the `.env` file with your actual OpenAI API key.

3. **Install Dependencies**:
   ```bash
   pip install -r requirements.txt
   ```

4. **Set path to your python project**:
    - Open the `common.py` file,
    - Adjust the `PROJECT_MAIN_FILE` and `PROJECT_FILE_PATH` variables to match your project's main file and path.

## Usage

To run the suite, execute the `all_agents.py` script. This script uses a `ThreadPoolExecutor` to run each agent
concurrently, allowing for efficient processing. This requires Python 3.10 or higher.

```bash
python all_agents.py
```

Each agent reads from a specified input file, analyzes the code, and generates an output file.
The outputs include:

- **Documentation** (German): Generated by `agent_documentation.py`, provides a clear and understandable documentation
  of the code functions in Markdown format.
- **Data Mesh Recommendations**: Created by `agent_data_mesh.py`, it suggests improvements to the code considering data
  mesh principles.
- **Refactored Code**: `agent_refactor.py` refactors the code based on clean code principles.
- **Security Analysis**: Conducted by `agent_security.py`, it assesses and rates the security of the code.
- **Unit Tests**: Generated by `agent_tests.py`, it creates unit tests for each function in the code.
- **Development Requirements**: `agent_requirements.py` creates a `requirements.txt` file based on the code's
  dependencies.
- **Code Review** (German): Performed by `agent_review.py`, it evaluates the code on various aspects like readability,
  structure, and maintainability.
- **Agile Feature Suggestions** (German): `agent_whatsnext.py` proposes new features and improvements for the code.

The agents continuously monitor for changes in the input file and update their outputs accordingly.

## Contributing

Contributions to this project are welcome. Please follow these steps to contribute:

1. **Fork the Repository**: Create your own copy of the project.
2. **Create a Feature Branch**: Make your changes in a new git branch.
3. **Commit Your Changes**: Commit your changes with clear commit messages.
4. **Push to the Branch**: Push your changes to your fork.
5. **Submit a Pull Request**: Open a pull request to the original repository with a clear title and description.

## License

This project is licensed under the MIT License - see the `LICENSE` file for details.