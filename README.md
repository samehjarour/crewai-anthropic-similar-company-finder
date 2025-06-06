# CrewAI Anthropic Similar Company Finder

[![Test Status](https://github.com/samehjarour/crewai-anthropic-similar-company-finder/workflows/Test%20CrewAI%20Anthropic%20Integration/badge.svg)](https://github.com/samehjarour/crewai-anthropic-similar-company-finder/actions)
[![Python 3.10+](https://img.shields.io/badge/python-3.10+-blue.svg)](https://www.python.org/downloads/)
[![CrewAI](https://img.shields.io/badge/CrewAI-0.76.2+-green.svg)](https://crewai.com)
[![Anthropic Claude](https://img.shields.io/badge/Anthropic-Claude%203.5%20Sonnet-orange.svg)](https://anthropic.com)
[![Docker](https://img.shields.io/badge/Docker-Ready-blue.svg)](https://docker.com)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)

Welcome to the CrewAI Anthropic Similar Company Finder project, powered by [crewAI](https://crewai.com) and [Anthropic's Claude](https://anthropic.com). This template is designed to help you set up a multi-agent AI system with ease, leveraging the powerful and flexible framework provided by crewAI. Our goal is to enable your agents to collaborate effectively on complex tasks, maximizing their collective intelligence and capabilities.

## Installation

Ensure you have Python >=3.10 <=3.13 installed on your system. This project uses [UV](https://docs.astral.sh/uv/) for dependency management and package handling, offering a seamless setup and execution experience.

First, if you haven't already, install uv:

```bash
pip install uv
```

Next, navigate to your project directory and install the dependencies:

1. First lock the dependencies and then install them:
```bash
uv lock
```
```bash
uv sync
```
### Customizing

**Add your `ANTHROPIC_API_KEY` into the `.env` file**

This project has been configured to use Anthropic's Claude models instead of OpenAI. You'll need an Anthropic API key from [Anthropic Console](https://console.anthropic.com/).

- Modify `src/similar_company_finder_template/config/agents.yaml` to define your agents
- Modify `src/similar_company_finder_template/config/tasks.yaml` to define your tasks
- Modify `src/similar_company_finder_template/crew.py` to add your own logic, tools and specific args
- Modify `src/similar_company_finder_template/main.py` to add custom inputs for your agents and tasks

## Running the Project

To kickstart your crew of AI agents and begin task execution, run this from the root folder of your project:

```bash
$ crewai run
```
or
```bash
uv run similar_company_finder_template
```

This command initializes the similar-company-finder-template Crew, assembling the agents and assigning them tasks as defined in your configuration.

This example, unmodified, will run the create a `approach_recommendations.md` file with the output of a company analysis in the root folder.

## Production Deployment

This project is production-ready and configured to use Anthropic's Claude models. For detailed deployment instructions, see [DEPLOYMENT.md](DEPLOYMENT.md).

### Quick Production Setup

1. **Set up environment variables:**
   ```bash
   cp .env .env.production
   # Edit .env.production with your actual API keys
   ```

2. **Deploy with Docker:**
   ```bash
   docker-compose up -d --build
   ```

3. **Monitor logs:**
   ```bash
   docker-compose logs -f similar-company-finder
   ```

### Environment Variables

- `ANTHROPIC_API_KEY`: Required - Your Anthropic API key
- `SERPER_API_KEY`: Optional - For web search functionality
- `TARGET_COMPANY`: The company to analyze
- `OUR_PRODUCT`: Your product description

## Understanding Your Crew

The similar-company-finder-template Crew is composed of multiple AI agents, each with unique roles, goals, and tools. These agents collaborate on a series of tasks, defined in `config/tasks.yaml`, leveraging their collective skills to achieve complex objectives. The `config/agents.yaml` file outlines the capabilities and configurations of each agent in your crew.

## Support

For support, questions, or feedback regarding the SimilarCompanyFinderTemplate Crew or crewAI.
- Visit our [documentation](https://docs.crewai.com)
- Reach out to us through our [GitHub repository](https://github.com/joaomdmoura/crewai)
- [Join our Discord](https://discord.com/invite/X4JWnZnxPb)
- [Chat with our docs](https://chatg.pt/DWjSBZn)

Let's create wonders together with the power and simplicity of crewAI.
