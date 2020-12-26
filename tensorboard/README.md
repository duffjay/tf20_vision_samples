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
## pip - tb24
note - pip installs tensororflow-gpu version 2.4 (20201226)

```
conda create -n tb24 python=3.7  
conda activate tb24  
conda install jupyter  
python -m ipykernel install --user --name tb24 --display-name "Python37 (tb24)" 
```

```
pip install boto
pip install pyasn1
pip install matplotlib
pip install scikit-learn
pip install cryptography
pip install tensorflow-gpu
pip install matplotlib
pip instal scikit-learn
```
