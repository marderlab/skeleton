# skeleton

MATLAB class to view, manipulate and analyse skeletons of neurons (in `.xml` or `.nml` file formats)


## Installation 

Clone this repository, or download all the files here. 

You will also need an additional toolbox. The recommended way to install that is using my package manager:

```matlab
urlwrite('http://srinivas.gs/install.m','install.m');
install sg-s/srinivas.gs_mtools
```

## Usage

Load a new `.xml` or `.nml` file:

```
s = skeleton('path/to/neuron.xml')
```

Visualize 3D structure

```
s.plot
```

Trace all processes from soma to terminals

```
s.traceProcesses;
```

Measure all process lengths

```
s.measureProcessLengths;
```

### Extended usage

hash the skeleton structure (converts the object into a md5 hash):

```
h = hash(s);
```

SHow the number of components, and get endpoints of all components (useful if your reconstruction has disconnected components that you want to fix):

```
s.getComponentEndpoints;
```

Measure "tortuosity", as defined in [this paper](https://elifesciences.org/articles/22352)

```
s.measureTortuosity
```


## License

GPLv3