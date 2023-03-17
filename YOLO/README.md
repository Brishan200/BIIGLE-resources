# DSCRU_AI
Pipeline to prepare datasets for training YOLO object detection CNN in Google Colab

! Work in progress !

You will need to have Rstudio installed: https://www.rstudio.com/products/rstudio/download/

It will help to have a python installation linked to r studio: https://rstudio.github.io/reticulate/

This is intended to integrate with the University of PLymouth Manual for Biigle [INSERT LINK] 

 # Usage
 1) First, clone the repository on you machine / Download the zip file. 
 2) Place it somewhere sensible on your computer. This will be your working directory where the scripts will look for data and write the files you will need in YOLO
 3) Run the envsetup.R script to make sure you have the needed packages and that your folders are in place
This should create a couple of folder in what should be your Working directory. 
It should 
- set up the pathway to where you saved the repository as your WD directory
- install the packages you need
- create some folders in that WD

### Once it is has finished, the folder you downloaded should contain: 

 - reports: where you put your Biigle files
 - colabfiles: this where the reshaped annotations in report folder will be. It should be empty when you start and contain several files when you are ready to move onto colab: 
    - a [projectName] folder, both regular and zipped versions. This is what you Will need to train the CNN on colab. It contains images and txt files with annotations
    - 2 csv files containing your annotations in table format - this is used for safekeeping and these files are not needed in colab
 - Taxonomy: A folder to host the tables of Biigle labels so you can add data to the API
   
   
 4) Once your env is in place: Download reports from Biigle  and place them (or it) into the report directory
  run the **Biigle to yolo** markdown document (V4 or V5 -- as of Nov 2022, V5 is recomended) 

* Do knot knit the document, it will probably fail *

Read the instruction in the document and Go through the markdown script cell by cell **some of them require your input**. 

Your input is needed to:
 - Decide how and where to get the images 
 - Decide which class and images you wish to use for  training
 - set some prameters relative the size of the dataset

There are several blocks that check if all is in order. Remember to look at those messages in the console or the output panels on the markdown document. 
 
Upload the [projectName] folder to your gdrive and connect to your favourite Colab notebook

# The Colab notebook to train and use a YoloV5 model: 
https://colab.research.google.com/drive/1q7SSKJ9cfpYar9bNf80AOYgePdlqK5XQ?usp=sharing 

You will have to save a copy of the notebook on your own GDrive to modify it and keep changes (pathways, parameters...) for later. if you dont save a copy you can still run the code but all modifications will be lost when you quit the runtime session.
