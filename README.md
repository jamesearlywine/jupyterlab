## Prerequisites

### Pyenv
https://github.com/pyenv/pyenv
#### Python 3.10

### Jupyter Lab 3.x
https://jupyter.org/install
- `pip install "jupyterlab>=3,<4"`
  - for compatibility with graph notebook
    - https://github.com/aws/graph-notebook

### YFiles for Neo4J Visualization
- https://github.com/yWorks/yfiles-jupyter-graphs-for-neo4j
  - `pip install yfiles_jupyter_graphs_for_neo4j`

## Start Jupyter Lab
- `jupyter lab`

## Start Neo4j
```
docker run \
    --publish=7474:7474 --publish=7687:7687 \
    --volume=$(pwd)/neo4j-data:/data \
    neo4j
```
---
## Optional
### TSLab for typescript notebooks
https://github.com/yunabe/tslab
- `npm install -g tslab`
- `tslab install`

#### Install typescript notebook dependencies
- `npm init -y`
- `npm install --save-dev typescript @types/node`
- `npm install --save-dev aws-sdk`
- ..any other dependencies you want to add to the ambient context for import within notebooks

#### Typescript graph visualization
- https://visjs.github.io/vis-network/examples/

---
### Graph Notebook (visualization isn't working)
https://github.com/aws/graph-notebook
- `pip install "graph-notebook`
- copy sample graph notebook
  - `python -m graph_notebook.notebooks.install --destination ~/jupyterlab`
- fix magic cell
  - `python -m graph_notebook.ipython_profile.configure_ipython_profile`
- start jupyter lab graph notebook
  - `python -m graph_notebook.start_jupyterlab --jupyter-dir ~/notebook/destination/dir`
    - `python -m graph_notebook.start_jupyterlab --jupyter-dir ./`
