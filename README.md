# Robosapien-Object-Detector-using-Darkflow  
Detect the Robosapien in an image  using darkflow.  
![alt text](https://res.cloudinary.com/ogbanugot/image/upload/v1530397120/temp2_sndqpl.png)  
  
  
![alt text](https://res.cloudinary.com/ogbanugot/image/upload/v1530394580/00000186_lphw76.jpg)



## Install Darkflow  
Install darkflow from [here](https://github.com/thtrieu/darkflow). You can build for both python2 and python3.  

## The necessary files  
The ./cfg and ./bin directories in this repository contain the cfg and weight file. You can use this to train a single class object detector from scratch.  
./pb contains the built graph as a protobuf (.pb) file and the meta file (.meta). See the darkflow repository for more on these files.  
Integrate these folders with their respective darkflow directories. You will have to create the ./built_graph directory in darkflow, just copy and paste it.
  
## Making a prediction  
Test the neural network with your own image containing the robosapien. In your darkflow repository run;  
  
flow --pbLoad built_graph/tiny-yolo-voc-1c.pb --metaLoad built_graph/tiny-yolo-voc-1c.meta --imgdir sample_img/  
  
Check darkflow/sample_img/out to see the results. 
  
## Training on more images  
You can train on your own robosapien dataset using the built graph. From darkflow/ run; 
  
flow --train --model cfg/tiny-yolo-voc-1c.cfg --load 3625  


