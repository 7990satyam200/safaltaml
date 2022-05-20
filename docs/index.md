# Repo contains source code related to recommendation engine for all major properties

This Repo was build with major python packages:

 - [scikit-learn](https://www.mkdocs.org)
 - [implicit](https://squidfunk.github.io/mkdocs-material/)
 - [pandas](https://facelessuser.github.io/pymdown-extensions/)
 - [flask](https://facelessuser.github.io/pymdown-extensions/)
 - [numpy](https://facelessuser.github.io/pymdown-extensions/)


## Features
Repo contains source code related to recommendation engine for all major properties

* Models have custom CUDA kernels - enabling fitting on compatible GPU’s.

* Model Implementations uses Alternating Least Squares as described in the paper: http://yifanhu.net/PUB/cf.pdf

GPU Support requires **at least version 9 of the NVidia CUDA Toolkit**. The build will use the nvcc compiler that is
found on the path, but this can be overriden by setting the CUDAHOME enviroment variable to point to your cuda
installation.

Only if not already installed:
NVidia CUDA Toolkit Installation Instructions from [https://developer.nvidia.com/cuda-downloads?target_os=Linux]:


## Getting Started

Head over the [getting started](getting_started) guide

## Cool stuff

### Code Highlights

See [here](https://squidfunk.github.io/mkdocs-material/reference/code-blocks/) for doc

```python

print("Hello World!")
```

### Admonition

See [here](https://squidfunk.github.io/mkdocs-material/reference/admonitions/) for doc

!!! note "Hello There"
    General Kenobi!

??? note "Hello There"
    General Kenobi!

!!! error
    Boom!
