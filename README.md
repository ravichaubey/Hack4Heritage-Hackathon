## Hackathon Information

![](https://techaeris.com/wp-content/uploads/2018/04/NVIDIA-deep-learning-ai-image-reconstruction.jpg)

**Problem Statement:-** The hackathon is divided into 2 phases.Phase 1 is where all participants take part and are asked to solve a smaller version of problem statement, related to basic `planning of art restoration using deep learning in 15 hours.` We conduct this phase in order to filter out the good brains in deep learning, so that our efforts are focused in Phase 2.

• End Objective for Phase 1:- Create the basic structure or framework (with logical functions) of the plan needed in the second phase.

• End Objective for Phase 2:- Create a Model that can restore broken images (similar to the initial sample dataset shared) and be able to demonstrate the same to any user while suggesting the level of accuracy achieved by the model

• End Objective at the end of Hackathon:- Create a system that reads a damaged image (with missing portions), identifies the areas that are damaged, and uses a model to fill the spaces that are missing using scientific assumptions drawn out of the sample datasets, effectively being able to restore any image similar to the sample dataset shared.

## Solution:-

Objective :-
   
   1.) Selection of Datasets.
   2.) Develop Flow of solution.
   3.) Creation of Logical Function.

## 1.) Dataset Selection:- 

Chosed the dataset similar to the sample given with the problem statement. We need data that have some discontinuity or similar to the given image examples and thus we ingested these images to our Data Folder using the sources(Google Images) given with the help of Python Scrip.
In these all images we have got some types of images. so we have collect them accordingly.

`DATA :->` 1. Martand_Sun_Temple_damaged_sculptures, 
           2. khajuraho_damaged_sculptures, 
           3. incomplete_caves_wall_painting, 
           4. ellora_caves_damaged_sculptures,
           5. ancient_damaged_wall_paining of india

## 2.) Develop Flow of solution:- 

**Data Acquisition & storage:-** We ingested data to our local system using Python Script from Google Images.
After Ingestion, Generally we store data on some database , But for phase 1 and smaller set of problem we used our local system as storage.

`Link to google_image_download :` https://pypi.org/project/google_images_download/

`Link to Acquired Data :` https://github.com/ravichaubey/Hackathon/tree/master/Data


**Data Retrival:-** We have retrieved our data from local using Python (OpenCV).
 
**Data Preparation:-**  For phase 1, We are just creating a simpler solution so we have resized image to a particular pixel. Later for complete solution we are going to build a Pipeline to read image, resize image image and augment image.
   
**Data Analyse:-** We have uses encoder-decoder with skip connections . Encoder downsample our image and decoder generate a new image by using upsample the output of encoder.

`Parameters of Network are below:`
        
1. Activation Function : LeakyReLU

2. Upsample Mode: bilinear
        
3. Downsample Mode : stride
        
4. Total Trainable Params: 2217573

**Reporting and Action:-** Basically reporting our action of our deep learning model is to bring system to work for users. Reporting is either reporting visuals or reporting information like metrics or some relationship. In this case we are reducing _loss_function_name_.

**Action:-** We are going to create a webpage to deploy our model. User can upload an image and get back re-generated image on same webpage. ‘Please note that we are not going to show this webpage in Phase 1, due to lack of time. But we are prepared for phase 2.’
