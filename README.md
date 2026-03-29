# IMDB-Sentiment2
This project focuses on binary sentiment classification in which we are trying to determine whether a given review is positive or negative. The goal of the project is to also compare models and evaluates their performances sing accuracy, precision recall confusion matrix and F1 score. Workflow:
1.	importing Libraries: we start by importing Libraries that are important for data manipulation text preprocessing machine learning visualization and deep learning
2.	Loading Dataset: the CSV file is loaded into the Data frame while converting the sentiment labels into numerical ones in which positive == 1 and negative == 0
3.	EDA we perform basic analysis to understand the dataset structure such as checking the shape and type of the data as well as missing values and duplicated rows
4.	Text preprocessing: we clean the review text before extracting and deep learning training steps that can include decoding HTML entities, converting text to lower case, removing extra spaces, keeping only useful content
5.	Vader and TextBlob: for the baseline model sentence-level polarity features are extracted. Features that convert each review into a small numerical vector representing sentiment intensity
6.	Train/ validation / test Split: we split the data set into 60% training 20% validation and 20% test
7.	Feature Scaling: the scaler used fit only on the training data and we applied it to the training validation and test sets to ensures proper normalization
8.	Architecture:
•	MLP: use of fully connected neural network along with hidden layers. The activation used ReLu and the output is in form of sigmoid
•	LSTM:  use Embedding layer, LSTM layer, dense layer dropout and output layer 
•	GRU: use of embedding layer, GRU layer, dense layer, dropout and  output layer
•	1D CNN: use of embedding layer Conv1D layer, GlobalMaxPooling1D, Dropout and output layer
9.	Techniques Applied:
•	Text Preprocessing: revolves around padding sequences for length. Vocabulary limitation and tokenization
•	Optimization techniques: use of Adam optimizer. Early stopping to prevent overfitting, and learning rate reduction (ReduceLRQnPlateau)
•	Regularization: revolves around dropout layers to reduce overfitting and validation split in training
•	 Hyperparameter Turing: experiments using dropout rates batch sizes number of epochs and number of units 
•	Evaluation Metrics: deals with accuracy, F1 score and Model comparison
10.	Results  and discussion 
•	Accuracy: we can see that the accuracy od MLP is 0.78, while that of LSTM  being 0.86, that of GRU being 0.66 and that of 1D CNN being 0.89.
•	F1 score:  MLP F1 score is 0.78, LSTM  0.86 that of GRU is 0.72 while that of 1D CNN is 0.89
•	Discussion: The results shows that the 1S CNN model achieves the best results, meaning the best performance while LSTM also performs well. However the GRU model underperforms suggesting that further turning may be a necessity 
