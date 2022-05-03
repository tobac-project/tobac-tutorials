
# How to Check if Sphinx-based Rendering of `tobac-tutorials` is Working?

## Setup 

The workflow has been tested in a linux system. We aim to build a static website out of the documentation material (incl. jupyter notebooks) present in `tobac-tutorials`.


### 1. Preparing the Local Environment

* **choose a separate place for your testing**

  I will use the temporary directory `/tmp/website-testing` which I need to create. You can use a dedicated place of your choice ...
  
  ```bash
  > mkdir /tmp/website-testing
  > cd /tmp/website-testing
  ```
  I will indicate my position now with the `/tmp/website-testing>` prompt.

* **get the official repository**

  ```bash
  /tmp/website-testing> git clone https://github.com/climate-processes/tobac-tutorials
  ```
  
* **Python environment**
    * create a python virtual env
        ```bash
        /tmp/website-testing> python -m venv .python3-venv
        ```
        
    * and install requirements
        ```bash
        # deactivation conda is only necessary if your loaded conda before ...
        /tmp/website-testing> conda deactivate

        # activate the new env and upgrade `pip`
        /tmp/website-testing> source .python3-venv/bin/activate
        /tmp/website-testing> pip install --upgrade pip
        
        # now everything is installed into the local python env!
        /tmp/website-testing> pip install -r tobac-tutorials/requirements.txt

        ```
        `pip`-based installation takes a bit of time, but is much faster than `conda`. If the installation runs without problems, you are ready to build the website.


### 2. Building the Website

Actually, only few steps are needed to build the website, i.e.


* **running sphinx for rendering**

    ```bash
    /tmp/website-testing> cd tobac-tutorials

    /tmp/website-testing/tobac-tutorials> make html
    ```
    
    If no severe error appeared
    
    
* **view the HTML content**

    ```bash
    /tmp/website-testing/tobac-tutorials> firefox _build/html/index.html
    ```


### 3. Parsing Your Local Changes

Now, we connect to your locally hosted `tobac-tutorials` repository and your development branch.

* **connect to your local repo**: 
    Assume your repo is located at `/tmp/tobac-tutorial-testing/tobac-tutorials`, then add a new remote alias and fetch all content with

    ```bash
    /tmp/website-testing/tobac-tutorials> git remote add local-repo /tmp/tobac-tutorial-testing/tobac-tutorials
    /tmp/website-testing/tobac-tutorials> git fetch --all
    ```    
* **check your development branch out**:
    Now, assume the your development branch is called `my-devel`, then do
  
    ```bash
    # to get a first overview on available branches
    /tmp/website-testing/tobac-tutorials> git branch --all
    
    # and then actually get your development branch
    /tmp/website-testing/tobac-tutorials> git checkout -b my-devel local-repo/my-devel
    ```
    
    You should see your developments, now ...
    
* **build and view website again**

    ```bash    
    /tmp/website-testing/tobac-tutorials> make clean
    /tmp/website-testing/tobac-tutorials> make html
    /tmp/website-testing/tobac-tutorials> firefox _build/html/index.html
    ```

