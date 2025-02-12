# Geomstats: a deep dive into discrete surfaces implementation

This repo contains installation instructions and small examples regarding the tutorial "Geomstats: a deep dive into discrete surfaces implementation", presented at [Infinite-dimensional Geometry: Theory and Applications](https://www.esi.ac.at/events/e550/).


## Installation

### Create a virtual environment

To avoid conflicts with other packages, let's start by creating a [conda environment](https://docs.conda.io/projects/conda/en/latest/user-guide/tasks/manage-environments.html) (feel free to use any alternative - e.g. [venv](https://docs.python.org/3/library/venv.html) -, or even install it in an existing environment):

```bash
conda create -n geomstats-esi python=3.12
```

To activate the environment:

```bash
conda activate geomstats-esi
```

Make sure you are within the environment. Do e.g.

```bash
which python
```

and verify python path is something like: `/home/<username>/miniconda3/envs/geomstats-esi/bin/python`.



### Install `geomstats`


You may want to look at `geomstats` code during the tutorial. For that purpose, cloning the repo may be the best way to bring `geomstats` locally:

```bash
git clone https://github.com/geomstats/geomstats.git
```


Installation can be done by:

```bash
cd geomstats
pip install -e .[pytorch,pykeops]
```

Some explanation:

* `cd geomstats` moves within `geomstats` root folder

* `-e` stands for editable, meaning your installation will be connected to the cloned folder (not necessary, but nice)

* `.` means "this directory"

* whithin square brackets are optional dependencies: we will need `pytorch` and `pykeops` (they both use gpu acceleration, but it is not essential for our purposes)


NB: if `zshell` (macos users), remember to backslash square brackets `pip install -e .\[pytorch,pykeops\]`.



Alternatively, you can install the latest released `geomstats` version from [PyPI](https://pypi.org/project/geomstats/).

```bash
pip install geomstats[pytorch,pykeops]
```

Or install the latest `geomstats` code directly from [github](https://github.com/geomstats/geomstats):



```bash
pip install geomstats[pytorch,pykeops]@git+https://github.com/geomstats/geomstats.git@main
```

Both are stable. github version is up to date.


### Install other dependencies


For preprocessing and data downloading, we also need [polpo](https://geometric-intelligence.github.io/polpo/index.html) (see [repo](https://github.com/geometric-intelligence/polpo)):



```bash
pip install polpo@git+https://github.com/geometric-intelligence/polpo.git@main
```

Additional dependencies:


```bash
pip install requests trimesh pyvista jupyter
```

If you get a dead kernel when trying to plot with `pyvista`, do also:

```bash
conda install gcc=12.1.0
```


## Resources


Papers:

* [(Hartman, 2023)](https://link.springer.com/article/10.1007/s11263-022-01743-0)

* [(Guigui, 2023)](https://ieeexplore.ieee.org/document/10063225)



Documentation:

* [geomstats](https://geomstats.github.io/)

* [polpo](https://geometric-intelligence.github.io/polpo/) (in particular, see [how-tos](https://geometric-intelligence.github.io/polpo/how_to/index.html))


Repos:

* [geomstats](https://github.com/geomstats/geomstats)

* [polpo](https://github.com/geometric-intelligence/polpo)



