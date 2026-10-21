Reinforcement Learning Human Feedback 

A general method to integrate stylistic and behavioral features into the models. Lead to modern LLM post-training, and was the technique used to enable the release of ChatGPT. Tends to generalize better across domains than [[IFT - SFT]].

Consider how you interact with an LLM,  RLHF determines how the style applies to your interaction. Style being things like tone or format of the information and how it's presented. 

Uses [[Contrasive Loss]]  to hand-tune LLM completions based on the response level, instead of looking at the next token specifically. Additionally tells the model what a better response _looks like_ rather than what a specific response _should be_. This can also be used to show the model what type of responses it should avoid via negative feedback.