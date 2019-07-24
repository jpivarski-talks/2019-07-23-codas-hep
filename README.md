# 2019-07-23-codas-hep

Jim's tutorials for CoDaS-HEP:

   * [The Scientific Python Ecosystem](https://indico.cern.ch/event/814979/timetable/#40-the-scientific-python-ecosy), Tuesday, July 23, 2019 in [407 Jadwin Hall](https://goo.gl/maps/Hy7dUgKgp6eBU1N59).
   * [Columnar Data Analysis](https://indico.cern.ch/event/814979/timetable/#41-columnar-data-analysis), Wednesday, July 24, 2019 (same location).
   * [Accelerating Python](https://indico.cern.ch/event/814979/timetable/#12-accelerating-python), Wednesday, July 24, 2019 (same location).

## How to participate (easy)

Press this button:

<p align="center">
  <a href="https://mybinder.org/v2/gh/jpivarski/2019-07-23-codas-hep/1.0?urlpath=lab">
    <img src="https://mybinder.org/badge_logo.svg" alt="Launch Binder" height="40">
  </a>
</p>

The exercises will run on a free public cloud service, which cannot save data and may take a minute or two to start up.

Navigate in the JupyterLab file view (left sidebar) to the desired lesson.

## How to participate using CoDaS-HEP resources

Launch a [private JupyterLab through SSL](https://ml-front.nautilus.optiputer.net/) as discussed in the CoDaS-HEP setup session (with the `ivukotic/ml_platform_auto:conda` image). In JupyterLab, click on "Terminal" and type (first time only):

```bash
cd /workspace
git clone https://github.com/jpivarski/2019-07-23-codas-hep.git
cd 2019-07-23-codas-hep
conda env create -f environment.yml
```

After the first time (e.g. on Wednesday; day 2), do

```bash
cd 2019-07-23-codas-hep
git pull
```

Then navigate in the JupyterLab file view (left sidebar) into the `2019-07-23-codas-hep` directory to the desired lesson. After you start the notebook, use the **Kernel** menu, **Change Kernel...** to ensure that it's in the `codashep-python-columnar` environment.

## To get this software on your laptop

**Short answer:** on a non-Windows computer, make sure you have [conda](https://docs.conda.io/en/latest/miniconda.html) installed and use the same instructions as the "CoDaS-HEP resources" section above (in your own choice of directory). Then switch to your new environment, manually install JupyterLab, and launch JupyterLab. It will open a web browser window and run on your machine.

```bash
conda activate codashep-python-columnar
conda install jupyterlab
jupyter lab
```

All of the software installed this way goes into an isolated environment that you can easily delete with

```bash
conda remove --name codashep-python-columnar --all
```

You can also look at [environment.yml](environment.yml) to pick and choose software to install. Everything in that list can be installed on Windows except ROOT, and everything can be installed using pip instead of conda except ROOT. The packages that must be installed with pip are in the `pip` section, and `root_numpy` must be installed _after_ ROOT. You can install ROOT manually [from here](https://root.cern/content/release-61800), and be sure to install the latest release, 6.18/00.
