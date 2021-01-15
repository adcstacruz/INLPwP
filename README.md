# Introduction to NLP with Python [Installation]


# Install Anaconda

Instructions: https://docs.anaconda.com/anaconda/install/

Verify installation: https://docs.anaconda.com/anaconda/install/verify-install/

# Setup the Conda environment


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

Activate the environment first

```
$ conda activate inlp
```

Validating that the environment is activated: you'll see the environment name at the beginning of your commandline, something similar to: 


```
$(inlp)
```

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

## 1 Packages 
```
$(inlp) conda install -c conda-forge pandas scikit-learn matplotlib wordcloud textblob spacy gensim nltk 
``` 

## 2 SpaCy model

```
$(inlp) python -m spacy download en_core_web_sm 
```

## 3 NLTK libraries


