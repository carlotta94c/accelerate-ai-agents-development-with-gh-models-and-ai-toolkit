# Migrate to Code

In this section, you will learn how to migrate the agent you've created in AI Toolkit to a code-based workflow.

The AI Toolkit provides generated code for agents created in Agent Builder. You can choose your preferred SDK as well as programming language. Once you have your code file, you can integrate your agent into your own app.

## Step 1: Generate the Code

In Agent Builder, scroll down towards the bottom of the left side of the screen and select **View Code**.

![View code button.](../img/view-code.png)

When prompted, select your preferred client SDK (e.g. *Microsoft Agent Framework*) and programming language (e.g. *Python*). Once the new file is created, save the file to your workspace.

## Step 2: View the Code

Before running the script, review the content of the file as there may be placeholders that must be modified before running. If you need assistance understanding the script logic, you could leverage GitHub Copilot Chat in **Ask** mode.

Save the generated code file to your workspace as 'src/python/ai-agent.py'. Be sure to have the file active so that GitHub Copilot Chat can use the file as context. Alternatively, you could reference the specific file itself in your prompt to GitHub Copilot Chat.

!!! note
    If you see a '+' icon besides the file name, that means ai-agent.py is suggested as context by GitHub Copilot Chat, but it's not yet added. Click on the '+' icon to add the file as context.

![Suggested file as context](../img/suggested_file_context.png)

For example try the following prompt:

```
Explain what's happening in this script.
```

If there's any changes that need to be made, you could switch to **Agent** mode and request the changes to be made. You'll be requested to approve any file changes prior to committing the file updates to the script.

## (Optional) Bonus

If you'd like to run the code, save the file and follow the comments at the top of the code file. The instructions will vary as it's dependent on the client SDK and language selected.

For example, if you selected the **Microsoft Agent Framework** SDK with **Python**, follow the instructions below:

1. Locate the section in the code file that configures the MCP server tool. It should look similar to this:

   ```python
    def create_mcp_tools() -> list[ToolProtocol]:
    return [
        MCPStdioTool(
            name="VSCode Tools".replace("-", "_"),
            description="MCP server for VSCode Tools",
            command="INSERT_COMMAND_HERE",
            args=[
                "INSERT_ARGUMENTS_HERE",
            ]
        ),
    ]
   ```
2. Replace the placeholders with the actual command and arguments, to configure the MCP server tool correctly. Your code snippet should now look like this:

   ```python
    def create_mcp_tools() -> list[ToolProtocol]:
    return [
        MCPStreamableHTTPTool(
            name="Learn_MCP_Server",
            description="MCP server for Microsoft Learn documentation - provides search and fetch capabilities for official Microsoft docs",
            url="https://learn.microsoft.com/api/mcp"
        ),
    ]
   ```
4. Open a terminal in Visual Studio Code by selecting **Terminal** -> **New Terminal** from the top menu.
5. Install the required dependencies by using:

```
pip install agent-framework --pre
```

6. Run the script using:

```
python ai-agent.py
```

## Key Takeaways

- Agent Builder automatically generates code for agents in multiple programming languages and SDKs, facilitating easy migration from prototype to production.
- Code files may contain placeholders that need modification before execution, requiring developers to understand and adapt the generated logic for their specific needs.
- Using GitHub Copilot Chat in Ask and Agent modes helps developers understand generated code and create additional components like UI elements for complete agent applications.

Click **Next** to proceed to the following section of the lab.