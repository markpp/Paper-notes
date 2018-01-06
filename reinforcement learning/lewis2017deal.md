# Deal or no deal? end-to-end learning for negotiation dialogues
[arXiv](https://arxiv.org/abs/1706.05125)
[github](https://github.com/facebookresearch/end-to-end-negotiator)
### Implementation

### What
- Learning to negotiate the division of items, where each agent values the items to various degrees
- First they teach an agent to imitate human-human negotiation using supervised training of recurrent network on a dataset of human negotiations
- Then they fine-tuned the model using self-play and reinforcement learning. In effect the supervised learning produced a mapping between language and meaning and reinforcement learning help determine when to say what
- The agent learned to show fake interest in certain aspects of a deal, only to give up on them later and benefit from its real goals
- When the parameters of both agents where allowed to be updated, the communication diverged from human language. This led to alarmed news stories.
- The language was kept human-like by keeping one of the models fixed.

### How
- Each agent has his own goal in the negotiations that the other does not know about. It’s impossible to leave the negotiations without a deal
- The models were trained end-to-end
- The model was prevented from developing a new language and trained to use human like language

### Experiments
- Tested in online conversations with people, of which many didn't notice that they were talking to a robotic
