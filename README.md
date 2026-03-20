[![DOI](https://zenodo.org/badge/DOI/10.5281/zenodo.19128415.svg)](https://doi.org/10.5281/zenodo.19128415)
[![python](https://img.shields.io/badge/Python-3.13.7-3776AB.svg?style=flat&logo=python&logoColor=white)](https://www.python.org)
[![License: MIT](https://img.shields.io/badge/License-MIT-blue.svg)](https://www.gnu.org/licenses/gpl-3.0)
[![mdr orcid](https://img.shields.io/badge/ORCID-0009--0008--1124--1420-A6CE39?style=flat&logo=orcid&logoColor=white)](https://orcid.org/0009-0008-1124-1420)
[![mdr github](https://img.shields.io/badge/GitHub-mruijzendaal-888.svg?style=flat&logo=github)](https://github.com/mruijzendaal)

# CO₂ Raman data and software for flow conservation laws 

This repository contains the script necessary to produce the figures in the publication M. D. Ruijzendaal *et al.*, "Flow recirculation and restriction in a CO₂ microwave plasma inferred from in-situ Raman scattering," *Plasma Sources Sci. Technol.*, 2026, [10.1088/1361-6595/ae4d87](http://dx.doi.org/10.1088/1361-6595/ae4d87).

Contents:
- `parse_data_and_fit.ipynb` for using the temperature and composition data of van de Steeg *et al.* ([10.1021/acsenergylett.1c01206](https://doi.org/10.1021/acsenergylett.1c01206)) and fitting mass- and heat flows to it.
- `radial_profiles_temperature_composition.ipynb` for plotting radial profiles of composition and specific enthalpy.
- `compare_flowrates.ipynb` for comparing the flowrates at different positions and flow conditions.
- `radiative_loss.ipynb` for calculating the radiative loss from the plasma.


## Installation
Tested on Python version 3.13.7.

1. Optional: create a virtual environment and activate it:  
  ```bash
  python -m venv venv
  source venv/bin/activate  # On Windows: venv\Scripts\activate
  ```  

2. Install the required packages:  
  ```bash
  pip install -r requirements.txt
  ```

3. Run the Jupyter notebooks to reproduce the figures. The recommended way to do this is to open the notebooks in VSCode and run the cells there. See the [Usage](#usage) section below for more details.

## Usage

First run `parse_data_and_fit.ipynb` to parse the data and fit the mass- and heat flows. This will save the fitted profiles in `output/data`. Repeat this for every measurement (10slm and 20slm, upstream and downstream).

Then run `radial_profiles_temperature_composition.ipynb` to plot the enthalpy profiles (Fig. 4, 6) and `compare_flowrates.ipynb` to compare the flowrates (Fig. 8). The resulting figures will be saved in `output/media/`.

## Citation

To cite the software and data in this repository:  
DOI: [10.5281/zenodo.19128415](http://doi.org/10.5281/zenodo.19128415)  
Bibtex:
```bibtex
@software{martijn_ruijzendaal_2026_19128415,
  author       = {Martijn Ruijzendaal},
  title        = {CO₂ Raman data and software for flow conservation laws},
  month        = mar,
  year         = 2026,
  publisher    = {Zenodo},
  version      = {v3.0},
  doi          = {10.5281/zenodo.19128415},
  url          = {https://doi.org/10.5281/zenodo.19128415},
}
```

To cite the article associated with this software:  
DOI: [10.1088/1361-6595/ae4d87](http://doi.org/10.1088/1361-6595/ae4d87)  
Bibtex:  
```bibtex
@article{Ruijzendaal2026,
  title = {Flow recirculation and restriction in a CO₂ microwave plasma inferred from in-situ Raman scattering},
  ISSN = {1361-6595},
  url = {http://dx.doi.org/10.1088/1361-6595/ae4d87},
  DOI = {10.1088/1361-6595/ae4d87},
  journal = {Plasma Sources Science and Technology},
  publisher = {IOP Publishing},
  author = {Ruijzendaal,  Martijn Daan and den Harder,  Niek and van Rooij,  Gerardus and Butterworth,  Thomas},
  year = {2026},
  month = mar 
}
```

