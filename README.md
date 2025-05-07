# Local AI Agent Deployment

Artificial Intelligence is becoming part of our everyday lives — from answering questions to automating tasks. So why not have your **own private, powerful local AI agent** running on your machine? It's **cool, fast, and secure** — and the best part? **You’re in control.**

This project demonstrates how to install and run your own local AI agent directly on your computer, ensuring full data privacy, and control over your environment.

---

## Why Deploy a Local AI Agent?

- **Full ownership of data**
- **Zero dependency on cloud services**
- **Faster interaction times**
- **Enhanced privacy and security**

---

## Table of Contents

- [Project Overview](#project-overview)
- [Installation Guide](#installation-guide)
- [Key Features](#key-features)
- [Use Cases](#use-cases)


---

## Project Overview

This project uses:

- **Ollama** – Lightweight LLM (Large Language Model) runtime, operating locally.
- **Open WebUI** – A browser-based interface to interact easily with your local AI.

By following this guide, you can install and interact with powerful language models entirely offline and securely.

---

## Installation Guide

### Requirements

- Linux OS (tested on Kali Linux)
- Python 3.11+ installed
- Docker installed
- Basic terminal knowledge

### Step 1: Install Ollama

This tool lets you run local AI models easily.

Visit the official [Ollama website](https://ollama.com) and download the Linux version.

Follow the installation instructions provided on the site.

Alternatively, install directly via terminal:

```bash
curl -fsSL https://ollama.com/install.sh | sh
```

Once installed, open your browser and navigate to:

```arduino
http://localhost:11434
```

If you see the Ollama service running, the installation is successful.

---

### Step 2: Download a Language Model

Pick a model that suits your needs from the Ollama Models Library.

Example to install `openhermes`:

```bash
ollama pull openhermes
```

To list installed models:

```bash
ollama list
```

---

### Step 3: Clone Web-UI Repository

Run the following commands in your terminal:

```bash
git clone https://github.com/browser-use/web-ui.git
cd web-ui
```

---

### Step 4: Set Up Python & Virtual Environment

You need Python 3.11+.

Create a virtual environment:

```bash
uv venv --python 3.11
```

Activate it:

```bash
source .venv/bin/activate
```

---

### Step 5: Install Dependencies

Next, install Python packages:

```bash
uv pip install -r requirements.txt
```

Additionally, install **Patchright** for Chromium browser support:

```bash
patchright install chromium
```

---

### Step 6: Configure Environment

Create a copy of the example environment file: 

```bash
cp .env.example .env
```

Register your personal API keys and other settings.
Open `.env` in your preferred text editor, for example:

```bash
vim .env 
```
![image](https://github.com/user-attachments/assets/eaf90b29-8090-40b4-a5cf-a133e3127ade)

Enter your API in this file.

Please note: If you enter your OPENAI_API_KEY, usage will be billed directly to your OpenAI account based on the number of tokens consumed.


### Step 7: Run the Agent on Your Machine

Launch your AI agent locally with:

```bash
python webui.py --ip 127.0.0.1 --port 7788
```

Leave this running in your terminal.

Now open your browser and navigate to:

```arduino
http://localhost:7788
```

🎉 You’re in! Your personal AI agent is now ready to work for you.

---

## Key Features

- 🖥️ **Fully Local Operation**: No external API calls.
- 🔒 **Enhanced Privacy**: Data remains on your machine.
- 🛠️ **Customizable Models**: Switch models according to needs.
- 🌐 **Browser-Based UI**: User-friendly experience with Open WebUI.

---

## Use Cases

- 📚 **Research Assistant**: Summarize notes, articles, and papers offline.
- 🛡️ **Secure Work Environments**: Operate AI in air-gapped or privacy-critical areas.
- 📝 **Content Generation**: Draft emails, reports, or articles without external exposure.
- 🔍 **Knowledge Management**: Upload and query your own private documents locally.

---





📎 **Ref**: [browser-use GitHub Repository](https://github.com/browser-use/browser-use)
