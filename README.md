# CopilotGenieAgent

## Summary

This repository contains a Power Apps solution file that creates a Copilot Agent integrated with a Custom Flow. The solution enables seamless connectivity to a Databricks Genie space, allowing users to interact with data and analytics through a conversational AI interface.

## Solution Components

The solution file in the src directory is based off of the [Copilot-and-Genie
](https://github.com/v7herman4/Copilot-and-Genie) repository posted by [Valter Herman](https://www.linkedin.com/in/valter-e-herman/) and [Melissa Lacefield](https://www.linkedin.com/in/melissa-lacefield-phd-2471116/).  They have documented many of the steps needed to import and configure the solution.

The key components of the solution file are the following:

| Name | Description |
|------|-------------|
| Databricks Genie Agent | This is the Copilot Studio Agent that we will use in the chat with your data scenario |
| Ask Databricks Genie | This is the cloud flow that is embedded into the Databricks Genie Agent under Tools. It handles the communication with the Databricks Genie Space. |
| Azure Key Vault Connection | This is used within the Ask Databricks Genie cloud flow to communicate with Azure Key Vault to retrieve the Databricks PAT. |
| Summarize JSON String | This AI Model is used within the Ask Databricks Genie cloud flow. |
| Databricks Workspace URL | This is saved as an environmental value within Dataverse and is called in the Ask Databricks Genie cloud flow. |
| Genie Space ID | This is saved as an environmental value within Dataverse and is called in the Ask Databricks Genie cloud flow. |

NOTE:  Before you import the solution, you will need to create a Key Vault Connection in Power Apps and have it validated, otherwise the solution will fail during the import process.  Go to https://make.powerapps.com/ and click on Connections and click <B>+ New connection</b> to add the Key Vault Connection beforehand.
