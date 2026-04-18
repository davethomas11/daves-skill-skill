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

### Why use a System Secure Store (Key Vault)?
A system secure store provides a significantly higher level of protection than a standard `.env` file:

- **Encryption at Rest:** Unlike a `.env` file, which is plain text, these stores encrypt your keys using industry-standard algorithms (like AES). Even if someone gains access to your files, they cannot read the keys.
- **Session-Based Access:** These stores are often tied to your **User Login Session**. This means the keys are only "unlocked" when you are actively logged in.
- **Protection from Network Attacks:** If an attacker gains unauthorized access to your file system through the network, they might be able to steal your `.env` file, but they **cannot** decrypt the secrets in a secure store without your system password or a specific master key.
- **Agent Context:** Because the AI agent runs with your user permissions, it can securely request the keys on your behalf while you are at the terminal, keeping them out of permanent cleartext files.

### Local and Cloud Key Stores
When dealing with sensitive information like API keys, it's crucial to understand the implications of storing them. Local key stores, such as environment variables or OS keychains, are suitable for development environments and single-user setups, providing a good balance of security and convenience. For production deployments or multi-user environments, consider more robust, centralized solutions like cloud key stores. Options include HashiCorp Vault, AWS SSM Parameter Store, or Azure Key Vault. These services offer enhanced security features, centralized management, and better scalability for protecting your secrets.

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
