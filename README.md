# 2023neckconnective

This repository collates the annotations and example code for Stürner and Brooks et al. "Comparative connectomics of the descending and ascending neurons of the Drosophila nervous system: stereotypy and sexual dimorphism", which combines FAFB, FANC and MANC neck connective neurons. The annotation data will be available to download here and have also been contributed to the portals for the three distinct datasets:

-   <https://codex.flywire.ai> for FAFB

-   <https://github.com/htem/FANC_auto_recon/wiki> for FANC and <https://neuprint.janelia.org/> for MANC. *Note that at the time of writing (27 Aug 2024) some annotation updates are still pending for FANC and MANC so the attached supplementary files remain the best resource*.

Annotations are used by the [fafbseg-py](https://fafbseg-py.readthedocs.io/) Python and the [fafbseg](https://natverse.org/fafbseg/) R package for programmatic analysis of the FAFB-Flywire dataset, the [malevnc](https://natverse.org/malevnc/) R package for the MANC dataset and [fancr](https://flyconnectome.github.io/fancr/) R package for the FANC dataset. Alternatively the [coconatfly](https://natverse.org/coconatfly/) package enables integrative connectomics across these three datasets.

## Annotations

-   [`/supplemental_files/Supplemental file 1 Seed planes.xlsx`](supplemental_files/Supplemental_file_1_Seed_planes.xlsx) contains the xyz coordinates, supervoxel_id, root_id, side and class of profiles passing through the FAFB or FANC seed plane; this file is the basis for **class** annotations of neck connective neurons in `fafbseg` and `fanc`.
-   [`/supplemental_files/Supplemental file 2 Typing and matching.xlsx`](supplemental_files/Supplemental_file_2_Typing_and_matching.xlsx) consists of 13 tabs contain all the annotations for descending neurons (DNs), ascending neurons (ANs) and sensory ascending neurons (SAs) for the three datasets FAFB, FANC and MANC; this file is the basis for the **cell type** annotations of neck connective neurons in `fafbseg` and `fanc`, and the new DN types in `manc`.

## Software tools

All software used in this paper is open-source and available through Github. Some of it was specifically developed for comparative analysis across the three datasets (coconatfly). Please open an issue in the respective repository if you have questions or run into problems.

### Python

The recommended entry point for Python is [fafbseg-py](https://github.com/flyconnectome/fafbseg-py).

| Name                                                                      | Description                                                                                            |
|-------------------|----------------------------------------------------|
| [navis](https://github.com/navis-org/navis)                               | Analysis and visualisation of neurons. Used e.g. for NBLAST.                                           |
| [navis-flybrains](https://github.com/navis-org/navis-flybrains)           | Used to transform data between template spaces (e.g. from hemibrain to FlyWire).                       |
| [fafbseg-py](https://github.com/flyconnectome/fafbseg-py)                 | Query and analyse FlyWire data (segmentation, meshes, skeletons, annotations).                         |
| [cocoa](https://github.com/flyconnectome/cocoa)                           | Analysis suite for comparative connectomics. Enables e.g. hemibrain-FlyWire connectivity clustering.   |
| [neuprint-python](https://github.com/connectome-neuprint/neuprint-python) | Query neuPrint instances (e.g. for the hemibrain, manc). Developed by FlyEM (Janelia Research Campus). |

### R

The recommended entry point for R is [coconatfly](https://natverse.org/coconatfly).

| Name                                            | Description                                                                                                                                                                                                                                                                                   |
|------------------|------------------------------------------------------|
| [coconatfly](https://natverse.org/coconatfly)   | Analysis suite for Drosophila comparative connectomics. Provides a uniform interface for analysis across datasets. Enables connectivity co-clustering of brain (FlyWire/hemibrain) and VNC (MANC/FANC) neurons. Builds on the generic [coconat](https://github.com/natverse/coconat) package. |
| [natverse](https://natverse.org)                | Analysis suite with a focus on neuroanatomical data.                                                                                                                                                                                                                                          |
| [malevnc](https://natverse.org/malevnc)         | Query and analyse the MANC data (segmentation, meshes, skeletons, annotations, connectivity).                                                                                                                                                                                                 |
| [fafbseg](https://natverse.org/fafbseg)         | Query and analyse FlyWire data (segmentation, meshes, skeletons, annotations,connectivity).                                                                                                                                                                                                   |
| [fancr](https://flyconnectome.github.io/fancr/) | Query and analyse FANC data (segmentation, meshes, skeletons, connectivity).                                                                                                                                                                                                                  |
| [neuprintr](https://natverse.org/neuprintr)     | Query neuPrint instances (e.g. for manc and hemibrain).                                                                                                                                                                                                                                       |

## Acknowledgements

Please cite this paper for the reconstruction and comprehensive annotation of DNs and ANs in the FAFB-FlyWire and FANC datasets as well as the matching of these neurons to the MANC dataset.

> Tomke Stürner, Paul Brooks, Laia Serratosa Capdevila, Billy J. Morris, Alexandre Javier, Siqi Fang, Marina Gkantia, Sebastian Cachero, Isabella R. Beckett, Andrew S. Champion, Ilina Moitra, Alana Richards, Finja Klemm, Leonie Kugel, Shigehiro Namiki, Han S.J. Cheong, Julie Kovalyak, Emily Tenshaw, Ruchi Parekh, Philipp Schlegel, Jasper S. Phelps, Brandon Mark, Sven Dorkenwald, Alexander S. Bates, Arie Matsliah, Szi-chieh Yu, Claire E. McKellar, Amy Sterling, Sebastian Seung, Mala Murthy, John Tuthill, Wei-Chung A. Lee, Gwyneth M. Card, Marta Costa, Gregory S.X.E. Jefferis, Katharina Eichler bioRxiv 2024.06.04.596633; doi: <https://doi.org/10.1101/2024.06.04.596633>

(citations for different reference managers are available from the *Citation Tools* link of the bioRxiv preprint).

It is likely that you will also want to cite some or all of the underlying datasets.

-   [Dorkenwald et al](https://www.biorxiv.org/content/10.1101/2023.06.27.546656) and [Schlegel et al](https://www.biorxiv.org/content/10.1101/2023.06.27.546055) for FAFB-FlyWire
-   [Azevedo et al](https://github.com/htem/FANC_auto_recon/wiki/Connectomic-reconstruction-of-a-female-Drosophila-ventral-nerve-cord-%28Azevedo%2C-Lesser%2C-Phelps%2C-Mark-et-al.-2024-Nature%29) for FANC
-   [Takemura et al](https://doi.org/10.7554/eLife.97769.1) for the MANC dataset; [Marin et al](https://doi.org/10.7554/eLife.97766) for the MANC dataset including comprehensive AN typing; [Cheong, Eichler, Stürner et al](https://doi.org/10.7554/eLife.96084.1) for comprehensive DN typing.

We appreciate that's a lot of references, but it was also a lot of work for a lot of people!

## Changelog

...
