# Complete Setup Guide

This document provides a detailed, step-by-step guide to setting up the Open WebUI Agentic Project from scratch on your local machine.

## Table of Contents
1.  [Prerequisites](#prerequisites)
2.  [Cloning the Repository](#cloning-the-repository)
3.  [Python Environment Setup](#python-environment-setup)
4.  [Installing Dependencies](#installing-dependencies)
5.  [Local LLM Setup (Ollama & Gemma)](#local-llm-setup-ollama--gemma)
6.  [Environment Configuration](#environment-configuration)
7.  [Running the Application](#running-the-application)

---

## 1. Prerequisites

Before you begin, ensure you have the following software installed:

*   **Python 3.11**: [Download Python](https://www.python.org/downloads/)
    *   *Note*: During installation on Windows, ensure you check "Add Python to PATH".
*   **Git**: [Download Git](https://git-scm.com/downloads)


```

## 2. Python Environment Setup

It is best practice to use a virtual environment to manage dependencies locally.

**Windows:**
```bash
python -m venv venv
.\venv\Scripts\activate
```

**macOS/Linux:**
```bash
python3 -m venv venv
source venv/bin/activate
```

*You will know the virtual environment is active when you see `(venv)` at the beginning of your terminal prompt.*

## 3. Installing Dependencies

With your virtual environment activated, install the required Python packages:

```bash
pip install -r temp_requirements.txt
```

*Alternatively, if you wish to just install the core Open WebUI package:*
```bash
pip install open-webui
```

## 4. Local LLM Setup (Ollama & Gemma)

For detailed, step-by-step instructions on setting up Ollama and the Gemma model, including visual guides, please refer to our dedicated documentation:

👉 **[Read the Ollama & Gemma Setup Guide](OLLAMA_SETUP.md)**

*Return here after you have successfully verified that `ollama run gemma` works in your terminal.*


## 5. Environment Configuration

The application may require specific environment variables to connect to various utilities.

1.  Check if there is a `.env.example` file in the project. If so, copy it to `.env`.
2.  Open the `.env` file (or create one) and add your keys if you are using external providers:
    ```env
    # Example Configuration
    # OPENAI_API_KEY=your_openai_key_here
    # ANTHROPIC_API_KEY=your_anthropic_key_here
    
    # Ollama is usually auto-detected at http://localhost:11434
    # OLLAMA_BASE_URL=http://localhost:11434
    ```

## 6. Running the Application

Now you are ready to start the server. Ensure your virtual environment is active (see Step 3) and run:

```bash
open-webui serve
```

*   The server will start up.
*   Open your web browser and navigate to: `http://localhost:8080`

**Congratulations! You have successfully set up the Open WebUI Agentic Project.**
