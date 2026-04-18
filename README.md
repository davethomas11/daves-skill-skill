# Dave's Skill-Skill: The Agentic Framework

This project provides a specialized, agent-agnostic skill that codifies a high-standard framework for building other Agentic Skills. It ensures your skills are secure, cross-agent compatible, and professionally documented.

> **Note:** This skill was built and tested primarily using **Gemini CLI**. While it includes installation support for Claude and GitHub Copilot, compatibility with those agents is provided on a best-effort basis.

## 🧠 What is an Agentic Skill?

Think of an **Agentic Skill** as a specialized "instruction manual" for your AI assistant. 

By default, AI agents are generalists. When you "install" this skill, you are giving your AI agent the specific tools, knowledge, and procedural instructions it needs to become an expert on a specific domain—in this case, the **Dave's Skill-Skill Framework**.

## 🛡️ Security & Transparency

This skill advocates for a **Security-First** approach, emphasizing the use of `.env` files and system-level secure stores (like macOS Keychain and Windows SecretStore) to protect sensitive credentials.

### Why use a System Secure Store (Key Vault)?
A system secure store provides a significantly higher level of protection than a standard `.env` file:

- **Encryption at Rest:** Unlike a `.env` file, which is plain text, these stores encrypt your keys using industry-standard algorithms (like AES). Even if someone gains access to your files, they cannot read the keys.
- **Session-Based Access:** These stores are often tied to your **User Login Session**. This means the keys are only "unlocked" when you are actively logged in.
- **Protection from Network Attacks:** If an attacker gains unauthorized access to your file system through the network, they might be able to steal your `.env` file, but they **cannot** decrypt the secrets in a secure store without your system password or a specific master key.
- **Agent Context:** Because the AI agent runs with your user permissions, it can securely request the keys on your behalf while you are at the terminal, keeping them out of permanent cleartext files.

---

## 🚀 The Four Pillars

1.  **Security-First Mindset**: Protect keys at all costs.
2.  **Agent-Agnostic Design**: Works with Gemini, Claude, and Copilot.
3.  **Unified Installation**: Interactive scripts for all agents.
4.  **Accessible Documentation**: Layman-friendly explanations and clear mandates.

---

## 🧪 Installation

You can install this framework skill itself using the provided scripts:

**On Windows (PowerShell):**
```powershell
.\install.ps1
```

**On Linux/macOS (Bash):**
```bash
chmod +x install.sh
./install.sh
```
