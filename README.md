# Enviroment setup for running the models

1. Install conda, it will help create a virtual env and launch Jupyter-Notebook for use over the disk.
2. You will see some script for conda in your ~/.bash_profile.rc
3. Run below command to source it and you will enter the base env. - 
```
data_science git:(main) ✗ source ~/.bash_profile.rc
```
4. Now check if conda is available - 
```
(base) ➜  data_science git:(main) ✗ conda --version
conda 22.9.0
```
5. Create a Virtual Env, with required libraries for running the models. You will enter new env 'test' after you activate it.
```
(base) ➜  data_science git:(main) ✗ conda create --name test python=3.8 jupyterlab numpy pandas matplotlib scikit-learn
(test) ➜  data_science git:(main) ✗ conda activate test
(test) ➜  data_science git:(main) ✗
```
6. For SVM we need a library called libsvm, conda does not provide direct access to it, so we use pip to install it - 
```
(test) ➜  data_science git:(main) ✗ pip install -U libsvm-official
 ```
 7. For CNN we cannot directly use our conda channel(tensorflow not available) so we add a new channel 'conda-forge', and then install tensorflow -
 ```
 (test) ➜  data_science git:(main) ✗ conda config --append channels conda-forge
 (test) ➜  data_science git:(main) ✗ conda install tensorflow
 ```
