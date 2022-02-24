# How to run Tobac-Tutorials

## Getting started: Installation

This documentation explains how to use tobac-tutorial notebooks for `tobac` 2.x 
using an Anaconda environment. For running tutorials on your local device, create
a new folder where the data will be located. When working with a Linux environment, 
open a terminal in your folder and clone the `tobac` repository from Github with:

```bash
git clone https://github.com/climate-processes/tobac
```

Change your directory to the `tobac` folder.

```bash
cd tobac
```

The tutorials need to be used within the v2.0-dev development branch. For fetching 
all branches and checking which branch you're on, use:
 
```bash
git branch -a
```

As you can see, you're either on v2.0-dev branch or master branch (not compatible 
with these tutorials, for that use examples provided on [tobac master branch](https://github.com/climate-processes/tobac/tree/master/examples)). 
You need to switch branches, so use:

```bash
git checkout --track origin/v2.0-dev
```

Check again which branch you're on. The active branch will appear with a * and 
in green color.

```bash
git branch
```

Now this works fine, but you'll also need to clone the respective repository where 
the tutorials are located. Change your directory pointing to the main directory 
and the clone the repository like before with:

```bash
cd ..
git clone https://github.com/climate-processes/tobac-tutorials
cd tobac-tutorials
```

This creates a second folder next to your `tobac` folder. Again, check what branch 
you're in (you'll notice there exists only one branch, the master branch.)

```bash 
git status
```

In the next step, you need to create a conda environment for providing all required 
software dependencies. First, you would need to go down and initiate a new conda 
environment with:

```bash
cd ..
conda create --prefix tobac-test-env python=3.7
```

Enter your environment's name and the Python version of your choice. Check the 
[travis.yml](https://github.com/climate-processes/tobac/blob/v2.0-dev/.travis.yml) 
for further information on currently supported Python versions. 

Activate your conda environment. Then, change to your main directory and install 
the `tobac` requirements from the provided [file](https://github.com/climate-processes/tobac/blob/v2.0-dev/conda-requirements.txt).

```bash
conda activate ./tobac-test-env
cd tobac
conda install -c conda-forge --file conda-requirements.txt
```

With this, all necessary prerequisites for running `tobac` are met so you can 
install the package.

```bash
pip install .
```

Up to this point, you should have successfully installed `tobac`. As the tutorials 
are provided by Jupyter Notebook, you'll need to install `jupyter` in your 
environment as well. 

In the active environment, you need to install additional packages that are exclusively used my the tutorial notebooks. These packages are however not mandatory for the execution of `tobac`itself. So please type: 

```bash
conda install jupyter boto3 basemap basemap-data-hires
pip install rioxarray
```

## Running Jupyter Notebook

For running the tutorials, change the directory to where the examples are located. 
E.g., if you want to know how the toolset can be applied to OLR model data, write: 

```bash
cd ..
cd tobac-tutorials
jupyter notebook
```

The Jupyter Notebook will be opened in a new browser. By clicking "Run" you can 
execute the code line after line and follow the examples for different data sets.

Please note: When running the tutorials for the first time, you'll need to modify 
the code in the part of "Download the data: ..." for downloading the example data 
from [Zenodo](https://zenodo.org/). Remove # for uncommenting the lines and enabling 
the download (only for lines with #, not ##). You only need to download the data 
once. So when the data for all examples is saved in your tobac-tutorials folder, 
uncomment the lines again. 
