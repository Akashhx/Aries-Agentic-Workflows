# Ollama & Gemma Setup Guide

This guide specifically covers how to set up the Ollama local LLM runner and deploy the Gemma model for use with Open WebUI.

## Overview
1.  **Install Ollama**: The runtime for local models.
2.  **Pull Gemma**: Downloading the model weights.
3.  **Verify Connection**: Ensuring Open WebUI can talk to Ollama.

---

## Step 1: Install Ollama

Ollama is a lightweight, extensible framework for building and running language models on your local machine.

1.  Visit the official website: [https://ollama.com/](https://ollama.com/)
2.  Click **Download** and select your operating system (Windows, macOS, or Linux).
3.  Run the installer and check that it completes successfully.
    *   *Windows Tip*: You may need to restart your terminal or computer after installation.

## Step 2: Pull the Gemma Model

Gemma is a family of lightweight, state-of-the-art open models built from the same research and technology used to create the Gemini models.

1.  Open your terminal (PowerShell, CMD, or Bash).
2.  Run the following command:

    ```bash
    ollama run gemma
    ```

3.  Wait for the download to complete. Once finished, you will drop into a chat prompt. You can test it by saying "Hello".
4.  Exit the chat by typing `/bye`.

> **Note**: Ollama runs in the background. As long as the icon is in your system tray (Windows/Mac) or the service is active (Linux), Open WebUI can connect to it.

## Step 3: Verify in Open WebUI

1.  Start your Open WebUI server if it's not already running:
    ```bash
    open-webui serve
    ```
2.  Go to `http://localhost:8080`.
3.  In the model selector (usually top-left or in Settings), look for **gemma**.

