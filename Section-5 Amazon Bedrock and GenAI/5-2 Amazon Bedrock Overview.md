### Amazon Bedrock

- Build Generative AI applications on AWS
- Fully managed service, no serviers for you to manage
- Keep ocntrol of your data to train the model
- Pay-per-use pricing model
- Unified APIs
- Leverage a wide array of foundation models
- Out of the box features: RAG, LLM Agents
- Security, Privacy, Governance and Responsible AI features


#### Foundation Models available 
- AI21 Labs
- Cohere
- Stability AI
- Amazon 
- Anthropic
- Meta
- Mistral AI

Note: 
- AWS Bedrock makes a copy of the FM available only to you, which you can further fine-tune with your own data
- None of your data is used to train the original  FM


### How to Choose FM
- Check fo model types, requirements, capabilities, compliances
- Level of customization, model size, inference options, licensing agreements, context windows, latency
- Multimodal models (varied types of input and outputs)
- Smaller models are most cost-effective but less capabilities

### Amazon Titan (FM)
- High performint FM models from AWS
- Image, text, multimodal model choices via fully managed APIs
- Can be customized with your own data


### Create Fine Tuning Job
- Bedrock offers fine-tune job to improve the knowledge of your LLM
- How it works
    - Go to Custom Models
    - Select Fine-Tuning Job
    - Select a Model
    - Add Fine Tune Model Name
    - Add Job Name
    - VPC Settings
    - Input Data, can be S3
    - Hyperparameters
        - epochs

