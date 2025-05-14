# Project Decomposition Template

This template provides a structured workflow for decomposing software projects using an AI assistant (like Cursor IDE's chat). It guides Project Managers (PMs) through a phased approach to break down complex projects into manageable components, features, and sub-features, outputting to a document ready for effort estimation.

## Prerequisites

*   Cursor IDE (or another AI-powered IDE/chat interface) installed.

## Setup

1.  **Clone or Download:** Clone this repository or download it as a ZIP and extract it.
2.  **Navigate:** Open this  (`decomply`, right?) directory or project in your terminal or IDE.
3.  **Input Materials:** Place all your project-specific input documents (e.g., client transcripts, requirements documents, design mockups) into the `input_materials/` folder.
4.  **Prepare Output File:** You can either create an empty `docs/project_decomposition.md` file now, or create it as you start pasting content from the AI. The structure of this file is exemplified in `docs/template_output_structure.md`.

## Workflow with AI Assistant (e.g., Cursor IDE Chat)

1.  **Initiate with AI:**
    *   Open your AI assistant's chat interface.
    *   Copy the *entire* content of `PROMPT.md` from this template.
    *   Paste the copied prompt into the AI chat.
    *   Immediately after pasting the prompt, add the following instruction to the AI:
        ```
        Let's begin the project decomposition process based on the prompt I just provided.
        My project input materials (transcripts, documents, etc.) are located in the 'input_materials/' folder in this project. Please refer to them as needed by using the '@' symbol to reference files (e.g., @input_materials/client_transcript.txt).
        Start with Phase 0: Project Information Gathering. Ask me what you need.
        ```

2.  **Interactive Decomposition (Phases 0 - 3):**
    *   The AI will now follow the instructions from `PROMPT.md`. It will:
        *   Ask for clarification on your input materials (Phase 0).
        *   Propose the number of decomposition levels (1-3) and await your approval (Phase 0.5).
        *   Generate Markdown tables for each agreed-upon decomposition level (Phase 1, and optionally Phase 2 and 3), adhering to the specified column structure which includes `Module Name`, `Feature`, `Sub-Feature`, `Description`, and empty `Estimate` columns.
    *   **For each phase where the AI generates a Markdown table:**
        *   Review the table carefully in the chat.
        *   Provide feedback or request modifications directly to the AI. Iterate until you are satisfied.
        *   Once approved, **copy the final approved Markdown table** for that phase from the chat.
        *   **Paste this table into your `docs/project_decomposition.md` file.** It's recommended to append each new table below the previous one, or integrate them if the AI generates a consolidated table per level. Use Markdown headings to clearly separate the levels if needed (e.g., `## Decomposition Level 1 Output`).

3.  **Finalizing the Document:**
    *   Once all agreed-upon decomposition levels are complete and their respective tables are copied into `docs/project_decomposition.md`, your structured project decomposition document is ready. The `Estimate (Min hours)` and `Estimate (Max hours)` columns will be empty, ready for the development team to fill in.

## Tips for Interacting with the AI

*   **Be Explicit:** Clearly state your approvals (e.g., "The Level 1 table is approved, proceed.") or your requests for changes.
*   **Reference Materials:** Remind the AI to use the `@` symbol to access files in your `input_materials/` folder if it seems to forget.
*   **Iterate:** Don't hesitate to ask the AI to refine its suggestions or tables until they meet your needs.
*   **Context:** If the conversation gets very long, the AI might lose some context. You can gently remind it of previous decisions or key aspects of the project.
