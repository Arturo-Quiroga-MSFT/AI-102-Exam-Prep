# Microsoft Learn Lab Files

This directory contains ZIP archives of all official Microsoft Learn repositories for AI-102 exam preparation.

## 📦 Included Lab Files

| ZIP File | Size | Repository | Description |
|----------|------|------------|-------------|
| **mslearn-ai-services.zip** | 1.6 MB | [mslearn-ai-services](https://github.com/MicrosoftLearning/mslearn-ai-services) | AI Services fundamentals, security, monitoring |
| **mslearn-ai-vision.zip** | 37 MB | [mslearn-ai-vision](https://github.com/MicrosoftLearning/mslearn-ai-vision) | Computer Vision, OCR, Face, Custom Vision |
| **mslearn-ai-language.zip** | 5.3 MB | [mslearn-ai-language](https://github.com/MicrosoftLearning/mslearn-ai-language) | Text analytics, translation, speech, CLU |
| **mslearn-ai-document-intelligence.zip** | 13 MB | [mslearn-ai-document-intelligence](https://github.com/MicrosoftLearning/mslearn-ai-document-intelligence) | Form extraction, custom models |
| **mslearn-knowledge-mining.zip** | 42 MB | [mslearn-knowledge-mining](https://github.com/MicrosoftLearning/mslearn-knowledge-mining) | Azure AI Search, skillsets, indexing |
| **mslearn-openai.zip** | 5.8 MB | [mslearn-openai](https://github.com/MicrosoftLearning/mslearn-openai) | Azure OpenAI, GPT, embeddings, RAG |

**Total Size:** ~105 MB

## 📂 How to Use These Files

### Option 1: Extract All at Once
```bash
# Navigate to lab-files directory
cd "/path/to/AI-102 EXAM/lab-files"

# Extract all ZIP files
unzip mslearn-ai-services.zip
unzip mslearn-ai-vision.zip
unzip mslearn-ai-language.zip
unzip mslearn-ai-document-intelligence.zip
unzip mslearn-knowledge-mining.zip
unzip mslearn-openai.zip
```

### Option 2: Extract Individual Labs
```bash
# Extract only the labs you need
unzip mslearn-ai-vision.zip -d mslearn-ai-vision
cd mslearn-ai-vision/mslearn-ai-vision-main/Labfiles
```

### Option 3: Work Directly from ZIP (macOS/Windows)
- Double-click any ZIP file to extract
- Navigate to the extracted folder
- Follow the lab instructions in the `Instructions/` folder

## 🔄 Updating Lab Files

These ZIP files contain snapshots of the repositories as of **November 7, 2025**.

To get the latest versions:
1. Visit the repository links above
2. Click "Code" → "Download ZIP"
3. Replace the old ZIP file with the new one

Or download directly via command line:
```bash
cd "/path/to/AI-102 EXAM/lab-files"

# Download latest version of any repo
curl -L -o mslearn-ai-services.zip "https://github.com/MicrosoftLearning/mslearn-ai-services/archive/refs/heads/main.zip"
```

## 🚀 Quick Start Guide

1. **Extract the repository you want to work with:**
   ```bash
   unzip mslearn-ai-vision.zip
   cd mslearn-ai-vision-main
   ```

2. **Read the instructions:**
   - Navigate to `Instructions/Labs/` or `Instructions/Exercises/`
   - Open the markdown files for step-by-step guidance

3. **Set up your environment:**
   - Configure Azure credentials in `.env` (Python) or `appsettings.json` (C#)
   - Install required packages
   - Run the labs!

## 📋 Lab Structure

Each extracted repository typically contains:
```
mslearn-[service]-main/
├── Instructions/
│   ├── Labs/           # Step-by-step lab instructions
│   └── Exercises/      # Alternative format instructions
├── Labfiles/
│   ├── 01-lab-name/
│   │   ├── Python/     # Python implementation
│   │   └── C-Sharp/    # C# implementation
│   └── ...
└── README.md           # Repository information
```

## 💡 Tips

- **Keep the ZIPs:** Don't delete the ZIP files after extraction - you may need to start fresh
- **Extract to a workspace:** Create a dedicated workspace folder outside this repo
- **Version Control:** The ZIPs are version-controlled in this repo, so you always have a backup
- **Clean Extractions:** Delete and re-extract if you modify files and want to start over

## ⚠️ Important Notes

- **Size:** Extracted files will take up ~300-400 MB of disk space
- **Credentials:** Never commit `.env` or `appsettings.json` files with real Azure credentials
- **Updates:** Microsoft updates these repositories regularly - check for updates monthly
- **Git:** Extracted folders contain `.git` directories - these are safe to delete if you don't need version history

---

**Downloaded:** November 7, 2025  
**Source:** Official Microsoft Learn Repositories  
**License:** MIT (per Microsoft Learning repositories)
