# CodeMonk-Submission

## Inputs
The input for training the model is a csv file:
- First column is the image_id
- Subsequently the 6 Categories with different number of classes for each category.
  - Color
  - Seasons
  - Gender
  - Master Category
  - Sub Category
  - Article Category
Each category is first tokenised and then one hot encoded before sending into the model for training.

For Evaluation only an image is necessary.

The architecture works by using pretrained weights of resnet to help form better feature maps that are then passed on to 6 fully connected layers(fc).
Each fc layers corresponds to one of the categories defined previously.

## Output
The ouput is then calculated against the target values using Cross Entropy Loss.
The losses are then calculated and then the weights are updated.
