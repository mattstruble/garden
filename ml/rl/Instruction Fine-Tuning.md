A prerequisite to [[RLHF]] (and other training pipelines), and the simplest method for adapting language models, where models are taught the question-answer format used in the majority of modeling interactions, instead of next-token prediction. Without it the model would not be able to follow basic instructions.

Compared to pretraining IFT uses smaller batch sizes, on a narrower data distribution, to maintain the pretraining generalization. It also uses the same autoregressive loss function, but with different masking policies. Prompt tokens are masked using [[Prompt Masking]] , or [[Multi-Turn Masking]] so the model isn't learning to predict user queries, just the responses. 

Best practices:
- High quality data has a high influence on performance, since the completions are what the prompt learns from 
- Only need around 1M prompts to create a model capable of [[Post-Training]] and [[RLHF]], anything more than that has diminishing returns 
- Best prompts are similar to what the downstream tasks will be 
- The overall optimization is more important than fixating on each individual stage of the process, models are capable of recovering from noise in IFT in later stages of training. 