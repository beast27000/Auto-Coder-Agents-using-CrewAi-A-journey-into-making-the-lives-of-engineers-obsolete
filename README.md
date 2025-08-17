# Coder Crew

Welcome to the Coder Crew project, powered by [CrewAI](https://crewai.com/). Unlike a simple LLM chatbot, this project demonstrates how agentic AI can work as a true autonomous system:

- Multiple AI agents collaborate to write their own code.
- The code is then executed inside a Docker container.
- Agents can evaluate the execution output and refine their work.
- Final results are automatically generated, with minimal or no human in the loop.

This showcases that agentic AI can function not just as a reasoning tool, but as an operational coding assistant capable of interacting with external tools, running processes, and closing the feedback loop end-to-end.

## Installation

Ensure you have Python >=3.10 <3.13 installed on your system. This project uses [UV](https://github.com/astral-sh/uv) for dependency management and package handling, offering a seamless setup and execution experience.

First, if you haven't already, install uv:

```bash
pip install uv
```

Next, navigate to your project directory and install the dependencies:

(Optional) Lock the dependencies and install them by using the CLI command:

```bash
crewai install
```

## Configuration

- Add your `OPENAI_API_KEY` into the `.env` file.
- Modify `src/coder/config/agents.yaml` to define your agents.
- Modify `src/coder/config/tasks.yaml` to define your tasks.
- Modify `src/coder/crew.py` to add your own logic, tools, and specific args.
- Modify `src/coder/main.py` to add custom inputs for your agents and tasks.

## Running the Project

To kickstart your crew of AI agents and begin task execution, run this from the root folder of your project:

```bash
crewai run
```

This command initializes the Coder Crew, assembling the agents and assigning them tasks as defined in your configuration.

Unmodified, this example will create a `report.md` file in the root folder — but more importantly, the agents will:

- Write working code for the assigned problem.
- Spin up a Docker container and execute that code.
- Capture and analyze outputs, iterating if needed.

## Understanding Your Crew

The Coder Crew is composed of multiple AI agents, each with unique roles, goals, and tools. These agents collaborate on a series of tasks, defined in `config/tasks.yaml`, leveraging their collective skills to achieve complex objectives.

The pipeline looks like this:

- **Planner Agent** → Designs the coding approach.
- **Coder Agent** → Writes the code.
- **Executor Agent** → Runs the code inside Docker.
- **Reviewer Agent** → Checks results and suggests improvements.

This workflow demonstrates how agentic AI can autonomously code, execute, and verify results without relying on humans to close the loop.

## Outcome

By the end of execution, the project showcases:

- Autonomous agents writing and running code.
- Containerized execution with Docker.
- Final outputs generated directly by the system.
- A live example of agentic AI replacing human-in-the-loop coding workflows.

## Support

For support, questions, or feedback regarding the Coder Crew or CrewAI:

- Visit our [documentation](https://docs.crewai.com/)
- Reach out to us through our [GitHub repository](https://github.com/crewAI)
- Join our [Discord](https://discord.com/invite/crewAI)
- Chat with our docs

Let’s create wonders together with the power and simplicity of CrewAI 🚀

Made by Vishvvesh Nagappan

![WhatsApp Image 2025-07-10 at 14 10 46_21485451](https://github.com/user-attachments/assets/5b6605d1-1810-4bf5-a2dc-36203ec2938f)
