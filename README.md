# Gender-Classification
The model predicts the gender of a person using a dataset containing  information about their tweets
1.Cleaning/EDA:
1.texts and vocab_length were cleaned by Tokenizers.
2.Unnecessary columns were dropped: _unit_id, name, profileimage, tweet_id


3.Unkown values were encoded and rows were dropped with missing target values
4.The column ‘label’ was encoded.
5.X was scaled with standard scalar

2.Independent and Dependent Feature:
Independent Feature: 

'_golden','_unit_state','_trusted_judgments','_last_judgment_at','gender:confidence', 'profile_yn', 'profile_yn:confidence', 'created', 'description', 'fav_number',
'link_color', 'name', 'profile image', 'retweet_count', 'sidebar_color', 'text', 'tweet_count', 'tweet_created', 'tweet_id', 'text_norm',  ‘description_norm'

Dependent Feature: Gender


3.Activation Function:

The Activation Function used here is ReLU[Rectified linear activation function] as hidden layers are used in this model.
It is piecewise linear function that will output the input directly if it is positive, otherwise, it will output zero.

The rectified linear activation function overcomes the vanishing gradient problem, allowing models to learn faster and perform better.
It does not activate all the neurons at the same time and it speeds up the training.

4.Optimizer used:

Adam optimizer is used in this model.
The dataset has sparse data and this algorithm will be able to handle it with the perfect adaptive learning rate.
It also possibly prevents overfitting of the model.


5.Neural Network/Model used:

DRNN[Deep Recurrent Neural Network] is used.

The reason that DRNN is used is because it has the most success when working with large sequences of words in a paragraph.
It takes an arbitrary input and output lengths
It also reduced the complexity of increasing parameters and memorizes each previous output by giving each output as input to the next hidden layer

Accuracy: 64.99%
