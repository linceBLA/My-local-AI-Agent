# My local AI Agent
# How I Installed My Own Local AI Agent on Kali Linux (or Linux/WSL)

Artificial Intelligence is becoming part of our everyday lives — from answering questions to automating tasks. So why not have your **own private, powerful local AI agent** running on your machine? It's **cool, fast, and secure** — and the best part? **You’re in control.**

This guide is based on the amazing video by [NetworkChuck on YouTube](https://www.youtube.com/watch?v=sxTNACldK3Y). I adapted it for **Kali Linux** — but it works on any Linux distro (or Windows via WSL).

> **💡 Important**: You need a local LLM (like via **Ollama**) installed and running first!

---

## 🚀 Step-by-Step Installation Guide (Linux / Kali / WSL)

### 1. 🛠️ Install Ollama

This tool lets you run local AI models easily.

In your terminal, run:

```bash
curl -fsSL https://ollama.com/install.sh | sh
```



Once installed, open your browser and go to:

[http://localhost:11434](http://localhost:11434)

If you see an Ollama welcome message, you're ready to go!

---

### 2. 🧩 Download a Language Model

Pick one that suits your needs on [https://ollama.com](https://ollama.com) → click **Models**. You can also ask ChatGPT for suggestions.

Example to install `openhermes`:

```bash
ollama pull openhermes
```



To list installed models:

```bash
ollama list
```



---

### 3. 🐍 Set Up Python & Virtual Environment

You need Python 3.11+.

Create a virtual environment:

```bash
python3 -m venv myenv
```

Activate it:

```bash
source myenv/bin/activate
```

---

### 4. 🤖 Install the Local AI Agent (browser-use)

Now install your own AI agent interface:

```bash
pip install browser-use
```

And install Patchright for Chromium browser support:

```bash
pip install patchright
```
```bash
patchright install chromium
```

---

### 5. 🔌 Run the Agent on Your Machine

Launch your AI agent locally with:

```bash
python webui.py --ip 127.0.0.1 --port 7788
```

Leave this running in your terminal.

Now open your browser and go to:

[http://localhost:7788](http://localhost:7788)

🎉 You’re in! Your personal AI agent is now ready to work for you.

---

## 🏁 You're Done — Congrats!

You can now:

- 🧠 Ask questions and get answers from your own private AI
- 🔁 Change models anytime using `ollama pull`
- 🌐 Connect APIs like GPT-4 if you want to mix local + cloud
- 🛡️ Keep your data safe, on your device — no cloud needed!

---

## ✅ Why Having a Local AI Agent Rocks

- 💸 **No monthly fees** — run your own AI 100% free
- 🔐 **Private** — your data never leaves your machine
- 🔄 **Flexible** — switch models anytime

---

📎 **Ref**: [browser-use GitHub Repository](https://github.com/)
