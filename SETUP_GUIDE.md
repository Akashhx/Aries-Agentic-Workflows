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

*   **Python 3.11 or higher**: [Download Python](https://www.python.org/downloads/)
    *   *Note*: During installation on Windows, ensure you check "Add Python to PATH".
*   **Git**: [Download Git](https://git-scm.com/downloads)

## 2. Cloning the Repository

Open your terminal or command prompt (PowerShell or CMD on Windows) and run the following commands to download the project code:

```bash
git clone <repository-url>
cd <repository-directory>
```
*Replace `<repository-url>` with the actual URL of this repository and `<repository-directory>` with the name of the folder created.*

## 3. Python Environment Setup

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

## 4. Installing Dependencies

With your virtual environment activated, install the required Python packages:

```bash
pip install -r temp_requirements.txt
```

*Alternatively, if you wish to just install the core Open WebUI package:*
```bash
pip install open-webui
```

## 5. Local LLM Setup (Ollama & Gemma)

This project uses Ollama to run local Large Language Models (LLMs) like Gemma.

### Step 5.1: Install Ollama
1.  Go to the [Ollama Website](https://ollama.com/).
2.  Download the installer for your OS (Windows, macOS, or Linux).
3.  Run the installer and follow the on-screen instructions.

### Step 5.2: Pull and Run Gemma
Once Ollama is installed, you need to download the Gemma model. Open a **new** terminal window (so it recognizes the `ollama` command) and run:

```bash
ollama run gemma
```

This command will:
1.  Download the Gemma model weights (this may take a few minutes depending on your internet connection).
2.  Start an interactive chat session with Gemma.
3.  You can type `/bye` to exit the chat, but keep the Ollama service running in the background.

## 6. Environment Configuration

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

## 7. Running the Application

Now you are ready to start the server. Ensure your virtual environment is active (see Step 3) and run:

```bash
open-webui serve
```

*   The server will start up.
*   Open your web browser and navigate to: `http://localhost:8080`

**Congratulations! You have successfully set up the Open WebUI Agentic Project.**
