---
PromptInfo:
 promptId: Generate related tags
 name: 🏷️ Generate related tags
 description: Generate related tags for content
bodyParams:
 max_tokens: 30
---
content: 
{{context}}
prompt:
suggest related tags for topics related for the content in markdown format.

Provide your answer as a list of in the following format: #topic
