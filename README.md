# deep-learning-challenge

*** OVERVIEW ***

The general purpose of this project was to create a neural net that can estimate whether a project will be successful based on a number of factors. Ideally we would take our existing data, train and test a model using it, and have some predictive model to use for the future.

To establish this we had to set our target to the IS_SUCCESSFUL column. This column is a dummy column with a 0 or 1 indicating whether that project was successful or not, 1 being successful and 0 being unsuccessful.

### FIRST MODEL
In my original model I drop the name and identifier column, then from the APPLICATION TYPE and CLASSIFICATION columns I bin all values under 100 into an "other" bin and finally create dummies of the remaining columns.

From there I scale the data and use a kernas neural network with three total layers and compile and fit my model with 100 epochs.

This model didn't do so great, it resulted in an above 0.5 loss and under a 0.75 accuracy.

### SECOND & THIRD MODEL

My second and third models dropped the STATUS column as well as the name and identifier as there was only 5 items that were not 1 in this boolean column out of the thousands of rows.

Next for each model I changed my bins to 50 instead of 100.

Lastly I adjusted the layers. For the second model I added another hidden layer that mimiced the 2nd layer and in my third model I adjusted the number of units in each model and changed the epochs to 150.

All of these changes actually decreased the accuracy of the model somewhat rather than improving the models.

### CONCLUSION

Overall...my model isn't great. I can interpret this as the data not being adequate to form a good neural network or that I just need to keep working and improving the model. The accuracy wasn't too low, about 0.72 for each model, but the loss of over 0.5 for each is really what threw me off on this one. I think I'll need to study a lot more to improve my modeling on neural networks.