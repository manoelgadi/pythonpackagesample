# pythonpackagesample
This is a simple minimal set of codes to create a Python Package

# Below is the list of instructions you need to follow in order to adapt and publish your own Python Package in your own github account, testpypi.org and pypi.org as of 16/July/2022 - a video with explanation will be posted here soon.
## Please give your start to this project if you like it!


## Download Git Bash


-> In Git Bash, go to a directory where you have permission to save things:

cd C:\....



-> There clone my github sample repository:

git clone https://github.com/manoelgadi/pythonpackagesample.git



-> enter in the folder: 

cd pythonpackagesample



-> login to your github account (make sure you have a GitHub account)

git init



-> Rename the directory pythonpackagesample to fairdetect_X (replace X with your group letter + your name so that you can follow this step if you want, example a_manoel)

-> Go your Github account and create the repository fairdetect_a_manoel

git remote rm origin



-> Replace https://github.com/... with the repository you've just created

git remote add origin https://github.com/...



-> Edit setup.py with your details

-> Edit the file __init__.py, inside the directory fairdetect_X, putting the fairdetect class there.

-> Add the files to be upload

git add .



-> Put a commit message, during the class I forgot to do it, so it was not uploading.... THIS WAS THE PROBLEM WE FACED IN CLASS!

git commit -m "uploading class"  



-> Now, open Anaconda Prompt - go to the directory where the package is:

cd C:\....

cd pythonpackagesample



-> Install wheel (for making the package) and twine (for uploading the package)

pip install wheel

pip install twine



-> Creating your python Package

python setup.py bdist_wheel sdist



-> Create an account for https://test.pypi.org/, confirm your email! and upload the package.

twine upload -r testpypi dist/



-> Create an account for https://pypi.org/, confirm your email! and upload the package.

twine upload -r pypi dist/



-> Now you and anyone can install your package by using:

pip install fairdetect_X





Please let me know if you have any issue following this steps. Welcome, you are now a Python packge creator ;-)



Best,

Prof. Manoel Gadi
