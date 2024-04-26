# Aware NLP Project Group 1
## Erdos Institute Data Science Bootcamp, April 2024

### Project team: Yangxiao Lue, Ness Mayker Chen, Merve Keskin

### Introduction

**Motivation and Goal**

AI systems that generate responses use the most relevant data available to them. Nevertheless, there is a possibility of hallucinations leading to inaccurate outcomes. Hence, it is crucial to develop systems capable of delivering answers that are relevant to the context. Where is the source of this relevant data within the system? How well does it fit into the specific context?

Our objective for this project is to create a fast delivery system that incorporates external contextual reference data. The system needs to have the ability to efficiently search and rank millions of texts in response to user queries. The system also incorporates mechanisms for evaluating the qualitative performance of the retrieval outputs.

**Data Organisation**

Challenge: accurately match the comments with submissions to create queries and answers.

Our work analyzes a vast public dataset comprising 5 million Reddit submissions and comments across 21 subreddits. The dataset consists of written submissions and corresponding comments. In order to establish a dependable connection between our questions and answers in the data, we eliminated all submissions that lacked comments. Then, we reorganized our data into a new format where each submission is stored in one row, and the corresponding comments are stored in a single column as vectorized data. This led us to create a submission-based data frame comprising 20613 observations.

**Model and Evaluation**

We use pre-trained sentence embedding for our retrieval. We combined the title, text, and subreddit category of each submission into one string. We used embeddings to transform the string into an encoded format. We went through this process for every submission to generate a vector database.

Then, we applied the KNN model to identify the most similar submissions to a particular one. We used `all-miniLM-L6-v2’ to return the most relevant comments to a query. 

We used Ragas to assess our LLM. Ragas considers both the retrieval and generation aspects of the model, including context recall, context relevancy, faithfulness, and answer relevancy. 

By utilizing Ragas, we generated ground truths by analyzing the most frequently uploaded comments for each submission. We then compared the relevance of answers between the outcomes produced by our Ilama 3-8B models with no contexts and those with contexts provided by our RAG system. According to the model comparison, our RAG system demonstrates better performance in answer relevancy compared to a large language model without context.

### Outline of Computational Pipeline

1. Using a pre-trained model to create sentence embeddings.
2. Model - Train a KNN model using the embeddings as inputs.
3. Evaluation - Evaluate model retrieval and generation with Ragas.

Notebook for NLP analysis: https://github.com/
