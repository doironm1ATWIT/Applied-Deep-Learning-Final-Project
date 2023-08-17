# Applied-Deep-Learning-Final-Project

## Summary of Chosen Paper
Paper: ColBERT: Using BERT Sentence Embedding in Parallel Neural Networks for Computational Humor

Link to Paper: [https://arxiv.org/pdf/2004.12765v7.pdf]

In the chosen paper, a approach for detecting humor in short texts is developed. Humor can be attained through different semantic mechanisms like wordplay, exaggeration, misunderstanding, etc. This make is difficult to detect if a sentence is humor in a neural network. The approach in the paper separates the text into sentences, then uses the BERT model to encode each sentence into embeddings. The embeddings are then fed into parallel hidden layers of a neural network to extract different latent features in each sentence. The last layers of the neural network then combines all the lines from the hidden layers to determine the relationshp between the sentences to predict the final output, which is if the sentence is indeed humor or not. 


The proposed methods obtained an accuracy score of 0.982 has outperformed supervised machine learning algorithms. Based on the results, the researchers identified two important factors in achieving high accuracy in the task which are the usage of sentence embeddings, and utilizing the linguistic structure of humor in designing the proposed model. 

Limitations of the papers are:
The researchers discovered in their dataset that there were some new headlines that were classified as humorous. They believe that human annotation on the dataset that they created could be beneficial in future work. 

### Model Results from the Paper:

<img width="526" alt="Screenshot 2023-08-15 at 6 39 14 PM" src="https://github.com/doironm1ATWIT/Applied-Deep-Learning-Final-Project/assets/59668854/e5fd09ea-8991-4085-9b29-4d28b80ed34a">




## Implementation Details

The paper's implementation:
1. There were 20,000 samples in their study. 
1. Each sentence was assessed separately and numerical features were extracted and tokenized individually.
2. Then the sentences were encoded using BERT sentence embeddings. An embedding was created for each sentence.
3. After obtaining the BERT sentence embeddings, the sentence embeddings were fed into a neural network that consisted of parallel hidden layers. 
4. The text as a whole is also looked at. The BERT sentence embedding is then used for the whole text, not just sentence level, and were fed into the hidden layers of the Neural Network. The output is a vector of size 60.
5. In the end, there are three sequential layers that make the model. The final layers combine the output of all the previous paths of hidden layers to predict the final output.



My implentation:
In my implementation, I used a similar approach. A sample size of 5000 due to limited RAM and GPU in Google Collab.

1. The text data from the humor dataset was tokenized at sentence level similar to the paper's implementation of this. 
2. The BERT embeddings model was utilized as well to create the embeddings that will be utlilized in the parallel lines portion of the model.
3. To create the parallel lines portion of the neural network, a dense layer was created for each of the sentences, and then all the layers were then concatenated.
4. A sequential model was defined for the final layers of the neural network. The concatenated layer is passed through the sequential layers, which creates the final model for the output.




## Comparison of Results and Conclusions

|                              | Train Size  | Accuracy Score |
| ---------------------------- | ----------- | -------------- |
| My Results                   |  1,000      |  0.4767        |
| Papers Results               |  20,000     |  0.9820        |

Due to the neural network being computationally expensive, my implementation was limited to the sample size that could affectively run the model. It was very computationaly expensive due to running through each sentence, and creating a embedding for each sentence, and then concatenating those layers. This is a significantly smaller sample than what was used in the model from the paper, so this does explain that why the accuracy scores differ significantly. My implementation has some future work that could be done, like implementing the whole text portion of the neural network that the paper utilized. This could benefit the accuracy score of my implementation. In the future, when working with a neural network model it is definitely more beneficial to work on a virtual machine to run the models. 

