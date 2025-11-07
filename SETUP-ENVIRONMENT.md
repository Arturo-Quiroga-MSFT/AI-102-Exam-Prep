# AI-102 Lab Environment Setup Guide

## Quick Start Checklist

### ✅ Already Installed
- Git ✅
- Visual Studio Code ✅
- macOS with zsh shell ✅

### 🔧 Required Installations

#### 1. Python 3.8 or Higher
```bash
# Check if Python 3 is installed
python3 --version

# If not installed, use Homebrew
brew install python3

# Install pip packages globally or use venv
pip3 install --upgrade pip
```

#### 2. .NET SDK 6.0 or Higher (for C# labs)
```bash
# Check if .NET is installed
dotnet --version

# If not installed, download from:
# https://dotnet.microsoft.com/download
# Or use Homebrew:
brew install --cask dotnet-sdk
```

#### 3. Azure CLI
```bash
# Check if Azure CLI is installed
az --version

# If not installed, use Homebrew:
brew update && brew install azure-cli

# Login to Azure
az login

# Set default subscription (optional)
az account set --subscription "YOUR_SUBSCRIPTION_ID"
```

#### 4. Node.js and npm (for some labs)
```bash
# Check if Node.js is installed
node --version
npm --version

# If not installed, use Homebrew:
brew install node
```

### 🎯 Recommended VS Code Extensions

Install these extensions for the best lab experience:

```bash
# Open VS Code and install extensions via command palette (Cmd+Shift+P)
# Or install via terminal:

# Python extension
code --install-extension ms-python.python

# C# extension  
code --install-extension ms-dotnettools.csharp

# Azure Account
code --install-extension ms-vscode.azure-account

# Azure Resources
code --install-extension ms-azuretools.vscode-azureresourcegroups

# Azure Functions (for serverless labs)
code --install-extension ms-azuretools.vscode-azurefunctions

# REST Client (for testing APIs)
code --install-extension humao.rest-client

# Jupyter (for Python notebooks)
code --install-extension ms-toolsai.jupyter
```

## 🔐 Azure Account Setup

### Create Azure Subscription
If you don't have an Azure subscription:
1. Go to [https://azure.microsoft.com/free/](https://azure.microsoft.com/free/)
2. Sign up for free trial ($200 credit for 30 days)
3. Or use your organization's subscription

### Verify Azure Access
```bash
# Login to Azure
az login

# List your subscriptions
az account list --output table

# Set active subscription
az account set --subscription "YOUR_SUBSCRIPTION_NAME_OR_ID"

# Verify current subscription
az account show --output table
```

### Create Resource Group for Labs
```bash
# Create a resource group for all AI-102 labs
az group create \
  --name ai-102-labs-rg \
  --location eastus

# List resource groups
az group list --output table
```

## 📦 Python Environment Setup

### Option 1: Virtual Environment (Recommended)
```bash
# Create a virtual environment for AI-102 labs
cd "/Users/arturoquiroga/AI-102 EXAM"
python3 -m venv ai102-venv

# Activate virtual environment
source ai102-venv/bin/activate

# Install common packages
pip install --upgrade pip
pip install azure-ai-textanalytics
pip install azure-ai-vision
pip install azure-cognitiveservices-speech
pip install azure-ai-formrecognizer
pip install azure-core
pip install python-dotenv
pip install openai
pip install azure-search-documents
```

### Option 2: Conda Environment
```bash
# If you use Conda
conda create -n ai102 python=3.11
conda activate ai102

# Install common packages
pip install azure-ai-textanalytics azure-ai-vision azure-cognitiveservices-speech
```

### Deactivate Virtual Environment
```bash
# When done working
deactivate
```

## 🧪 Test Your Setup

### Test Python
```bash
python3 --version
pip3 --version

# Test Azure SDK
python3 -c "import azure.ai.textanalytics; print('Azure SDK: OK')"
```

### Test .NET
```bash
dotnet --version

# Test .NET project creation
cd ~
mkdir test-dotnet && cd test-dotnet
dotnet new console
dotnet run
cd .. && rm -rf test-dotnet
```

### Test Azure CLI
```bash
az --version
az account show

# Test Azure AI Services CLI
az cognitiveservices account list --output table
```

## 📁 Workspace Organization

Your current structure:
```
/Users/arturoquiroga/AI-102 EXAM/
├── AI-102-STUDY-GUIDE.md
├── SETUP-ENVIRONMENT.md
├── mslearn-ai-services/
├── mslearn-ai-vision/
├── mslearn-ai-language/
├── mslearn-ai-document-intelligence-main/
├── mslearn-knowledge-mining/
└── mslearn-openai/
```

## 🔑 Managing Azure Credentials

### Using Environment Variables (.env files)
Most labs use `.env` files for configuration:

```bash
# Example .env file structure
AZURE_AI_SERVICES_KEY=your_key_here
AZURE_AI_SERVICES_ENDPOINT=https://your-resource.cognitiveservices.azure.com/
AZURE_SUBSCRIPTION_ID=your_subscription_id
```

### Using appsettings.json (C# labs)
```json
{
  "AIServicesEndpoint": "YOUR_ENDPOINT",
  "AIServicesKey": "YOUR_KEY"
}
```

### ⚠️ Security Best Practice
```bash
# NEVER commit credentials to Git
# Add to .gitignore:
echo ".env" >> .gitignore
echo "appsettings.json" >> .gitignore
echo "*.key" >> .gitignore
```

## 🚀 Starting a Lab - Typical Workflow

### Python Lab Example:
```bash
# 1. Navigate to lab folder
cd "/Users/arturoquiroga/AI-102 EXAM/mslearn-ai-vision/Labfiles/01-analyze-images/Python"

# 2. Activate virtual environment (if using)
source ~/AI-102\ EXAM/ai102-venv/bin/activate

# 3. Install dependencies
pip install -r requirements.txt  # if available

# 4. Configure credentials
# Edit .env file with your Azure resources

# 5. Run the application
python analyze-image.py
```

### C# Lab Example:
```bash
# 1. Navigate to lab folder  
cd "/Users/arturoquiroga/AI-102 EXAM/mslearn-ai-vision/Labfiles/01-analyze-images/C-Sharp"

# 2. Restore packages
dotnet restore

# 3. Configure credentials
# Edit appsettings.json with your Azure resources

# 4. Run the application
dotnet run
```

## 🐛 Common Issues & Solutions

### Issue: Python module not found
```bash
# Solution: Install in virtual environment
source ai102-venv/bin/activate
pip install <module-name>
```

### Issue: Azure authentication fails
```bash
# Solution: Re-login to Azure
az logout
az login
az account set --subscription "YOUR_SUBSCRIPTION"
```

### Issue: .NET SDK not found
```bash
# Solution: Verify installation and path
which dotnet
dotnet --info

# Add to PATH if needed (add to ~/.zshrc)
export PATH="$PATH:/usr/local/share/dotnet"
```

### Issue: VS Code can't find Python interpreter
```bash
# Solution: In VS Code
# 1. Cmd+Shift+P
# 2. "Python: Select Interpreter"
# 3. Choose your ai102-venv environment
```

## 💰 Cost Management Tips

### Use Free Tiers When Available:
- **Azure AI Services:** F0 tier (free tier available for most services)
- **Azure OpenAI:** Pay-as-you-go (no free tier, use sparingly)
- **Azure Search:** Free tier available
- **Storage Accounts:** Free tier with limited transactions

### Monitor Costs:
```bash
# Check your Azure costs
az consumption usage list --output table

# Set up cost alerts in Azure Portal
# Portal > Cost Management + Billing > Cost alerts
```

### Clean Up Resources After Labs:
```bash
# Delete resource group and all resources
az group delete --name ai-102-labs-rg --yes --no-wait

# List all resource groups
az group list --output table
```

## 📚 Additional Tools (Optional)

### Postman or Thunder Client
For testing REST APIs:
```bash
# Install REST Client for VS Code
code --install-extension humao.rest-client
```

### Azure Storage Explorer
For managing storage accounts:
- Download from [https://azure.microsoft.com/features/storage-explorer/](https://azure.microsoft.com/features/storage-explorer/)

### Bot Framework Emulator (for bot labs)
- Download from [https://github.com/Microsoft/BotFramework-Emulator](https://github.com/Microsoft/BotFramework-Emulator)

## ✅ Environment Verification Script

Save this as `verify-setup.sh`:
```bash
#!/bin/bash

echo "🔍 Verifying AI-102 Lab Environment..."
echo ""

# Check Python
if command -v python3 &> /dev/null; then
    echo "✅ Python: $(python3 --version)"
else
    echo "❌ Python: NOT FOUND"
fi

# Check .NET
if command -v dotnet &> /dev/null; then
    echo "✅ .NET: $(dotnet --version)"
else
    echo "❌ .NET: NOT FOUND"
fi

# Check Azure CLI
if command -v az &> /dev/null; then
    echo "✅ Azure CLI: $(az --version | head -n 1)"
else
    echo "❌ Azure CLI: NOT FOUND"
fi

# Check Node.js
if command -v node &> /dev/null; then
    echo "✅ Node.js: $(node --version)"
else
    echo "⚠️  Node.js: NOT FOUND (optional)"
fi

# Check Git
if command -v git &> /dev/null; then
    echo "✅ Git: $(git --version)"
else
    echo "❌ Git: NOT FOUND"
fi

# Check VS Code
if command -v code &> /dev/null; then
    echo "✅ VS Code: Installed"
else
    echo "❌ VS Code: NOT FOUND"
fi

echo ""
echo "🎓 Environment verification complete!"
```

Run with:
```bash
chmod +x verify-setup.sh
./verify-setup.sh
```

---

**You're now ready to start your AI-102 labs! 🚀**

*Last Updated: November 2025*
