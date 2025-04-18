# Deep Heart Segmentation

Fully automatic deep learning system to segment the heart in CT scans.

## Repository Structure

The DeepHeartSeg repository is structured as follows:

* All the source code to run the deep-learning-based pipeline is found under the `src` folder.
* Four sample subjects' CT data and the associated manual segmentation masks, as well as all the models weights necessary to run the pipeline, are stored under the `data` folder.

Additional details on the content of the subdirectories and their structure can be found in the markdown files stored in the former.

## Max's Miniconda Set-up
### DeepHeartSeg Setup with Miniconda

This guide walks you through setting up the DeepHeartSeg environment using Miniconda.

### Prerequisites
- Ensure [Miniconda](https://docs.conda.io/en/latest/miniconda.html) is installed.
- DeepHeartSeg was developed and tested with Python 2.7.

### Steps

Open a terminal and create a new conda environment named `deepheartseg` with Python 2.7:

Ensure you are operating within the appropriate working directory.

```
conda env create -f environment.yml

```


## Original Recommended Set-up

This code was developed and tested using Python 2.7.17.

For the code to run as intended, all the packages under `requirements.txt` should be installed. In order not to break previous installations and ensure full compatibility, it's highly recommended to create a virtual environment to run the DeepCAC pipeline in. Here follows an example of set-up using `python virtualenv`:

```
# install python's virtualenv
sudo pip install virtualenv

# parse the path to the python2 interpreter
export PY2PATH=$(which python2)

# create a virtualenv with such python2 interpreter named "venv"
# (common name, already found in .gitignore)
virtualenv -p $PY2PATH venv 

# activate the virtualenv
source venv/bin/activate
```

At this point, `(venv)` should be displayed at the start of each bash line. Furthermore, the command `which python2` should return a path similar to `/path/to/folder/venv/bin/python2`. Once the virtual environment is activated:

```
# once the virtualenv is activated, install the dependencies
pip install -r requirements.txt
```

At this stage, everything should be ready for the data to be processed by 
the DeepHeartSeg pipeline. Additional details can be found in the markdown file 
under `src`.

The virtual environment can be deactivated by running:

```
deactivate
```

## Acknowledgements

Code development: RZ <br>
Code testing, refactoring and documentation: DB

## Disclaimer

The code and data of this repository are provided to promote reproducible 
research. They are not intended for clinical care or commercial use.

The software is provided "as is", without warranty of any kind, express or 
implied, including but not limited to the warranties of merchantability, 
fitness for a particular purpose and noninfringement. In no event shall the 
authors or copyright holders be liable for any claim, damages or other 
liability, whether in an action of contract, tort or otherwise, arising 
from, out of or in connection with the software or the use or other 
dealings in the software.
