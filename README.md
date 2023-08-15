# Applied-Deep-Learning-Final-Project

## Summary of Chosen Paper
Paper: ColBERT: Using BERT Sentence Embedding in Parallel Neural Networks for Computational Humor
Link to Paper: [https://arxiv.org/pdf/2004.12765v7.pdf]

In the chosen paper, a approach for detecting humor in short texts is developed. Humor can be attained through different semantic mechanisms like wordplay, exaggeration, misunderstanding, etc. This make is difficult to detect if a sentence is humor in a neural network. The approach in the paper separates the text into sentences, then uses the BERT model to encode each sentence into embeddings. The embeddings are then fed into parallel hidden layers of a neural network to extract different latent features in each sentence. The last layers of the neural network then combines all the lines from the hidden layers to determine the relationshp between the sentences to predict the final output, which is if the sentence is indeed humor or not. 




## Implementation Details

## Comparison of Results
