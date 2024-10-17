# [cocoglancer ](https://tinyurl.com/NeckConnective)

[neuroglancer](https://github.com/google/neuroglancer) is a web viewer for volumetric EM data (Maitin-Shepard et al. 2021). We have created a Neck Connective ‘scene’ within neuroglancer (cocoglancer) to co-visualize neurons from the three datasets from our manuscript simultaneously: FAFB, FANC, and MANC, which includes all neck connective neurons, as well as the intrinsic motor and pre-motor neurons described in the manuscript.

cocoglancer allows for male and female VNC neurons to be overlaid and compared morphologically. It also allows brain (FAFB) and VNC neurons to be selected simultaneously for visual analysis of entire DN neurons in the CNS. (Note that only light-matched neurons are possible to visualise in their entirety.)

## Navigating cocoglancer

The cocoglancer web viewer, available at https://tinyurl.com/NeckConnective is split into 3 windows (A, B, C).

A. Data Layers (green)

B. 3D Visualisation (orange)

C. Annotation (blue)

![](images/full_window.png "full neuroglancer window")

### Data Layers (Window A)

![](images/data_layer.png "neuroglancer data panel")

This window contains 7 layers corresponding to:

1. **Flywire** - Flywire segmentation version 783 loaded with meshes in static maleCNS space.
2. **MANC** - Static MANC meshes loaded in MANC space (prepared by Sebastian Cachero).
3. **FANC** - FANC static meshes mapped to MANC space (prepared by Sebastian Cachero).
4. **Neuropil Shell** - FAFB central brain and optic lobe meshes (prepared by flyEM, Janelia).
5. **ROI** - FAFB neuropil meshes listed by abbreviation (see below for the list), (prepared by flyEM, Janelia).
6. **FAFB Brain Shell** - Whole FAFB brain mesh prepared from Flywire synapse data by Philipp Schlegel and flyEM, Janelia).
7. **VNC Shell** - Whole MANC VNC mesh. (prepared bt FlyEM, Janelia)

- Right-clicking on layers 1-3 brings up segment window B, where neurons can be selected.
- Left-clicking on a layer toggles visibility.




### 3D Visualization (Window B)

The 3D visualization window allows simple rotation and zooming in on selected profiles. When many profiles are selected, you can double-click to hide a profile.

- To rotate: Left-click and drag the mouse.
- To zoom in: Use the mouse wheel.
- Right-click centers the screen around the cursor.

![](images/3d_visualisation.png "visualisation window")

### Annotation (Window C)

The annotation window contains all the neurons within each data layer. IDs or neuron names can be typed or pasted in, or neurons can be manually selected from the list under the "ID" tab.

- To view a profile, click the "eye" to toggle between hidden and in view.
- Under "label," information about each neuron is displayed, such as type, side, and class (e.g., DNa02_L_descending).
- You can use regex in the search window to manually select multiple types of neurons. For example, to select DNp103 and DNp104: `/DNp(103|104)`.

![](images/annotation.png "annotation window")

### Extra Features

![](images/help_bar.png "help bar only")

In the top-right corner of the cocoglancer window, there are icons for further control. For this simplified version of Neuroglancer, only the **?** icon will be useful. Clicking it displays a popup with shortcuts to various other functions.

**Note**: Ask others about adding links to specific neurons from the manuscript, e.g., all sex-specific/dimorphic neurons or some specific subsets.

## Acknowledgements

Neuroglancer was developed by the Connectomics at Google team by  [Jeremy Maitin-Shepard](https://github.com/jbms) from Google Brain team.
