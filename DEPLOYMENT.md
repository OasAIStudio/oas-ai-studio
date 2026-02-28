# Vercel Deployment Setup

## Prerequisites

You need to get the following information from Vercel:

1. **VERCEL_TOKEN** - Your Vercel API token
2. **VERCEL_ORG_ID** - Your Vercel organization/team ID (optional)
3. **VERCEL_PROJECT_ID** - Your Vercel project ID (optional)

## Step 1: Get Vercel Token

1. Go to https://vercel.com/account/tokens
2. Click **"Create Token"**
3. Give it a name (e.g., "GitHub Actions")
4. Copy the token (you'll only see it once!)

## Step 2: Get Project Information (Optional)

If you want to link to an existing Vercel project:

```bash
# Install Vercel CLI
npm i -g vercel

# Login and link project
cd /path/to/your/project
vercel link

# Get project info
cat .vercel/project.json
```

This will show you:
- `projectId` - Your VERCEL_PROJECT_ID
- `orgId` - Your VERCEL_ORG_ID

## Step 3: Add Secrets to GitHub

1. Go to your GitHub repository: https://github.com/OasAIStudio/oas-ai-studio
2. Click **Settings** → **Secrets and variables** → **Actions**
3. Click **"New repository secret"**
4. Add the following secrets:

### Required:
- Name: `VERCEL_TOKEN`
- Value: [Your Vercel token from Step 1]

### Optional (for existing project):
- Name: `VERCEL_ORG_ID`
- Value: [Your org ID from .vercel/project.json]

- Name: `VERCEL_PROJECT_ID`
- Value: [Your project ID from .vercel/project.json]

## Step 4: Test the Deployment

Once secrets are added:

1. Push any commit to the `main` branch
2. Go to **Actions** tab in GitHub
3. Watch the deployment workflow run
4. Your site will be deployed to Vercel automatically!

## Workflow Behavior

- **Push to `main`**: Automatically deploys to production
- **Pull Request**: Creates a preview deployment
- **Manual trigger**: Can be triggered from Actions tab

## Troubleshooting

If deployment fails:

1. Check that `VERCEL_TOKEN` is set correctly in GitHub Secrets
2. Make sure the token has the right permissions
3. Check the Actions logs for detailed error messages
4. Verify your Vercel project settings

## Manual Deployment (Alternative)

If you prefer manual deployment:

```bash
# Install Vercel CLI
npm i -g vercel

# Deploy
vercel --prod
```
