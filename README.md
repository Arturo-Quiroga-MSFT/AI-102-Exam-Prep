# 🎓 AI-102 Exam Preparation - Complete Resource Index

> **Microsoft Certified: Azure AI Engineer Associate**  
> Exam Code: AI-102  
> Study Materials Prepared: November 2025

---

## 📚 What's Included

This workspace contains **ALL official Microsoft Learn repositories** with hands-on labs for the AI-102 certification exam, plus comprehensive study guides.

### ✅ Repository Status

| Repository | Status | Labs | Topics |
|------------|--------|------|--------|
| **mslearn-ai-services** | ✅ Cloned | 5 | AI Services fundamentals, security, monitoring |
| **mslearn-ai-vision** | ✅ Cloned | 9 | Computer Vision, OCR, Face, Custom Vision |
| **mslearn-ai-language** | ✅ Cloned | Multiple | Text analytics, translation, speech, CLU |
| **mslearn-ai-document-intelligence** | ✅ Cloned | 4 | Form extraction, custom models |
| **mslearn-knowledge-mining** | ✅ Cloned | Multiple | Azure AI Search, skillsets, indexing |
| **mslearn-openai** | ✅ Cloned | Multiple | Azure OpenAI, GPT, embeddings, RAG |

### 📖 Study Guides Created

| Document | Purpose | Status |
|----------|---------|--------|
| **AI-102-STUDY-GUIDE.md** | Complete exam overview, study path, progress tracking | ✅ Created |
| **SETUP-ENVIRONMENT.md** | Dev environment setup, tools installation | ✅ Created |
| **QUICK-START-LABS.md** | Lab examples, code samples, quick start guide | ✅ Created |
| **README.md** | This file - central navigation hub | ✅ Created |

---

## 🚀 Quick Start

### First Time Setup (Do This First!)

1. **Review Your Environment:**
   ```bash
   cat SETUP-ENVIRONMENT.md
   ```
   Your current status:
   - ✅ Python 3.12.10 installed
   - ✅ .NET 9.0.203 installed
   - ✅ Azure CLI 2.78.0 installed
   - ✅ Git installed
   - ✅ Visual Studio Code installed

2. **Read the Study Guide:**
   ```bash
   cat AI-102-STUDY-GUIDE.md
   ```

3. **Set Up Azure Account:**
   ```bash
   # Login to Azure
   az login
   
   # Create resource group for all labs
   az group create --name ai-102-labs-rg --location eastus
   ```

4. **Start Your First Lab:**
   ```bash
   cat QUICK-START-LABS.md
   ```

---

## 📋 Navigation Guide

### By Learning Path

#### 🟢 Week 1-2: Foundations
**Start Here** → `mslearn-ai-services/`
- **Focus:** Core Azure AI concepts, security, monitoring
- **Instructions:** `mslearn-ai-services/Instructions/Labs/`
- **Lab Files:** `mslearn-ai-services/Labfiles/`

#### 🔵 Week 3-4: Vision & Documents
**Computer Vision** → `mslearn-ai-vision/`
- **Focus:** Image analysis, OCR, face detection, Custom Vision
- **Instructions:** `mslearn-ai-vision/Instructions/Exercises/`
- **Lab Files:** `mslearn-ai-vision/Labfiles/`

**Document Intelligence** → `mslearn-ai-document-intelligence-main/`
- **Focus:** Form extraction, invoice processing, custom models
- **Instructions:** `mslearn-ai-document-intelligence-main/Instructions/`
- **Lab Files:** `mslearn-ai-document-intelligence-main/Labfiles/`

#### 🟡 Week 5-6: Language & Conversation
**Language Services** → `mslearn-ai-language/`
- **Focus:** Text analytics, translation, speech, conversational AI
- **Instructions:** `mslearn-ai-language/Instructions/`
- **Lab Files:** `mslearn-ai-language/Labfiles/`

#### 🟣 Week 7: Search & Knowledge Mining
**Azure AI Search** → `mslearn-knowledge-mining/`
- **Focus:** Full-text search, AI enrichment, skillsets
- **Instructions:** `mslearn-knowledge-mining/Instructions/`
- **Lab Files:** `mslearn-knowledge-mining/Labfiles/`

#### 🔴 Week 8: Generative AI
**Azure OpenAI** → `mslearn-openai/`
- **Focus:** GPT models, embeddings, RAG, prompt engineering
- **Instructions:** `mslearn-openai/Instructions/`
- **Lab Files:** `mslearn-openai/Labfiles/`

---

## 🎯 Exam Preparation Roadmap

### Phase 1: Foundation (Weeks 1-2)
```bash
cd mslearn-ai-services
# Complete Labs 1-5
# Topics: Resource creation, security, monitoring, containers
```

**Key Skills to Master:**
- Creating and managing Azure AI Services resources
- Implementing security best practices
- Monitoring usage and costs
- Deploying containerized solutions

### Phase 2: Core AI Services (Weeks 3-6)
```bash
# Vision
cd mslearn-ai-vision
# Complete all 9 labs

# Document Intelligence  
cd mslearn-ai-document-intelligence-main
# Complete Labs 1-4

# Language
cd mslearn-ai-language
# Complete all language labs
```

**Key Skills to Master:**
- Image analysis and classification
- OCR and text extraction
- Face detection (with current API limitations)
- Text analytics and sentiment analysis
- Translation services
- Speech recognition and synthesis
- Conversational language understanding

### Phase 3: Advanced Services (Weeks 7-8)
```bash
# Search & Knowledge Mining
cd mslearn-knowledge-mining
# Complete all search labs

# Azure OpenAI
cd mslearn-openai
# Complete all OpenAI labs
```

**Key Skills to Master:**
- Building search solutions
- Creating custom skills
- Knowledge store creation
- Using Azure OpenAI models
- Implementing RAG patterns
- Responsible AI practices

### Phase 4: Review & Practice (Weeks 9-10)
- Revisit challenging labs
- Build sample projects
- Take practice exams
- Review weak areas

---

## 📖 Essential Documentation Links

### Official Microsoft Resources
- **Exam Page:** [AI-102 Exam Details](https://learn.microsoft.com/credentials/certifications/exams/ai-102/)
- **Learning Path:** [Azure AI Engineer Learning Path](https://learn.microsoft.com/training/browse/?roles=ai-engineer)
- **Practice Assessment:** [Official Practice Test](https://learn.microsoft.com/credentials/certifications/azure-ai-engineer/practice/assessment)
- **Azure AI Docs:** [Azure AI Services Documentation](https://learn.microsoft.com/azure/ai-services/)

### GitHub Repositories (Already Cloned)
- [mslearn-ai-services](https://github.com/MicrosoftLearning/mslearn-ai-services)
- [mslearn-ai-vision](https://github.com/MicrosoftLearning/mslearn-ai-vision)
- [mslearn-ai-language](https://github.com/MicrosoftLearning/mslearn-ai-language)
- [mslearn-ai-document-intelligence](https://github.com/MicrosoftLearning/mslearn-ai-document-intelligence)
- [mslearn-knowledge-mining](https://github.com/MicrosoftLearning/mslearn-knowledge-mining)
- [mslearn-openai](https://github.com/MicrosoftLearning/mslearn-openai)

---

## 🛠️ Common Commands Cheat Sheet

### Navigate to a Lab
```bash
# General pattern:
cd "/Users/arturoquiroga/AI-102 EXAM/<repository>/Labfiles/<lab-number>/<language>"

# Example - Python lab:
cd "/Users/arturoquiroga/AI-102 EXAM/mslearn-ai-vision/Labfiles/01-analyze-images/Python"

# Example - C# lab:
cd "/Users/arturoquiroga/AI-102 EXAM/mslearn-ai-vision/Labfiles/01-analyze-images/C-Sharp"
```

### Set Up Python Lab
```bash
# Create virtual environment (first time only)
python3 -m venv venv

# Activate virtual environment
source venv/bin/activate

# Install dependencies
pip install -r requirements.txt  # if available
# OR install manually:
pip install azure-ai-vision-imageanalysis python-dotenv

# Configure credentials (edit .env file)
nano .env

# Run the lab
python your-script.py
```

### Set Up C# Lab
```bash
# Restore packages
dotnet restore

# Configure credentials (edit appsettings.json)
nano appsettings.json

# Run the lab
dotnet run
```

### Azure CLI Commands
```bash
# Login
az login

# Create resource group
az group create --name ai-102-labs-rg --location eastus

# Create AI Services resource
az cognitiveservices account create \
  --name ai-102-services \
  --resource-group ai-102-labs-rg \
  --kind CognitiveServices \
  --sku S0 \
  --location eastus

# Get keys
az cognitiveservices account keys list \
  --name ai-102-services \
  --resource-group ai-102-labs-rg

# Clean up resources
az group delete --name ai-102-labs-rg --yes
```

---

## 📊 Progress Tracking

### Track Your Progress
Edit the study guide to mark completed labs:
```bash
# Edit progress tracker
code AI-102-STUDY-GUIDE.md
# Update checkboxes as you complete labs
```

### Create Daily Notes
```bash
# Create a notes file
cat > study-notes.md << 'EOF'
# AI-102 Study Notes

## Date: YYYY-MM-DD
### Lab: [Lab Name]
- Key Concepts Learned:
- Challenges Faced:
- Important Code Snippets:
- Questions/Topics to Review:

EOF
```

---

## 💡 Pro Tips

### 1. Lab Best Practices
- ✅ **Always** read the instruction markdown files first
- ✅ Use **Free tier (F0)** resources when available for labs
- ✅ Create a **dedicated resource group** for labs (easy cleanup)
- ✅ **Clean up resources** after each session to avoid charges
- ✅ Keep your **credentials secure** (never commit .env files)

### 2. Cost Management
```bash
# Monitor costs
az consumption usage list --output table

# Delete resource group when done
az group delete --name ai-102-labs-rg --yes

# Use free tiers:
# - Azure AI Services: F0 (free)
# - Azure Search: Free tier
# - Storage: Free tier
```

### 3. Study Strategy
- 📚 **Hands-on First:** Complete labs before deep-diving into theory
- 🔄 **Repeat Labs:** Do challenging labs multiple times
- 🏗️ **Build Projects:** Combine multiple services in real projects
- 📝 **Document Learning:** Take notes on each lab
- 👥 **Join Community:** r/AzureCertification, Microsoft Q&A

### 4. Exam Preparation
- ⏰ **Pace Yourself:** 8-10 weeks of consistent study
- 📊 **Take Practice Tests:** Official Microsoft practice assessments
- 🎯 **Focus on Weak Areas:** Identify and review challenging topics
- 💼 **Understand Business Context:** Know when to use each service
- 💰 **Know Pricing Models:** Understand tiers and cost implications

---

## 🚨 Common Issues & Solutions

### Issue: "Module not found" in Python
```bash
# Activate virtual environment
source venv/bin/activate
# Install missing package
pip install <package-name>
```

### Issue: Azure authentication fails
```bash
# Re-login
az logout
az login
az account set --subscription "YOUR_SUBSCRIPTION"
```

### Issue: Resource quota exceeded
```bash
# Check usage
az cognitiveservices account list-usage \
  --name your-resource \
  --resource-group your-rg

# Use F0 (free) tier or delete unused resources
```

### Issue: VS Code can't find Python interpreter
- Press `Cmd+Shift+P`
- Type "Python: Select Interpreter"
- Choose your virtual environment

---

## 📅 Suggested Study Schedule

| Week | Focus Area | Repositories | Time Commitment |
|------|------------|--------------|-----------------|
| 1-2 | Foundations | mslearn-ai-services | 10-15 hrs/week |
| 3 | Computer Vision | mslearn-ai-vision | 10-15 hrs/week |
| 4 | Documents & Forms | mslearn-ai-document-intelligence | 8-10 hrs/week |
| 5-6 | Language & Speech | mslearn-ai-language | 12-15 hrs/week |
| 7 | Search & Mining | mslearn-knowledge-mining | 8-10 hrs/week |
| 8 | Generative AI | mslearn-openai | 10-12 hrs/week |
| 9-10 | Review & Practice | All repositories | 15-20 hrs/week |

**Total Estimated Study Time:** 80-120 hours

---

## 🎓 Ready to Begin?

### Start Your Journey Now:

1. **Open the Study Guide:**
   ```bash
   code AI-102-STUDY-GUIDE.md
   ```

2. **Review Setup Instructions:**
   ```bash
   code SETUP-ENVIRONMENT.md
   ```

3. **Launch Your First Lab:**
   ```bash
   code QUICK-START-LABS.md
   ```

4. **Navigate to Lab Files:**
   ```bash
   cd mslearn-ai-services/Instructions/Labs
   ls -la
   ```

---

## 📞 Additional Resources

### Community & Support
- **Microsoft Q&A:** [Azure AI Forum](https://learn.microsoft.com/answers/topics/azure-ai-services.html)
- **Reddit:** [r/AzureCertification](https://reddit.com/r/AzureCertification)
- **Discord:** Microsoft Community Discord
- **Stack Overflow:** Tag: `azure-cognitive-services`

### Books & Courses
- Official Microsoft Learning Path (Free)
- Pluralsight: Azure AI Engineer paths
- Udemy: AI-102 preparation courses
- Microsoft Learn modules

### Practice Exams
- Official Microsoft Practice Assessment
- MeasureUp practice exams
- Whizlabs AI-102 practice tests

---

## ✅ Final Checklist Before Exam

- [ ] Completed all labs in mslearn-ai-services
- [ ] Completed all labs in mslearn-ai-vision
- [ ] Completed all labs in mslearn-ai-language
- [ ] Completed all labs in mslearn-ai-document-intelligence
- [ ] Completed all labs in mslearn-knowledge-mining
- [ ] Completed all labs in mslearn-openai
- [ ] Taken official practice assessment
- [ ] Scored 80%+ on practice tests
- [ ] Built at least one sample project
- [ ] Reviewed Azure pricing models
- [ ] Understand service limits and quotas
- [ ] Know security best practices
- [ ] Familiar with deployment patterns
- [ ] Scheduled exam date

---

## 🎉 You're All Set!

**Everything you need to prepare for the AI-102 exam is now at your fingertips!**

### Your Workspace Structure:
```
/Users/arturoquiroga/AI-102 EXAM/
├── 📖 AI-102-STUDY-GUIDE.md          ← Comprehensive study plan
├── 🛠️ SETUP-ENVIRONMENT.md           ← Environment setup
├── 🚀 QUICK-START-LABS.md            ← Lab quick start guide
├── 📋 README.md                       ← This file (central hub)
├── 📁 mslearn-ai-services/           ← Foundation labs
├── 📁 mslearn-ai-vision/             ← Computer Vision labs
├── 📁 mslearn-ai-language/           ← Language & Speech labs
├── 📁 mslearn-ai-document-intelligence-main/  ← Document AI labs
├── 📁 mslearn-knowledge-mining/      ← Search labs
└── 📁 mslearn-openai/                ← Generative AI labs
```

### Next Step:
```bash
# Start with the study guide
open AI-102-STUDY-GUIDE.md

# Then begin your first lab
cd mslearn-ai-services/Instructions/Labs
open 01-use-azure-ai-services.md
```

---

**Good luck on your AI-102 certification journey! 🚀🎓**

*Last Updated: November 7, 2025*  
*Prepared for: Arturo Quiroga*  
*Exam: AI-102 - Azure AI Engineer Associate*

---

## 📌 Quick Reference Card

**Key Paths:**
- Study Guide: `AI-102-STUDY-GUIDE.md`
- Setup: `SETUP-ENVIRONMENT.md`
- Quick Start: `QUICK-START-LABS.md`
- Labs: `<repository>/Labfiles/`
- Instructions: `<repository>/Instructions/`

**Essential Commands:**
- Login Azure: `az login`
- Activate venv: `source venv/bin/activate`
- Run Python lab: `python script.py`
- Run C# lab: `dotnet run`
- Clean up: `az group delete --name <rg> --yes`

**Support:**
- Microsoft Learn: [learn.microsoft.com](https://learn.microsoft.com)
- Azure Docs: [docs.microsoft.com/azure](https://docs.microsoft.com/azure)
- Q&A Forum: [Microsoft Q&A](https://learn.microsoft.com/answers)
