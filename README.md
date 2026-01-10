# ai-news-summary
This Github Repo stores the N8N-Workflow for my AI-News-Summary Workflow that delivers a tailored weekly digest of RSS-Feed-News.

This version excludes sensitive information such as emails and Credential_IDs. 

You can find more information about this project in the blog post on my [website](https://www.peer-schlieker.de/projects/ai-news-summary).

## Importing
If you import this workflow into your n8n instance, you may encounter issues with the ```executeCommand``` node that I use to update my website. If you don't need this node, you don't need to worry about it; otherwise, you need to add the following to your environment variables in your Docker container: ```NODES_EXCLUDE="[]"``` to the environment variables in your Docker container. However, if you add this, nodes that could damage your system if used inappropriately will be activated, so please think twice before doing so. Another option is to only enable this node by adding ```N8N_NODES_INCLUDE=n8n-nodes-base.executeCommand```

After importing it, you need to set up the Mail and the Agent Node with an API Key. OpenRouter provides some free models.