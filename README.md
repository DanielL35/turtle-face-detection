# turtle-face-detection
This is a solution for a Zindi challenge on a face detection tool for sea turtles.

https://zindi.africa/competitions/local-ocean-conservation-sea-turtle-face-detection

YOLOv5 segmentation is used to detect the head of a turtle in an image.
This is the first step for developing a tool to identify individuals based on their unique faces.

The challenge does not allow commercial tools. Therefore, the first step of creating of the dataset with roboflow still needs to be replaced with an open-source solution.

# 1. Creating a training data set with roboflow
The images are annotated and augmented using roboflow. 145 are used for training.

# 2. Training a YOLOv5 segmentation model
100 epochs took about an hour in google colab.

# 3. Predict the polygons and save text files
The prediction of the images was done in a few minutes in google colab. For each image a text file with the polygon coordinates is saved.

# 4. Transform the text files to the required format.
Eventually the data is saved as a csv file.

More detailled descriptions are available in the notebook.
