A prerequisite to [[RLHF]] where models are taught the question-answer format used in the majority of modeling interactions.

Teaches the model to respond to an instruction-response format rather than just continuing text. 

Simplest method for adapting language models to a desired task distribution. 

Most pipelines (like [[RLHF]]) cannot perform without the basic level of instruction-following abilities that IFT imparts on the model. 

Uses smaller batch sizes than pre-training to optimize on narrow data distributions while maintaining the pre-training generalization. 

Prompt tokens are masked using [[Prompt Masking]] so the model isn't learning to predict user queries, just the responses. 

Uses the same autoregressive loss function used in pretraining, but with different data and masking. 

Best practices:
- High quality data has a high influence on performance, since the completions are what the prompt learns from 
- Only need around 1M prompts to create a model capable of [[Post-Training]] and [[RLHF]], anything more than that has diminishing returns 
- Best prompts are similar to what the downstream tasks will be 
- The overall optimization is more important than fixating on each individual stage of the process, models are capable of recovering from noise in IFT in later stages of training. 