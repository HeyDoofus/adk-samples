# Tech Context

## Technologies Used

- Google Agent Development Kit (ADK) - Python library (`adk-python`)
- Python
- Poetry (for dependency management)
- Google Cloud Platform (GCP) services (Vertex AI, BigQuery, etc. - varies by agent)
- Google AI Models (Gemini, etc.)
- `.env` files for configuration/secrets management

## Development Setup

1.  Install ADK (`adk-python`).
2.  Clone the `adk-samples` repository.
3.  Navigate to a specific agent directory (`agents/<agent_name>`).
4.  Create a `.env` file (often by copying `.env.example`) and populate it with necessary credentials (API keys, GCP project ID/location) following ADK installation/quickstart guides.
5.  Install agent-specific dependencies using `poetry install`.
6.  Follow the agent's `README.md` to run.

## Technical Constraints

- Assumes familiarity with Python and potentially GCP.
- Requires proper setup of environment variables and credentials, which can be complex.
- Designed and tested primarily with Google models on Vertex AI, though other models might work.

## Dependencies

- `adk-python` library.
- Agent-specific Python packages (managed via Poetry).
- External services (e.g., Google Cloud APIs, potentially others depending on the agent). 