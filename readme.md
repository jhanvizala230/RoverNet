# RoVERNet: Responsive observation and Vision for Exoplanetary Rovers Network using Deep Learning

## Dataset files
Filename :  rovernet_final_code\combine_ai4mars.ipynb
Filename :  rovernet_final_code\combine_marsv2.ipynb
Filename :  rovernet_final_code\combine_s5mars.ipynb

From the separate folder created above combine all the datasets in one "final_dataset" folder
Folder structure should be as follows for each dataset and final dataset folder:

## Visualize Each Dataset
Filename : rovernet_final_code\dataset_visualization.ipynb

To visualize each dataset use the above given file. The file requires an input of folder name for each dataset like the root image folder of ai4mars, s5_mars and marsv2 

## Convert TO COCO format
Use this file to convert your dataset to coco format. Provide the final dataset image and mask path. The three different paths each for train, test and validation should be given. To get three different JSON files respectively

Filename : rovernet_final_code\image_to_instance_json.ipynb

For COCO format information refer to this link

## Train MaskRCNN Model
Use the following given file to fine-tune the model. Some configuration parameters are defined in the file. You can alter it according to your wish. Provide the file path of all the coco format JSON files and the relevant image directory to register and use those datasets. during training.

Filename  : rovernet_final_code\instance_seg_model_train.ipynb

The model output is saved in the "rovernet_final_code\outputname of output directory}" directory

## Prediction and Visualization

Filename : rovernet_final_code\Prediction.ipynb

After the training and evaluation model is saved in the output directory in this "instance_segmentation\output\{name of output directory}\model_final.pth" path use this file as a model weights file to get a prediction on your test. More than 1800 files are available that would provide visualization on 50 images.

This file also saves the bounding box data along with each instance category and unsegmented area all in one JSON file.
