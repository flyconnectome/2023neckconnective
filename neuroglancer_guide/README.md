# [cocoglancer ](https://tinyurl.com/NeckConnective)

[neuroglancer](https://github.com/google/neuroglancer) is a web viewer for volumetric EM data (Maitin-Shepard et al. 2021). We have created a Neck Connective ‘scene’ within neuroglancer (**cocoglancer**) to co-visualize neurons from the three datasets from our manuscript simultaneously: FAFB, FANC and MANC. It includes all neck connective neurons, as well as the intrinsic motor and pre-motor neurons described in the manuscript.

cocoglancer allows male and female VNC neurons to be overlaid and morphologically compared. It also enables the simultaneous selection of brain (FAFB) and VNC (FANC, MANC) neurons  effectively simulating their complete CNS morphology. However, this is restricted to neurons that are matched to confocal images of the entire CNS (i.e., DNs without the additional "e", such as DNa02, etc.).

[Section 1](#section-1)  of this guide outlines the basic functionality of cocoglancer. [Section 2](#section-2) has links to the neurons described in each of the main figures of the manuscript.

## Section #1 

## Navigating cocoglancer

The cocoglancer web viewer, available at https://tinyurl.com/NeckConnective is split into 3 windows (A, B, C).

A. Data Layers (green)

B. 3D Visualisation (orange)

C. Annotation (blue)

![](images/full_window.png "full neuroglancer window")

### Data Layers (Window A)

![](images/data_layer.png "neuroglancer data panel")

This window contains 7 data layers corresponding to:

1. **flywire(783)** - Flywire segmentation version 783, with meshes in static maleCNS space.
2. **MANC(v1.2.1)** - Static MANC meshes v1.2.1 in MANC space (prepared by Sebastian Cachero).
3. **FANC (NeckConnective)** - FANC static meshes in MANC space (prepared by Sebastian Cachero).
4. **neuropil-shell** - FAFB central brain and optic lobe meshes (prepared by FlyEM, Janelia).
5. **roi** - FAFB neuropil meshes listed by abbreviation (see below for the list) prepared by FlyEM, Janelia.
6. **brain-shell** - Whole FAFB brain mesh prepared from Flywire synapse data by Philipp Schlegel and FlyEM, Janelia.
7. **vnc-shell** - Whole MANC surface mesh prepared by FlyEM, Janelia.

- Right-clicking on layers 1-3 brings up segment window C, where neurons can be searched and selected.
- Left-clicking on a layer toggles visibility.




### 3D Visualization (Window B)

The 3D visualization window allows simple rotation and zooming in on selected neurons. When many neurons are selected, you can double-click on one to hide it.

- To rotate: Left-click and drag the mouse.
- To zoom in: Press Ctrl + scroll the mouse wheel.
- Right-click centers the screen around the cursor.

![](images/3d_visualisation.png "visualisation window")

### Annotation (Window C)

The annotation window shows all the neurons within each data layer. IDs or neuron names can be typed or pasted in, or neurons can be manually selected from the list under the "id" column.

- To view a neuron, click the "eye" to toggle between hidden and in view.
- Under "label," information about each neuron is displayed, such as type, side, and class (e.g., DNa02_L_descending).
- You can use regex in the search window to manually select multiple types of neurons. For example, to select DNp103 and DNp104: `/DNp10(3|4)`.

![](images/annotation.png "annotation window")

### Extra Features

![](images/help_bar.png "help bar only")

In the top-right corner of the cocoglancer window, there are icons for further control. For this simplified version of neuroglancer, only the **?** icon will be useful. Clicking it displays a popup with shortcuts to various other functions.

## Section #2

# Links to specific neurons from the manuscript

Each link contains multiple layers, each corresponding to a subset of neurons found in the main figures. The prefix FAFB, MANC and FANC of each layer indicates dataset. Layers can be viewed in isolation, or overlayed for comparison.

[SAs by subclass](https://neuroglancer-demo.appspot.com/#!gs://flyem-user-links/short/SAs_by_subclass.json) - Figure 1.  Sensory ascending neuron subclasses as shown in figure 1 and extended figure 2.

[DNs by soma location](https://neuroglancer-demo.appspot.com/#!gs://flyem-user-links/short/DNs_by_soma_location.json) - Figure 2. Descending neurons shown across datasets by soma location as shown in figure 2 and extended figure 3.

[DNs by sensory clusters](https://neuroglancer-demo.appspot.com/#!gs://flyem-user-links/short/DNSensoryClusters.json) - Figure 3. Sensory neuron modality ranked by strength of connection to descending neurons.

[DNx02 network](https://neuroglancer-demo.appspot.com/#!gs://flyem-user-links/short/DNx02.json) - Figure 4e. DNx02 network in FAFB and MANC

[DNa02 downstream stereotypy](https://neuroglancer-demo.appspot.com/#!gs://flyem-user-links/short/DNa02_circuit.json) - Figure 5e-g. DNa02 motor neuron leg circuit stereotypy between FANC and MANC

[Dimorphic DNs and ANs](https://neuroglancer-demo.appspot.com/#!gs://flyem-user-links/short/dimorphic_DNs_ANs.json) - Figure 6. All sex-specific and dimorphic descending and ascending neurons

[DNp13 and DNa12 circuits](https://neuroglancer-demo.appspot.com/#!gs://flyem-user-links/short/DNp13_and_DNa12_circuits.json) - Figure 7. Sex dimorphic networks of DNp13 and DNa12 in FANC and MANC

[ANs of 08B hemilineage](https://neuroglancer-demo.appspot.com/#!gs://flyem-user-links/short/sex-specific_ANs_of_08B_hemilineage.json) - Figure 8. Sex-specific and dimorphic ascending neurons of 08B hemilineage



## Acknowledgements

Neuroglancer was developed by the Connectomics at Google team by  [Jeremy Maitin-Shepard](https://github.com/jbms) from Google Brain team.
