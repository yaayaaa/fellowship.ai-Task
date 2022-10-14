# fellowship.ai Task
This repo is part of the interview process for fellowship.ai

**Through the Notebook I demonstrated how we can do transfer learning with PyTorch for the Resnet50 model with its pre-trained weights**

We used the data set of Stanford cars but tweaked one which the data is as the below 

----->root directory
    
    
    |
    |
    
    
    -> stanford-cars-dataset
    
    |
    |
    
    
    -->train
    
    |
    |
    
    
    ---> classes
    ---> classes
    
    
    |
    |
    
    
    -->test
    
    
    |
    |
    ---> classes
    ---> classes
 
 Which is easier to load other than the original dataset that was just incrementing .jpg files in the train and test directories and there was a .mat file that has the annotations of these photos and the class names
 
 In the notebook first I made frozen layers and removed the fully connected layer of the network and made up a new layer for the classification of the 196 classes we have in the dataset.
 
 Then I did another two models with more late layer trainability which made up less accuracy but there is so much to search about through the data set because we didn't use any of other accuracy measurements like F1  score or confusion matrix or any of this and we need to try more epochs to get better results and the data set distribution of 50-50 between the training dataset should be varied also so we can understand how the data set and the model works the best.
 
 Lastly, transfer learning is a very powerful approach to solving problems like this and it could be used.
 
 **The transfer learning concept in a snippet and why the first model did better than the other two:**
  
1. The transfer learning concept is taking a model and its weights' which did pretty good on some classification problem like resnet50 VGG16 or so whatever and use it as a feature generator to the classification layers and just train the last classification layers as needed and you can edit the structure of the model to match your data set and how you need it to be and that's how I did use it for the first model of the notebook.
  
2. And if it doesn't give you the accuracy you need you can unfreeze some of the late layers to tweak the generation of the sophisticated feature.
  because the early layers are responsible of more naive feature generation which leads to more of the sophisticated features
