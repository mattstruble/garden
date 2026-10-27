The initial method for post-training an LM around the time ChatGPT came out. 

1. **[[Instruction Fine-Tuning]] on 10k examples** Teaches the model to follow question-answer format
2. **Training reward model on ~100k prompts** Captures diverse values to model in their final training. This is the optimization target for [[RLHF]]
3. **Training instruction tuned model with [[RLHF]] on ~100k prompts** Model is optimized against the reward model. 
