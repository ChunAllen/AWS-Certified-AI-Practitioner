### AWS Bedrock - Fine Tuning a Model
- Adapt a copy of foundation model with your own data
- Fine-Tuning will change the weights of the base foundation model
- Training data must:
    - Adhere to a specific format
    - Be stored in Amazon S3
- You must use "Provisioned Throuput", there is no On-Demand
- Note: Not all models can be fine-tuned


##### Example of Fine Tuning:
- For LLAMA2 and S3
    - JSON should contain these keys
    ```
    {
        "prompt": "What is AWS",
        "completion": "It's Amazon Web Services"
    }
    ```
    - OR 
    ```
    {
        "input": "AWS stands for Amazon Web Services"
    }
    ```

- The output of this is LLAMA2 Fine-tuned Custom

### Different types of Fine Tuning

1) Instruction-based Fine Tuning
- Improves the performance of a pre-trained FM on a domain specific tasks
- Further trained on a particular field or area of knowledge
- Instruction-based fine-runing uses **labeled examples** that are **prompt-response pairs**
- Example of Instruction-Based Fine Tuning, there's **prompt** and **completion**
```
{
    "prompt": "What is AWS",
    "completion": "AWS, short for Amazon Web Services, is the world's most comprehensive and broadly adopted cloud platform. It's a suite of cloud computing services that offer a wide range of capabilities, from compute and storage to databases, analytics, networking, and more"
}
```


2) Continued Pre-training (Domain Adaptation fine-tuning)
- Provide **unlabeled data** to continue the training of an FM
- To make a model expert in a specific domain
- Good to feed industry-specific terminology into a model (acronyms, etc...)
- For example: Feeding the entire AWS documentation to a model to make it an expert on AWS
```
{
    "input": "You can use AWS for storage, backup, hosting websites, running gaming servers, developing mobile and web applications, and managing big data. It's also used for tasks like deploying virtual machines, creating serverless applications, and building and scaling AI/ML models."
}
```

3) Single-Turn Messaging
- Part of instruction-based fine-tuning
- `system` (optional): context for the conversation
- `messages`: An array of message
- `role`: Either user or assistant
- `content`: The text content of the message
- Example:
```
{
    "system": "You are a helpful assistant",
    "messages": [
        {
            "role": "user",
            "content": "What is AWS"
        },
        {
            "role": "assistant",
            "content": "it's Amazon Web Services"
        }
    ]
}
```

4) Multi-Turn Messaging
- To provide instruction-based fine tuning for a conversation (vs Single-Turn Messaging)
- Chatbots = multi-turn environment
- You must alternate between `user` and `assistant` roles

```
{
    "system": "You are an AI assistant specializing in AWS Services",
    "messages": [
        { "role": "user" "content": "Tell me about Amazon SageMaker" },
        { "role": "assistant" "content": "Amazon SageMaker is a fully managed service..." },
        { "role": "user" "content": "How does it integrate with other AWS Services?" },
        { "role": "assistant" "content": "It integrates with AWS Services like S3 for data storage, lambda for event-driven computing, and CloudWatch for monitoring" }
    ]

}
```

### Summary
- Re-training an FM requires a higher budget
- Instruction-based fine-tuning is usually cheaper as computations are less intense and the amount of data required usually less
- It also requies experienced ML engineers to perform the task
- You must prepare the data, do the fine-tuning, evaluate the model. 


### Transfer Learning 
- the broader concept of reusing a pre-trained model to adapt it to a new related task
    - Widely used foer image classification
    - and for NLP (models like BERT and GPT)
- Can appear in the exam as a general ML Concept

### Use Cases of Fine-Tuning
- A charbot designed with particular persona or tone, or geared towards a specific purpose (e.g. assisting customers, crafting advertisements)
- Traning using more up-to-date information than what the language model previously accessed. 
- Training with exclusive data (e.g. your historical emails or messages records from customer service interactions)