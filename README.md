# Aware NLP Project Group 1
## Erdos Institute Data Science Bootcamp, April 2024

### Project team: Yangxiao Lue, Ness Mayker Chen, Merve Keskin

### Introduction

**Motivation and Goal**
AI systems that generate responses use the most relevant data available to them. Nevertheless, there is a possibility of hallucinations leading to inaccurate outcomes. Hence, it is crucial to develop systems capable of delivering answers that are relevant to the context. Where is the source of this relevant data within the system? How well does it fit into the specific context?

Our objective for this project is to create a fast delivery system that incorporates external contextual reference data. The system needs to have the ability to efficiently search and rank millions of texts in response to user queries. The system also incorporates mechanisms for evaluating the qualitative performance of the retrieval outputs.

**Data Organisation**

Challenge: accurately match the comments with submissions to create queries and answers.

Our work involves analyzing a vast public dataset comprising 5 million Reddit submissions and comments across 21 subreddits. The dataset consists of written submissions and corresponding comments. In order to establish a dependable connection between our questions and answers in the data, we eliminated all submissions that lacked comments. Then, we reorganized our data into a new format where each submission is stored in one row, and the corresponding comments are stored in a single column as vectorized data. This led us to create a submission-based dataframe, consisting of 20613 observations.

**Model and Evaluation:**
We utilized Ragas to evaluate our LLM. Ragas takes into account both the retrieval and generation parts of the model, such as context recall, context relevancy, faithfulness, answer relevancy, using synthetic data based on the LLM.

### Outline of Computational Pipeline

1. 
2. Model - Train a KNN model using the embeddings as inputs.
3. Evaluation - Evaluate model retrieval and generation.

Notebook for NLP analysis: https://github.com/
