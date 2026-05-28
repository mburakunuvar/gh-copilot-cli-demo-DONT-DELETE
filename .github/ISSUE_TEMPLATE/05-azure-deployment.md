---
name: "Issue 5 — Azure Deployment"
about: "Verify and trigger deployment after home, primitives & APE are done"
title: "Azure Deployment"
labels: "agent-mode"
---

## Task
The application is deployed to Azure Container Apps and a CI/CD workflow is in place (`.github/workflows/azure-container-apps.yml`).

> ⚠️ **Important**: The workflow only triggers on `workflow_dispatch` — **not on push**. Do NOT push to remote expecting a deployment. Trigger it manually with:
> ```bash
> gh workflow run "Azure Container Apps CI/CD"
> ```

For this step:
1. Confirm the **Azure Container Apps Setup**, **Home Page**, **Primitives Page**, and **APE Page** issues are closed
2. Verify the latest changes are live at the deployed URL
3. If anything needs to be re-triggered, trigger the workflow manually using the command above

> ⚠️ **Prerequisite**: The **Home Page**, **Primitives**, and **APE** issues must be closed before deployment. The **Code Review and Performance** issue happens after this step.

## Assigned to
Agent Mode in IDE (VS Code) — prompt: *"The Home Page, Primitives, and APE issues are resolved. Verify the app is deployed and the live site reflects all the latest changes. Trigger a re-deployment if needed."*

## Pre-flight requirement
The presenter must have already completed the **Azure Container Apps Setup** issue before the demo:
- Azure Container App and Container Apps environment created
- Deployment secrets configured (`AZURE_CLIENT_ID`, `AZURE_TENANT_ID`, `AZURE_SUBSCRIPTION_ID`, `AZURE_CLIENT_SECRET`, `ACR_LOGIN_SERVER`, `ACR_USERNAME`, `ACR_PASSWORD`, `AZURE_RESOURCE_GROUP`, `AZURE_CONTAINERAPP_NAME`, `AZURE_CONTAINERAPPS_ENVIRONMENT`)

## Completion
Once deployment is verified and the live site is confirmed working, close this issue from the GitHub UI or with `gh issue close <this-issue-number>`.
