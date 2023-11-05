# Workshop 1

## Lokalnie

```bash
# create the conda env:
conda create -n workshop_applied_ml_1
conda activate workshop_applied_ml_1
```

Korzystamy channels z [conda-forge](https://anaconda.org/conda-forge/repo) i [fastchan](https://anaconda.org/fastchan):

```bash
# basic libs:
conda install --channel conda-forge -y jupyterlab \
                                       ipywidgets

conda install --channel fastchan -y nbdev

conda install --channel conda-forge -y scikit-learn \
                                       matplotlib \
                                       pandas
```

Zainstaluj `quarto` z pomocą instrukcji na [oficjalnej stronie](https://quarto.org/docs/get-started/) lub użyj komendy z `nbdev` ([Tutorial nbenv](https://nbdev.fast.ai/tutorials/tutorial.html)):

```bash
nbdev_install_quarto
```

Teraz jesteśmy gotowi do działania:

```bash
jupyter lab
```

Zainstaluj z pomocą Jupyter mgmt, abyśmy mogli skorzystać z funkjonalności `quarto`, na przykład diagramy [mermaid](https://mermaid.live): `jupyter_quarto`.

## Google Colab

0. (Optional) Fork the repository;
1. New notebook from github;
2. Uruchom według wskazówek.

Zauważ: dla diagramów [Mermaid](https://github.com/mermaid-js/mermaid) skorzystaj z [mermaid.live](https://mermaid.live).
