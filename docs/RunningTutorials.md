## How to run Tobac-Tutorials

#### Getting started

This documentation explains how to use tobac-tutorial notebooks for `tobac` 2.x using an Anaconda environment. For running tutorials on your local device, create a new folder where the data will be located. When working with a Linux environment, open a terminal in your folder and clone the `tobac` repository from Github with\
`git clone https://github.com/climate-processes/tobac`

Change your directory to the `tobac` folder. The tutorials need to be used within the v2.0-dev development branch. For fetching all branches and checking which branch you're on, use\
`git fetch`\
`git status`

As you can see, you're either on v2.0-dev branch or master branch (not compatible with these tutorials, for that use examples provided on [tobac master branch](https://github.com/climate-processes/tobac/tree/master/examples)). If you need to switch branches, use\
`git checkout v2.0-dev`

Check again which branch you're on. The active branch will appear with a * and in green color\
`git branch`

Now this works fine, but you'll also need to clone the respective repository where the tutorials are located. Change your directory pointing to the main directory and the clone the repository like before with\
`git clone https://github.com/climate-processes/tobac-tutorials`

This creates a second folder next to your `tobac` folder. Again, check what branch you're in (you'll notice there exists only one branch, the master branch.)\
`git status`

In the next step, you need to create a conda environment for providing all required software dependencies. First, initiate a new conda environment with\
`conda create -n NAME_ENVIRONMENT python=PYTHON_VERSION`

Enter your environment's name and the Python version of your choice. Check the [travis.yml](https://github.com/climate-processes/tobac/blob/v2.0-dev/.travis.yml) for further information on currently supported Python versions. 

Activate your conda environment and install the `tobac` requirements from the provided [file](https://github.com/climate-processes/tobac/blob/v2.0-dev/conda-requirements.txt) with\
`conda activate NAME_ENVIRONMENT`\
`conda install -c conda-forge --file conda-requirements.txt`

With this, all necessary prerequisites for running `tobac` are met so you can install the package with\
`pip install .`

#### Running Jupyter Notebook

Up to this point, you should have successfully installed `tobac`. As the tutorials are provided by Jupyter Notebook, you'll need to install `jupyter` in your environment as well. In the active environment, type\
`pip install jupyter`

For running the tutorials, change the directory to where the examples are located. E.g., if you want to know how the toolset can be applied to OLR model data write 
`cd YOUR_PATH/tobac-tutorials/themes/tobac_v1/Example_OLR_Tracking_model`\
`jupyter notebook`

The Jupyter Notebook will be opened in a new browser. By clicking "Run" you can execute the code line after line and follow the examples for different data sets.

Please note: When running the tutorials for the first time, you'll need to modify the code in the part of "Download the data: ..." for downloading the example data from [Zenodo](https://zenodo.org/). Remove # for uncommenting the lines and enabling the download (only for lines with #, not ##). You only need to download the data once. So when the data for all examples is saved in your tobac-tutorials folder, uncomment the lines again. 
