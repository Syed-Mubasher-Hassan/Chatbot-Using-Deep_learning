# Chatbot-Using-Deep_learning


1. Introduction

A topical chatbot is a specialized AI designed for conversations about a specific subject, providing accurate and helpful information within its domain. Unlike general chatbots, which have broad conversational abilities, topical chatbots focus on one topic, such as medicine or finance.

2. Objective

The primary objective of this project is to create a topical chatbot capable of understanding and engaging in conversations related to a specific subject matter. In this case, the chatbot is trained to understand and respond to conversations with various sentiments.

3. Methodology

3.1 Data Collection

The project utilizes a JSON dataset containing conversations with different sentiments. Each conversation consists of messages from two agents, and the sentiment associated with each message is used as the training label. The dataset is loaded and processed using Python.

3.2 Data Preprocessing

Training sentences and labels are extracted from the dataset.
Responses from "agent_2" are separated for further analysis.
Label encoding is performed to convert sentiment labels into numerical values.
Tokenization and padding are applied to the text data for input into a neural network.
3.3 Model Architecture

A sequential neural network model is constructed using TensorFlow and Keras. The architecture consists of the following layers:

Embedding layer with a vocabulary size of 40,000 and an embedding dimension of 200.
Three LSTM layers with varying numbers of units and dropout layers to prevent overfitting.
Dense layers for classification, with the final layer having eight output units representing the sentiment classes.
The model is compiled with the sparse categorical cross-entropy loss function and the Adam optimizer.

4. Results

The training history of the model is as follows:

Epochs: 10
Training Accuracy: 86.57%
Validation Accuracy: 41.58%
Test Accuracy: 42.50%


5. Discussion

The chatbot model shows strong performance on the training data, achieving an accuracy of 86.57%. However, the validation and test accuracies are significantly lower, indicating potential overfitting. Further investigation is required to address this issue, which may involve adjusting the model architecture or training parameters.

6. Conclusion

In conclusion, this project aimed to create a topical chatbot capable of understanding and responding to conversations with different sentiments. While the model achieved high accuracy on the training data, it displayed lower performance on the validation and test sets. Future work should focus on improving the generalization of the model and potentially exploring more advanced architectures.

7. Future Work

Experiment with different neural network architectures to improve generalization.
Explore techniques such as transfer learning or pre-trained embeddings to enhance the model's performance.
Collect and incorporate more data to further train and evaluate the chatbot.
