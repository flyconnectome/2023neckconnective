# 2023neckconnective

This repository collates the annotations and example code for Stürner and Brooks et al. [Comparative connectomics of the descending and ascending neurons of the Drosophila nervous system: stereotypy and sexual dimorphism](https://doi.org/10.1101/2024.06.04.596633), which combines FAFB (female brain), FANC (female nerve cord) and MANC (male nerve cord) neurons that run through the neck. The annotation data will be available to download here and have also been contributed to the portals for the three distinct datasets:

-   <https://codex.flywire.ai> for FAFB

-   <https://github.com/htem/FANC_auto_recon/wiki> for FANC

-   <https://neuprint.janelia.org/> for MANC.

*Note that at the time of writing (27 Aug 2024) some annotation updates are still pending for FANC and MANC so the attached supplementary files remain the best resource*.

Annotations are used by the [fafbseg-py](https://fafbseg-py.readthedocs.io/) Python and the [fafbseg](https://natverse.org/fafbseg/) R package for programmatic analysis of the FAFB-Flywire dataset, the [malevnc](https://natverse.org/malevnc/) R package for the MANC dataset and [fancr](https://flyconnectome.github.io/fancr/) R package for the FANC dataset. Alternatively the [coconatfly](https://natverse.org/coconatfly/) package enables integrative connectomics across these three datasets in R.

## Annotations

-   [`/Supplemental_files/Supplemental_file1_FAFB_seed_plane.tsv`](Supplemental_files/Supplemental_file1_FAFB_seed_plane.tsv) contains the xyz coordinates, supervoxel_id, root_id, side and class of profiles passing through the FAFB seed plane; this file is the basis for **class** annotations of neck connective neurons in `fafbseg`.
-   [`/Supplemental_files/Supplemental_file2_FANC_seed_plane.tsv`](Supplemental_files/Supplemental_file2_FANC_seed_plane.tsv) contains the xyz coordinates, supervoxel_id, root_id, side and class of profiles passing through the FANC seed plane; this file is the basis for **class** annotations of neck connective neurons in `fanc`.
-   [`/Supplemental_files/Supplemental_file3_FAFB_SA_identification.tsv`](Supplemental_files/Supplemental_file3_FAFB_SA_identification.tsv) contains the sensory ascending (SA) subclass identification in the FAFB dataset with the reference to slide code of light microscopy images taken from genetic driver lines.
-   [`/Supplemental_files/Supplemental_file4_DN_identification.tsv`](Supplemental_files/Supplemental_file4_DN_identification.tsv) contains the slide code of light microscopy images taken from genetic driver lines to identify descending neurons (DNs).

The following Supplemental files 5-11 are the basis for the **cell type** annotations of neck connective neurons in `fafbseg` and `fanc`, and the new DN types in `manc`.
-   [`/Supplemental_files/Supplemental_file5_FAFB_DNs.tsv`](Supplemental_files/Supplemental_file5_FAFB_DNs.tsv) contains the neuronal ids, types and annotations of DNs in the FAFB dataset.
-   [`/Supplemental_files/Supplemental_file6_FANC_DNs.tsv`](Supplemental_files/Supplemental_file6_FANC_DNs.tsv) contains the neuronal ids, types and annotations of DNs in the FANC dataset.
-   [`/Supplemental_files/Supplemental_file7_MANC_DNs.tsv`](Supplemental_files/Supplemental_file7_MANC_DNs.tsv) contains the neuronal ids, types and annotations of DNs in the MANC dataset.
-   [`/Supplemental_files/Supplemental_file8_FAFB_ANs_SAs.tsv`](Supplemental_files/Supplemental_file8_FAFB_ANs_SAs.tsv) contains the neuronal ids, types and annotations of ascending neurons (ANs) and SAs in the FAFB dataset.
-   [`/Supplemental_files/Supplemental_file9_FANC_ANs.tsv`](Supplemental_files/Supplemental_file9_FANC_ANs.tsv) contains the neuronal ids, types and annotations of ANs in the FANC dataset.
-   [`/Supplemental_files/Supplemental_file10_FANC_SAs.tsv`](Supplemental_files/Supplemental_file10_FANC_SAs.tsv) contains the neuronal ids, types and annotations of SAs in the FANC dataset.
-   [`/Supplemental_files/Supplemental_file11_MANC_ANs.tsv`](Supplemental_files/Supplemental_file11_MANC_ANs.tsv) contains the neuronal ids, types and annotations of ANs in the MANC dataset.

-   [`/Supplemental_files/Supplemental_file12_AN_identification.tsv`](Supplemental_files/Supplemental_file12_AN_identification.tsv) contains the the slide code of light microscopy images taken from genetic driver lines to identify 3 new AN types.
-   [`/Supplemental_files/Supplemental_file13_other_MANC_FANC_matching.tsv`](Supplemental_files/Supplemental_file13_other_MANC_FANC_matching.tsv) contains the the neuronal ids, types and annotations in the FANC dataset that are not DNs, ANs or SAs; apart from 64 MNs that have previously been annotated in the [Azevedo et al. 2024](https://www.nature.com/articles/s41586-024-07389-x) this file is the basis for **cell type** annotations of these 736 intrinsich neurons (INs) in `fanc`.
-   [`/Supplemental_files/Supplemental_file14_dimorphic_DNs.tsv`](Supplemental_files/Supplemental_file14_dimorphic_DNs.tsv) contains the neuronal ids, types and annotations of dimorphic or sex-specific DNs from all three datasets.
-   [`/Supplemental_files/Supplemental_file15_dimorphic_ANs.tsv`](Supplemental_files/Supplemental_file15_dimorphic_ANs.tsv) contains the neuronal ids, types and annotations of dimorphic or sex-specific ANs from all three datasets.


## Software tools

All software used in this paper is open-source and available through Github. Some of it was specifically developed for comparative analysis across the three datasets (`coconatfly`). Please open an issue in the respective repository if you have questions or run into problems.

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

-   [Dorkenwald et al](https://www.biorxiv.org/content/10.1101/2023.06.27.546656) and [Schlegel et al](https://www.biorxiv.org/content/10.1101/2023.06.27.546055) for FAFB-FlyWire, see [guidelines](https://flywire.ai/guidelines) for details
-   [Azevedo et al](https://github.com/htem/FANC_auto_recon/wiki/Connectomic-reconstruction-of-a-female-Drosophila-ventral-nerve-cord-%28Azevedo%2C-Lesser%2C-Phelps%2C-Mark-et-al.-2024-Nature%29) for the FANC dataset, including muscle targets of the MNs.
-   [Takemura et al](https://doi.org/10.7554/eLife.97769.1) for the MANC dataset; [Marin et al](https://doi.org/10.7554/eLife.97766) for the MANC dataset including comprehensive typing of the VNC, including AN, SA and IN typing; [Cheong, Eichler, Stürner et al](https://doi.org/10.7554/eLife.96084.1) for comprehensive DN and MN typing.

We appreciate that's a lot of references, but it was also a lot of work for a lot of people!

## Changelog

-   [v0.1](https://github.com/flyconnectome/2023neckconnective/releases/tag/v0.1) This is the version reported on in the Stürner and Brooks et al. bioRxiv preprint June 28, 2024.
