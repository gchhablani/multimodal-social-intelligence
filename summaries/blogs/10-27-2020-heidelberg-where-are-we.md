---
url: https://nlpblog.cl.uni-heidelberg.de/index.php/2020/10/27/multimodal-commonsense-reasoning/
title: (Multimodal) Commonsense Reasoning- Where are we and where could we go?
author: Ines Pisetta
date: 10-27-2020
---

## What is Commonsense Reasoning?
- Commonsense Reasoning requires a machine to reason based on 'knowledge about the everyday world'.

- To perform Commonsense Reasoning, one has to consider facts about time, space, physics, biology, psychology, social interactions and many more.

## How to test for commonsense?
### Winograd Schema Challenge
- Alternative to Turing test.
- A sentence and a binary question with two possible answers.
- Each schema has two parties, a pronoun or possesive which can refer to either parties.

- Example:
```
The trophy doesn’t fit in the brown suitcase because it’s too big.
What is too big?
Answer 0: the trophy
Answer 1: the suitcase
```
- `Special word` that appears in sentence/question. If replaced with `alternative word`, the answer to the question changes. In example - `big` to `small`, answer changes from `trophy` to `suitcase`.

- **Systems that have succeeded on WSC273, didn’t show the ability to solve other Natural Language Understanding tasks like Commonsense Reasoning**

### Other Benchmarks
- [**ConceptNet**](https://www.media.mit.edu/publications/bttj/Paper23Pages211-226.pdf): A wide range of commonsense concepts and their relations.
![ConceptNet Image](./images/conceptnet-768x525.jpg)

- [**Story Cloze Test/ROC Stories**](https://www.aclweb.org/anthology/N16-1098.pdf): System has to choose between a right and a wrong ending to four-sentence stories.

- [**SWAG**](https://www.aclweb.org/anthology/D18-1009.pdf): A MCQA dataset from video captions with the aim of predicting new dataset (*using a new method to construct a non-biased dataset - Adversarial Filtering**) [TBD]

- [**CommonsenseQA**](https://www.aclweb.org/anthology/N19-1421.pdf): Answer questions based on a specific source concept and choose from five possible answers.

- [**DROP**](https://www.aclweb.org/anthology/N19-1246.pdf): Dicrete Reasoning Over Paragraphs - Reading Comprehension where a system has to reason using subtraction, comparision, coreference resolutoin, count, sort, addition, arithmetics, etc.

- [**CoS-E**](https://www.aclweb.org/anthology/P19-1487.pdf): Provided with a question, three choices and an explanation from the Common Sense Explanations, a system has to generate valid explanations.

- [**CODAH**](https://www.aclweb.org/anthology/W19-2008.pdf) - includeS idioms, negation, polysemy, reference and quantitative reasoning.

- [**Event2Mind**](https://www.aclweb.org/anthology/P18-1043.pdf): Event to intents/reactions.

- [**Social IQA**](https://arxiv.org/pdf/1904.09728): Answer questions about social situations in a multiple choice setting.


## CR in Computer Vision and Multimodality

### VCR
- https://arxiv.org/pdf/1811.10830.pdf
- Based on SWAG paper.
- List of regions is provided.
- Two-step question answering
    - Choose right answer from multiple choices for a question.
    - And a reasonable rationale to justify its answer.
```
However, also retrieving the incorrect choice via crowd-sourcing was a) expensive and b) had the risk of annotation artifacts (subtle patterns injected unknowingly into the data by the workers).
Therefore, the authors made use of a technique called ‘Adversarial Matching’, where the incorrect answers or counterfactuals have to be as relevant as possible for the given query but at the same time not too similar to the correct response or rationale.
```


## Useful Links:
- MOSAIC Commonsense Benchmarks: https://mosaic.allenai.org/projects/mosaic-commonsense-benchmarks

- Sebastian Ruder's NLP Progress GitHub, Common Sense section: https://github.com/sebastianruder/NLP-progress/blob/master/english/common_sense.md