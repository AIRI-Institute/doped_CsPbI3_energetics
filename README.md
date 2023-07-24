# Doped CsPbI<sub>3</sub> Energetics: Dataset for "Graph Neural Networks for Predicting Structural Stability of Cd- and Zn-doped $\gamma$-CsPbI<sub>3</sub>"

This repository contains various neural networks predictions on Cd- and Zn-doped $\gamma$-CsPbI<sub>3</sub> dataset.

More details can be found in the [paper](link).


If you are using this dataset in your research paper, please cite us as
```
bibtex citation
```

Dataset
-----
The dataset contains  Cd- and Zn-doped $\gamma$-CsPbI<sub>3</sub> systems and various neural networks predictions. Two models, *SchNet* and *allegro*^ were trained on different subsamples and with/without pretraining to illustrate ???

|       | both-both       | element-both    |
|-------|-----------------|-----------------|
| None  | [SchNet](https://github.com/AIRI-Institute/doped_CsPbI3_energetics/blob/main/data/nn%20inference/both_both_schnet_non-pr.pkl.gz), [allegro](https://github.com/AIRI-Institute/doped_CsPbI3_energetics/blob/main/data/nn%20inference/both_both_allegro_non-pr.pkl.gz) | [Schnet](https://github.com/AIRI-Institute/doped_CsPbI3_energetics/blob/main/data/nn%20inference/element_both_schnet_non-pr.pkl.gz), [allegro](https://github.com/AIRI-Institute/doped_CsPbI3_energetics/blob/main/data/nn%20inference/element_both_allegro_non-pr.pkl.gz) |
| OCP   | [allegro](https://github.com/AIRI-Institute/doped_CsPbI3_energetics/blob/main/data/nn%20inference/both_both_allegro_ocpr.pkl.gz)           | [allegro](https://github.com/AIRI-Institute/doped_CsPbI3_energetics/blob/main/data/nn%20inference/element_both_allegro_ocpr.pkl.gz)           |
| aflow | [allegro](https://github.com/AIRI-Institute/doped_CsPbI3_energetics/blob/main/data/nn%20inference/both_both_allegro_aflowpr.pkl.gz)           | [allegro](https://github.com/AIRI-Institute/doped_CsPbI3_energetics/blob/main/data/nn%20inference/element_both_allegro_aflowpr.pkl.gz)           |

| **Sample** | **Size** |
|:----------:|:--------:|
|  train_val |    142   |
|    test    |    60    |
|  inference |   73760  |

Скрипт
-----


Links
-----
* [Open Catalyst Project](https://opencatalystproject.org/index.html)
* [Schnet](https://arxiv.org/abs/1706.08566)
* [Allegro](https://arxiv.org/abs/2204.05249)
