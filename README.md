# tf20_vision_samples

## Python
3.7  
Anaconda  

20201210 - Anaconda supports TF 2.2 (not 2.3)

### tf22
Anaconda managed  
```
conda create -n tf22 python=3.7  
conda activate tf22  
using anaconda-naviagor, install jupyter  
python -m ipykernel install --user --name tf22 --display-name "Python37 (tf22)"  
```
create a jupyter notebook (from tf22) to verify

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
