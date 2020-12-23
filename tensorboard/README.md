# Tensorboard

Use this environment instead of using tensorflow - because it may mess with the packages.    Example, you may need to load keras which messed up the tf24 environment and downgraded tf.

## Python

## conda - tb22
conda managed
```
conda create -n tb22 python=3.7  
conda activate tb22  
conda install jupyter  
python -m ipykernel install --user --name tb22 --display-name "Python37 (tb22)" 
```
confirm jupyter notebook and kernel

```
conda install tensflow-gpu
conda install matplotlib
conda install -c conda-forge scikit-learn
```
