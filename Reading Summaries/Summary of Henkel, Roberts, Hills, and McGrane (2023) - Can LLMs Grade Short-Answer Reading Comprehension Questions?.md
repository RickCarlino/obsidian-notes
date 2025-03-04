**Note:** This is an LLM-generated summary of the  [original paper](https://arxiv.org/pdf/2310.18373). I find this research particularly interesting for spaced repetition system development.

**Authors:** Owen Henkel, Bill Roberts, Libby Hills, Joshua McGrane

**Published:** October 2023

**Abstract:**
Grading open-ended questions, like short answers, can be time-consuming and prone to errors. Teachers often avoid using them even though they give better insights into students' understanding. The newest generation of Large Language Models (LLMs) might help automate this grading process, making it easier and more accurate. This study looks at whether LLMs can grade short-answer reading comprehension questions effectively. It introduces a new dataset from students in Ghana and evaluates how well various LLMs, including GPT-4, can grade these responses compared to human experts.

### Introduction

LLMs have many potential uses in education, especially for grading student work in formative assessments, which help track student progress. While multiple-choice questions are easy to grade, they don't always reflect a student's understanding. Short-answer questions are better but harder to grade consistently. Previous automatic grading models were complex and not widely used. Recent LLMs, like GPT-4, are more user-friendly and might make grading short-answer questions more feasible.

### Prior Work

Automatic short answer grading (ASAG) has been researched for over a decade. Early models were complex and required lots of specific data. Transfer learning, where a model trained on one task is adapted for another, improved performance but still had limitations, like needing technical expertise and large labeled datasets. These models also struggled to generalize across different tasks.

The newest LLMs, such as GPT-4, have shown promise in various tasks with minimal training data. They can understand and generate text based on prompts, making them potentially useful for grading. However, there are concerns about their reliability and biases.

### The Study

**Dataset:** The study introduces the University of Oxford & Rising Academies Ghanaian Student Reading Comprehension Short Answer Dataset. It includes reading comprehension questions and answers from 130 students in Ghana. The dataset was used to evaluate how well GPT-4 and other LLMs can grade student responses.

**Methodology:** The models were tested with different prompting strategies to see how well they could classify student answers as correct, partially correct, or incorrect. The results were compared to grades given by human experts.

### Results

GPT-4 performed very well, reaching near-parity with human raters. In some cases, it even matched or exceeded human agreement levels. The study found that GPT-4 could grade short-answer questions accurately with minimal prompt engineering.

### Discussion

These findings suggest that LLMs like GPT-4 could be used for grading in real-world educational settings, providing reliable and consistent feedback on student performance. This could be particularly beneficial in lower-resourced schools or regions.

### Conclusion

The study demonstrates the potential of LLMs for automated grading of short-answer questions. GPT-4 performed exceptionally well, suggesting that such models could support more effective formative assessments in education.
