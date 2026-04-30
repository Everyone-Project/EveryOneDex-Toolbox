# EveryOneDex

**EveryOneDex** is a standalone analysis toolbox developed within the **EVERYONE Project** (*thE individual VulnERabilitY Of brain Network*). The platform estimates individual motor dexterity from resting-state functional connectomes using graph-theoretical measures of modular brain organization.


## Overview

EveryoneDex implements a fully automated pipeline that:

1. **Binarizes** weighted functional connectomes using adaptive percolation-based thresholding;
2. **Computes modularity** via Louvain community detection optimization;
3. **Extracts the participation index (PI)** from a set of predefined target regions of interest;
4. **Predicts manual dexterity** at the individual level using a pre-trained Support Vector Regression (SVR) model;
5. **Positions** the predicted dexterity score within the normative distribution derived from the Human Connectome Project (HCP) dataset.


## Input Requirements

The functional connectome provided as input must satisfy the following constraints:

* **Parcellation**: the connectome must be defined on the exact node set specified in `MEG_Parcel_EveryOne`, provided in `.xls` formats;
* **Directionality**: the matrix must be undirected (symmetric);
* **Edge weights**: edge values must represent functional connectivity (e.g., Pearson correlation coefficients);
* **Format**: the connectome must be provided as an *N* × *N* matrix consistent with the supplied parcel definition.


## Output

EveryoneDex returns a predicted dexterity score for the input subject, expressed in normalized units (population mean = 100, SD = 15), and positioned within the normative HCP distribution to facilitate individual-level interpretation.


## Citation

If you use EveryoneDex in your research, please cite:

> [WORK IN PROGRESS]


## License

This toolbox is distributed under the [MIT License](LICENSE).


## Contact

For questions or feedback, please open an issue on this repository or contact the corresponding author at andrea.caporali@unicam.it.

