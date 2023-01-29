# turtle-face-detection
This is a solution for a Zindi challenge on a face detection tool for sea turtles.

https://zindi.africa/competitions/local-ocean-conservation-sea-turtle-face-detection

YOLOv5 segmentation is used to detect the head of a turtle in an image.
This is the first step for developing a tool to identify individuals based on their unique faces.

The challenge does not allow commercial tools. Therefore, the first step of creating of the dataset with roboflow still needs to be replaced with an open-source solution.

## 1. Creating a training data set with roboflow
The images are annotated and augmented using roboflow. 145 are used for training.
This is done manually and looks like this:
![train set](https://user-images.githubusercontent.com/66785534/215327641-94e3d5c9-401b-4213-8643-c69a3f0ab7fa.png)


## 2. Training a YOLOv5 segmentation model
100 epochs took about an hour in google colab.

## 3. Predict the polygons and save text files
The prediction of the images was done in a few minutes in google colab. For each image a text file with the polygon coordinates is saved.

<img src="https://user-images.githubusercontent.com/66785534/215327669-9774cd95-a5aa-4430-a994-c2e08758e809.jpeg" alt="drawing" width="400"/>
<img src="https://user-images.githubusercontent.com/66785534/215327663-e858bfcf-3c82-4e16-855a-7eff0fe47aa5.jpeg" alt="drawing" width="400"/>



## 4. Transform the text files to the required format.
Eventually the data is saved as a csv file. The actual polygons are not needed and transformed into bounding boxes.

![bounding boxes](https://user-images.githubusercontent.com/66785534/215327659-bcf88865-d21d-4935-bef9-2052e2dd30d6.png)

More detailled descriptions are available in the notebook.
