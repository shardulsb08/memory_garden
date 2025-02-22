# Memory Garden

**Memory Garden** is a manual memory retention system designed to simulate continuity across chat sessions with AI models that do not retain memory between sessions. It organizes past discussions into a structured, tree-like category system, making it easy to maintain context and track progress over time.

## Features
- **Memory Templates**: Summarize and store key points from each chat session.
- **Category Tree**: Organize memories hierarchically for easy access and management.
- **Short and Long Forms**: Each memory entry includes a concise summary and a detailed version.
- **Maintenance Sessions**: Regular sessions to optimize the category tree and memory entries.
- **Prompts**: Predefined prompts to guide the start, end, and maintenance of chat sessions.

## Setup and Usage

### Prerequisites
- A Git client installed (e.g., Git Bash, GitHub Desktop).
- A text editor for modifying files (e.g., VS Code, Notepad++).
- Familiarity with Markdown for viewing and editing files.

### Steps to Run
1. **Clone the Repository**:  
   Download the project files to your local machine.
   In bash:
   git clone https://github.com/yourusername/memory_garden.git
   cd memory_garden

### Explore the Prompts:
    Navigate to the prompts/ directory and review the following files:
        001_Start_of_Session_Prompt.txt: Used at the beginning of each chat session to provide context.
        002_Exit_Prompt: Used at the end of each session to create a new memory entry and update the category tree.
        003_Maintenance_Window_Prompt: Used periodically to optimize the memory system.
    Start a Chat Session:
        Open your AI chat interface (e.g., ChatGPT, Grok).
        Copy the content of 001_Start_of_Session_Prompt.txt, replace placeholders with relevant memory templates (e.g., from short_memories.md), and paste it into the chat.
    End a Chat Session:
        Copy the content of 002_Exit_Prompt and paste it into the chat session.
        Follow the AI’s response, which will include a new memory entry and updates to the category tree.
        Save the memory entry in the memories/ directory (e.g., memories/projects/session_001.md) and update categories.md and relevant short_memories.md files as instructed.
    Perform Maintenance:
        Periodically, use 003_Maintenance_Window_Prompt to initiate a maintenance session.
        Provide the current categories.md and memory entries, then follow the AI’s instructions to optimize the system.
        Log changes in maintenance_history.md.

### File Structure

    categories.md: Defines the current category tree structure (e.g., projects > scripts > cvss_tools).
    maintenance_history.md: Tracks changes made during maintenance sessions.
    prompts/: Contains the prompt files:
        001_Start_of_Session_Prompt.txt
        002_Exit_Prompt
        003_Maintenance_Window_Prompt
    memories/: Stores memory entries, organized by category paths (e.g., memories/projects/scripts/session_001.md).
    short_memories.md: Found in each category directory, aggregating short summaries of memories from that directory and its subdirectories.

### Additional Notes

    Prompt Usage: Each prompt file contains placeholders (e.g., [CATEGORY_TREE], [MEMORY_SUMMARIES]) that you’ll replace with current data before using them in a chat session.
    Scalability: As your memory entries grow, maintenance sessions become crucial to keep the system efficient.

### Contributing

Contributions are welcome! To contribute:

1. Fork the repository.
2. Create a new branch for your changes (git checkout -b feature/your-feature-name).
3. Commit your changes (git commit -m "Add your message here").
4. Push to your branch (git push origin feature/your-feature-name).
5. Submit a pull request.

Note: By contributing to this project, you agree to license your contributions under the GNU General Public License v2. This ensures that all modifications remain open-source and freely distributable under the same terms.

For major changes, please open an issue first to discuss your ideas.
License

This project is licensed under the GNU General Public License v2. See the LICENSE file in the repository for details.

Important: Under the GPL v2, anyone who distributes this software must also distribute the source code under the same license. This ensures that all modifications remain open-source and freely available.
