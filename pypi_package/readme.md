# How to upload this package to pypi
To upload this package to your pypi account, you would need to do a number of things.

Create a setup.cfg file, README.md file, and license.txt file. You'll also need to create accounts for the pypi test repository and pypi repository by visiting https://test.pypi.org/ and https://pypi.org/ respectively. 

**Important:** Don't forget to keep your passwords; you'll need to type them into the command line.

Once you have all the files set up correctly, you can use the following commands on the command line (please do note that you need to make the name of the package unique, so change the name of the package from **my-gaubi-distributions** to something else. That means changing the information in the setup.py and the folder name):

+ cd pypi_package
+ python setup.py sdist
+ pip install twine

# Run these commands to upload to the pypi test repository
    twine upload --repository-url https://test.pypi.org/legacy/ dist/*
    pip install --index-url https://test.pypi.org/simple/ distributions`

# Run these commands to upload to the pypi repository
    twine upload dist/*
    pip install distributions
