This is a program which will conduct a sentimental analysis on various financial news titles.
One piece of news could have a huge impact to the market performance, such as fluctuations in oil price. 
Thousands of pieces of news could be produced at the same time and the impacts they could exert could be too complicated to be analyzed by humans. 
Thus, I designed this program using LSTM (Long Short-Term Memory) network under Tensorflow.keras library.
The sequence of the words inside a sentence is important to the sentimental analysis. Thus, LSTM is used. This network is also useful when analyzing time series data. 
By tokenizing words inside the database, natural language is turned into several number sequences for further processing. By inputing these number sequences into the pre-designed network with several bidirectional and dropout layers, a list of sentiment predictions will be given.
I have also tried to use some pre-trained vectors to tokenize and embed the sequences to see whether the prediction results could be better.
The objective is to find out a model that could generate predictions as precise as possible. For the database I used in this project, the highest precision is 82% (weighted average). The precision for negative sentiment is not high enough (55%). This is because the negative sentiments are the least among the three categories. Further improvements could be made if more data would be included to make the dataset more balanced. 
Future possible optimization: 
  1. Input a news title by the user. Use the model I trained in the project to give a prediction result. (Useful for real work environment)
  2. The model could also predict to what extent the news could affect the market. For example, the war in middle east will cause a 5% increase in oil price (5% is the prediction given by the model).
