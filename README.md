# Fast Conda-based Dev Containers + Codespaces

This is a template reposotory that can be used to start with a minimal Dev Container setup that provides conda and mamba for setting up Python environments.

Steps to use:

1. Create a repo of your own by cloning this template to your account.

**Work on your computer**
2. 

**Start working instantly on Codespaces**
2. From you clone of the template use the green button to create a codespace. You don't need to use any more than the base tier for the template, but depending on what you use for your environments, you may need more ram/disc space.

## Ways to customize the template

- Change the container name in [devcontainer.json](.devcontainer/devcontainer.json) on line 4.
- Change the default conda env name by changing the first line of [environment.yml](environment.yml) and change _python.defaultInterpreterPath_ in [devcontainer.json](.devcontainer/devcontainer.json).