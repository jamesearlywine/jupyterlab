# Prerequisites

### Pyenv
https://github.com/pyenv/pyenv
#### Python 3.10

### Jupyter Lab 3.x
https://jupyter.org/install
- `pip install "jupyterlab>=3,<4"`
  - for compatibility with graph notebook
    - https://github.com/aws/graph-notebook

### TSLab (for typescript)
https://github.com/yunabe/tslab
- `npm install -g tslab`
- `tslab install`

### Graph Notebook
https://github.com/aws/graph-notebook
- `pip install graph-notebook`
- copy sample graph notebook
  - `python -m graph_notebook.notebooks.install --destination ~/jupyterlab`
- fix magic cell
  - `python -m graph_notebook.ipython_profile.configure_ipython_profile`
- start jupyter lab graph notebook
  - `python -m graph_notebook.start_jupyterlab --jupyter-dir ~/notebook/destination/dir`
  - `jupyter-up.sh`

### Install typescript notebook dependencies
- `npm init -y`
- `npm install --save-dev typescript @types/node`
- `npm install --save-dev aws-sdk`
- ..any other dependencies you want to add to the mabient context for import within notebooks

# start jupyterlab
- `jupyter lab`

# start Neo4j
```
docker run \
    --publish=7474:7474 --publish=7687:7687 \
    --volume=$(PWD)/neo4j-data:/data \
    neo4j
```