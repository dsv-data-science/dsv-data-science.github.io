---
title: AutoGrade
status: inactive
highlight: low
description: |
  Automatic grading of electronic exams<br>
  <b>Internal pilot project: 2021-2022</b>

people:
  - Papapetrou
  - Lee

layout: project
last-updated: 2022-10-25
---

## AutoGrade


**Project team**:
- Panagiotis Papapetrou, Professor, DSV, SU
- Uno Fors, Professor, DSV, SU
- Ioannis Pavlopoulos, Affiliated Researcher, DSV, SU (2021)
- Zed Lee, PhD student, DSV, SU
- Maximilian Törnqvist, Research Assistant, DSV, SU (2022)
- Mosleh Mahamud, Research Assistant, DSV, SU (2022)
- Alexandra Farazouli, Research Assistant, DSV, SU (2021)
- Jimmy Ljungman, Research Assistant, DSV, SU (2021)
- Vanessa Lislevand, Research Assistant, DSV, SU (2021)

**Project period:** 2021-03-01 to 2022-12-31

**Funding source:** DSV internal project

**Budget:** 1.5M SEK


<br>

### Description

The project is about automatic grading and assessment of electonic exams. The goal is to explore algorithmic solutions from natural language processing (NLP) and predictive modeling for automating grading of free text exam questions. Special focus will be given on explainability and more concretely on highlighting parts of the exam text that contribute positively or negatively to the assessment. Our models will be built and assessed on both English and Swedish exam papers.

- **Objective 1: Language models for assessment of free-text questions.** We will develop transformer-based solutions (e.g., BERT) for distinghuishing high-scorer vs low-scorer answers. This will then be expanded to more fine-grained grade ranges, and eventually to the regression problem of predicting the actual grade.

- **Objective 2: Topic-specific language models for exam assessment.** We will further extend these models from free-text and question-specific to exam-based and topic-specific, and eventually explore their transferability across different exams. Our intended final framework will be an ensemble of question-based models for each topic. Finally, we will include the question text into the model as well as additional student perfomance indicators including the performance on homework assignments or earlier exam questions.

- **Objective 3: Ethics and explainability of automated exam assessment.** With the intention of being GDPR compliant we will include explainability features in our models so that each grade recommendation will be coupled with an explanation indicating the parts of the text in the answer that are positively or negatively contributing affecting the grade decision. A final assessment report will be generated based on the overall score and performance in the exam functioning as general feedback.

{% comment %}
<br>

### Implementation

<br>

### Results
{% endcomment %}