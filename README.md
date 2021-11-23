[![status: experimental](https://github.com/GIScience/badges/raw/master/status/experimental.svg)](https://github.com/GIScience/badges#experimental)
[![MIT License](https://img.shields.io/badge/License-MIT-lightgray.svg)](LICENSE)
![Python Version](https://img.shields.io/badge/Python-3.9.0-blue.svg)

![Banner of NHS AI Lab Skunkworks ](docs/banner.png)

# NHS AI Lab Skunkworks project: Bed Tetris

The NHSX AI Skunkworks team and the Kettering General Hospital NHS Foundation Trust (KGH) commissioned a 12-week project via the Accelerated Capability Environment (ACE) to test whether Machine Learning (ML) can assist with the ‘bed tetris’ challenge.

Faculty, a world leading applied AI company was engaged 
to collaborate closely with KGH to develop a Proof of Concept (PoC) to demonstrate how artificial intelligence (AI) could be used to enable both site managers and less experienced staff members to allocate and optimise patient movement and safety within the hospital. 

## Intended Purpose

The PoC Hospital Bed Allocation Tool (the "Product") is provided strictly and only as a Proof-of-Concept. It is released for demonstration purposes only. In its current state the Product must not be integrated into any live hospital IT infrastructure and it is not suitable for use as a live service. It is being offered as prototype software and has been subject only to limited internal testing only. The Product is provided as-is and no guarantees are made as to its performance. Faculty makes no representation, warranty or undertaking, express or implied, as to the functionality, safety, accuracy, reliability, completeness or reasonableness of the Product or its performance. Faculty does not accept any liability whatsoever for any direct, consequential or indirect loss arising, directly or indirectly, from any use or reliance on this Product. 

## Description

This project consists of 4 components:
<ol>
<li> Virtual Hospital Environment
<li> Allocation Agents
<li> Demand Forecast
<li> UI
</ol>

The virtual hospital environment is within the `hospital` submodule (`src/hospital`). Guidance on usage is provided in `1.Virtual_Hospital_Environment.ipynb` notebook. 

The Allocation agents are within the `agent` submodule (`src/agent`). Guidance on usage and full documentation of the method if provided in the notebooks `2.Greedy_Allocation.ipynb` and `3.MCTS_Allocation.ipynb`. 

The deman forecast components including the Bayesian time series model are within the `forecasting` submodule (`src/forecasting`). However, to comply with IG regulations, the training data and model are not provdided. PDF versions of the forcasting notebooks are provided in `docs/`, along with schema information on the PAS and Patient Flow fields used, for pedagogical purposes. 

The UI component is built with Plotly Dash and designed to work with synthetic data.

## Installation

This project requires Python 3, If your system is running an older version
of Python we recommend creating a conda environment with Python 3.9 to install
the package.

For standard installation run `pip install .` from within the repo.

To install in dev mode with the [Pytest](https://docs.pytest.org/en/6.2.x/) testing suite available run
```pip install -e ."[testing]"```.

To launch the UI run `python app/run.py`.

## Licence

Unless stated otherwise, the codebase is released under [the MIT Licence][mit].
This covers both the codebase and any sample code in the documentation.

The documentation is [© Crown copyright][copyright] and available under the terms
of the [Open Government 3.0][ogl] licence.

[mit]: LICENCE
[copyright]: http://www.nationalarchives.gov.uk/information-management/re-using-public-sector-information/uk-government-licensing-framework/crown-copyright/
[ogl]: http://www.nationalarchives.gov.uk/doc/open-government-licence/version/3/