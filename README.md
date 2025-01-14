# Applied Machine Learning

This is a team-based final project for the course COMSW 4995 Applied Machine Learning during Fall 2024 in Columbia University.

In educational settings, students often harbor certain misconceptions that lead them to choose incorrect answers and hinder the learning process. Identifying these underlying misconceptions is crucial for teachers, as it allows for more targeted instruction and intervention, ultimately improving educational outcomes. To this end, Diagnostic Questions
have been introduced as an effective tool. A Diagnostic Question is a multiple-choice question with four options: one correct answer and three distractors (incorrect answers) - each specifically crafted to capture a specific misconception.

However, manually tagging distractors with appropriate misconceptions is both time-consuming and prone to inconsistency among different human annotators. This inconsistency can undermine the accuracy and utility of the diagnostic process.

In this project, we propose to design an automatic distractor labeling system leveraging the reasoning ability of Large Language Models (LLMs) to improve the understanding and management of misconceptions, enhancing the educational experience for teachers and students.

Final report file lists more details about data manipulation, exploration, as well as model structure and techniques used, feel free to take a look.

## File List

### Data:
This folder contains the original data files from the Kaggle project: https://www.kaggle.com/competitions/eedi-mining-misconceptions-in-mathematics/data
1. misconception_mapping.csv: MisconceptionName corresponding with 	      MisconceptionId in the train.csv
2. train.csv: train data
3. test.csv: test data
4. sample_submission.csv: a submission file in the correct format

### Data Exploration:
AML_Data_Explore.ipynb: Exploratory data analysis and visualization for the train dataset, more specifically for the question constructor, question subject, and answer misconceptions in the train.csv


### Data Cleaning:
1. AML_Data_Cleanup.ipynb: deal with the missing value & data imbalance
2. preprocessed.csv: contains the preprocessed data


### Model:
1. train_query.csv: train query we constructed
2. eedi-embedding.ipynb: get embedding for training dataset
3. train_query_embedding.npy: embedding file for train_query
4. misconception_embedding.npy: embedding file for misconception
5. train.ipynb: code for sampling hard examples and training embedding projector
6. inference_v1.ipynb: code for embedding distractor/query with Mistral-7B and retrieving top 25 directly with embedding
7. inference_v2.ipynb: code for embedding distractor/query with Mistral-7B, and post-retrieval selection with Qwen-Instruct-32B 


### Proposal & File report:
AML_Project_Proposal.pdf
AML_Final_Report.pdf
