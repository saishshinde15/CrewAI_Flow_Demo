# CrewAI Flow Demo

A demonstration of creating comprehensive guides using CrewAI flows.

## Features

- Create structured guides on any topic
- Customize content for different audience levels
- Automatic outline generation
- Section-by-section content creation
- Markdown output formatting

## Setup

1. Create a virtual environment:
```bash
python -m venv .venv
source .venv/bin/activate  # On Windows: .venv\Scripts\activate
```

2. Install dependencies:
```bash
pip install crewai
```

## Usage

Run the guide creator flow:
```bash
python src/guide_creator_flow/main.py
```

The guide will be saved in the `output` directory as `complete_guide.md`.

## Project Structure

```
guide_creator_flow/
├── src/
│   └── guide_creator_flow/
│       ├── crews/
│       │   └── content_crew/
│       │       ├── content_crew.py
│       │       └── config/
│       │           ├── agents.yaml
│       │           └── tasks.yaml
│       └── main.py
└── output/
    └── complete_guide.md
```

## Installation

Ensure you have Python >=3.10 <3.13 installed on your system. This project uses [UV](https://docs.astral.sh/uv/) for dependency management and package handling, offering a seamless setup and execution experience.

First, if you haven't already, install uv:

```bash
pip install uv
```

Next, navigate to your project directory and install the dependencies:

(Optional) Lock the dependencies and install them by using the CLI command:
```bash
crewai install
```

### Customizing

**Add your `OPENAI_API_KEY` into the `.env` file**

- Modify `src/guide_creator_flow/config/agents.yaml` to define your agents
- Modify `src/guide_creator_flow/config/tasks.yaml` to define your tasks
- Modify `src/guide_creator_flow/crew.py` to add your own logic, tools and specific args
- Modify `src/guide_creator_flow/main.py` to add custom inputs for your agents and tasks

## Running the Project

To kickstart your flow and begin execution, run this from the root folder of your project:

```bash
crewai run
```

This command initializes the guide_creator_flow Flow as defined in your configuration.

This example, unmodified, will run the create a `report.md` file with the output of a research on LLMs in the root folder.

## Understanding Your Crew

The guide_creator_flow Crew is composed of multiple AI agents, each with unique roles, goals, and tools. These agents collaborate on a series of tasks, defined in `config/tasks.yaml`, leveraging their collective skills to achieve complex objectives. The `config/agents.yaml` file outlines the capabilities and configurations of each agent in your crew.

## Support

For support, questions, or feedback regarding the CrewAI Flow Demo or crewAI.

- Visit our [documentation](https://docs.crewai.com)
- Reach out to us through our [GitHub repository](https://github.com/joaomdmoura/crewai)
- [Join our Discord](https://discord.com/invite/X4JWnZnxPb)
- [Chat with our docs](https://chatg.pt/DWjSBZn)

Let's create wonders together with the power and simplicity of crewAI.
