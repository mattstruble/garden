Reinforcement Learning Human Feedback 

A general method to integrate stylistic and behavioral features into the models. Lead to modern LLM post-training, and was the technique used to enable the release of ChatGPT. Tends to generalize better across domains than [[IFT - SFT]]. RL on languages models is considered to be robust, scalable, effective, and flexible, which allows for lots of experimentation.

Consider how you interact with an LLM,  RLHF determines how the style applies to your interaction. Style being things like tone or format of the information and how it's presented. In other words, RLHF tries to map the complexities of human values and objectives into a systematic approach.

Basic premise is that RL is given a signal of which actions are good, in the form of tokens that a LM generates, and then derives update rules that are attributed to different actions/parameters within the model. In RLHF a learned model of human preferences is used instead of an environmental reward function. Also, the attribution of a reward is done for an entire sequence of actions (rollout, episode, etc), instead of a fine-grained reward. So, RLHF is inspired by RL optimizers, but is very distinct from traditional RL.

Uses [[Contrasive Loss]]  to hand-tune LLM completions based on the response level, instead of looking at the next token specifically. Additionally tells the model what a better response _looks like_ rather than what a specific response _should be_. This can also be used to show the model what type of responses it should avoid via negative feedback. This act of optimizing over a simple loss function involves training multiple language models in sequence and then linking them together. Need to be careful with the optimization though to avoid drifting away from the base model, and should instead be considered as fixing the "rough edges" of the base model to make it easier to chat with.

