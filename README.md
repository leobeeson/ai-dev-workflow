# AI-Assisted Software Development Workflow

This repository contains a set of specialized prompts to help solo developers and AI engineers create professional-grade software with proper planning and documentation. By leveraging AI development tools like Claude Code, Aider, Codex CLI, VSCode Copilot, Cursor, Windsurf, or similar tools, you can efficiently generate the essential artifacts typically produced by larger teams, and then use these artifacts as structured context for your AI tools to generate high-quality, robust, and business-relevant code aligned with clear requirements and architectural decisions.

## Problem Statement: The Risks of "Vibe Coding"

Many engineers are using AI development tools in what can be described as "vibe coding", providing minimal context and essentially taking their hands off the steering wheel, closing their eyes, and hoping the LLM can build a robust, safe, and business-relevant application on its own.

This approach introduces several critical risks:

- **Unvetted Assumptions**: The AI may make significant architectural or business decisions without your awareness.
- **Misaligned Business Goals**: Generated code may not fulfil actual business requirements or user needs.
- **Technical Debt**: Implementations may be expedient but difficult to maintain or extend.
- **Hidden Security Vulnerabilities**: Critical security considerations may be overlooked.
- **Integration Challenges**: Components may not work together cohesively in the larger system.
- **Suboptimal Performance**: Non-optimized implementations for your specific context.
- **Unclear Knowledge Transfer**: Difficulty explaining or justifying implementation decisions to stakeholders.

It's important to note that the issue isn't the quality of code LLMs can produce, which is often impressive and continues to improve rapidly. The fundamental problem lies in the assumptions an LLM might make on your behalf, which you won't be aware of unless you thoroughly read and understand what was implemented.

This workflow provides a structured approach to harness the power of AI development tools while maintaining appropriate engineering oversight and direction. Think of it as providing your AI not just with permission to drive, but with a detailed map and guardrails, ensuring you reach your destination safely and on time.

## Why Use This Workflow?

As a solo developer or small team, it's tempting to jump straight into coding. However, proper planning and documentation:

- Significantly reduces development time by preventing rework and uncertainty.
- Creates a clear roadmap for implementation.
- Forces clarity on requirements and constraints.
- Minimizes the probability of going down unfruitful rabbit holes.
- Increases overall application quality and customer satisfaction.
- Improves communication with clients, stakeholders, and collaborators.
- Enables better expectation management and timely feedback.
- Provides professional deliverables that can be shared with stakeholders.
- Reduces anxiety around implementation details.
- Improves project success rates.

This workflow helps bridge the gap between "just coding" and enterprise-level software development practices.

## Workflow Overview

This workflow is designed to be completed in 3-5 days before actual coding begins:

1. **Project Initialization (0.5-1 day)**: Define vision, stakeholders, and business case.
2. **Requirements Definition (1-1.5 days)**: Create PRD, user personas, and acceptance criteria.
3. **System Architecture (1-1.5 days)**: Design technical architecture and data flows.
4. **Implementation Planning (0.5-1 day)**: Develop WBS, user stories, and test strategy.
5. **Development Setup (0.5 day)**: Configure environment, repository, and CI/CD.
6. **Implementation Phase**: Use the Implementation Planning document as a task management system to guide and prompt your AI development tools in generating code for each specific task.

In the Implementation Phase, you'll leverage the artifacts created in previous phases to provide structured context for your AI development tools, allowing them to generate high-quality code aligned with your requirements and architecture.

## Prompt Files

- `01_project_initialisation_prompt.md` - For creating a project charter and business case.
- `02_requirements_definition_prompt.md` - For creating a PRD and user personas.
- `03_system_architecture_prompt.md` - For designing technical architecture.
- `04_implementation_planning_prompt.md` - For creating WBS and user stories.
- `05_development_setup_prompt.md` - For configuring development environment.

## Example Workflow

1. Start with the Project Initialization prompt.
2. Engage in dialogue until you have a clear project charter.
3. Use the project charter as input when starting Requirements Definition.
4. Continue this pattern through all five planning phases.
5. Use your Implementation Planning document to create a task list.
6. For each task:.
   - Create a new AI development tool session.
   - Provide the specific task description and relevant context.
   - Review the generated code for correctness and alignment with requirements.
   - Integrate the code into your project.
   - Test against acceptance criteria.
7. Conduct regular integration testing as you complete groups of related tasks.
8. Hold milestone reviews to ensure the project remains on track.

This structured approach allows you to harness the efficiency of AI code generation while maintaining engineering oversight and ensuring the final product meets business requirements.

## Adapting the Workflow

Feel free to:

- Adjust the order of phases for your specific needs.
- Combine phases for smaller projects.
- Add specialized prompts for your domain.
- Iterate and refine artifacts as you learn more.

## How to Use These Prompts

### Setup

1. Choose an AI development tool (Claude Code, Aider, VSCode GitHub Copilot, Codex CLI, Cursor, Windsurf, etc.).
2. Create a new project folder to store generated artifacts.
3. Set aside dedicated time for each phase (this investment will save significant time during development).

### For Each Phase

1. Start a new terminal or chat session with your AI development tool.
2. Copy the entire prompt for the current phase.
3. Begin the iterative dialogue with the AI consultant.
4. Answer questions thoroughly and thoughtfully.
5. Ask clarifying questions if you're unsure what the AI is asking.
6. Continue until all aspects of that phase are explored.
7. Request the final document when ready.
8. Save the generated artifact in your project folder.
9. Review and refine the document before proceeding to the next phase.

### For the Implementation Phase

1. Use your Implementation Planning document as a task management system.
2. Create separate sessions/terminals for each task or related group of tasks.
   - This allows you to focus on one task at a time and maintain clarity in your context.
   - For example, if you have a task to implement a user authentication feature, create a new session specifically for that task.
   - If you have multiple related tasks (e.g., user authentication and user profile management), consider grouping them into a single session for efficiency.
3. Provide only the relevant context for each specific task:
   - The task description from your WBS.
   - Relevant portions of your architecture document.
   - Specific requirements related to the task.
4. Review each code generation thoroughly before accepting it.
5. Ensure you understand what was implemented and why.
6. Test each implementation against your acceptance criteria.
7. Commit the code to your version control system regularly.

### Tips for Effective Use

#### Documentation Phases

- **Be honest about unknowns**: It's okay to tell the AI you're not sure about something.
- **Use the outputs as inputs**: Share previous artifacts when starting a new phase.
- **Don't skip phases**: Each builds on the previous one.
- **Revise when needed**: Return to earlier phases if requirements change.
- **Consider domain expertise**: Supplement with research for specialized domains.
- **Save conversations**: Keep the full dialogues for future reference.

#### Implementation Phase

- **Task isolation**: Create individual sessions for each implementation task (when using Claude Code, Aider, or Codex CLI) or .chats (when using GitHub Copilot, Cursor, or Windsurf)
- **Maintain oversight**: Always review and understand the generated code.
- **Regular integration**: Frequently integrate completed tasks to identify integration issues early.
- **Milestone reviews**: Conduct thorough reviews at key development milestones.
- **Keep the engineer-in-the-loop**: Remember that you are still the architect and responsible engineer.
- **Set Auto-Commit to False**: It is recommended to set the auto-commit option to false in your AI development tool, so you can review and approve each change before it is committed to your version control system.

#### MCP Use

During the Documentation Phases, it is important to have access to domain-specific knowledge, research, and insights. The Model Context Protocol (MCP) can be used to enhance the capabilities of your AI development tools by providing them with access to external knowledge sources and tools.

- **Web Research**: Provide MCP servers to your AI development tools to enable them to search the web for relevant information and documentation. Some recommended ones are:
  - [Fetch MCP Serve](https://github.com/modelcontextprotocol/servers/tree/main/src/fetch): A Model Context Protocol server that provides web content fetching capabilities. This server enables LLMs to retrieve and process content from web pages, converting HTML to markdown for easier consumption.
  - [Perplexity Ask MCP Server](https://github.com/ppl-ai/modelcontextprotocol): An MCP server implementation that integrates the Sonar API to provide Claude with unparalleled real-time, web-wide research. (Requires API key)
  - [Firecrawl MCP Server](https://github.com/mendableai/firecrawl-mcp-server): A Model Context Protocol (MCP) server implementation that integrates with Firecrawl for web scraping capabilities. (Requires API key)

For a rapidly expanding list of available MCP tools, check out [MCP's official server repository](https://github.com/modelcontextprotocol/servers).

## Other Resources

The best course I've taken for AI Development Tool and AI-Assisted Development Workflows (I have no association nor financial interest in it):

- [Principled AI Coding](https://agenticengineer.com/principled-ai-coding)

This course is by IndyDevDan. Highly recommend his channel for AI development tools and workflows:

- [IndyDevDan](https://www.youtube.com/@indydevdan)

My favourite channel and community for AI Engineers and Data Developers:

- [Dave Ebbelaar](https://www.youtube.com/@daveebbelaar)
- [Datalumina](https://www.datalumina.com/data-freelancer)

If you use Cursor, there's an interesting tool called [claude-task-master](https://github.com/eyaltoledano/claude-task-master) for task management for AI assisted development:

- [How I reduced 90% errors for my Cursor (+ any other AI IDE)](https://www.youtube.com/watch?v=1L509JK8p1I)
- [How I Made Cursor 99% More Effective (Task Master is The Move in 2025)](https://www.youtube.com/watch?v=R5kF70d_jCY)

Other AI-Powered Developer Tools:

- [Awesome AI-Powered Developer Tools](https://github.com/jamesmurdza/awesome-ai-devtools)

## Contributing

If you enhance these prompts or develop additional ones for specialized domains, please consider contributing them back to this repository.

## License

This project is licensed under the MIT License - see the LICENSE file for details.
