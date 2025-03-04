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

- [ ] Implement context caching in all Koala prompts.
- [ ] Read [the papers presented in the page about data generation](https://www.promptingguide.ai/applications/generating_textbooks). Use GPT to summarize if needed.
```
To tackle the diversity issue, the authors prepared a vocabulary of around 1500 basic words, mirroring a typical child's vocabulary, divided into nouns, verbs, and adjectives. In each generation, one verb, one noun, and one adjective were randomly selected. The model then generates a story integrating these random words.
```

```
Write a short story (3-5 paragraphs) which only uses very simple words that a 3 year old child would likely understand. The story should use the verb ”{random.choice(verbs_list)}”, the noun ”{random.choice(nouns_list)}” and the adjective ”{random.choice(adjectives_list)}”. The story should have the following features: {random.choice(features_list)}, {random.choice(features_list)}. Remember to only use simple words!
```
- [x] Try this for sentence generation :point_up:

```
주제: {주제 입력}

말투: {말투 입력} (예: 격식체, 비격식체, 구어체, 문어체 등)

위의 주제에 대해 {말투}로 한 단락의 짧은 글을 작성해주세요. 이 글은 한국어 학습자를 위한 읽기 자료입니다.
```
```
{
    "환경 보전": "격식체",
    "인공지능": "비격식체",
    "우정": "구어체",
    "우주 탐사": "문어체",
    "건강한 식습관": "일상체",
    "문화적 다양성": "격식체",
    "교육에서의 기술": "비격식체",
    "기후 변화": "과학체",
    "해외 여행": "비격식체",
    "독서의 중요성": "문어체",
    "운동과 체력": "일상체",
    "사이버 보안": "격식체",
    "마음챙김과 명상": "비격식체",
    "소셜 미디어의 영향": "구어체",
    "예술의 역사": "문어체",
    "자원 봉사": "격식체",
    "디지털 노마드 라이프스타일": "일상체",
    "재무 지식": "비격식체",
    "리더십 기술": "격식체",
    "도시화": "과학체"
}
```
[[Experimental prompt output]]
