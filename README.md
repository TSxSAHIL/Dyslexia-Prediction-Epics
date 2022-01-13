# HackathonML
Predicting Dyslexia using Machine Learning.

● There are a series of questions that need to be answered by the user, and on the basis of the results, scores are given for language, memory, speed,
visual and audio skills.
● The objective of this model is to give an accurate prediction of the chances of the user having dyslexia, using the above scores as input.

Introduction of Dataset <br />
In this project, we are making predictions using Machine Learning, on the basis of quiz scores of a person to see whether they have Dyslexia. In our dataset, we have the columns ‘Language_vocab’, ‘Memory’, ‘Speed’, ‘Visual_discrimination’, ‘Audio_Discrimination’, ‘Survey_Score’ and ‘Label’. Every applicant is required to take a quiz which has different questions to test language vocabulary, memory, speed, visual discrimination and audio discrimination. On the basis of their answers of these questions, points for each section are calculated and put into the first five columns of the dataset, respectively. Another survey is also conducted on the basis of which ‘Survey_Score’ is calculated. These scores are analysed to get the value of ‘Label’, which ranges from 0 to 2. The values 0, 1 and 2 mean that the chances of the applicant having dyslexia are low, moderate and high, respectively. 

Working of Model <br />
The purpose of this project is to predict the ‘Label’ i.e., chances of the applicant having dyslexia, if the values of ‘Language_vocab’, ‘Memory’, ‘Speed’, ‘Visual_discrimination’, ‘Audio_Discrimination’ and ‘Survey_Score’ are provided. In the file [DyslexiaML](https://github.com/Manvi-Kaur/HackathonML/blob/main/DyslexiaML.ipynb), we have created five different models to find the one which is the best fit for the given dataset. The comparison has been made between DecisionTree, RandomForest, SVM, RandomForest with GridSearch and SVM with GridSearch, on the basis of error, precision and recall. On comparing all of these parameters, we found that RandomForest with GridSearch is the best fit for our dataset. <br />
On the basis of our findings, we then created the final model using RandomForestClassifier with GridSearchCV in order to make the most accurate predictions, in [DyslexiaML_final](https://github.com/Manvi-Kaur/HackathonML/blob/main/DyslexiaML_final.ipynb) file. <br/>
This model was then tested in [Test_Model](https://github.com/Manvi-Kaur/HackathonML/blob/main/Test_Model.ipynb) on a new dataset to find the labels, which were then compared with the actual label values. After this check we found out that our model was able to make predictions for dyslexia with a 5.8% error rate.<br/>
At last, we've created a user-friendly file [Input_test](https://github.com/Manvi-Kaur/HackathonML/blob/main/Input_test.ipynb), wherein the user is given a brief introduction of the model, followed by which they can enter the values of ‘Language_vocab’, ‘Memory’, ‘Speed’, ‘Visual_discrimination’, ‘Audio_Discrimination’ and ‘Survey_Score’, followed by which the final model created is used to provide the result in a readable format. <br/>

Calculations of Scores - <br />
(Shown as per respective question numbers)<br />
Language_vocab = (Ans.1 + Ans.2 + Ans.3 + Ans.4 + Ans.5 + Ans.6 + Ans.8)/28<br />
Memory = (Ans.2 + Ans.9)/8 <br />
Speed = Calculated on the basis of time taken to complete the quiz <br />
Visual_discrimination = (Ans.1 + Ans.3 + Ans.4 + Ans.6)/16 <br />
Audio_Discrimination = (Ans.7 + Ans.10)/8 <br />
Survey_Score = (Sum of all answers)/80 <br />


