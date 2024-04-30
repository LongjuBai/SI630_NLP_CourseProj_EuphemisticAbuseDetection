# SI630_NLP_CourseProj_EuphemisticAbuseDetection
This is the repo for SI630 NLP course project, focusing on Euphemistic Abuse Detection. we compared two approaches to solving this task:
* Supervisied training using RoBERTa with both the original training data and the augmented data using different models (flan-t5-large, flan-t5-xxl, gpt4)
* Few shot in-context learning with chain of thought method using different models (flan-t5-large, flan-t5-xxl, gpt4, llama3)

All the prompt files and the scripts have been uploaded in this repo

## Abstract
This project addresses the challenge of identifying euphemistic abuse in online communications. This research explores how hidden abusive meanings can be more accurately detected by utilizing Large Language Models (LLMs) and a novel approach that combines data augmentation with the Chain of Thoughts (CoT) method. A comparative study across various models, including few-shot techniques with GPT4, highlights the CoT method's superior performance, suggesting a pivotal role for LLMs in advancing abuse detection. The project has demonstrated the potential of leveraging in-context learning and reasoning abilities of LLMs for complex NLP tasks. This approach demonstrates not only State-Of-The-Art results in euphemistic detection task but also a promising direction for future research and practical applications in content moderation and online safety. Code and datasets from this study are made available for community use and further investigation.

## Results:

| **Classifier**                | **Precision** | **Recall** | **F1-Score** |
|-------------------------------|---------------|------------|--------------|
|                               |               |            |              |
| **Baseline Classifiers**      |               |            |              |
| Random Performance            | 35.6%         | 35.6%      | 35.6%        |
| Majority-Class                | 32.2%         | 50.0%      | 39.2%        |
| Original Train Set            | 58.1%         | 50.4%      | 54.0%        |
| GPT3 data_aug                 | 73.7%         | 69.1%      | 71.3%        |
|                               |               |            |              |
| **Experimental Classifiers - Data Augmentation** |  |    |              |
| flan-t5-large data_aug        | 58.9%         | 44.1%      | 50.5%        |
| flan-t5-xxl data_aug          | 63.7%         | 56.7%      | 60.0%        |
| GPT4 data_aug                 | 61.4%         | 74.0%      | 67.1%        |
|                               |               |            |              |
| **Experimental Classifiers - CoT Few-Shot** |     |       |              |
| CoT&flan-t5-large             | 63.6%         | 62.8%      | 61.6%        |
| CoT&flan-t5-xxl               | 74.4%         | 70.7%      | 71.8%        |
| CoT&LlaMa3                    | 78.3%         | 74.7%      | 75.5%        |
| CoT&GPT4                      | 83.7%         | 83.6%      | 83.6%        |
