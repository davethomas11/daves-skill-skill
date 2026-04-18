# [Project Name]

[A generic, agent-agnostic description of the skill's purpose.]

> **Note:** This skill was built and tested primarily using **Gemini CLI**. While it includes installation support for Claude and GitHub Copilot, compatibility with those agents is provided on a best-effort basis.

## 🧠 What is an Agentic Skill?

Think of an **Agentic Skill** as a specialized "instruction manual" for your AI assistant. 

By default, AI agents are generalists. When you "install" this skill, you are giving your AI agent the specific tools, knowledge, and procedural instructions it needs to become an expert on [Skill Domain].

## 🛡️ Security & Transparency

### Safe Key Management
This skill is designed to use **environment variables** for sensitive information. By using a `.env` file, your keys are automatically redacted from all CLI logs and terminal output.

### System Secure Store (Optional)
For extra security, you can store your keys in your OS keychain instead of a `.env` file.

[OS-specific instructions: Set-Secret (Windows) or security (macOS)]

---

## 🧪 Testing & Installation

### Installation
The easiest way to install the skill for all supported agents (Gemini, Claude, Copilot) is to use the provided scripts:

**On Windows (PowerShell):**
```powershell
.\install.ps1
```

**On Linux/macOS (Bash):**
```bash
chmod +x install.sh
./install.sh
```
