# Fast Conda-based Dev Containers + Codespaces

This is a template repository that can be used to start with a minimal [Dev Container](https://containers.dev/) setup that provides [conda](https://github.com/conda/conda) and [mamba](https://github.com/mamba-org/mamba) for setting up Python environments.
This repo contains a sample Conda environment file ([environment.yml](environment.yml)), demo Jupyter notebook, and Dev Container configuration files that describe how a containerized development can be built for the repo.
These configuration files work for both local Dev Containers as well as [Codespaces](https://github.com/features/codespaces), a GitHub-hosted cloud environment.

The Docker setup for the Dev Container starts with a miniconda image that then will install whatever conda environment file you have at the root of the repo.
There are some additional configuration options in the comments of the [Docker](.devcontainer/Dockerfile) and [devcontainer.json](.devcontainer/devcontainer.json) that have some examples of other steps you may want to add to your Dev Container, like what VS Code extensions to install when the container is launched.

## How to use this template

0. Create a repo of your own by [creating a repo from this template](https://docs.github.com/en/repositories/creating-and-managing-repositories/creating-a-repository-from-a-template) to your GitHub account.

### Work on your computer (requires Docker and VS Code installed)

1. Clone your newly created repo to your local machine and open it in VS Code.
2. Install the Remote Development extension (if you don't already have it).
3. Open the command pallet and run _Dev Containers: Reopen in Container_. Alternately, you can click on the left-most button on the bottom status bar (little arrows facing each other) and choose _Reopen in Container_.
4. This will take a few minutes to download the Docker image and build the rest of the container.
5. You should now have a VS Code window with your clone of the template repo open, running in a local Dev Container.

### Start working instantly on Codespaces

1. From you clone of the template use the green _Code_ button to create a codespace. If you click the triple dots you can customize the type of machine you want to be running your Codespace. You don't need to use any more than the 2-core for the template, but depending on what you use for your environments, you may need more ram/disc space.
2. The Codespace will take a few moments to start, which can be shortened by turning on Codespaces Pre-Builds on your repo*.
3. You should now have a VS Code window in your browser with your clone of the template repo open, running in a Codespace.

\* This can get expensive so make sure to check the settings when enabling this feature.

## Ways to customize the template

- Change the container `name` in [devcontainer.json](.devcontainer/devcontainer.json).
- Change the default conda env name by changing the first line of [environment.yml](environment.yml) and change _python.defaultInterpreterPath_ in [devcontainer.json](.devcontainer/devcontainer.json).
