# pythonpackagesample
This is a simple minimal set of codes to create a Python Package

## Below is the list of instructions

You need to follow in order to adapt and publish your own Python Package in your own github account, testpypi.org and pypi.org as of 16/July/2022 - a video with explanation will be posted here soon.

## Please give your start to this project if you like it!


## Download Git Bash


## Open Git Bash, and inside Git Bash go to a directory where you have permission to save things:

cd C:\....



## In that directory, clone my github sample repository:

git clone https://github.com/manoelgadi/pythonpackagesample.git



## Enter inside the cloned folder: 

cd pythonpackagesample



## Login to your github account (if you don't have a GitHub account, create one and confirm your email before proceding)

git init

## Rename the directory pythonpackagesample to the name you want to give to your own project, in my example I will rename it to fairdetect_X

## Go your Github account and create the repository with the name you just created, my wil be fairdetect_X

## Break the connection of your cloned repo to my original repo
git remote rm origin

## Connect with your own repo, replace https://github.com/... with the repository you've just created in your github account
git remote add origin https://github.com/...

## In any editor, open the file setup.py and edit it with your details
## Also, open the file __init__.py, inside the directory "fairdetect_X", putting there the Python code you want to share with the Python community.

## Add all files to be upload to your GitHub repo
git add .

## Put a commit message, it is mandatory!
git commit -m "uploading my first python package"  

## Now, open Anaconda Prompt - go to the directory where the package is:
cd C:\....

cd pythonpackagesample

## Install wheel (for making the package) and twine (for uploading the package)
pip install wheel

pip install twine



## Create your python Package using wheel
python setup.py bdist_wheel sdist



## Create an account for https://test.pypi.org/, confirm your email before proceeding and upload the package to https://test.pypi.org/ using twine.

twine upload -r testpypi dist/



## Create an account for https://pypi.org/, confirm your email before proceeding and upload the package to https://pypi.org/ using twine.

twine upload -r pypi dist/



## Now you and anyone can install your package by using:

pip install fairdetect_X




Please let me know if you have any issue you drop me an email: mfalonso@faculty.ie.edu

Best,
Prof. Manoel Gadi
