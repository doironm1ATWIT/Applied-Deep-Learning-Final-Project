# Applied-Deep-Learning-Final-Project

## Summary of Chosen Paper
Paper: ColBERT: Using BERT Sentence Embedding in Parallel Neural Networks for Computational Humor
Link to Paper: [https://arxiv.org/pdf/2004.12765v7.pdf]

In the chosen paper, a approach for detecting humor in short texts is developed. Humor can be attained through different semantic mechanisms like wordplay, exaggeration, misunderstanding, etc. This make is difficult to detect if a sentence is humor in a neural network. The approach in the paper separates the text into sentences, then uses the BERT model to encode each sentence into embeddings. The embeddings are then fed into parallel hidden layers of a neural network to extract different latent features in each sentence. The last layers of the neural network then combines all the lines from the hidden layers to determine the relationshp between the sentences to predict the final output, which is if the sentence is indeed humor or not. The researchers also expanded contractions, cleaned punctuations marks, and cleaned special characters in the dataset before implementing the model. 


The proposed methods obtained F1 Scores of 0.982 and 0.869 on two different settings and has outperformed state of the art models. Based on the results, the researchers identified two important factors in achieving high accuracy in the task which are the usage of sentence embeddings, and utilizing the linguistic structure of humor in designing the proposed model. 

Limitations of the papers are:
The researchers discovered in their dataset that there were some new headlines that were classified as humorous. They believe that human annotation on the dataset that they created could be beneficial in future work. 

### Model Results from the Paper:

<img width="526" alt="Screenshot 2023-08-15 at 6 39 14 PM" src="https://github.com/doironm1ATWIT/Applied-Deep-Learning-Final-Project/assets/59668854/e5fd09ea-8991-4085-9b29-4d28b80ed34a">




## Implementation Details

## Comparison of Results
