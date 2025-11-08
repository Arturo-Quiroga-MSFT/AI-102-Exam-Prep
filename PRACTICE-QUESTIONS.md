# AI-102 Practice Questions
## Based on Microsoft Learn Module Topics

> **Note:** These practice questions are based on Microsoft Learn module learning objectives and exam skills measured. For official knowledge checks, please visit each module on Microsoft Learn while logged in.

---

## Module 1: Plan and Manage Azure AI Solutions

### Question 1
You need to provision an Azure AI Services resource for a production application. Which pricing tier should you select?

A) F0 (Free tier)  
B) S0 (Standard tier)  
C) It doesn't matter, both provide the same SLA  
D) Use separate single-service resources for better performance

<details>
<summary>Answer</summary>

**B) S0 (Standard tier)**

Explanation: Free tier (F0) has limited requests and no SLA guarantee. Production applications require S0 (Standard) tier for:
- Guaranteed SLA
- Higher rate limits
- Better support
- No request limits per month
</details>

---

### Question 2
Which of the following authentication methods is the MOST secure for accessing Azure AI Services in a production environment?

A) Using subscription keys from the Azure portal  
B) Using Microsoft Entra ID (Azure AD) authentication with managed identities  
C) Storing keys in application code  
D) Sharing keys across multiple applications

<details>
<summary>Answer</summary>

**B) Using Microsoft Entra ID (Azure AD) authentication with managed identities**

Explanation: Managed identities provide the most secure approach because:
- No credentials stored in code
- Automatic credential rotation
- Azure manages the identity lifecycle
- Follows principle of least privilege
- Keys can be compromised or leaked; managed identities cannot
</details>

---

### Question 3
You want to monitor the total number of API calls made to your Azure AI Services resource. Which Azure service should you use?

A) Azure Monitor  
B) Application Insights  
C) Azure Log Analytics  
D) Azure Service Health

<details>
<summary>Answer</summary>

**A) Azure Monitor**

Explanation: Azure Monitor provides metrics and logs for Azure AI Services including:
- Total calls
- Successful calls
- Error rates
- Data in/out
- Latency metrics
</details>

---

### Question 4
What is the benefit of deploying Azure AI Services in containers?

A) Lower cost  
B) Better performance  
C) Ability to run on-premises or at the edge  
D) Unlimited API requests

<details>
<summary>Answer</summary>

**C) Ability to run on-premises or at the edge**

Explanation: Container deployment enables:
- Running in disconnected environments
- Meeting data residency requirements
- Reducing latency by running locally
- Hybrid cloud scenarios
- Note: Containers still require connectivity to Azure for billing
</details>

---

### Question 5
You need to regenerate your Azure AI Services access keys without causing downtime. What should you do?

A) Delete and recreate the resource  
B) Regenerate key1, update applications to use key2, then regenerate key2  
C) Regenerate both keys simultaneously  
D) Disable the service temporarily

<details>
<summary>Answer</summary>

**B) Regenerate key1, update applications to use key2, then regenerate key2**

Explanation: Best practice for key rotation without downtime:
1. Ensure apps use key1
2. Regenerate key2 (key1 still works)
3. Update apps to use new key2
4. Test apps work with key2
5. Regenerate key1
6. Update apps back to key1 if needed
</details>

---

## Module 2: Computer Vision Solutions

### Question 6
Which Azure AI Vision feature should you use to determine if an image contains a person, a building, or a tree?

A) Face detection  
B) Image tagging  
C) OCR (Optical Character Recognition)  
D) Thumbnail generation

<details>
<summary>Answer</summary>

**B) Image tagging**

Explanation: Image tagging identifies objects, living things, scenery, and actions in images. Returns descriptive tags with confidence scores.
</details>

---

### Question 7
You need to detect and extract text from a scanned PDF document. Which service should you use?

A) Azure AI Vision - Analyze Image  
B) Azure AI Vision - Read API  
C) Face API  
D) Custom Vision

<details>
<summary>Answer</summary>

**B) Azure AI Vision - Read API**

Explanation: The Read API is optimized for:
- Text-heavy documents
- PDFs
- Handwritten text
- Mixed printed and handwritten text
- Multiple languages
</details>

---

### Question 8
You're building a custom image classification model to identify defective products. Which Azure service should you use?

A) Azure AI Vision - Analyze Image  
B) Custom Vision  
C) Face API  
D) Video Indexer

<details>
<summary>Answer</summary>

**B) Custom Vision**

Explanation: Custom Vision is designed for:
- Training custom image classification models
- Custom object detection
- Domain-specific scenarios
- Easy model training with small datasets
</details>

---

### Question 9
What is the minimum number of images required per category to train a Custom Vision image classification model?

A) 1 image  
B) 5 images  
C) 15 images  
D) 50 images

<details>
<summary>Answer</summary>

**B) 5 images**

Explanation: Minimum requirements:
- Image classification: 5 images per tag minimum
- Object detection: 15 images per tag minimum
- Recommended: 50+ images per tag for better accuracy
</details>

---

### Question 10
You need to detect faces in an image and determine the approximate age of each person. Which feature should you use?

A) Face Detection with Face API  
B) Image Analysis with Azure AI Vision  
C) Custom Vision  
D) Video Indexer

<details>
<summary>Answer</summary>

**A) Face Detection with Face API**

Explanation: Face API provides:
- Face detection
- Face attributes (age, gender, emotion, etc.)
- Face recognition
- Face verification
Note: Due to Responsible AI updates, age detection may require Limited Access approval
</details>

---

## Module 3: Natural Language Processing

### Question 11
You need to determine the sentiment (positive, negative, neutral) of customer reviews. Which Azure AI Language feature should you use?

A) Key phrase extraction  
B) Entity recognition  
C) Sentiment analysis  
D) Language detection

<details>
<summary>Answer</summary>

**C) Sentiment analysis**

Explanation: Sentiment analysis provides:
- Overall sentiment (positive/negative/neutral/mixed)
- Confidence scores for each sentiment
- Sentence-level sentiment
- Opinion mining for aspect-based sentiment
</details>

---

### Question 12
Which Azure AI Language service should you use to extract names of people, organizations, and locations from text?

A) Key phrase extraction  
B) Named Entity Recognition (NER)  
C) Language detection  
D) Text translation

<details>
<summary>Answer</summary>

**B) Named Entity Recognition (NER)**

Explanation: NER identifies and categorizes:
- Person names
- Organizations
- Locations
- Dates/times
- Quantities
- Custom entity types
</details>

---

### Question 13
You're building a chatbot that needs to understand user intents like "BookFlight" or "CancelReservation". Which service should you use?

A) Question Answering  
B) Conversational Language Understanding (CLU)  
C) Text Analytics  
D) Translator

<details>
<summary>Answer</summary>

**B) Conversational Language Understanding (CLU)**

Explanation: CLU provides:
- Intent recognition
- Entity extraction
- Utterance training
- Multi-language support
- Integration with bot frameworks
</details>

---

### Question 14
What is the primary difference between Conversational Language Understanding and Question Answering?

A) CLU extracts intents and entities; QnA matches questions to answers from a knowledge base  
B) CLU is for chat; QnA is for voice  
C) CLU requires more training data  
D) There is no difference

<details>
<summary>Answer</summary>

**A) CLU extracts intents and entities; QnA matches questions to answers from a knowledge base**

Explanation:
- **CLU**: Understands user intent in conversational context (what user wants to do)
- **QnA**: Retrieves answers to specific questions from FAQ/documents (information retrieval)
</details>

---

### Question 15
You need to translate user input text from English to Spanish in real-time. Which service should you use?

A) Azure AI Language - Text Analytics  
B) Azure AI Translator  
C) Speech Service  
D) Custom Translator

<details>
<summary>Answer</summary>

**B) Azure AI Translator**

Explanation: Azure AI Translator provides:
- Text translation across 100+ languages
- Real-time translation
- Document translation
- Custom translation models (optional)
</details>

---

## Module 4: Speech Services

### Question 16
You're building an application that converts spoken audio to text. Which Azure service feature should you use?

A) Speech synthesis (text-to-speech)  
B) Speech recognition (speech-to-text)  
C) Speech translation  
D) Speaker recognition

<details>
<summary>Answer</summary>

**B) Speech recognition (speech-to-text)**

Explanation: Speech-to-text provides:
- Real-time transcription
- Batch transcription
- Support for multiple languages
- Custom speech models
</details>

---

### Question 17
You want to generate natural-sounding speech from text with a specific voice. What should you use?

A) Speech recognition  
B) Speech Synthesis Markup Language (SSML)  
C) Custom Speech  
D) Speech translation

<details>
<summary>Answer</summary>

**B) Speech Synthesis Markup Language (SSML)**

Explanation: SSML allows you to:
- Select specific voices
- Control pronunciation
- Adjust speaking rate and pitch
- Add pauses and emphasis
- Use different languages
</details>

---

### Question 18
You need to transcribe audio that contains domain-specific terminology not recognized well by default models. What should you do?

A) Use standard speech-to-text  
B) Train a Custom Speech model  
C) Use speech translation  
D) Increase audio quality

<details>
<summary>Answer</summary>

**B) Train a Custom Speech model**

Explanation: Custom Speech allows you to:
- Improve recognition for specific vocabularies
- Adapt to accents or speaking styles
- Handle domain-specific terms
- Train with your own audio and transcriptions
</details>

---

### Question 19
Which format is recommended for audio input to Azure Speech Services for best results?

A) MP3, 128 kbps  
B) WAV, 16 kHz, 16-bit, mono  
C) AAC, 44.1 kHz  
D) Any format works equally well

<details>
<summary>Answer</summary>

**B) WAV, 16 kHz, 16-bit, mono**

Explanation: Recommended audio specifications:
- Format: WAV (uncompressed)
- Sample rate: 16 kHz or 8 kHz
- Bit depth: 16-bit
- Channels: Mono
- Quality impacts recognition accuracy
</details>

---

### Question 20
You need to detect specific keywords in streaming audio. Which Speech Service feature should you use?

A) Speech-to-text  
B) Keyword recognition  
C) Intent recognition  
D) Speaker verification

<details>
<summary>Answer</summary>

**B) Keyword recognition**

Explanation: Keyword recognition:
- Detects predefined keywords in audio streams
- Low latency activation
- Works offline on devices
- Common for "wake words" (e.g., "Hey Cortana")
</details>

---

## Module 5: Document Intelligence

### Question 21
You need to extract data from invoices without training a custom model. What should you use?

A) Custom model  
B) Prebuilt invoice model  
C) Layout API  
D) General document model

<details>
<summary>Answer</summary>

**B) Prebuilt invoice model**

Explanation: Prebuilt models are available for:
- Invoices
- Receipts
- Business cards
- ID documents
- W-2 forms
No training required, ready to use
</details>

---

### Question 22
You're training a custom Document Intelligence model. What is the minimum number of sample documents required?

A) 1 document  
B) 5 documents  
C) 10 documents  
D) 50 documents

<details>
<summary>Answer</summary>

**B) 5 documents**

Explanation: Minimum requirements:
- Custom extraction: 5 sample documents
- Recommended: 10-15 for better accuracy
- Documents should represent variations in your forms
</details>

---

### Question 23
You have multiple form types (invoices, purchase orders, receipts) that need processing. What is the best approach?

A) Create one model for all forms  
B) Create separate models and use a composed model  
C) Use only prebuilt models  
D) Process them manually

<details>
<summary>Answer</summary>

**B) Create separate models and use a composed model**

Explanation: Composed models:
- Combine multiple custom models
- Auto-route documents to the right model
- Single endpoint for all document types
- Better accuracy than one generic model
</details>

---

### Question 24
Which Document Intelligence feature should you use to extract tables from documents?

A) Read API  
B) Layout API  
C) Prebuilt invoice model  
D) Custom model only

<details>
<summary>Answer</summary>

**B) Layout API**

Explanation: Layout API extracts:
- Text
- Tables (structure and content)
- Selection marks (checkboxes)
- Document structure
Used as foundation for custom models
</details>

---

### Question 25
You need to extract custom fields from internal company forms. What should you create?

A) Use prebuilt model  
B) Train a custom extraction model  
C) Use OCR only  
D) Use Layout API

<details>
<summary>Answer</summary>

**B) Train a custom extraction model**

Explanation: Custom models are needed when:
- Forms are specific to your organization
- No prebuilt model matches your needs
- You need specific field extraction
- You have labeled training data
</details>

---

## Module 6: Azure AI Search (Knowledge Mining)

### Question 26
What is the purpose of an indexer in Azure AI Search?

A) To store documents  
B) To automatically crawl and index data from data sources  
C) To query the index  
D) To secure the search service

<details>
<summary>Answer</summary>

**B) To automatically crawl and index data from data sources**

Explanation: Indexers:
- Connect to data sources (Blob Storage, SQL, Cosmos DB)
- Extract content and metadata
- Run on schedule or on-demand
- Populate the search index
- Apply skillsets during indexing
</details>

---

### Question 27
You want to enrich your search index by extracting entities and key phrases from documents. What should you use?

A) Basic indexer  
B) Skillset with cognitive skills  
C) Custom analyzer  
D) Synonym map

<details>
<summary>Answer</summary>

**B) Skillset with cognitive skills**

Explanation: Skillsets apply AI enrichment:
- Built-in skills (entity extraction, OCR, translation)
- Custom skills (your own logic)
- Applied during indexing
- Enrich documents with AI-generated data
</details>

---

### Question 28
Which Azure AI Search feature enables you to store enriched data outside the search index for further analysis?

A) Synonym maps  
B) Knowledge store  
C) Search results  
D) Suggester

<details>
<summary>Answer</summary>

**B) Knowledge store**

Explanation: Knowledge store:
- Persists enriched data to Azure Storage
- Creates projections (tables, objects, files)
- Enables downstream analytics with Power BI
- Preserves AI enrichments for reuse
</details>

---

### Question 29
You need to implement a search feature that understands natural language queries and returns semantically relevant results. What should you use?

A) Simple query syntax  
B) Full Lucene query syntax  
C) Semantic search (semantic ranking)  
D) Wildcard search

<details>
<summary>Answer</summary>

**C) Semantic search (semantic ranking)**

Explanation: Semantic search:
- Uses AI to understand query intent
- Returns semantically relevant results
- Generates captions and answers
- Ranks results by meaning, not just keywords
- Requires S1 tier or higher
</details>

---

### Question 30
You want to add your own custom logic to process documents during indexing (e.g., call an external API). What should you implement?

A) Built-in skill  
B) Custom skill  
C) Analyzer  
D) Synonym map

<details>
<summary>Answer</summary>

**B) Custom skill**

Explanation: Custom skills allow you to:
- Integrate your own code/APIs
- Implement custom enrichment logic
- Call Azure Functions or web services
- Extend beyond built-in cognitive skills
</details>

---

## Module 7: Azure OpenAI and Generative AI

### Question 31
Which Azure OpenAI model is best suited for generating human-like conversational responses?

A) GPT-4  
B) DALL-E  
C) Embeddings (text-embedding-ada-002)  
D) Whisper

<details>
<summary>Answer</summary>

**A) GPT-4**

Explanation: GPT models are designed for:
- Natural language generation
- Conversational AI
- Text completion
- Code generation
GPT-4 is more capable than GPT-3.5 but more expensive
</details>

---

### Question 32
You want to generate images from text descriptions. Which Azure OpenAI model should you use?

A) GPT-4  
B) GPT-3.5-turbo  
C) DALL-E 3  
D) text-embedding-ada-002

<details>
<summary>Answer</summary>

**C) DALL-E 3**

Explanation: DALL-E models:
- Generate images from text prompts
- Create original images
- Edit existing images
- Multiple size options
DALL-E 3 is the latest version with improved quality
</details>

---

### Question 33
What is the purpose of embeddings in Azure OpenAI?

A) To generate text  
B) To create images  
C) To convert text into vector representations for semantic search  
D) To translate languages

<details>
<summary>Answer</summary>

**C) To convert text into vector representations for semantic search**

Explanation: Embeddings:
- Convert text to numerical vectors
- Enable semantic similarity search
- Foundation for RAG (Retrieval Augmented Generation)
- Used in recommendation systems
- Model: text-embedding-ada-002
</details>

---

### Question 34
You want to provide your generative AI model with access to your company's private documents. What pattern should you implement?

A) Fine-tuning  
B) Few-shot learning  
C) Retrieval Augmented Generation (RAG)  
D) Zero-shot learning

<details>
<summary>Answer</summary>

**C) Retrieval Augmented Generation (RAG)**

Explanation: RAG pattern:
- Retrieves relevant documents from your data
- Provides context to the model in the prompt
- Model generates responses based on your data
- No model retraining required
- Keeps data updated without retraining
</details>

---

### Question 35
Which parameter controls the randomness/creativity of Azure OpenAI completions?

A) max_tokens  
B) temperature  
C) top_p  
D) frequency_penalty

<details>
<summary>Answer</summary>

**B) temperature**

Explanation: Temperature parameter:
- Range: 0 to 2
- Lower (0-0.3): More deterministic, focused
- Higher (0.7-1.0): More creative, diverse
- Default: Often 0.7
- Use low temperature for factual tasks, high for creative tasks
</details>

---

### Question 36
You need to prevent your Azure OpenAI model from generating harmful content. What should you implement?

A) Lower temperature  
B) Content filters  
C) Few-shot learning  
D) Increase max_tokens

<details>
<summary>Answer</summary>

**B) Content filters**

Explanation: Content filters:
- Built-in safety system in Azure OpenAI
- Detects and blocks harmful content
- Categories: Hate, sexual, violence, self-harm
- Configurable severity levels
- Apply to both input and output
</details>

---

### Question 37
What is "prompt engineering"?

A) Coding prompts in Python  
B) Designing effective prompts to get desired outputs from AI models  
C) Creating model architectures  
D) Fine-tuning models

<details>
<summary>Answer</summary>

**B) Designing effective prompts to get desired outputs from AI models**

Explanation: Prompt engineering involves:
- Crafting clear, specific instructions
- Providing context and examples
- Using system messages effectively
- Iterating to improve results
- Critical skill for working with LLMs
</details>

---

### Question 38
You want to include examples in your prompt to guide the model's responses. What technique is this?

A) Zero-shot learning  
B) Few-shot learning  
C) Fine-tuning  
D) Transfer learning

<details>
<summary>Answer</summary>

**B) Few-shot learning**

Explanation: Few-shot learning:
- Provide examples in the prompt
- Model learns the pattern from examples
- No training required
- More effective than zero-shot for complex tasks
- Examples: "Here are some customer reviews and their sentiments..."
</details>

---

### Question 39
Which Azure service helps you build, test, and deploy generative AI applications using prompt flow?

A) Azure Machine Learning  
B) Azure AI Foundry  
C) Azure Functions  
D) Azure Logic Apps

<details>
<summary>Answer</summary>

**B) Azure AI Foundry**

Explanation: Azure AI Foundry provides:
- Prompt flow for designing AI workflows
- Model deployment and management
- Evaluation and testing tools
- Integration with Azure OpenAI
- RAG pattern implementation
</details>

---

### Question 40
You need to customize an Azure OpenAI model with your organization's specific data and writing style. What should you do?

A) Use RAG  
B) Fine-tune the model  
C) Increase temperature  
D) Use better prompts only

<details>
<summary>Answer</summary>

**B) Fine-tune the model**

Explanation: Fine-tuning:
- Trains model on your specific data
- Adapts model behavior and style
- More expensive and time-consuming than RAG
- Best for consistent style/format requirements
- Requires quality training data
When to use: Style consistency > factual knowledge = RAG
</details>

---

## Exam Scenario-Based Questions

### Scenario 1: E-commerce Platform

Your company is building an e-commerce platform that needs to:
- Analyze product images to generate tags
- Extract text from product labels
- Provide a chatbot for customer support
- Detect inappropriate product listings

### Question 41
Which Azure services would you use for this solution? (Select all that apply)

A) Azure AI Vision - Image Analysis  
B) Azure AI Vision - Read API  
C) Conversational Language Understanding  
D) Azure AI Content Safety  
E) Face API

<details>
<summary>Answer</summary>

**A, B, C, D are correct**

Explanation:
- **A) Image Analysis**: Generate tags for product images
- **B) Read API**: Extract text from product labels
- **C) CLU**: Power the chatbot with intent understanding
- **D) Content Safety**: Detect inappropriate content
- E is incorrect: Face API not needed for products
</details>

---

### Scenario 2: Healthcare Document Processing

A healthcare provider needs to process thousands of medical forms daily to extract patient information, diagnoses, and prescriptions.

### Question 42
What is the recommended Azure AI solution architecture?

A) Use Azure AI Vision Read API for all forms  
B) Train custom Document Intelligence models for each form type, then create a composed model  
C) Manually process forms  
D) Use only prebuilt models

<details>
<summary>Answer</summary>

**B) Train custom Document Intelligence models for each form type, then create a composed model**

Explanation:
- Medical forms are specialized (no prebuilt models)
- Multiple form types require separate models
- Composed model provides single endpoint
- Better accuracy than generic approach
- Can handle routing automatically
</details>

---

### Scenario 3: Multi-language Customer Support

Your global company needs a solution to:
- Accept customer questions in any language
- Respond with answers from an FAQ knowledge base
- Support voice and text input

### Question 43
Which services should you combine? (Select all that apply)

A) Speech Service (speech-to-text)  
B) Azure AI Translator  
C) Question Answering  
D) Custom Vision  
E) Speech Service (text-to-speech)

<details>
<summary>Answer</summary>

**A, B, C, E are correct**

Explanation:
- **A) Speech-to-text**: Convert voice input to text
- **B) Translator**: Handle multiple languages
- **C) Question Answering**: Match questions to FAQ answers
- **E) Text-to-speech**: Provide voice responses
- D is incorrect: Custom Vision not relevant here
</details>

---

### Scenario 4: Content Moderation Platform

You're building a social media platform that needs to:
- Detect harmful text content
- Identify inappropriate images
- Flag personally identifiable information (PII)

### Question 44
Which Azure AI services should you use? (Select all that apply)

A) Azure AI Content Safety  
B) Azure AI Language - PII Detection  
C) Azure AI Vision - Image Analysis  
D) Speech Service  
E) Document Intelligence

<details>
<summary>Answer</summary>

**A, B, C are correct**

Explanation:
- **A) Content Safety**: Detect harmful content (text & images)
- **B) PII Detection**: Identify and redact PII in text
- **C) Image Analysis**: Analyze images for inappropriate content
- D & E are incorrect: Not relevant for content moderation
</details>

---

### Scenario 5: Intelligent Search Solution

Your organization wants to implement an intelligent search across PDFs, Word documents, and images stored in Azure Blob Storage.

### Question 45
What components do you need? (Select all that apply)

A) Azure AI Search service  
B) Indexer with blob data source  
C) Skillset with OCR and entity extraction  
D) Custom Vision  
E) Knowledge store for analytics

<details>
<summary>Answer</summary>

**A, B, C, E are correct**

Explanation:
- **A) Azure AI Search**: Core search service
- **B) Indexer**: Crawl blob storage automatically
- **C) Skillset**: OCR for images, entity extraction for enrichment
- **E) Knowledge store**: Store enrichments for Power BI analysis
- D is incorrect: Custom Vision not needed for search
</details>

---

## Best Practices and Responsible AI

### Question 46
Which of the following is a principle of Responsible AI?

A) Maximize profit at all costs  
B) Fairness and inclusiveness  
C) Always use the most complex model  
D) Collect as much personal data as possible

<details>
<summary>Answer</summary>

**B) Fairness and inclusiveness**

Explanation: Microsoft's Responsible AI principles:
1. **Fairness**: AI should treat everyone fairly
2. **Reliability & Safety**: AI should perform reliably
3. **Privacy & Security**: AI should be secure and respect privacy
4. **Inclusiveness**: AI should empower and engage everyone
5. **Transparency**: AI should be understandable
6. **Accountability**: People should be accountable for AI
</details>

---

### Question 47
You're deploying a face recognition system for building access. What Responsible AI considerations should you address? (Select all that apply)

A) Ensure diverse training data to prevent bias  
B) Implement privacy controls and data protection  
C) Provide transparency about how the system works  
D) Disable all logging to maximize privacy  
E) Establish accountability for system decisions

<details>
<summary>Answer</summary>

**A, B, C, E are correct**

Explanation:
- **A) Fairness**: Diverse data prevents bias
- **B) Privacy**: Protect sensitive biometric data
- **C) Transparency**: Users should know how it works
- **E) Accountability**: Clear responsibility for decisions
- D is incorrect: Some logging needed for auditing and debugging
</details>

---

### Question 48
You notice your sentiment analysis model performs poorly on reviews from a specific demographic. What should you do?

A) Ignore it, the overall accuracy is good  
B) Retrain the model with more diverse and representative data  
C) Remove reviews from that demographic  
D) Lower the confidence threshold

<details>
<summary>Answer</summary>

**B) Retrain the model with more diverse and representative data**

Explanation: This is a **fairness** issue:
- Model shows bias toward certain groups
- Need representative training data
- Test across all demographics
- Monitor for disparate impact
- Iterate to improve fairness
</details>

---

### Question 49
Which Azure feature helps you identify and redact sensitive information before storing or processing text?

A) Sentiment analysis  
B) PII (Personally Identifiable Information) detection  
C) Key phrase extraction  
D) Entity recognition

<details>
<summary>Answer</summary>

**B) PII (Personally Identifiable Information) detection**

Explanation: PII detection identifies:
- Names
- Email addresses
- Phone numbers
- Social security numbers
- Credit card numbers
- IP addresses
Supports redaction/masking for privacy
</details>

---

### Question 50
Your Azure OpenAI application is generating inconsistent responses. What should you do FIRST?

A) Fine-tune a new model  
B) Review and improve your prompts (prompt engineering)  
C) Increase the temperature parameter  
D) Switch to a different model

<details>
<summary>Answer</summary>

**B) Review and improve your prompts (prompt engineering)**

Explanation: Troubleshooting order:
1. **Improve prompts**: Clearer instructions, examples, context
2. Adjust parameters: Temperature, top_p, etc.
3. Try few-shot learning: Add examples
4. Consider RAG: Provide relevant data
5. Fine-tune: Last resort, most expensive
Always start with prompt engineering!
</details>

---

## Summary and Next Steps

### Total Practice Questions: 50

**By Module:**
- Plan and Manage Azure AI: 5 questions
- Computer Vision: 5 questions  
- Natural Language Processing: 5 questions
- Speech Services: 5 questions
- Document Intelligence: 5 questions
- Azure AI Search: 5 questions
- Azure OpenAI/Generative AI: 10 questions
- Scenario-Based: 5 questions
- Responsible AI: 5 questions

### How to Use These Questions:

1. **First Pass**: Answer all questions without looking at answers
2. **Review**: Check answers and read explanations
3. **Study**: Focus on topics where you scored below 80%
4. **Repeat**: Take quiz again after studying
5. **Track Progress**: Record your scores over time

### Additional Practice Resources:

1. **Official Practice Assessment** (Free)
   - https://learn.microsoft.com/credentials/certifications/azure-ai-engineer/practice/assessment
   - ~50 questions, same format as exam
   - Take multiple times

2. **Microsoft Learn Module Assessments**
   - Complete knowledge checks in each learning module
   - Login required to access
   - Questions are module-specific

3. **MeasureUp Practice Tests** ($99-129)
   - Official Microsoft practice tests
   - ~120 questions
   - Most realistic simulation

4. **Hands-on Labs**
   - Complete ALL labs in `lab-files/` directory
   - Practical experience is crucial
   - Questions often test applied knowledge

### Exam Tips:

- **Time Management**: ~2 minutes per question
- **Read Carefully**: Watch for "NOT", "MOST", "LEAST"
- **Elimination**: Remove obviously wrong answers first
- **Flag & Return**: Don't get stuck on hard questions
- **Case Studies**: Allocate extra time for these
- **Review**: Use review screen before submitting

### Target Score:

- **Practice Tests**: Aim for 85%+ consistently
- **Real Exam**: 700+ out of 1000 to pass
- **Confidence Level**: Should recognize correct answers quickly

---

**Ready for More?**

1. Visit each Microsoft Learn module for interactive knowledge checks
2. Take the official free practice assessment
3. Complete all hands-on labs in the repo
4. Consider MeasureUp for additional practice

**Good luck with your AI-102 exam! 🚀**

*Last Updated: November 2025*
