# Cd- and Zn-doped CsPbI<sub>3</sub> Energetics: DFT-derived Properties and GNN-based Predictions

This repository contains various neural networks predictions on Cd- and Zn-doped $\gamma$-CsPbI<sub>3</sub> dataset.
<!--
More details can be found in the [paper](link).

If you are using this dataset in your research paper, please cite us as
```
bibtex citation
```
-->

Dataset
-----
The dataset contains  Cd- and Zn-doped $\gamma$-CsPbI<sub>3</sub> systems and various neural networks predictions. Two models, *SchNet* and *Allegro*^ were trained on different subsamples and with/without pretraining to illustrate ???

|   pretraining mode  | both-both       | element-both    |
|-------|-----------------|-----------------|
| non-pretrained  | [SchNet](https://github.com/AIRI-Institute/doped_CsPbI3_energetics/blob/main/data/nn%20inference/both_both_schnet_non-pr.pkl.gz), [Allegro](https://github.com/AIRI-Institute/doped_CsPbI3_energetics/blob/main/data/nn%20inference/both_both_allegro_non-pr.pkl.gz) | [SchNet](https://github.com/AIRI-Institute/doped_CsPbI3_energetics/blob/main/data/nn%20inference/element_both_schnet_non-pr.pkl.gz), [Allegro](https://github.com/AIRI-Institute/doped_CsPbI3_energetics/blob/main/data/nn%20inference/element_both_allegro_non-pr.pkl.gz) |
| [OCP](https://opencatalystproject.org/index.html)   | [Allegro](https://github.com/AIRI-Institute/doped_CsPbI3_energetics/blob/main/data/nn%20inference/both_both_allegro_ocpr.pkl.gz)           | [Allegro](https://github.com/AIRI-Institute/doped_CsPbI3_energetics/blob/main/data/nn%20inference/element_both_allegro_ocpr.pkl.gz)           |
| [aflow](https://www.aflowlib.org) | [Allegro](https://github.com/AIRI-Institute/doped_CsPbI3_energetics/blob/main/data/nn%20inference/both_both_allegro_aflowpr.pkl.gz)           | [Allegro](https://github.com/AIRI-Institute/doped_CsPbI3_energetics/blob/main/data/nn%20inference/element_both_allegro_aflowpr.pkl.gz)           |

<!--
| **Sample** | **Size** |
|:----------:|:--------:|
|  train_val |    142   |
|    test    |    60    |
|  inference |   73760  |
-->

Скрипт
-----


Models
-----
* [SchNet: A continuous-filter convolutional neural network for modeling quantum interactions](https://arxiv.org/abs/1706.08566)
* [Learning Local Equivariant Representations for Large-Scale Atomistic Dynamics (Allegro)](https://arxiv.org/abs/2204.05249)

| ordinal number | column tag | content description |
| --- | --- | --- |
|1| phase | yellow/black (corresponds to the phase studied) |
|2| supercell | the supercells used (depends on phase) |
|3| subst | the number of substituted Pb positions |
|4| index | structure id (unique within a certain composition) |
|5| weight | corresponds to the number of symmetrically equivalent structures within combinatorial composition/configuration space |
|6| dopant | Cd/Zn (dopant type in the structure) |
|7| space_group_number | space symmetry of the doped structure before relaxation |
|8| formula | chemical formula (OrderedDict type) |
|9| natoms | 160 (the number of atoms in the model cells - constant feature) |
|10| atomic_numbers | atomic numbers of the structure |
|11| nelements | the number of chemical elements in the structure |
|12| cell | model cell sizes (before relaxation - constant feature for a certain phase) |
|13| pos | atomic positions (before relaxation) |
|14-61| val_i | GNN-predicted formation energy per atom (in eV/atom) for the $i^{th}$ validation subset |
|62| relaxed_cell_DFT | model cell sizes after DFT relaxation |
|63| relaxed_pos_DFT | DFT-relaxed atomic positions |
|64| relaxed_pressure_DFT | pressure (in kbar) for the DFT-relaxed structure |
|65| relaxed_forces_DFT | atomic forces (in eV/angstrom) for the DFT-relaxed structure |
|66| relaxed_energy_DFT | relaxed energy per cell (in eV) for the DFT-relaxed structure |
|67| relaxed_energy_pa_DFT | relaxed energy per atom (in eV/atom) for the DFT-relaxed structure |
|68| formation_energy_pa_DFT | formation energy per atom (in eV/atom) for the DFT-relaxed structure |
|69-116| val_i_DFT | boolean flag showing whether the configuration is in the $i^{th}$ validation subset |
|117| inWhichPart | tr_val, test, or inference (corresponds to the data usage within the approach proposed)|
