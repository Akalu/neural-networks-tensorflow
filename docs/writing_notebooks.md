## Creating notebooks

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

