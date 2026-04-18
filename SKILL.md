---
name: daves-skill-skill
description: A high-standard framework for building agentic skills that are secure, agent-agnostic, and user-friendly. Use when creating or refining skills for Gemini, Claude, or Copilot.
---

# Dave's Skill-Skill: The Agentic Framework

This skill guides the creation of high-quality, professional-grade Agentic Skills. It prioritizes security, cross-agent compatibility, and clear user communication.

## The Four Pillars

### 1. Security-First Mindset
Always assume the environment is potentially compromised.
- **Redaction**: Rely on built-in CLI redaction for `.env` files.
- **System Stores**: Support fallback to **macOS Keychain** (`security`) and **Windows PowerShell SecretStore** (`Get-Secret`).
- **PII Protection**: Never commit personal IDs or real keys to Git history.

### 2. Agent-Agnostic Design
Skills should work across multiple AI assistants (Gemini, Claude, Copilot).
- Use the standard `SKILL.md` format.
- Avoid agent-specific jargon in the core instructions.
- Provide clear triggers in the YAML frontmatter.

### 3. Unified Installation
Every skill project must include root-level install scripts for easy setup.
- **Bash (`install.sh`)**: For Linux/macOS.
- **PowerShell (`install.ps1`)**: For Windows.
- **Interactive**: Scripts should ask the user for the intended **Agent** (Gemini, Claude, Copilot) and **Scope** (Workspace or User).

### 4. Comprehensive & Accessible Documentation
Documentation should be professional but approachable.
- **README.md**: Include a layman's explanation of what a "Skill" is.
- **GEMINI.md**: Set foundational security mandates for the AI agent itself.
- **Troubleshooting**: Document precise UI steps (e.g., "Hamburger Menu -> Confirmations") for API setup hurdles.

## Workflows

### 1. Initialize a New Skill
1. Use `node <path-to-skill-creator>/scripts/init_skill.cjs <name>`.
2. Create a root `README.md` and `GEMINI.md` using the templates in `assets/`.
3. Implement the `install.sh` and `install.ps1` scripts using the provided patterns.

### 2. Implement Secure Scripting
When writing scripts (Python, Node, etc.) that require API keys:
- Check environment variables first (`os.environ`).
- Fallback to calling system tools for SecretStore/Keychain if keys are missing.

## Assets
Reference these templates when building:
- `assets/README_TEMPLATE.md`
- `assets/GEMINI_TEMPLATE.md`
- `assets/INSTALL_BASH_TEMPLATE.sh`
- `assets/INSTALL_PS_TEMPLATE.ps1`
