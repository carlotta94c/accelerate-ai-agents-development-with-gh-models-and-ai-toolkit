# Summary

In this lab, you learned how to:

- Explore and compare models to select the best fit for your business scenario
- Augment models with prompts and data to get more accurate and grounded responses
- Prototype an agent by combining models and instructions with tools via MCP (Model Context Protocol)
- Extract the agent's code for further customization and deployment

## Next steps

As you move forward in your development journey with AI agents, and consider deploying them in production environments, there's a few important considerations to keep in mind:

- **Azure hosted models**: While this lab focused on using GitHub-hosted models for prototyping, for production scenarios, it's advisable to use Azure-hosted models. These models offer better performance, reliability, and compliance with enterprise standards. You can explore the available catalog in [Azure AI Foundry Models](https://ai.azure.com/catalog).
- **Evaluation**: Before deploying an agent, it's crucial to evaluate its performance thoroughly. This includes testing its responses for accuracy, relevance, and safety. Consider using a mix of automated tests and human evaluations. You can learn more about agent evaluation in the [official documentation](https://code.visualstudio.com/docs/intelligentapps/evaluation).
- **Monitoring**: Once deployed, continuously monitor the agent's performance in real-world scenarios. This helps in identifying any issues or areas for improvement. Set up logging and alerting mechanisms to track the agent's behavior and performance metrics. The observability features in Azure AI Foundry can be very helpful for this purpose. Discover more in the [official documentation](https://learn.microsoft.com/azure/ai-foundry/how-to/monitor-applications).
- **Continuous improvement**: AI agents can always be improved. Gather user feedback and analyze the agent's interactions to identify areas for enhancement. Regularly update the agent's model, prompts, and tools to keep it effective and relevant.

## Useful Resources

1. Install the AI Toolkit in VS code: [aka.ms/AIToolkit](https://aka.ms/AIToolkit)
2. Read the AI toolkit docs: [aka.ms/AIToolkit/docs](https://aka.ms/AIToolkit/docs)
3. Look at a real-world use case: [aka.ms/BRK441GHrepo](https://aka.ms/BRK441GHrepo)
4. Share your learnings with the community and get support: [aka.ms/foundrydevs](https://aka.ms/foundrydevs)