# Using the Project Management Framework Rule

This document explains the process for initiating and managing projects using the `project-management-framework` Cursor rule.

## Goal

The primary goal of this framework is to keep the AI agent focused and on-task throughout a project lifecycle, ensuring each step is successfully completed and verified before proceeding to the next.

## Workflow Initiation

1.  **Start a New Conversation:** Begin a fresh chat session in Cursor.
2.  **Attach the Rule Context:** Manually attach the `.cursor/rules/project-management-framework.mdc` file to the conversation context.
3.  **State Your Goal:** Clearly explain the project, feature, or implementation you want to build. Provide detailed requirements.
4.  **Initiate Planning:** Instruct the agent to begin planning using the framework. For example: "Let's plan a new project to implement [your detailed feature description] using the attached project management framework rule."

## Project Lifecycle & Structure

*   **Planning Phase:** The agent will create a detailed markdown file outlining the project. This file will break the project down into distinct phases, and each phase into specific, actionable tasks.
*   **Directory Structure:** The agent will create a `.cursor-projects` directory in the repository root if it doesn't exist. Inside `.cursor-projects`, it will maintain three subdirectories:
    *   `planned/`: Newly created project plan markdown files are stored here initially.
    *   `active/`: When work begins on a project, the agent moves the corresponding markdown file to this directory.
    *   `completed/`: Once all tasks in a project plan are finished and verified, the agent moves the markdown file here.
*   **Task Execution:** The agent will work through the tasks listed in the active project's markdown file sequentially.
*   **Task Completion & Verification:** As the agent completes each task, it will mark it off (e.g., using checkbox syntax `[x]`) within the markdown file. Crucially, the agent must verify the success of each task (e.g., through testing, building, linting) before marking it complete and moving on.
*   **Project Completion:** Once all tasks in all phases are marked as complete and verified, the agent will move the project's markdown file from `active/` to `completed/`.

This structured approach ensures a methodical progression through the project, maintaining focus and verifying success at each stage. 