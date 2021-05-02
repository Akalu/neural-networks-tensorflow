## Tensorboard

Tensorboard is the interface used to visualize the graph and other tools to
understand, debug, and optimize the model.

1) Open notebook notebooks/tensorboard_demo.ipynb

2) Run all steps

3) To launch Tensorboard, you can use for example this command (tensorboard is always present in appropriate env directory):

```
c:\ProgramData\anaconda3\envs\test-tf\Scripts\tensorboard --logdir=.\notebooks\train\linregression
```

From active env this command could be more concise:

```
tensorboard --logdir=.\notebooks\train\linregression
```

Tensorboard will start at localhost:6006:

```
(test-tf) E:\repositories-my\tf>tensorboard --logdir=e:\repositories-my\neural-networks-tensorflow\notebooks\train\linregression\
2021-05-02 16:54:37.788567: W tensorflow/stream_executor/platform/default/dso_loader.cc:60] Could not load dynamic library 'cudart64_110.dll'; dlerror: cudart64_110.dll not found
2021-05-02 16:54:37.794279: I tensorflow/stream_executor/cuda/cudart_stub.cc:29] Ignore above cudart dlerror if you do not have a GPU set up on your machine.
W0502 16:54:39.810209  3388 plugin_event_accumulator.py:317] Found more than one graph event per run, or there was a metagraph containing a graph_def, as well as one or more graph events.  Overwriting the graph with the newest event
.
W0502 16:54:39.810209  3388 plugin_event_accumulator.py:329] Found more than one metagraph event per run. Overwriting the metagraph with the newest event.
Serving TensorBoard on localhost; to expose to the network, use a proxy or pass --bind_all
TensorBoard 2.5.0 at http://localhost:6006/ (Press CTRL+C to quit)

```