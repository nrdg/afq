# Jupyterhub

We maintain a [pangeo](http://pangeo.io/)-powered Jupyterhub at XXX.

To gain access to this hub, please ask Ariel to add you to the
[NRDG GitHub organization](https://github.com/nrdg). Please make sure that
your membership in the organization is set to public. That can be adjusted on
[this](https://github.com/orgs/nrdg/people) page.

## Installing other software

The computational environment in the hub is managed through a Docker
configuration that is stored in [its own repo](https://github.com/nrdg/hcp-pangeo-docker).
To add more [conda](https://docs.conda.io/en/latest/)-installed dependencies,
submit a PR with changes to the `environment.yml` file. The format of this
file is explained [here](https://docs.conda.io/projects/conda/en/latest/user-guide/tasks/manage-environments.html#create-env-file-manually). If you need
something installed using [Aptitude](https://wiki.debian.org/Aptitude), please
add that to the `apt.txt` file. This file contains one package per line. Imagine
you are running `sudo apt-get install $x` for each line of the file.
Additional *arbitrary* command line commands can be run by including them in
the `postBuild` file, so if there's something not covered by conda and apt,
add it in there. For now, we don't have automated builds for this, so once the
changes are merged, someone (Ariel, probably) will have to pull the changes
build the Docker image and then upload that into the hub.

## Jupyterlab

XXX

## Starting and using dask clusters in the hub

XXX
