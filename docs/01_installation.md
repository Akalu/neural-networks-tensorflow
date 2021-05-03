## Installing TensorFlow

Requirements:

* Python (any version).
* Anaconda Distribution Package.

1) download and install the latest version of Anaconda from https://www.anaconda.com/products/individual
2) activate c:\ProgramData\Anaconda3\Scripts\activate base

Create a test environment for ML projects

use a simple description file for that from 
name: test-tf
dependencies:
  - python=3.8
  - jupyter
  - ipython
  - pandas

NOTE: on windows installation one can get the http connection error when performing network operations on the anaconda 
(see https://stackoverflow.com/questions/42563757/conda-update-condahttperror-http-none)

In this case copy libcrypto-1_1-x64.dll and libssl-1_1-x64.dll from anaconda3\Library\bin to anaconda3\DLLs directory

```
c:\ProgramData\Anaconda3>.\Scripts\conda.exe update conda

Collecting package metadata (current_repodata.json): done
Solving environment: done

## Package Plan ##

  environment location: c:\ProgramData\Anaconda3

  added / updated specs:
    - conda
```
Create a new environment:

```
c:\ProgramData\Anaconda3>.\Scripts\conda.exe env create -f test-tf.yml

Collecting package metadata (repodata.json): done
Solving environment: done

Downloading and Extracting Packages
defusedxml-0.7.1     | 23 KB     | ############################################################################ | 100%
cffi-1.14.5          | 224 KB    | ############################################################################ | 100%
argon2-cffi-20.1.0   | 49 KB     | ############################################################################ | 100%

...

nest-asyncio-1.5.1   | 10 KB     | ############################################################################ | 100%
Preparing transaction: done
Verifying transaction: done
Executing transaction: / DEBUG menuinst_win32:__init__(198): Menu: name: 'Anaconda${PY_VER} ${PLATFORM}', prefix: 'c:\ProgramData\Anaconda3\envs\test-tf', env_name: 'test-tf', mode: 'system', used_mode: 'system'
DEBUG menuinst_win32:create(323): Shortcut cmd is c:\ProgramData\Anaconda3\python.exe, args are ['c:\\ProgramData\\Anaconda3\\cwp.py', 'c:\\ProgramData\\Anaconda3\\envs\\test-tf', 'c:\\ProgramData\\Anaconda3\\envs\\test-tf\\python.exe', 'c:\\ProgramData\\Anaconda3\\envs\\test-tf\\Scripts\\jupyter-notebook-script.py', '"%USERPROFILE%/"']
done
#
# To activate this environment, use
#
#     $ conda activate test-tf
#
# To deactivate an active environment, use
#
#     $ conda deactivate

```


List available environments:

```
c:\ProgramData\Anaconda3>.\Scripts\conda.exe env list
# conda environments:
#
base                  *  c:\ProgramData\Anaconda3
test-tf                  c:\ProgramData\Anaconda3\envs\test-tf
```

Activate necessary environment:

```
c:\ProgramData\Anaconda3>.\Scripts\activate test-tf

(test-tf) c:\ProgramData\Anaconda3>
```
	
Check that all necessary components have been installed in the same environment using where command:

```
(test-tf) c:\ProgramData\Anaconda3>where python
c:\ProgramData\Anaconda3\python.exe
c:\ProgramData\Anaconda3\envs\test-tf\python.exe


(test-tf) c:\ProgramData\Anaconda3>where jupyter
c:\ProgramData\Anaconda3\envs\test-tf\Scripts\jupyter.exe

(test-tf) c:\ProgramData\Anaconda3>where ipython
c:\ProgramData\Anaconda3\envs\test-tf\Scripts\ipython.exe
```

For windows it is necessary to install TensorFlow in a separate command:

```
pip install tensorflow
```

After succesful installation open Jupyter notebook to test the environment:

```
jupyter notebook
```

It starts by http://localhost:8888



A newly created conda environment one can use along with PyCharm or similar IDEs:

1) Click on Configure -> Settings to open up settings in PyCharm

2) Navigate to Project -> Project Interpreter

3) Click on Add local via the Settings button

4) Select "conda environment"

5) Click on "Existing environment" and navigate to the environment that you want to use. Note that you have to select the bin/python file inside the conda environment for PyCharm to be able to recognise the environment

6) Make sure to click the "Make available to all projects" if you want the interpreter to be used by multiple projects

