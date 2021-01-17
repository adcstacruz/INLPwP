# Introduction to NLP with Python [Installation]


# Install Anaconda

Instructions: https://docs.anaconda.com/anaconda/install/

Verify installation: https://docs.anaconda.com/anaconda/install/verify-install/

# Set up the Conda environment


## 1. Create environment

```
$(base) conda create -n inlp python=3.7
```

## 2. Activate the environment first

```
$(base) conda activate inlp
```

Validating that the environment is activated: you'll see the environment name at the beginning of your commandline, something similar to: 

```
$(inlp)
```

Notice that the environment was changed from `base` to `inlp`

## 3. Register kernel to the notebook 

Install Ipykernel through the conda-forge channel. Ipykernel enables us to use our environment in our jupyter notebooks. Note: please make sure that the environment is activated before proceeding. 

```
$(inlp) conda install -c conda-forge ipykernel
```

Register the kernel:

```
$(inlp) python -m ipykernel install --user --name=inlp
```

This should print out the following: 

```
Installed kernelspec inlp in some_directory/inlp
```

Check if the kernel is available in jupyter notebook: open a new terminal. Make sure that you are using the base environment. Again, open a new terminal to do this. No need to activate the `inlp` environment. 

```
$(base) jupyter notebook
```

Click new and you should see `inlp` as one of the kernel options. 


# Install packages and models for this course

Note: activate the `inlp` environment, if not activated.



## 1. Packages - MacOS and Linux  
```
$(inlp) conda install -c conda-forge pandas scikit-learn matplotlib wordcloud textblob spacy gensim nltk 
``` 

END OF PACKAGE INSTALLATION FOR MAC/LINUX USERS. Please proceed to 2. SpaCy model

## 1. Packages - Windows
IF YOU ARE USING WINDOWS, please follow the instructions below. 

**Install certain packages from the default channels/where these packages are available.**

```
$(inlp) conda install pandas scikit-learn spacy gensim nltk 
``` 

**Install the remaining packges from the conda-forge channel**

```
$(inlp) conda install -c conda-forge wordcloud textblob matplotlib
``` 

**Install a specific version of smart_open**
```
$(inlp) conda install smart_open==2.0.0
```

**Installing pillow**

We'll install pillow through python wheels. First, download the wheel which is posted in our google classroom.

Download `Pillow-8.1.0-cp37-cp37m-win_amd64.whl` if your machine is 64-bit. If you are using a 32-bit machine, please download `Pillow‑8.1.0‑cp37‑cp37m‑win32.whl`.

NOTE: Please check where the file was downloaded

After downloading the wheel from google classroom, install the wheel through pip. Note that you should have activated your environment. To install, the command is:

```
$(inlp) pip install --no-deps --force-reinstall --user "PATH_TO_FILE\WHEEL_PACKAGE
```

For example, if the I have saved the wheel package in "C:\Users\user\Downloads". The command will be: 

```
$(inlp) pip install --no-deps --force-reinstall --user "C:\Users\user\Downloads\Pillow-8.1.0-cp37-cp37m-win_amd64.whl"
```


## 2 SpaCy model

Under the hood, spacy uses a model which we should download. We'll use the (small) English core model. To download:

```
$(inlp) python -m spacy download en_core_web_sm 
```

**If you encountered an error** -- specifically `ReadTimeoutError`, please download `en_core_web_sm-2.3.1.tar.gz` which is posted in our google classroom. 

```
$(inlp) pip install "PATH_TO_FILE\en_core_web_sm-2.3.1.tar.gz"
```
For example:
```
$(inlp) pip install "C:\Users\user\Downloads\en_core_web_sm-2.3.1.tar.gz"
```

## 3 NLTK libraries


