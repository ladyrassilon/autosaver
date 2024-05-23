# AutoSaver

Given the issues in the world we all need to make savings, including our usage of various tools.

Takes a list of recomended savings from a trusted source, and then automatically applies them to your account.

## Current status 23/05/2024

The preliminary version of the notebook now works, its a little rough and ready, but if you run it following the instructions, it'll work through the list, and make sure you've got all the savings.

It'll report back if there's been a problem with applying any of the savings, and then you can re-run the script and it'll make sure all the savings are applied, I will try to make this step unnecessary in a future version.

## Prereqs

- An version of python 3.6 or greater. [Simple Install](https://www.datacamp.com/blog/how-to-install-python) [^1]
- [Firefox](https://www.mozilla.org/en-GB/firefox/) [^2]

## How to get running

### Checkout the repo
```bash
git clone https://github.com/ladyrassilon/autosaver.git
```
You could also download the repo from [github](https://github.com/ladyrassilon/autosaver)

### Install the dependencies

```bash
cd autosaver
pip install -r autosaver/requirements.txt 
```

You will see output of the form like this
```bash
Collecting ipywidgets (from ipython[notebook]->-r autosaver/requirements.txt (line 1))
  Obtaining dependency information for ipywidgets from https://files.pythonhosted.org/packages/70/1a/7edeedb1c089d63ccd8bd5c0612334774e90cf9337de9fe6c82d90081791/ipywidgets-8.1.2-py3-none-any.whl.metadata
  Using cached ipywidgets-8.1.2-py3-none-any.whl.metadata (2.4 kB)
Collecting notebook (from ipython[notebook]->-r autosaver/requirements.txt (line 1))
  Obtaining dependency information for notebook from https://files.pythonhosted.org/packages/64/76/4437268f47f452fb4cd5cf73fa831241ea8130ae0ab9c64d5c4ffca9f121/notebook-7.2.0-py3-none-any.whl.metadata
  Downloading notebook-7.2.0-py3-none-any.whl.metadata (10 kB)
Requirement already satisfied: types-python-dateutil>=2.8.10 in /Users/<homeuser>/.pyenv/versions/3.11.7/envs/autosaver/lib/python3.11/site-packages (from arrow>=0.15.0->isoduration->jsonschema>=4.18.0->jupyterlab-server<3,>=2.22.1->notebook->ipython[notebook]->-r requirements.txt (line 1)) (2.9.0.20240316)

[notice] A new release of pip is available: 23.2.1 -> 24.0
[notice] To update, run: python3.11 -m pip install --upgrade pip
```

### Get those savings
Run the notebook environment
```bash
jupyter-notebook 
```

Once you see output like this
```bash
[I 2024-05-22 17:34:03.247 ServerApp] Jupyter Server 2.14.0 is running at:
[I 2024-05-22 17:34:03.247 ServerApp] http://localhost:8888/tree?token=<a-mysterious-token>
[I 2024-05-22 17:34:03.247 ServerApp]     http://127.0.0.1:8888/tree?token=<a-mysterious-token>
[I 2024-05-22 17:34:03.247 ServerApp] Use Control-C to stop this server and shut down all kernels (twice to skip confirmation).
```
A browser should open.



## Sources

The savings lists are the two backup savings accounts after something unusual happened to the main savings account.

## Notebooks

- [Update Lists](./update-lists-with-private-api.ipynb) This updates the json/text files as needed, using instagram private api[^3]. 

## Why I'm doing this

Caelan Conrad suggested that this might be something important to help out with

https://www.youtube.com/watch?v=wj8ZxXonwFk

[![Hippocratic License HL3-BDS-CL-ECO-EXTR-FFD-LAW-MEDIA-MIL-MY-SUP-SV-TAL-USTA-XUAR](https://img.shields.io/static/v1?label=Hippocratic%20License&message=HL3-BDS-CL-ECO-EXTR-FFD-LAW-MEDIA-MIL-MY-SUP-SV-TAL-USTA-XUAR&labelColor=5e2751&color=bc8c3d)](https://firstdonoharm.dev/version/3/0/bds-cl-eco-extr-ffd-law-media-mil-my-sup-sv-tal-usta-xuar.html)

[^1]: I personally use [pyenv](https://github.com/pyenv/pyenv) to manage my python versions, but I have ~10 different ones on my computer, but you don't need anything like this if you're not doing development.

[^2]: It might work with chrome, or other automated browsers, but I was trying to get this to work asap, so I used firefox and haven't tested porting the code as yet.

[^3]: You shouldn't need to run this, because it uses an unsupported api that I do not trust/recommend you use with your main instagram account