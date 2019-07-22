# 2019-07-23-codas-hep

Jim's tutorials for CoDaS-HEP:

   * [The Scientific Python Ecosystem](https://indico.cern.ch/event/814979/timetable/#40-the-scientific-python-ecosy), Tuesday, July 23, 2019 in [407 Jadwin Hall](https://goo.gl/maps/Hy7dUgKgp6eBU1N59).
   * [Columnar Data Analysis](https://indico.cern.ch/event/814979/timetable/#41-columnar-data-analysis), Wednesday, July 24, 2019 (same location).
   * [Accelerating Python](https://indico.cern.ch/event/814979/timetable/#12-accelerating-python), Wednesday, July 24, 2019 (same location).

To participate, launch a [private JupyterLab through SSL](https://ml-front.nautilus.optiputer.net/) as discussed in the CoDaS-HEP setup session. Open a terminal and type

```bash
git clone https://github.com/jpivarski/2019-07-23-codas-hep.git
```

then navigate in the file view (left sidebar) for `01-scientific-python-ecosystem.ipynb`. Under the **Kernel** menu, select **Change Kernel...** and pick the first option: "Python [conda env:codas-hep]".

Then follow along in the notebook while I present the same material as slides as a lecture. We can both change any cell to explore these topics interactively.

## Alternative way to participate

If the above doesn't work for you, click the button below.

<p align="center">
  <a href="https://mybinder.org/v2/gh/jpivarski/2019-07-23-codas-hep/0.2?urlpath=lab">
    <img src="https://mybinder.org/badge_logo.svg" alt="Launch Binder" height="40">
  </a>
</p>

Binder is free and public but doesn't let you save data and may be a little slow. However, you don't need to do the `git clone` or **Change Kernel...** The notebooks are ready to use after Binder launches (takes a minute or two).

## To get this software 

You might want to install some or all of this software on your laptop for later use. All of it can be installed using [conda](https://docs.conda.io/en/latest/miniconda.html) (except ROOT if you are using Windows) and [pip](https://realpython.com/what-is-pip) (except ROOT on all systems). ROOT can be manually installed [from here](https://root.cern/content/release-61800) (we use features from 6.18/00, the latest release).

You can pick and choose packages from [environment.yml](environment.yml) or you can install them all in an isolated environment (that can be removed at any time with `conda remove --name codashep-python-columnar --all`) with the following:

```bash
git clone https://github.com/jpivarski/2019-07-23-codas-hep.git
cd 2019-07-23-codas-hep
conda create -f environment.yml             # create an isolated environment and install everything
conda activate codashep-python-columnar     # switch to that environment (maybe "source activate...")
conda install jupyterlab                    # not included in the package because Binder has it
jupyter lab                                 # runs on your machine, controlled by your web browser
```
