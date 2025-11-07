# AI-102 Quick Start Lab Examples

## 🎯 Your First Lab - Getting Started

### Lab 1: Analyze Images with Azure AI Vision

Let's start with a hands-on example to verify everything works:

#### Step 1: Create Azure AI Services Resource
```bash
# Login to Azure
az login

# Create resource group
az group create \
  --name ai-102-quickstart-rg \
  --location eastus

# Create AI Services resource (multi-service)
az cognitiveservices account create \
  --name ai-102-quickstart-ai \
  --resource-group ai-102-quickstart-rg \
  --kind CognitiveServices \
  --sku S0 \
  --location eastus \
  --yes

# Get endpoint and key
az cognitiveservices account show \
  --name ai-102-quickstart-ai \
  --resource-group ai-102-quickstart-rg \
  --query properties.endpoint \
  --output tsv

az cognitiveservices account keys list \
  --name ai-102-quickstart-ai \
  --resource-group ai-102-quickstart-rg \
  --query key1 \
  --output tsv
```

#### Step 2: Set Up Your First Python Lab
```bash
# Navigate to the vision lab
cd "/Users/arturoquiroga/AI-102 EXAM/mslearn-ai-vision/Labfiles/01-analyze-images/Python"

# Create virtual environment (if not already created)
python3 -m venv venv
source venv/bin/activate

# Install required packages
pip install azure-ai-vision-imageanalysis python-dotenv pillow

# Create .env file
cat > .env << 'EOF'
AI_SERVICE_ENDPOINT=your_endpoint_here
AI_SERVICE_KEY=your_key_here
EOF

echo "⚠️  IMPORTANT: Edit .env file with your actual Azure credentials!"
```

#### Step 3: Run Your First Lab
```bash
# After configuring .env with your credentials
python image-analysis.py images/street.jpg
```

---

## 📋 Lab Recommendations by Topic

### Week 1: Foundation Labs (Start Here)

#### 1. Azure AI Services Basics
**Repository:** `mslearn-ai-services`

```bash
cd "/Users/arturoquiroga/AI-102 EXAM/mslearn-ai-services"

# Lab 1: Get Started with Azure AI Services
cd Labfiles/01-use-azure-ai-services/Python
# Follow Instructions/Labs/01-use-azure-ai-services.md

# Lab 2: Security
cd ../02-ai-services-security/Python
# Follow Instructions/Labs/02-ai-services-security.md
```

**What You'll Learn:**
- Create and manage AI Services resources
- Secure endpoints with keys and managed identities
- Monitor usage and costs
- Deploy in containers

---

### Week 2: Computer Vision

#### 2. Image Analysis
**Repository:** `mslearn-ai-vision`

```bash
cd "/Users/arturoquiroga/AI-102 EXAM/mslearn-ai-vision"

# Lab 1: Analyze Images
cd Labfiles/01-analyze-images/Python
# Key skills: Image analysis, tagging, caption generation

# Lab 2: Read Text (OCR)
cd ../05-ocr/Python
# Key skills: Extract text from images and PDFs

# Lab 3: Face Detection
cd ../04-face/Python
# Key skills: Detect and analyze faces
```

**Sample Code - Image Analysis:**
```python
from azure.ai.vision.imageanalysis import ImageAnalysisClient
from azure.ai.vision.imageanalysis.models import VisualFeatures
from azure.core.credentials import AzureKeyCredential
import os
from dotenv import load_dotenv

# Load environment variables
load_dotenv()
endpoint = os.getenv('AI_SERVICE_ENDPOINT')
key = os.getenv('AI_SERVICE_KEY')

# Create client
client = ImageAnalysisClient(
    endpoint=endpoint,
    credential=AzureKeyCredential(key)
)

# Analyze image
image_path = "images/street.jpg"
with open(image_path, "rb") as f:
    image_data = f.read()

result = client.analyze(
    image_data=image_data,
    visual_features=[
        VisualFeatures.CAPTION,
        VisualFeatures.TAGS,
        VisualFeatures.OBJECTS,
        VisualFeatures.PEOPLE
    ]
)

print(f"Caption: {result.caption.text}")
print(f"Confidence: {result.caption.confidence:.2f}")
```

---

### Week 3: Language Understanding

#### 3. Text Analytics & Language
**Repository:** `mslearn-ai-language`

```bash
cd "/Users/arturoquiroga/AI-102 EXAM/mslearn-ai-language"

# Lab: Analyze Text
cd Labfiles/01-analyze-text/Python

# Lab: Translate Text
cd ../06-translate-text/Python

# Lab: Conversational Language Understanding
cd ../07-speech/Python
```

**Sample Code - Text Analytics:**
```python
from azure.ai.textanalytics import TextAnalyticsClient
from azure.core.credentials import AzureKeyCredential
import os
from dotenv import load_dotenv

load_dotenv()

# Create client
client = TextAnalyticsClient(
    endpoint=os.getenv('LANGUAGE_ENDPOINT'),
    credential=AzureKeyCredential(os.getenv('LANGUAGE_KEY'))
)

# Analyze sentiment
documents = [
    "I love using Azure AI services! They are amazing.",
    "This is terrible and I hate it.",
    "It's okay, nothing special."
]

response = client.analyze_sentiment(documents)
for idx, doc in enumerate(response):
    print(f"Document {idx + 1}: {doc.sentiment}")
    print(f"  Positive: {doc.confidence_scores.positive:.2f}")
    print(f"  Neutral: {doc.confidence_scores.neutral:.2f}")
    print(f"  Negative: {doc.confidence_scores.negative:.2f}")
```

---

### Week 4: Document Intelligence

#### 4. Form & Document Processing
**Repository:** `mslearn-ai-document-intelligence-main`

```bash
cd "/Users/arturoquiroga/AI-102 EXAM/mslearn-ai-document-intelligence-main"

# Lab 1: Prebuilt Models
cd Labfiles/01-prebuild-models/Python

# Lab 2: Custom Models
cd ../02-custom-document-intelligence/Python
```

**What You'll Learn:**
- Extract data from invoices, receipts, business cards
- Train custom extraction models
- Compose multiple models

---

### Week 5: Azure OpenAI

#### 5. Generative AI
**Repository:** `mslearn-openai`

```bash
cd "/Users/arturoquiroga/AI-102 EXAM/mslearn-openai"

# Lab: Get Started with Azure OpenAI
cd Labfiles/01-get-started/Python

# Lab: Use Azure OpenAI SDK
cd ../02-use-openai-sdk/Python

# Lab: Prompt Engineering
cd ../03-prompt-engineering/Python
```

**Sample Code - Azure OpenAI Chat:**
```python
from openai import AzureOpenAI
import os
from dotenv import load_dotenv

load_dotenv()

client = AzureOpenAI(
    api_key=os.getenv("AZURE_OPENAI_KEY"),
    api_version="2024-02-15-preview",
    azure_endpoint=os.getenv("AZURE_OPENAI_ENDPOINT")
)

# Create chat completion
response = client.chat.completions.create(
    model="gpt-35-turbo",  # deployment name
    messages=[
        {"role": "system", "content": "You are a helpful AI assistant."},
        {"role": "user", "content": "Explain Azure AI Services in 3 sentences."}
    ],
    temperature=0.7,
    max_tokens=200
)

print(response.choices[0].message.content)
```

---

### Week 6: Knowledge Mining & Search

#### 6. Azure AI Search
**Repository:** `mslearn-knowledge-mining`

```bash
cd "/Users/arturoquiroga/AI-102 EXAM/mslearn-knowledge-mining"

# Lab: Create Search Solution
cd Labfiles/01-azure-search/Python

# Lab: Custom Skills
cd ../02-search-skills/Python
```

---

## 🛠️ Common Lab Tasks

### Task 1: Configure Environment Variables

Every lab needs configuration. Here's the pattern:

**Python (.env file):**
```bash
AI_SERVICE_ENDPOINT=https://your-resource.cognitiveservices.azure.com/
AI_SERVICE_KEY=your_key_here
LANGUAGE_ENDPOINT=https://your-language.cognitiveservices.azure.com/
LANGUAGE_KEY=your_language_key
```

**C# (appsettings.json):**
```json
{
  "AIServicesEndpoint": "https://your-resource.cognitiveservices.azure.com/",
  "AIServicesKey": "your_key_here"
}
```

### Task 2: Install Python Dependencies

Most Python labs need these packages:
```bash
# Activate virtual environment
source venv/bin/activate

# Common packages
pip install azure-ai-textanalytics
pip install azure-ai-vision-imageanalysis
pip install azure-cognitiveservices-speech
pip install azure-ai-formrecognizer
pip install azure-search-documents
pip install openai
pip install python-dotenv
```

### Task 3: Run C# Labs

```bash
# Navigate to C# folder
cd C-Sharp

# Restore packages
dotnet restore

# Build
dotnet build

# Run
dotnet run
```

---

## 📊 Lab Completion Tracker

Create a simple tracker file:

```bash
# Create tracking file
cd "/Users/arturoquiroga/AI-102 EXAM"
cat > lab-progress.md << 'EOF'
# AI-102 Lab Progress Tracker

## AI Services (mslearn-ai-services)
- [ ] Lab 01: Get Started (Date: ____)
- [ ] Lab 02: Security (Date: ____)
- [ ] Lab 03: Monitoring (Date: ____)
- [ ] Lab 04: Containers (Date: ____)
- [ ] Lab 05: Content Safety (Date: ____)

## Vision (mslearn-ai-vision)
- [ ] Lab 01: Analyze Images (Date: ____)
- [ ] Lab 02: Image Classification (Date: ____)
- [ ] Lab 03: Object Detection (Date: ____)
- [ ] Lab 04: Face Detection (Date: ____)
- [ ] Lab 05: OCR (Date: ____)
- [ ] Lab 06: Video Indexer (Date: ____)

## Language (mslearn-ai-language)
- [ ] Lab: Text Analytics (Date: ____)
- [ ] Lab: Translation (Date: ____)
- [ ] Lab: Speech (Date: ____)
- [ ] Lab: Conversational AI (Date: ____)
- [ ] Lab: Question Answering (Date: ____)

## Document Intelligence (mslearn-ai-document-intelligence)
- [ ] Lab 01: Prebuilt Models (Date: ____)
- [ ] Lab 02: Custom Models (Date: ____)
- [ ] Lab 03: Composed Models (Date: ____)

## Knowledge Mining (mslearn-knowledge-mining)
- [ ] Lab: Create Search Solution (Date: ____)
- [ ] Lab: Enrich with Skillsets (Date: ____)
- [ ] Lab: Custom Skills (Date: ____)

## OpenAI (mslearn-openai)
- [ ] Lab: Get Started (Date: ____)
- [ ] Lab: Use SDK (Date: ____)
- [ ] Lab: Prompt Engineering (Date: ____)
- [ ] Lab: Embeddings (Date: ____)
- [ ] Lab: RAG Pattern (Date: ____)

## Notes & Key Learnings
- 
- 
- 
EOF

cat lab-progress.md
```

---

## 🚨 Troubleshooting Guide

### Problem: Authentication Fails

```bash
# Solution 1: Re-login to Azure
az logout
az login
az account set --subscription "YOUR_SUBSCRIPTION"

# Solution 2: Verify resource exists
az cognitiveservices account list --output table

# Solution 3: Regenerate keys
az cognitiveservices account keys list \
  --name your-resource-name \
  --resource-group your-rg
```

### Problem: Module Not Found (Python)

```bash
# Solution: Verify virtual environment
which python
# Should show: .../venv/bin/python

# If not in venv:
source venv/bin/activate

# Reinstall packages
pip install -r requirements.txt
```

### Problem: Resource Quota Exceeded

```bash
# Solution: Check your Azure limits
az cognitiveservices account list-usage \
  --name your-resource-name \
  --resource-group your-rg

# Use Free tier for labs when available
# F0 tier: Free (limited requests per month)
# S0 tier: Standard (pay as you go)
```

---

## 💡 Pro Tips for Labs

1. **Always Read Instructions First:** Each lab's `Instructions/` folder has detailed markdown guides

2. **Use Multi-Service Resources:** Create one Azure AI Services resource instead of individual services

3. **Clean Up After Each Lab:**
   ```bash
   # Delete test resources
   az group delete --name test-lab-rg --yes --no-wait
   ```

4. **Keep Track of Costs:**
   ```bash
   # Check costs
   az consumption usage list --output table
   ```

5. **Use Version Control:** Track your modified lab code
   ```bash
   git init
   git add .
   git commit -m "Completed Lab 01"
   ```

---

## 🎓 Ready to Start?

### Recommended First Lab:
```bash
cd "/Users/arturoquiroga/AI-102 EXAM/mslearn-ai-services"
open Instructions/Labs/01-use-azure-ai-services.md
```

### Follow Along:
1. Read the instruction markdown file
2. Navigate to the corresponding `Labfiles/` folder
3. Choose Python or C-Sharp
4. Configure your credentials
5. Run the lab
6. Experiment and modify the code

---

**Good luck with your hands-on labs! 🚀**

*Remember: The key to AI-102 success is HANDS-ON PRACTICE!*
