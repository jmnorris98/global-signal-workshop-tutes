# Global Signal Data Analysis Workshop 

This repo contains tutorial notebooks and data
for the global signal data analysis workshop,
held on March 5, 2026. 

## Setting Up

Clone this repo, then intsall `uv` if you don't already have it:

```
curl -LsSf https://astral.sh/uv/install.sh | sh
```

Then make sure you're in the top-level directory of this repo
and do:

```
uv sync
```

Then install the jupyter kernel with

```
uv run python -m ipykernel install --user --name edges-workshop
```

Finally, get the data you'll need for this tutorial by doing:

```
mkdir data
wget https://galileo.sese.asu.edu/edges-data/2016-259.gsh5
wget https://galileo.sese.asu.edu/edges-data/2016-261.gsh5
wget https://galileo.sese.asu.edu/edges-data/2016-263.gsh5
wget https://galileo.sese.asu.edu/edges-data/2016-265.gsh5
mv *.gsh5 data/
```

## Following the tutorials

One of the sessions will be dedicated to going through the tutorials
to introduce both `pygsdata` and `edges-analysis`. 

The order of the tutorials is:

* `data_loading_writing.ipynb`
* `data_flagging.ipynb`
* `modeling_and_averaging.ipynb`

To run jupyter, simply do the following in the top-level
directory:

```
uv run jupyter lab
```

(If you already have a jupyter instance running elsewhere, that's totally fine,
just use that, but choose the `edges-workshop` kernel when you open the notebook.

