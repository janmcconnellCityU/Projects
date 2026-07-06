# 🛰️ Satellite Orbit Data Exploration

<p align="left">
  <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/python/python-original.svg" width="35"/>
  <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/pandas/pandas-original.svg" width="35"/>
  <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/matplotlib/matplotlib-original.svg" width="35"/>
  <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/jupyter/jupyter-original.svg" width="35"/>
  <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/vscode/vscode-original.svg" width="35"/>
</p>

This project explores orbital element data for active satellites using publicly available datasets from Celestrak. The goal is to examine how satellites are distributed across different orbital regimes and to identify patterns in their orbital characteristics.

Satellite orbits are described using parameters derived from NORAD Two-Line Element (TLE) records. These parameters capture the orientation, shape, and motion of each orbit. By analyzing these variables, it is possible to observe clear clustering patterns that reflect how modern satellite systems are designed and deployed.

The notebook performs exploratory analysis on several key orbital parameters, including inclination, eccentricity, and mean motion. Derived variables such as orbital period are calculated, and visualizations are used to reveal structure within the satellite population and highlight unusual or highly elliptical orbits.

## ❓ Key Questions

This exploration focuses on several simple questions:

- How are satellites distributed across different orbital regimes?
- What inclinations are most common in modern satellite deployments?
- Which satellites have highly elliptical or unusual orbits?
- What patterns emerge when orbital motion and inclination are analyzed together?

## 🔍 Topics Explored

The notebook demonstrates a small exploratory data analysis workflow using Python and pandas.

Key topics include:
- orbital regime classification (LEO, MEO, high orbit)
- distribution of orbital inclinations
- detection of highly elliptical orbits
- visualization of relationships between orbital parameters
- identification of clusters representing common orbital corridors

## 📊 Observations from the Data

A few clear patterns appear in the satellite population:
- Most satellites operate in Low Earth Orbit (LEO) with orbital periods of roughly 90 to 100 minutes.
- Large clusters of satellites appear near 53° inclination, reflecting modern communication constellations.
- A strong peak near 98° inclination corresponds to sun-synchronous Earth observation orbits.
- A small number of satellites use highly elliptical orbits, often for scientific missions or high-latitude communications.

These patterns illustrate how satellite deployments concentrate in specific orbital corridors designed for particular mission types.

Dataset

This analysis uses publicly available satellite orbital element data from Celestrak.

## 🌐 Dataset Source
https://celestrak.org/NORAD/elements/gp.php?GROUP=active&FORMAT=csv

The dataset contains orbital element parameters derived from NORAD Two-Line Element records, including mean motion, eccentricity, inclination, and other orbital parameters.

The dataset is not stored in this repository because the element sets are updated frequently.

To reproduce the analysis, download the CSV from the link above and place it in the project directory as:

NORAD_elements.csv

## 🧰 Tools Used

<p>&nbsp&nbsp&nbsp&nbsp&nbsp&nbsp&nbsp&nbsp&nbsp&nbsp<img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/python/python-original.svg" width="24"/> <b>Python</b> – data analysis and scripting</p>
<p>&nbsp&nbsp&nbsp&nbsp&nbsp&nbsp&nbsp&nbsp&nbsp&nbsp<img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/pandas/pandas-original.svg" width="24"/> <b>pandas</b> – data manipulation and exploratory analysis</p>
<p>&nbsp&nbsp&nbsp&nbsp&nbsp&nbsp&nbsp&nbsp&nbsp&nbsp<img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/matplotlib/matplotlib-original.svg" width="24"/> <b>matplotlib</b> – data visualization</p>
<p>&nbsp&nbsp&nbsp&nbsp&nbsp&nbsp&nbsp&nbsp&nbsp&nbsp<img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/jupyter/jupyter-original.svg" width="24"/> <b>Jupyter Notebook</b> – interactive analysis environment</p>
<p>&nbsp&nbsp&nbsp&nbsp&nbsp&nbsp&nbsp&nbsp&nbsp&nbsp<img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/vscode/vscode-original.svg" width="24"/> <b>Visual Studio Code</b> – development environment for running notebooks and managing the project</p>
