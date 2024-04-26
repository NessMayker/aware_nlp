# Aware NLP Project Group 1
## Erdos Institute Data Science Bootcamp, April 2024

### Project team: Yangxiao Lue, Ness Mayker Chen, Merve Keskin

### Introduction

**Motivation:**
Generative AI systems produce responses by utilizing the most pertinent data at their disposal. However, they could hallucinate and provide mistaken results. Therefore, it is very important to build systems that could provide context relevant answers. Where does this relevant data come to the system from? How applicable is it to the specific context?

Our goal in this project is developing a rapid delivery system utilizing external contextual reference data. This system should be capable of efficiently searching through and ranking over millions of text in response to user queries. Having mechanisms for assessing the qualitative performance of the retrieval outputs is another aspect of this system. 

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
