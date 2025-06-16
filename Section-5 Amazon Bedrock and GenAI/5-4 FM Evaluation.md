### FM Evaluation
- Choosing a model sometimes you need to use evaluation
- Evaluate a model for quality control
- Bring your own prompt datase ot use built-in curated prompt datasets
- Scores are calculated automatically 

#### How it Works
1) User will provide Benchmark Questions and Benchmark Answers (Answers you think for the benchmark questions)
2) Model will evaluate
3) Model will provide generated answers
4) There will be a Judge Model that will provide a Grading Score

#### Benchmark Datasets
- Curated collections of data designed specifically at evaluating the performance of language models
- Some benchmarks datasets allow you to very quickly any kind of bias and potential discrimination against a group of people. 

### Automate Metrics to Evaluate an FM
- ROUGE (Recall-Oriented Understudy for Gisting Evaluation) 
    - evaluating automatic summarizations and machin translation systems
    - ROUGE-N - mesaure the number of matching n-grams between reference and generated text
    - ROUGE-L - longest common subsequence between reference and generated text

- BLEU (Bilingual Evaluation Understudy)
    - Evaludate the quality of generated text, specially for translations

- BERTScore (Bidirectional Encoder Represneations from Transformers)
    - Semantic similarity between generated text
    - Uses a pre-train BERT Models 

- Perplexity
    - How well the model predicts the next token (lower is better)

### Business Metrics to Evaluate a Model On
- User Satisfaction - gather uer's feedbacks and assess their satisfaction with the model respones
- Average Revenue Per User (ARPU) - average revenue per user attributed to Gen-AI app
- Cross-Domain Performance - measure the model's ability to perform cross different domains tasks
- Conversion Rate - Generate recommended desired outomes such as purchases
- Efficiency - evaluate the model's efficiency in computation, resource utilization
