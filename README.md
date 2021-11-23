[![status: experimental](https://github.com/GIScience/badges/raw/master/status/experimental.svg)](https://github.com/GIScience/badges#experimental)
[![MIT License](https://img.shields.io/badge/License-MIT-lightgray.svg)](LICENSE)
![Python Version](https://img.shields.io/badge/Python-3.9.0-blue.svg)

![Banner of NHS AI Lab Skunkworks ](docs/banner.png)

# NHS AI Lab Skunkworks project: Bed Allocation

> A pilot project for the NHS AI (Artificial Intelligence) Lab Skunkworks team, Bed Allocation aims to explore whether machine learning can effectively aid bed management in Kettering General Hospital.

Bed Allocation was selected as a project in {DATE SELECTED} following a succesful pitch to the AI Skunkworks problem-sourcing programme.

## Intended Use

This proof of concept ([TRL 4](https://en.wikipedia.org/wiki/Technology_readiness_level)) is intended to demonstrate different approaches to forecasting and bed allocation using machine learning. It is not intended for deployment in a clinical or non-clinical setting without further development and compliance with the [UK Medical Device Regulations 2002](https://www.legislation.gov.uk/uksi/2002/618/contents/made) where the product qualifies as a medical device.

## Background

The NHS AI Lab Skunkworks team and the Kettering General Hospital NHS Foundation Trust (KGH) commissioned a 12-week project via the Accelerated Capability Environment (ACE) to test whether Machine Learning (ML) can assist with bed allocation.

Faculty, an applied AI company, was engaged 
to collaborate closely with KGH to develop a Proof of Concept (PoC) to demonstrate how artificial intelligence (AI) could be used to enable both site managers and less experienced staff members to allocate and optimise patient movement and safety within the hospital. 

## Data Protection

This project was subject to a Data Protection Impact Assessment (DPIA), ensuring the protection of the data used in line with the [UK Data Protection Act 2018](https://www.legislation.gov.uk/ukpga/2018/12/contents/enacted) and [UK GDPR](https://ico.org.uk/for-organisations/dp-at-the-end-of-the-transition-period/data-protection-and-the-eu-in-detail/the-uk-gdpr/). No data or trained models are shared in this repository.

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