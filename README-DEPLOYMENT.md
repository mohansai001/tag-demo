# Azure Deployment Setup

## Prerequisites

1. **Azure Web Apps (Already Created):**
   - Backend: `TagAIBackend`
   - Frontend: `TagAIFrontend`

2. **Add GitHub Secrets:**
   - Go to your GitHub repository → Settings → Secrets and variables → Actions
   - Add these individual secrets:
     - `AZURE_CLIENT_ID`: Your Azure client ID
     - `AZURE_CLIENT_SECRET`: Your Azure client secret
     - `AZURE_SUBSCRIPTION_ID`: Your Azure subscription ID
     - `AZURE_TENANT_ID`: Your Azure tenant ID

## Deployment Process

The workflow will:
1. Build and test backend
2. Build frontend with production API URL
3. Deploy backend to `tagaibackend.azurewebsites.net`
4. Deploy frontend to `tagaifrontend.azurewebsites.net`

## Environment Configuration

- Frontend will use `https://tagaibackend.azurewebsites.net` as API base URL in production
- Update backend CORS settings to allow frontend domain
- Configure any required environment variables in Azure App Settings

## Manual Deployment

Push to `main` branch or trigger workflow manually from GitHub Actions tab.