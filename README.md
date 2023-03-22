# tobac-tutorials

Tobac tutorials show different application cases for the cloud and precipitation tracking software tobac using jupyter notebooks. The rendered versions of our tutorials are provided at [https://tobac-tutorials.readthedocs.io](https://tobac-tutorials.readthedocs.io). Please have a look there, first!


## Getting Started

Tutorial notebooks for tobac 2.x (currently in active development). Please use them together with the [v2.0-dev](https://github.com/climate-processes/tobac/tree/v2.0-dev/) development branch. 

A step-by-step description to run the tutorials with jupyter is located [here](docs/RunningTutorials.md).


## Limitations

If you are using tobac 1.x, the notebooks here won#t work because of changes in the code structure. The equivalent notebooks can be found in the [examples](https://github.com/climate-processes/tobac/tree/master/examples) folder in the [tobac master branch](https://github.com/climate-processes/tobac/tree/master/examples).


## Contributing
You contribution is welcome! 

Each additional tutorial notbeook helps new `tobac` users to understand the capability of the tracking software and supports creative use of feature identification and tracking in the atmospheric science context.


### Pull Request Requirements

Please provide a separate pull request:

* **with your example notebook included**
  * please extensively use markdown elements to structure and explain your notebook
  * check already existing notebooks to get an idea about our tutorial style
  * please upload your example data to [zenodo]( https://zenodo.org/ ) (see next paragraph)
  * please check if your notebook is running in the recommended standard conda enviroment [see here]((docs/RunningTutorials.md) and update the [list of required python packages](./requirements.txt) if needed

* **with your suggestions to change the documentation elements**, e.g. `index.rst`
  * please care that sphinx-based rendering is still working correctly, [see here](docs/Testing-Sphinx-based-Rendering.md) for an intro to sphinx-based rendering of our tutorial content



### Example Data

Our tutorials live from realistic examples and example data.

We recommend: 
* to upload your example data (preferably as netcdf file) to [zenodo]( https://zenodo.org/ )
* to label the data such that "tobac" is included in the zenodo title

Already existing `tobac` data can be found here:
* [**tobac on zenodo**]( https://zenodo.org/search?page=1&size=20&q=tobac )

