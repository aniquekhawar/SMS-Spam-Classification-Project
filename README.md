# SMS-Spam-Classification-Project
> In this project, I worked with [UCI's Spam SMS message dataset](https://www.kaggle.com/uciml/sms-spam-collection-dataset) for my final project in the MSDS-453 course (Natural Language Processing) at Northwestern University.

> If you want to view the code easily, you can download the HTML file and view it locally in your browser.

## Models used
**Note**: All models employed use the scikit-learn library unless otherwise specified.
- Logistic Regression
- Naive Bayes Classifier
- Support Vector Machine
- Decision Tree
- Random Forest
- AdaBoost Classifier
- K-Nearest Neighbors
- Neural Network (Tensorflow + Keras)

## Results
> It's important to evaluate the different models. In a real world scenario, we would have more data and our training time may increase. The image below shows how long each model took to train. **Note**: We have to search for the best parameters on models to get the best performance out of them. This means that training time can vary across models.

### Training Time for Models
![](images/Training%20Time%20for%20Models.png)

### Prediction Time for Models
![](images/Prediction%20Time%20(ms)%20for%20Models.png)

### Performance Metrics
- Precision means how good we are at predicting ham (legitimate) messages. Mistaking ham messages as spam means a user could have their messages placed in a spam folder or worse, not receive their message at all.

![](images/Precision%20Score%20for%20Models.png)

- Recall means how good we are at predicting spam. A high recall prevents spam messages from appearing in your inbox.

![](images/Recall%20Score%20for%20Models.png)

- If we want the best of both worlds, an F1 score combines precision and recall, though the results can be harder to interpret.

![](images/F1-Score%20for%20Models.png)

## Conclusions
If our aim is to prevent all spam, we should seek a high recall. If our aim is to prevent important messages from being misplaced into a spam folder, we should prioritize precision. If we have to re-train our models in an offline fashion (on the entire dataset when it is updated), a faster model like decision trees should suffice. Last, if we want fast prediction times, decision trees or logistic regression models provide fast predictions.

### Limitations or mistakes made
- The Naive Bayes Classifier performed poorly versus the rest of the models. This might have to do with how I set up the model.
