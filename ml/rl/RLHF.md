Reinforcement Learning Human Feedback 

A general method to integrate stylistic and behavioral features into the models. Lead to modern LLM post-training, and was the technique used to enable the release of ChatGPT. Tends to generalize better across domains than [[IFT - SFT]].

Consider how you interact with an LLM,  RLHF determines how the style applies to your interaction. Style being things like tone or format of the information and how it's presented. 

Uses [[Contrasive Loss]]  to hand-tune LLM completions based on the response level, instead of looking at the next token specifically. Additionally tells the model what a better response _looks like_ rather than what a specific response _should be_. This can also be used to show the model what type of responses it should avoid via negative feedback.

Basic premise is that RL is given a signal of which actions are good, in the form of tokens that a LM generates, and then derives update rules that are attributed to different actions/parameters within the model. Reinforcement Learning is given a signal of which actions are good, in the form of tokens that a language model generates, and derives

Tries to map the complexities of human values and objectives into a system. 

The act of optimizing a simple loss function in RLHF involves training multiple different LM models in sequence and then linking them together via online optimization. 

Unlike traditional RL, RLHF uses a learned model of human preferences instead of an environmental reward function. RLHF also the attribution of a reward is done for an entire sequence of actions (rollout, episode), instead of the traditional fine-grained manner. RLHF therefore can considered to be inspired by RL optimizers, but is very distinct from traditional RL. 

With RLHF starting from a pretrained base model a lot of the work is to prevent the optimization from drifting too far from the initial model policy. Can think of it as fixing the "rough edges" of a model and making it easier to chat with. 

RL on LM is robust, scalable, effective, and flexible, which allows for lots of experimentation.