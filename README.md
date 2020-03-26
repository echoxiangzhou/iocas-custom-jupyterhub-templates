# Custom JupyterHub Templates for IODAP-IOCAS Ocean Data Analysis Platform

This repo contains html jinja2 templates for customising the appearance of JupyterHub. Each HTML file here will override the files in `https://github.com/jupyterhub/jupyterhub/tree/master/share/jupyterhub`.

## Usage

To use this repo ensure it is checked out and available somewhere that JupyterHub can find it. In thie example we will assume we have cloned it somewhere and created the following symlinks

`/path/to/repo/templates` -> `/usr/local/share/jupyterhub/custom_templates`
`/path/to/repo/assets` -> `/usr/local/share/jupyterhub/static/custom`

Add the following to your JupyterHub config

Configure JupyterHub.template_paths in the jupyterHub_config.yaml 
```python
c.JupyterHub.template_paths = ['/srv/conda/envs/pangeo/jupyterhub/custom_templates/']
```
