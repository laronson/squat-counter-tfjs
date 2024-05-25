# squat-counter-tfjs

Squat counter leveraging tfjs and BlazePose

# About the Project

This project was created to learn more about how I could use pre trained models for transfer learning in the creation of my own models. In this project, I use the 33 body-position output dataset from the BlazePose model to train and predict specific when the user was performing a squat. The output of the model is a 1D tensor that contains the percent confidence that the user is squatting. If the model is over 95% confident that the user is performing a squat, the count is increased by 1.

# Potential Risks and Issues

One potential risk this model poses is that the model is not pre-trained and must be trained by the user before use. This can lead to a wide range of results depending on the quality and quantity of the recorded training data. In the future, I could pre-train this model, save it, and ship it with some pre-training. The opportunity for the user to train the model future would still be available, but at the very least, with this solution, the starting place for each user would be constant.

# Future Applications

Although I chose to focus on squats for this project, this model, as it sits, could really be used to predict any constant and repeating motion.

# Run Instructions

1. Install dependencies with `yarn install`.
2. Run the application using `yarn start`.
3. Enable camera using the enable camera button.
4. Collect training data by hitting the "record training data" button.
5. To properly collect data, toggle the "Record Squatting Data" button when performing a squat. When you finish performing the squat, make suure to toggle the button off so your training data accurately represents poses in and out of the squatting position.
6. Once you are finished collecting training data, toggle off the "Record Training Data" button and select the "Train Model" button.
7. When your model has completed its training, select the "Use Squat Count Model" button to have your model analyze new input from the camera.
