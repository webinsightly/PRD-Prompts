# 🚀 AI Dev Tasks for Cursor 🤖

Welcome to **AI Dev Tasks**! This repository provides a collection of `.mdc` (Markdown Command) files designed to supercharge your feature development workflow within the [Cursor](https://cursor.sh/) editor. By leveraging these commands with Cursor's AI Agent, you can systematically approach building features, from ideation to implementation, with built-in checkpoints for verification.

Stop wrestling with monolithic AI requests and start guiding your AI collaborator step-by-step!

## ✨ The Core Idea

Building complex features with AI can sometimes feel like a black box. This workflow aims to bring structure, clarity, and control to the process by:

1.  **Defining Scope:** Clearly outlining what needs to be built with a Product Requirement Document (PRD).
2.  **Detailed Planning:** Breaking down the PRD into a granular, actionable task list.
3.  **Iterative Implementation:** Guiding the AI to tackle one task at a time, allowing you to review and approve each change.

This structured approach helps ensure the AI stays on track, makes it easier to debug issues, and gives you confidence in the generated code.

## Workflow: From Idea to Implemented Feature 💡➡️💻

Here's the step-by-step process using the `.mdc` files in this repository:

### 1️⃣ Create a Product Requirement Document (PRD)

First, lay out the blueprint for your feature. A PRD clarifies what you're building, for whom, and why.

You can create a lightweight PRD directly within Cursor:

1.  Ensure you have the `create-prd.mdc` file from this repository accessible.
2.  In Cursor's Agent chat, initiate PRD creation:

    ```
    Use @create-prd.mdc
    Here's the feature I want to build: [Describe your feature in detail]
    Reference these files to help you: [Optional: @file1.py @file2.ts]
    ```
    *(Pro Tip: For complex PRDs, using MAX mode in Cursor is highly recommended if your budget allows for more comprehensive generation.)*

    ![Example of initiating PRD creation](https://pbs.twimg.com/media/Go6DDlyX0AAS7JE?format=jpg&name=large)

### 2️⃣ Generate Your Task List from the PRD

With your PRD drafted (e.g., `MyFeature-PRD.md`), the next step is to generate a detailed, step-by-step implementation plan for your AI Developer.

1.  Ensure you have `generate-tasks-from-prd.mdc` accessible.
2.  In Cursor's Agent chat, use the PRD to create tasks:

    ```
    Now take @MyFeature-PRD.md and create tasks using @generate-tasks-from-prd.mdc
    ```
    *(Note: Replace `@MyFeature-PRD.md` with the actual filename of the PRD you generated in step 1.)*

    ![Example of generating tasks from PRD](https://pbs.twimg.com/media/Go6FITbWkAA-RCT?format=jpg&name=medium)

### 3️⃣ Examine Your Task List

You'll now have a well-structured task list, often with tasks and sub-tasks, ready for the AI to start working on. This provides a clear roadmap for implementation.

![Example of a generated task list](https://pbs.twimg.com/media/Go6GNuOWsAEcSDm?format=jpg&name=medium)

### 4️⃣ Instruct the AI to Work Through Tasks (and Mark Completion)

To ensure methodical progress and allow for verification, we'll use `process-task-list.mdc`. This command instructs the AI to focus on one task at a time and wait for your go-ahead before moving to the next.

1.  Create or ensure you have the `process-task-list.mdc` file accessible.
2.  In Cursor's Agent chat, tell the AI to start with the first task (e.g., `1.1`):

    ```
    Please start on task 1.1 and use @process-task-list.mdc
    ```
    *(Important: You only need to reference `@process-task-list.mdc` for the *first* task. The instructions within it guide the AI for subsequent tasks.)*

    The AI will attempt the task and then prompt you to review.

    ![Example of starting on a task with process-task-list.mdc](https://pbs.twimg.com/media/Go6I41KWcAAAlHc?format=jpg&name=medium)

### 5️⃣ Review, Approve, and Progress ✅

As the AI completes each task, you review the changes.
*   If the changes are good, simply reply with "yes" (or a similar affirmative) to instruct the AI to mark the task complete and move to the next one.
*   If changes are needed, provide feedback to the AI to correct the current task before moving on.

You'll see a satisfying list of completed items grow, providing a clear visual of your feature coming to life!

![Example of a progressing task list with completed items](https://pbs.twimg.com/media/Go6KrXZWkAA_UuX?format=jpg&name=medium)

While it's not always perfect, this method has proven to be a very reliable way to build out larger features with AI assistance.


## 🗂️ Files in this Repository

*   **`create-prd.mdc`**: Guides the AI in generating a Product Requirement Document for your feature.
*   **`generate-tasks-from-prd.mdc`**: Takes a PRD markdown file as input and helps the AI break it down into a detailed, step-by-step implementation task list.
*   **`process-task-list.mdc`**: Instructs the AI on how to process the generated task list, tackling one task at a time and waiting for your approval before proceeding. (This file also contains logic for the AI to mark tasks as complete).

## 🌟 Benefits

*   **Structured Development:** Enforces a clear process from idea to code.
*   **Step-by-Step Verification:** Allows you to review and approve AI-generated code at each small step, ensuring quality and control.
*   **Manages Complexity:** Breaks down large features into smaller, digestible tasks for the AI, reducing the chance of it getting lost or generating overly complex, incorrect code.
*   **Improved Reliability:** Offers a more dependable approach to leveraging AI for significant development work compared to single, large prompts.
*   **Clear Progress Tracking:** Provides a visual representation of completed tasks, making it easy to see how much has been done and what's next.

## 🛠️ How to Use

1.  **Clone or Download:** Get these `.mdc` files into your project or a central location where Cursor can access them.
2.  **Follow the Workflow:** Systematically use the `.mdc` files in Cursor's Agent chat as described in the 5-step workflow above.
3.  **Adapt and Iterate:**
    *   Feel free to modify the prompts within the `.mdc` files to better suit your specific needs or coding style.
    *   If the AI struggles with a task, try rephrasing your initial feature description or breaking down tasks even further.

## 💡 Tips for Success

*   **Be Specific:** The more context and clear instructions you provide (both in your initial feature description and any clarifications), the better the AI's output will be.
*   **MAX Mode for PRDs:** As mentioned, using MAX mode in Cursor for PRD creation (`create-prd.mdc`) can yield more thorough and higher-quality results if your budget supports it.
*   **Correct File Tagging:** Always ensure you're accurately tagging the PRD filename (e.g., `@MyFeature-PRD.md`) when generating tasks.
*   **Patience and Iteration:** AI is a powerful tool, but it's not magic. Be prepared to guide, correct, and iterate. This workflow is designed to make that iteration process smoother.

## 🤝 Contributing

Got ideas to improve these `.mdc` files or have new ones that fit this workflow? Contributions are welcome!
Please feel free to:
*   Open an issue to discuss changes or suggest new features.
*   Submit a pull request with your enhancements.

---

Happy AI-assisted developing!

# PRD Prompts - Rule Categories and Documentation

This repository contains a collection of rules and guidelines for Product Requirements Documentation (PRD) and development practices. The rules are organized into several categories for better navigation and understanding.

## Categories

### 1. Development Standards
- **Java 21 Programming** (`rules/java21-programming-always.mdc`)
  - Standards and best practices for Java 21 development
  - Modern Java features and patterns

- **Functional Programming** (`rules/functional-coding-practices.mdc`)
  - Functional programming principles
  - Immutable data structures
  - Pure functions and side effects

- **Code Quality** (`rules/no-hardcoded-strings.mdc`)
  - String management
  - Internationalization
  - Configuration handling

### 2. Documentation and Communication
- **Documentation Standards** (`rules/documentation-and-comments-and-logs.mdc`)
  - Code documentation
  - Commenting guidelines
  - Logging practices

- **AI Communication** (`rules/global-ai-communication-behavior-always.mdc`)
  - AI interaction guidelines
  - Communication protocols
  - Response formatting

- **Emoji Usage** (`rules/emoji-communication-always.mdc`)
  - Emoji guidelines
  - Communication enhancement
  - Visual feedback

### 3. Process and Workflow
- **PRD Creation** (`rules/create-prd.mdc`)
  - Product requirements documentation
  - Feature specification
  - User story mapping

- **Task Management** (`rules/generate-tasks.mdc`, `rules/process-task-list.mdc`)
  - Task generation
  - Task processing
  - Workflow management

### 4. Performance and Architecture
- **Performance Review** (`rules/performance-scalability-review.mdc`)
  - Performance optimization
  - Scalability considerations
  - Resource management

- **Logic Visualization** (`rules/visualize-logic-and-flow.mdc`)
  - Flow diagrams
  - Logic mapping
  - System architecture

### 5. Git and Version Control
- **Jira ID Compliance** (`rules/git-rules/enforce-jira-id-git-in-branch-or-commit.mdc`)
  - Branch naming conventions
  - Commit message standards
  - Jira ticket traceability
  - Version control best practices

### 6. Meta Rules
- **Rule Index** (`rules/rule-index.mdc`)
  - Rule validation
  - Rule configuration
  - Rule maintenance

- **Coding Instructions** (`rules/coding-instructions.mdc`)
  - General coding guidelines
  - Development standards
  - Best practices

## Usage

Each rule file (`.mdc`) contains:
- Clear description of the rule
- Implementation guidelines
- Examples and best practices
- Validation requirements
- Integration points

## Contributing

When adding new rules:
1. Follow the rule structure template
2. Include all required metadata
3. Ensure proper categorization
4. Add validation methods
5. Update the rule index

## Maintenance

Rules are regularly reviewed and updated to ensure:
- Current best practices
- Tool compatibility
- Clear documentation
- Proper validation
- Effective integration

## License

This project is licensed under the terms of the included LICENSE file.
