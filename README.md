# CO₂ Raman data and software for flow conservation laws 

This repository contains the script necessary to produce the figures in the publication M. D. Ruijzendaal *et al.*, "Flow recirculation and restriction in a CO₂ microwave plasma inferred from in-situ Raman scattering," *Plasma Sources Sci. Technol.*, 2026, doi: [10.1088/1361-6595/ae4d87](http://dx.doi.org/10.1088/1361-6595/ae4d87).

- `parse_data_and_fit.ipynb` for using the output data of Alex (temperatures and compositions) and fitting mass- and heat flows to it.
- `enthalpy_profiles.ipynb` for plotting the enthalpy profiles.


## Installation
Recommended Python version: 3.13.7

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

Please cite the following article when using the data or software in this repository:  
DOI: [10.1088/1361-6595/ae4d87](http://dx.doi.org/10.1088/1361-6595/ae4d87)  
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