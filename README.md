# 2023neckconnective
This repository collates the annotations and example code of the Stürner and Brooks et al. "Comparative connectomics of the descending and ascending neurons of the Drosophila nervous system: stereotypy and sexual dimorphism" paper that combines FAFB, FANC and MANC neck connective neurons. The annotation data will be available to download here and have also been contributed to the portals of the three distinct datasets: https://codex.flywire.ai for FAFB, https://github.com/htem/FANC_auto_recon/wiki for FANC (not yet included) and https://neuprint.janelia.org/ for MANC. 

Annotations are used by the [fafbseg-py](https://fafbseg-py.readthedocs.io/) Python and the [fafbseg](https://natverse.org/fafbseg/) R package for programmatic analysis of the FAFB-Flywire dataset, the [malevnc](https://natverse.org/malevnc/) R package for the MANC dataset and [fancr](https://flyconnectome.github.io/fancr/) R package for the FANC dataset. Altenatively the [coconatfly](https://natverse.org/coconatfly/) package enables integrative connectomics across these three datasets.

## Annotations

- [`/supplemental_files/Supplemental file 1 Seed planes.xlsx`](supplemental_files/Supplemental_file_1_Seed_planes.xlsx) contains the xyz coorindates, svid, root_id, side and class of profiles passing through the FAFB or FANC seed plane; this file is the basis for class annotations of neck connective neurons in `fafbseg` and `fanc`.
- [`/supplemental_files/Supplemental file 2 Typing and matching.xlsx`](supplemental_files/Supplemental_file_2_Typing_and_matching.xlsx) consists of 13 files that contain all the annotations for descending neurons (DNs), ascending neurons (ANs) and sensory ascending neurons (SAs) for the three datasets FAFB, FANC and MANC; this file is the basis for the cell typing and annotations of neck connective neurons in `fafbseg` and `fanc`, and the new DN types in `manc`.

## Software tools
All software used in this paper is open-source and available through Github. Some of it was specifically developed for comparative analysis across the thee datasets (coconatfly). Please open an issue in the respective repository if you have questions or run into problems.

### Python

| Name             | Description |
| ---------------- | ----------- |
| [navis](https://github.com/navis-org/navis)            		   | Analysis and visualisation of neurons. Used e.g. for NBLAST.  |
| [navis-flybrains](https://github.com/navis-org/navis-flybrains)  | Used to transform data between template spaces (e.g. from hemibrain to FlyWire). |
| [fafbseg-py](https://github.com/flyconnectome/fafbseg-py)           | Query and analyse FlyWire data (segmentation, meshes, skeletons, annotations). |
| [cocoa](https://github.com/flyconnectome/cocoa) | Analysis suite for comparative connectomics. Enables e.g. hemibrain-FlyWire connectivity clustering. |
| [neuprint-python](https://github.com/connectome-neuprint/neuprint-python)  | Query neuPrint instances (e.g. for the hemibrain). Developed by FlyEM (Janelia Research Campus). |

The recommended entry point for Python is [fafbseg-py](https://github.com/flyconnectome/fafbseg-py).

### R

| Name             | Description |
| ---------------- | ----------- |
| [coconatfly](https://natverse.org/coconatfly)    | Analysis suite for Drosophila comparative connectomics. Enables hemibrain-FlyWire connectivity clustering. See also [coconat](https://github.com/natverse/coconat). |
| [natverse](https://natverse.org)        		   | Analysis suite with a focus on neuroanatomical data.  |
| [malevnc](https://natverse.org/malevnc)      | Query and analyse the MANC data (segmentation, meshes, skeletons, annotations, connectivity). |
| [fafbseg](https://natverse.org/fafbseg)          | Query and analyse FlyWire data (segmentation, meshes, skeletons, annotations,connectivity). |
| [fancr](https://flyconnectome.github.io/fancr/))          | Query and analyse FANC data (segmentation, meshes, skeletons, connectivity). |
| [neuprintr](https://natverse.org/neuprintr)      | Query neuPrint instances (e.g. for the manc). |

The recommended entry point for R is [coconatfly](https://natverse.org/coconatfly).

## Changelog

