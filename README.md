# tf20_vision_samples

## Python
3.7  
Anaconda  

20201210 - Anaconda supports TF 2.2 (not 2.3)

!! ASUS tf22 is really tf24 - this is because the TF step upgraded automatically from 2.x to 2.4
Dell Laptop tf24 is tf24

###WARNING:
- the tutorial setup will upgrade to tf 2.4
- the tensorboard tutorial will require `$ conda install keras`  This will move to tf 2.3
- conda install tensorflow-gpu ==> 2.2
- pip install tensorflow-gpu ==> 2.3
what a mess!

### tf22
Anaconda managed  
```
conda create -n tf22 python=3.7  
conda activate tf22  
using anaconda-naviagor, install jupyter  
python -m ipykernel install --user --name tf22 --display-name "Python37 (tf22)"  
```
create a jupyter notebook (from tf22) to verify

tf 2.2  
keras 2.4.3  

### tf23
Expect to drop this someday (when Anaconda supports 2.3)  
conda create -n tf23 python=3.7  
conda activate tf23
using anaconda-navigator, install jupyter
python -m ipykernel install --user --name tf23 --display-name "Python37 (tf23)"
create a jupyter notebook to verify

### using anaconda-navigator
create environment (tf20) Python 3.7  
install Jupyter
using anaconda-navigator, install jupyter

opencv -- used pip install 4.4 (should I have used conda?  3.4?)
conda install tensorflow-gpu
- cuda toolkit 10.1
- protobuf 3.
- tf 2.2
- tensorboard


### command prompt

conda activate tf20  
python -m ipykernel install --user --name tf20 --display-name "Python37 (tf20)"
pip install opencv-python 
conda install matplotlib

#### Required with the Master Computer Vision Book
These packages are not necessarily used with your final applications.    If you are creating a more streamlined python environment, you may omit them or think hard about what you need (e.g. PIL or opencv?)  

conda install pillow  
conda install ImageHash
pip install scikit-image  
conda install pandas  
conda install keras  
conda install boto3
conda install bs4

## Master Computer Vision with TensorFlow 2.x

git clone https://github.com/PacktPublishing/Mastering-Computer-Vision-with-TensorFlow-2.0.git  


### Data
local:  ~/data/furniture_img  
?? is the data redudant?  /data/img & /data/furniture_img/

kaggle 

## Tensflow 2.x Object Detection Tutorial

### SageMaker

Install the /models 
```
mkdir /home/ec2-user/SageMaker/tensorflow
cd /home/ec2-user/SageMaker/tensorflow
git clone https://github.com/tensorflow/models.git
```
#### Compile Protobuf
on SageMaker, the compiler is already installed, v3.13.  So, you can skip the installation!

```
cd models/research/
protoc object_detection/protos/*.proto --python_out=.
ls object_detection/protos/ -l
```
super fast (like I thought it did nothing) but, you should see _pb2.py

#### pycocotools
should be installed because it's a TF2.x dependency.   If not, see the tutorial installation page - it has instructions to manually install.   On my SageMaker - it did not appear to be there
```
# got a fatal error in the make operation - stackoverflow says:  install cython first
pip install cython
ls /home/ec2-user/SageMaker/tensorflow/models/research//TensorFlow/models/research/
# no pycoco
cp -r pycocotools /home/ec2-user/SageMaker/tensorflow/models/research/
ls /home/ec2-user/SageMaker/tensorflow/models/research/
# now you see pycocotools

```
#### Eval Metrics
default is Pascal VOC, you can use COCO - see the note in the tutorial

#### Object Detection API

Watch the console!!! when you do this, it will uninstall TF 2.2 and install TF 2.4!!
```
cd /home/ec2-user/SageMaker/tensorflow/models/research/
ls -l

cp object_detection/packages/tf2/setup.py .
ls -l

# failed on dependencies
# can't conda activate on SageMaker!!
python -m pip install .
```
run through the cp step, then go to the Jupyter notebook:  TF22_Installation and you can do the pip install there.   You have to do it from the Jupyter notebook because I couldn't figure out how to get $conda activate to work from a terminal on Jupyter.   This worked in previous releases but it isn't configured now. 
