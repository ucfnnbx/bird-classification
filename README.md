# bird-classification
## Definition of problem being solved 
### Project Overview
In this project, transfer learning based on a pre-trained CNN model is used to build a classifier for bird species that are frequently spotted around the area of UCL East campus. Four types of birds can be classified in the current stage, which are crow, double brested cormorant, Eurasian magpie and gull. 
### Research Question
Can a CNN-based transfer learning model be used to classify main bird species around UCL East with good accuracy?
Anticipated outcome is positive.
### Dataset
The dataset used was chosen from Kaggle BIRDS 510 SPECIES dataset, which has around 200 training images for each kind of bird. A few self-shot images are also added in the dataset.
Available at: https://www.kaggle.com/datasets/gpiosenka/100-bird-species
### Application Design
Edge Impulse was used as the platform to store, tag and split the data; build, train and test the model; deploy the model to a mobile phone. 

## Documentation of experiments and results 
The final trained model achieved 95.83% accuracy. To train the model, a series of experiments were run to solve overfitting problem and achieve a higher accuracy. The model architecture was a MobileNet-v2 (160x160 0.35) with the top four layers disabled. Also, the impact of data augmentation, greyscale preprocessing, learning rate and quantization on the performance of model was experimented. Details of results can be found in the report. 

## Critical reflection and learning from experiments 
### Observations from experiments
Overfitting leads to a decrease of accuracy, which can be solved by reducing layers in the model, adding dropout and setting suitable training epochs. 
### Weaknesses
One limitation found with the model is that the bird needs to take up most of the image and be centered or the result might be wrong. This might impact the application of this bird detection system because sometimes it might be hard to get birds centered in the image. To solve this issue, an object detection system could be developed to frame the bird in an image and only processing the framed part. 
### Potential improvements
In the current stage, four common bird species can be classified with the model. Potential improvement to be done is to increase more types of bird that occur around UCL East. The model may need to be more complex to achieve the same or higher accuracy.
