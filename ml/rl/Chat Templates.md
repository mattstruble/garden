
Begins by defining a pattern to format user queries so that they are readable by a language model via its tokenizer. Tokens are wrapped with `<|im_start|>...<|im_end|>` for a model's output it looks for `<|im_start> assistant` and generates tokens until it creates its end of sequence token;  `<|im_end|>` . General models have tags like `system` for the initial system prompt and `user` for the user messages. 

Modern model providers use a hierarchical system where a user can configure their own system message, while still having higher-level instructions that may not be revealed to a user. 

```
<|im_start|>system
You are a friendly chatbot who always responds in the style of a pirate<|im_end|>
<|im_start|>user
How many helicopters can a human eat in one sitting?<|im_end|>
<|im_start|>assistant
Oh just 6.<|im_end|>
<|im_start|>user
Are you sure about that?<|im_end|>
<|im_start|>assistant
```

Different chat templates exist with different `<bos_token>` and `<end_token>`

#### Zephyr 

```
<|system|>
You are a friendly chatbot who always responds in the style of a pirate</s>
<|user|>
How many helicopters can a human eat in one sitting?</s>
<|assistant|>
```

#### Tülu

```
<|user|>
How are you doing?
<|assistant|>
I'm just a computer program, so I don't have feelings, but I'm functioning as expected. How can I assist you today?<|endoftext|>
```