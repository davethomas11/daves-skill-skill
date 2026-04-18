# Gemini CLI Instructions: [Project Name]

These instructions are foundational mandates for any Gemini CLI agent working within this workspace.

## 🛡️ Security & Privacy Mandates (Priority 1)

1.  **Strict Credential Protection**:
    *   **NEVER** log, print, or echo the contents of any `.env` file.
    *   **NEVER** include real API keys or personal identifiers in code, documentation, or commit messages. Always use placeholders.
    *   **NEVER** commit the `.env` file. Verify it is always listed in `.gitignore`.

2.  **Redaction Protocol**:
    *   Rely on Gemini CLI's built-in redaction. If a tool might bypass redaction, DO NOT execute it with sensitive variables.

## 🛠️ Operational Guidelines

1.  **Skill Integrity**:
    *   The `.skill` file is a build artifact. If you modify any files in the skill source folder, you **must** repackage the skill.

2.  **User Guidance**:
    *   Always provide precise UI steps for complex API setup hurdles.
