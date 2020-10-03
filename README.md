# NASA SpaceApps Hackathon (AgriCarer)

## Introduction

Our team (AgriCarer) is seeking to tackle the knowledge inequality problem currently faced by many farmers from developing countries. From our research and personal conversations with a local farmer in Malaysia, we found that most farmers in developing countries are smallholders farmers that generally lack access to best agriculture practices, data and information. Smallholders farmers do not have funding/investments necessary to procure state-of-the-art technologies and seek expert advice. Thus, local farmers are very vulnerable to the occurences of diseases and pest in ruining their entire crop and reducing their crop productivity. In some cases, the whole farm may have no yield as no proper actions are taken due to the lack of knowledge. This can lead to problems such as food insecurity, environmental issues and harm to the wellbeing of the farmers.


# Idea Proposal
We are proposing an user friendly smartphone app to support farmers with state-of-the-art technologies and expert research advice to solve the problem of the knowledge gap and the problem of yield losses in crop plants. Most local farmers that we talked to does not have the necessary extra funds to invest in technology and they are also averse to new technology. Therefore, a smartphone app was suggested by the team as it will lower down the cost of entry for farmers as most farmers already owns a smartphone which makes the technology much easier to adopt.


The smartphone app proposed will have features such as remote sensing technology, plant disease diagnosis, and timely reminders to support farmers in taking care of their farms. 



## Remote Sensing Technology 

The remote sensing technology will done by collecting free open-source satellite data from space agencies around the world such as NASA, CSA, CNES, JAXA, and ESA.


edgar + jiaren write more ...? put some maps, your findings.



## Plant Disease Diagnosis

This repository consist of a simple prototype/proof of an AI system that is able to classify different plant diseases. We used the FastAI API to train on our dataset. The dataset was obtained from PlantVillage. [PlantVillage](https://arxiv.org/abs/1511.08060) is an open-source dataset consisting of over 50,000 expertly curated images of healthy and infected leaves of crop plants. 

In this case of our proof, we decided to train on a subset of the PlantVillage dataset and took only three categories namely Tomato Healthy, Tomato Early Blight and Tomato Late Blight. Data used can be found [HERE](https://drive.google.com/drive/folders/1fLFJAc4h7pcL2QFuUs2R-R8-i32eg44L?usp=sharing), there is a total of 4500 raw images in it. Utilising a ResNet50 with data augmentation, we were already able to achieve  98.89% accuracy on the validation set consisting of 900 images (20% of 4500 raw images was used for validation) as seen of the confusion matrix below:


<p align="center">
  <img src="https://github.com/timothylimyl/SpaceApps_Hackathon/blob/main/images/confusion_matrix.png" alt="Sublime's custom image"/>
</p>



However, it is worth noting that the model trained on PlantVillage data does not transfer well to the real-domain which is of expectation as the AI system is trained using supervised learning. Supervised learning depends heavily on the quantity, quality and diversity of the datasets to perform well. The PlantVillage database is taken under controlled lab conditions with a single leaf in the photo as shown below. 

<p align="center">
  <img src="https://github.com/timothylimyl/SpaceApps_Hackathon/blob/main/images/plantvillage_sample.JPG" alt="Sublime's custom image"/>
</p>

Thus, when a plant is taken as a whole, the AI will most probably fail to classify correctly as the AI is overfitting the images taken under controlled lab conditions.  An example of misclassification, a healthy tomato plant is classified as late blight:

<p align="center">
  <img src="https://github.com/timothylimyl/SpaceApps_Hackathon/blob/main/images/misclassification.JPG" alt="Sublime's custom image"/>
</p>


Our team is well aware of the problem of misclassification which is why we believe that this making an app that is widely available and accessible is a great idea for mass data collection in order to train a more robust AI model. We believe that by pre-processing images taken by the farmer and allowing farmers to pick out leaves of interest for diagnosis (classification) will ensure great AI classification results that farmers can confidently trust in. The most important principle for success is a sound standardized imaging procedure that yields repeatable results. Our team also believes that the classifier can be extended to classify pests to support farmers.

An illustration of our app prototype after the classifying process:

Put a gif from the app (flows from camera -> diagnosis)


We will approach plant pathologist and researchers to seek out expert advice on what kind of immediate actions are required, general advices and preventative measures for the specific disease detected. These informations can then be immediately disseminated to the farmers right after the plant is classified through the app. Thus, the app can greatly support farmers in identifying diseases and recommend the best course of actions. We believe that this will increase the crop yield of local farmers and bridge the gap between farmers and researchers.



## Prototype: Smartphone App









