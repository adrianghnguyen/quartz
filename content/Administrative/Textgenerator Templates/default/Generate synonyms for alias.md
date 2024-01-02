---
aliases: Generate synonyms for alias
file-created: 2023-05-16
file-modified: 2023-07-18
tags: [ ]
bodyParams:
 max_tokens: 500
linter-yaml-title-alias: Generate synonyms for alias
PromptInfo:
 promptId: Generate related alias
 name: 🏷️ Generate related aliases
 description: Generate related aliases for content
bodyParams:
 max_tokens: 500
---
content: 
{{context}}
prompt:
Create different aliases for the overall theme of the passage, Provide it as comma separated values.
