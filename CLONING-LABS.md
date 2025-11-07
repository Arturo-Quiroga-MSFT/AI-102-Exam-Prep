# Microsoft Learn Lab Files

This repository contains study guides and documentation for AI-102 exam preparation. **The lab files are included as ZIP archives** in the `lab-files/` directory.

## 📦 Lab Files Included

All official Microsoft Learn lab repositories are provided as ZIP files (~105 MB total):

- ✅ **mslearn-ai-services.zip** (1.6 MB)
- ✅ **mslearn-ai-vision.zip** (37 MB)
- ✅ **mslearn-ai-language.zip** (5.3 MB)
- ✅ **mslearn-ai-document-intelligence.zip** (13 MB)
- ✅ **mslearn-knowledge-mining.zip** (42 MB)
- ✅ **mslearn-openai.zip** (5.8 MB)

See `lab-files/README.md` for detailed information about each archive.

## 🚀 Quick Start - Extract Lab Files

### Option 1: Extract All Labs
```bash
# Navigate to lab-files directory
cd lab-files

# Extract all ZIP files (macOS/Linux)
unzip mslearn-ai-services.zip
unzip mslearn-ai-vision.zip
unzip mslearn-ai-language.zip
unzip mslearn-ai-document-intelligence.zip
unzip mslearn-knowledge-mining.zip
unzip mslearn-openai.zip

# Or extract all at once
unzip '*.zip'
```

### Option 2: Extract Individual Labs
```bash
# Extract only what you need
cd lab-files
unzip mslearn-ai-vision.zip

# Navigate to the labs
cd mslearn-ai-vision-main/Labfiles
```

### Option 3: Double-Click (GUI)
- Open the `lab-files/` folder
- Double-click any ZIP file to extract
- Start working through the labs!

## 📂 Alternative: Download Directly from GitHub

If you prefer to always have the latest versions, you can download directly:

```bash
# Download latest ZIPs
curl -L -o mslearn-ai-services.zip "https://github.com/MicrosoftLearning/mslearn-ai-services/archive/refs/heads/main.zip"
curl -L -o mslearn-ai-vision.zip "https://github.com/MicrosoftLearning/mslearn-ai-vision/archive/refs/heads/main.zip"
# ... etc
```

Or clone the repositories (if you want Git history):

```bash
git clone https://github.com/MicrosoftLearning/mslearn-ai-services.git
git clone https://github.com/MicrosoftLearning/mslearn-ai-vision.git
git clone https://github.com/MicrosoftLearning/mslearn-ai-language.git
git clone https://github.com/MicrosoftLearning/mslearn-ai-document-intelligence.git
git clone https://github.com/MicrosoftLearning/mslearn-knowledge-mining.git
git clone https://github.com/MicrosoftLearning/mslearn-openai.git
```

## 📚 Repository Links

| Repository | Purpose | GitHub Link | ZIP in This Repo |
|------------|---------|-------------|------------------|
| mslearn-ai-services | AI Services fundamentals, security, monitoring | [GitHub](https://github.com/MicrosoftLearning/mslearn-ai-services) | ✅ `lab-files/mslearn-ai-services.zip` |
| mslearn-ai-vision | Computer Vision, OCR, Face, Custom Vision | [GitHub](https://github.com/MicrosoftLearning/mslearn-ai-vision) | ✅ `lab-files/mslearn-ai-vision.zip` |
| mslearn-ai-language | Text analytics, translation, speech, CLU | [GitHub](https://github.com/MicrosoftLearning/mslearn-ai-language) | ✅ `lab-files/mslearn-ai-language.zip` |
| mslearn-ai-document-intelligence | Form extraction, custom models | [GitHub](https://github.com/MicrosoftLearning/mslearn-ai-document-intelligence) | ✅ `lab-files/mslearn-ai-document-intelligence.zip` |
| mslearn-knowledge-mining | Azure AI Search, skillsets, indexing | [GitHub](https://github.com/MicrosoftLearning/mslearn-knowledge-mining) | ✅ `lab-files/mslearn-knowledge-mining.zip` |
| mslearn-openai | Azure OpenAI, GPT, embeddings, RAG | [GitHub](https://github.com/MicrosoftLearning/mslearn-openai) | ✅ `lab-files/mslearn-openai.zip` |

## 📁 Recommended Workspace Structure

After extracting the lab files:

```
your-ai-102-workspace/
├── AI-102-Exam-Prep/                    ← This repository (study guides)
│   ├── README.md
│   ├── AI-102-STUDY-GUIDE.md
│   ├── SETUP-ENVIRONMENT.md
│   ├── QUICK-START-LABS.md
│   └── lab-files/                       ← ZIP archives
│       ├── mslearn-ai-services.zip
│       ├── mslearn-ai-vision.zip
│       ├── mslearn-ai-language.zip
│       ├── mslearn-ai-document-intelligence.zip
│       ├── mslearn-knowledge-mining.zip
│       └── mslearn-openai.zip
│
└── extracted-labs/                      ← Extract ZIPs here (optional)
    ├── mslearn-ai-services-main/
    ├── mslearn-ai-vision-main/
    ├── mslearn-ai-language-main/
    ├── mslearn-ai-document-intelligence-main/
    ├── mslearn-knowledge-mining-main/
    └── mslearn-openai-main/
```

## ℹ️ Why Use ZIP Files?

**Advantages:**
- ✅ **No Git conflicts** - Clean, simple file structure
- ✅ **Version controlled** - ZIPs are tracked in this repo
- ✅ **Faster downloads** - Single file per repository
- ✅ **Easy updates** - Replace ZIP files when Microsoft updates
- ✅ **Smaller repo size** - No nested .git directories

**When to use Git Clone instead:**
- You want to contribute back to Microsoft Learning
- You need full Git history
- You want to track your own changes with Git

## 🔄 Updating Lab Files

The ZIP files included were downloaded on **November 7, 2025**.

To update to the latest versions:

### Update Individual Repository
```bash
cd lab-files

# Download latest version
curl -L -o mslearn-ai-vision.zip "https://github.com/MicrosoftLearning/mslearn-ai-vision/archive/refs/heads/main.zip"
```

### Update All Repositories
```bash
cd lab-files

curl -L -o mslearn-ai-services.zip "https://github.com/MicrosoftLearning/mslearn-ai-services/archive/refs/heads/main.zip"
curl -L -o mslearn-ai-vision.zip "https://github.com/MicrosoftLearning/mslearn-ai-vision/archive/refs/heads/main.zip"
curl -L -o mslearn-ai-language.zip "https://github.com/MicrosoftLearning/mslearn-ai-language/archive/refs/heads/main.zip"
curl -L -o mslearn-ai-document-intelligence.zip "https://github.com/MicrosoftLearning/mslearn-ai-document-intelligence/archive/refs/heads/main.zip"
curl -L -o mslearn-knowledge-mining.zip "https://github.com/MicrosoftLearning/mslearn-knowledge-mining/archive/refs/heads/main.zip"
curl -L -o mslearn-openai.zip "https://github.com/MicrosoftLearning/mslearn-openai/archive/refs/heads/main.zip"
```

## 🚀 Quick Start

1. **Clone or download this repository:**
   ```bash
   git clone https://github.com/Arturo-Quiroga-MSFT/AI-102-Exam-Prep.git
   cd AI-102-Exam-Prep
   ```

2. **Read the study guide:**
   ```bash
   cat README.md
   ```

3. **Extract the lab files you need:**
   ```bash
   cd lab-files
   unzip mslearn-ai-vision.zip
   cd mslearn-ai-vision-main/Labfiles
   ```

4. **Start your first lab!**
   - Follow instructions in `Instructions/Labs/` folder
   - Configure Azure credentials
   - Run the exercises

---

**Note:** Lab ZIP files are included in this repository for convenience. They contain official Microsoft Learning content (MIT License) and are updated periodically.
