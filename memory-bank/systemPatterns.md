# System Patterns

## System Architecture

- Monorepo containing multiple independent sample agent applications.
- Each agent resides in its own subdirectory within `agents/`.
- Each agent typically follows ADK patterns (e.g., using `Agent`, `Tool`, potentially `HumanInTheLoop`, evaluation components).
- Agents often interact with external APIs (especially Google Cloud) via tools.

## Key Technical Decisions

- Use of Google ADK as the core framework.
- Modular design with separate directories for each agent.
- Use of Poetry for dependency management per agent.
- Reliance on `.env` files for configuration.

## Design Patterns

- Agent-Based Systems (Core ADK concept)
- Tool Usage (Agents leveraging specific functions/APIs)
- Potentially: Chain-of-Thought, ReAct (depending on specific agent implementations)
- Configuration Management (via `.env`)
- Dependency Injection (likely within ADK framework)

## Component Relationships

- The main repository (`adk-samples`) acts as a container.
- Individual agents (`agents/<agent_name>`) are largely self-contained applications.
- Agents utilize the `adk-python` library for core functionality.
- Agents interact with external services (GCP, etc.) through configured credentials. 