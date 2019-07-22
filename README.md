# 2019-07-23-codas-hep

Jim's tutorials for CoDaS-HEP:

   * [The Scientific Python Ecosystem](https://indico.cern.ch/event/814979/timetable/#40-the-scientific-python-ecosy), Tuesday, July 23, 2019 in [407 Jadwin Hall](https://goo.gl/maps/Hy7dUgKgp6eBU1N59).
   * [Columnar Data Analysis](https://indico.cern.ch/event/814979/timetable/#41-columnar-data-analysis), Wednesday, July 24, 2019 (same location).
   * [Accelerating Python](https://indico.cern.ch/event/814979/timetable/#12-accelerating-python), Wednesday, July 24, 2019 (same location).

To participate, either launch a [private JupyterLab through SSL](https://ml-front.nautilus.optiputer.net/) (as discussed in the CoDaS-HEP setup session) or press this button

<a href="mybinder.org/v2/gh/jpivarski/2019-07-23-codas-hep/0.2?urlpath=lab" target="_blank"><img src="https://mybinder.org/badge_logo.svg" alt="Launch Binder"></a>
                           
to run it on Binder (free, public, but no saving of data and can be slow).

## To get this software 

You might want to install some or all of this software on your laptop for later use. All of it can be installed using [conda](https://docs.conda.io/en/latest/miniconda.html) (except ROOT if you are using Windows) and [pip](https://realpython.com/what-is-pip) (except ROOT on all systems).

You can pick and choose packages from [environment.yml](environment.yml) or you can install them all in an isolated environment (that can be removed at any time with `conda remove --name codashep-python-columnar --all`) with the following:

```bash
git clone https://github.com/jpivarski/2019-07-23-codas-hep.git
cd 2019-07-23-codas-hep
conda create -f environment.yml             # create an isolated environment and install everything
conda activate codashep-python-columnar     # switch to that environment (maybe "source activate...")
conda install jupyterlab                    # not included in the package because Binder has it
jupyter lab                                 # runs on your machine, controlled by your web browser
```
