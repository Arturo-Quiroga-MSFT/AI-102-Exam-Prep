# Cloning Microsoft Learn Lab Repositories

This repository contains study guides and documentation for AI-102 exam preparation. The actual lab files are maintained in official Microsoft Learn repositories.

## 📥 Clone All Required Lab Repositories

Run these commands to get all the hands-on lab materials:

```bash
# Navigate to your workspace
cd /path/to/your/AI-102-workspace

# Clone all Microsoft Learn repositories
git clone https://github.com/MicrosoftLearning/mslearn-ai-services.git
git clone https://github.com/MicrosoftLearning/mslearn-ai-vision.git
git clone https://github.com/MicrosoftLearning/mslearn-ai-language.git
git clone https://github.com/MicrosoftLearning/mslearn-ai-document-intelligence.git
git clone https://github.com/MicrosoftLearning/mslearn-knowledge-mining.git
git clone https://github.com/MicrosoftLearning/mslearn-openai.git
```

## 🔄 Or Clone All at Once

```bash
#!/bin/bash
# Clone all AI-102 lab repositories

repos=(
  "mslearn-ai-services"
  "mslearn-ai-vision"
  "mslearn-ai-language"
  "mslearn-ai-document-intelligence"
  "mslearn-knowledge-mining"
  "mslearn-openai"
)

for repo in "${repos[@]}"; do
  echo "Cloning $repo..."
  git clone "https://github.com/MicrosoftLearning/$repo.git"
done

echo "✅ All repositories cloned successfully!"
```

## 📚 Repository Links

| Repository | Purpose | Link |
|------------|---------|------|
| mslearn-ai-services | AI Services fundamentals, security, monitoring | [Link](https://github.com/MicrosoftLearning/mslearn-ai-services) |
| mslearn-ai-vision | Computer Vision, OCR, Face, Custom Vision | [Link](https://github.com/MicrosoftLearning/mslearn-ai-vision) |
| mslearn-ai-language | Text analytics, translation, speech, CLU | [Link](https://github.com/MicrosoftLearning/mslearn-ai-language) |
| mslearn-ai-document-intelligence | Form extraction, custom models | [Link](https://github.com/MicrosoftLearning/mslearn-ai-document-intelligence) |
| mslearn-knowledge-mining | Azure AI Search, skillsets, indexing | [Link](https://github.com/MicrosoftLearning/mslearn-knowledge-mining) |
| mslearn-openai | Azure OpenAI, GPT, embeddings, RAG | [Link](https://github.com/MicrosoftLearning/mslearn-openai) |

## 📁 Recommended Workspace Structure

After cloning, your workspace should look like this:

```
your-workspace/
├── AI-102-Exam-Prep/              ← This repository (study guides)
│   ├── README.md
│   ├── AI-102-STUDY-GUIDE.md
│   ├── SETUP-ENVIRONMENT.md
│   └── QUICK-START-LABS.md
├── mslearn-ai-services/            ← Lab files
├── mslearn-ai-vision/              ← Lab files
├── mslearn-ai-language/            ← Lab files
├── mslearn-ai-document-intelligence/ ← Lab files
├── mslearn-knowledge-mining/       ← Lab files
└── mslearn-openai/                 ← Lab files
```

## ℹ️ Why Separate Repositories?

The Microsoft Learn lab repositories are:
- **Large** (contain many images, data files, and sample code)
- **Frequently updated** by Microsoft
- **Official sources** maintained by Microsoft Learning team
- Best kept as separate clones so you can pull updates

This study guide repository focuses on:
- Curated documentation and study plans
- Environment setup guides
- Quick reference materials
- Progress tracking

## 🔄 Keeping Labs Updated

To get the latest lab updates:

```bash
# Update all repositories
cd mslearn-ai-services && git pull origin main && cd ..
cd mslearn-ai-vision && git pull origin main && cd ..
cd mslearn-ai-language && git pull origin main && cd ..
cd mslearn-ai-document-intelligence && git pull origin main && cd ..
cd mslearn-knowledge-mining && git pull origin main && cd ..
cd mslearn-openai && git pull origin main && cd ..
```

## 🚀 Quick Start

1. **Clone this study guide repository:**
   ```bash
   git clone https://github.com/Arturo-Quiroga-MSFT/AI-102-Exam-Prep.git
   cd AI-102-Exam-Prep
   ```

2. **Read the study guide:**
   ```bash
   cat README.md
   ```

3. **Clone the lab repositories** (use script above)

4. **Start your first lab!**

---

**Note:** These are official Microsoft Learning repositories. We don't include them as submodules to keep this repository lightweight and to allow you to manage lab updates independently.
