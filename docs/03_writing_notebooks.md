## Creating notebooks

Jupyter notebook is a web application where one can run Python and R codes. 
It is easy to share and deliver rich data analysis with Jupyter. 
A cell contains your Python code. The kernel will read the code one by one



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
Create a folder notebooks/, start the jupiter notebook,  and create a new notebook hello_world

```
jupyter notebook
```

Create a simple notebook with code:

```
import tensorflow as tf

hello = tf.constant('Hello, World!')
hello

```

