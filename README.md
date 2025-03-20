# DRep Template Repository
Repo with automations to generate markdown tables of DRep votes

## Setup Instructions

### 1. GitHub Actions Permissions
To allow the workflow to commit and push changes to your repository, you need to configure the proper permissions:

1. Go to your repository's Settings
2. Navigate to "Actions" under "Security"
3. In the "Workflow permissions" section, select "Read and write permissions"
4. Save the changes

### 2. Koios API Key Setup
The automation requires a Koios API key to fetch DRep voting data. Here's how to get one:

1. Visit [Koios Profile Page](https://koios.rest/Profile.html)
2. Connect your Cardano wallet
3. Choose the free tier
4. Create an API key

### 3. Add API Key to Repository Secrets
Once you have your Koios API key:

1. Go to your repository's Settings
2. Navigate to "Secrets and variables" → "Actions"
3. Click "New repository secret"
4. Name: `KOIOS_API_KEY`
5. Value: Your API key from Koios
6. Click "Add secret"

## Usage
After completing the setup:
1. Update the `config.json` file with your DRep ID and organization name
2. The GitHub Action will run automatically every Monday at midnight UTC
3. You can also trigger it manually from the Actions tab

The action will generate markdown files containing your voting history, organized by year in the `voting-history` directory.
