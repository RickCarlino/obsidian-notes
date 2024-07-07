Many types of language learning software, such as spaced repetition or quiz apps, operate on the concept of providing a prompt to the user and then soliciting a response. Once the software has a response, it will do one of two things:

- Grade the response via simple string comparison (Readlang, Anki typing mode)
- Ask the user to grade the response by themselves (Anki, most SRS systems)

Self-grading is problematic because it is subjective and can easily be influenced by a number of factors such as the student's mood or gaps in the student's understanding of the target language.

Conversely, software packages that attempt to grade a user's response are often too inflexible to be useful. They will mark the response as incorrect if the spelling differs by one character. They will not accept an equivalent phrase, even if it is grammatically correct and equivalent to the requested prompt.

I've spent a lot of time thinking about this while building [Koala Cards](https://koala.cards), and I've found that off-the-shelf large language models can do a decent job of identifying equivalent phrases, but it is still not 100% accurate. As I collect more training data on my own use of koala cards, I will attempt to fine tune a model and also create a system for judging the accuracy of different prompts and models.

### Research / Experiments
 - [Phrase equivalence detection code in Koala Cards](https://github.com/RickCarlino/KoalaCards/blob/main/koala/quiz-evaluators/listening.ts)
