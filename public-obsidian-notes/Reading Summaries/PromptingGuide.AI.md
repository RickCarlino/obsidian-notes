Re-visiting PromptingGuide.AI since it had a bunch of updates since the last time I read it.

**Frequency Penalty** - Applies a penalty to frequently repeated tokens in the response and prompt, reducing the likelihood of repeated words by assigning higher penalties to tokens that appear more frequently.

**Presence Penalty** - Applies an equal penalty to all repeated tokens, regardless of frequency, which helps in generating more diverse responses by discouraging repeated phrases without regard to repetition count.

**Top P** - A sampling technique that limits responses to tokens within a probability threshold, with lower values favoring confident responses and higher values increasing diversity by including less likely options.

**Zero-shot prompting** - A technique where the model performs a task without examples, relying on general language knowledge to interpret and respond appropriately.

**Few-shot prompting** - Similar to zero-shot prompting, but includes examples to guide the model’s response style or format.

**Few-shot pro-tip** - Selecting random labels from a true distribution of labels (instead of a uniform distribution) also helps.

Interesting tidbit from [the part on CoT prompting](https://www.promptingguide.ai/techniques/cot):

> "...the authors claim that this is an emergent ability that arises with sufficiently large language models."

**Meta-prompting** - Similar to CoT prompting but the focus is on the structure of the prompt language rather than examples.

- [ ] Try building an example sentence generator with meta prompting.

**Prompt Chaining** - Common use of multi-step prompts. [Anthropic docs.](https://docs.anthropic.com/en/docs/build-with-claude/prompt-engineering/chain-prompts)

- [ ] Try a [tree of thought prompt](https://www.promptingguide.ai/techniques/tot). Docs were not deep enough.
- [ ] What is "Named entity recognition"?
- [ ] Find some real world uses of ReAct prompting
	- [ ] Look into AlfWorld ReAct examples

[Stopped here](https://www.promptingguide.ai/applications/finetuning-gpt4o)
