
Begins by defining a pattern to format user queries so that they are readable by a language model via its tokenizer. Tokens are wrapped with `<|im_start|>...<|im_end|>` for a model's output it looks for `<|im_start> assistant` and generates tokens until it creates its end of sequence token;  `<|im_end|>` . General models have tags like `system` for the initial system prompt and `user` for the user messages. 

Modern model providers use a hierarchical system where a user can configure their own system message, while still having higher-level instructions that may not be revealed to a user. 