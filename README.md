# Open WebUI Agentic Project

This project is an instance of [Open WebUI](https://github.com/open-webui/open-webui), an extensible, feature-rich, and user-friendly self-hosted WebUI designed to operate entirely offline. It supports various LLM runners, including Ollama and OpenAI-compatible APIs.

## Technology Stack

### Agents & Frameworks
-   **Open WebUI**: The core platform providing the chat interface and agentic capabilities.
-   **LangChain**: Used for building LLM-powered applications and chains (`langchain`, `langchain-community`, `langchain-core` installed).
-   **LangGraph**: Used for building stateful, multi-actor applications with LLMs (`langgraph`, `langgraph-checkpoint`, `langgraph-sdk` installed).

### Programming Languages
-   **Python**: The primary backend language handling the application logic and integrations.
-   **JavaScript/TypeScript**: Used for the frontend interface (standard for Open WebUI).

### LLMs (Large Language Models)
The project is configured to support multiple model providers:
-   **Ollama**: For running local models (e.g., Llama 3, Mistral).
-   **OpenAI**: Integration for GPT models (`openai` package installed).
-   **Anthropic**: Integration for Claude models (`anthropic` package installed).
-   **Google Gemini**: Integration for Google's Generative AI (`google-generativeai`, `google-genai` packages installed).

## Setup Instructions

### Prerequisites
-   **Python 3.11+**
-   **Git**

### Installation

1.  **Clone the repository** (if moving to a new device):
    ```bash
    git clone <repository-url>
    cd <repository-directory>
    ```

2.  **Create and Activate Virtual Environment**:
    ```bash
    # Windows
    python -m venv venv
    .\venv\Scripts\activate
    ```

3.  **Install Dependencies**:
    ```bash
    pip install -r temp_requirements.txt
    # OR if you want to install the latest open-webui
    pip install open-webui
    ```

### Running the Application

To start the Open WebUI server, ensure your virtual environment is activated and run:

```bash
open-webui serve
```

The application should be accessible at `http://localhost:8080`.

### Environment Configuration
Ensure you have the necessary environment variables set for your LLM providers (e.g., `OPENAI_API_KEY`, `ANTHROPIC_API_KEY`, `OLLAMA_BASE_URL`).
