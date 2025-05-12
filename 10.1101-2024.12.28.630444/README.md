# Particle annotations for the large-scale cryo-ET dataset of *Chlamydomonas reinhardtii*

In the scope of the work introducing the dataset ([doi:10.1101/2024.12.28.630444](https://doi.org/10.1101/2024.12.28.630444)), annotations of 7 particles were created: ATPase, Microtubule, Nucleosome, Clathrin, Photosystem II, Ribosome, Rubisco. Unbinned particle coordinates and orientations are stored in the RELION-3 `.star` file format with the pixel size of 1.96 Å - available in the [star](star) folder.

The annotations of each particle were used to create the subtomogram averages - available in the [densities](densities) folder. Please note, that some densities were obtained by additional filtering and postprocessing of the subtomograms using various software package such as WarpM, etc. - thus simply averaging the subtomograms at the given coordinates won't lead to exactly the same maps.

----

## Opening the annotations in Python

```bash
pip install starfile
```
```python
df = starfile.read('atp.star')
```

| rlnCoordinateX | rlnCoordinateY | rlnCoordinateZ | rlnAngleRot | rlnAngleTilt |  rlnAnglePsi | rlnTomoName | rlnTomoMdocName | rlnParticleName |
| -------------- | -------------- | -------------- | ----------- | ------------ | ------------ | ----------- | --------------- | --------------- |
| 1507.044913 | 3671.044913 | 143.764913 | 70.017559 | 154.710832 | -72.044680 | tomo_0024 | 01122021_BrnoKrios_arctis_lam3_pos29 | atpase |
| 1429.204913 | 3515.764913 | 145.204913 | -54.784770 | 30.163455 | 110.222227 | tomo_0024 | 01122021_BrnoKrios_arctis_lam3_pos29 | atpase |
| ... |

----
## Visualizing the densities in Python

```bash
pip install mrcfile matplotlib
```
```python
import mrcfile
import matplotlib.pyplot as plt
density = mrcfile.open('densities/atp.mrc').data
plt.imshow(density.sum(axis=1))  # Simple projection over one of the axes
```
![projection of atp density](https://github.com/user-attachments/assets/bf0e2736-7061-4b73-aa29-c8b235c03d29 "Projection of ATP density.")

----
## Visualizing the densities in ChimeraX

Install ChimeraX software from https://www.cgl.ucsf.edu/chimerax/
```bash
chimerax open densities/atp.mrc
```
![3d visualization of atp density](https://github.com/user-attachments/assets/0dd3461f-3e5d-4cf6-a272-deaed7ec7f98 "ATP density.")

----
## Visualizing the annotations in ArtiaX

1. Install ArtiaX plugin for ChimeraX from https://github.com/FrangakisLab/ArtiaX.
1. Download the tomogram over which you would like to overlay it's annotations.
1. Run ChimeraX with `chimerax` command.
1. Click Open and choose the desired tomogram (.mrc or .rec file)
1. Run `volume #1 origin 0,0,0` to reset the tomogram's origin.
1. Click on ArtiaX plugin tab and click the `Launch` button.
1. In the `Particle lists` section click the `Open list` button and choose desired star file.
1. In `ArtiaX options > Select/Manipulate` change `Pixel size factors Origin` to 1.96.
1. In the same section, go to `Selection/Display` and choose `Show particles`.
1. Click `Add selector` and using `rlnTomoName` specify your selected tomogram's name.
1. In the `Tomogram` tab, use `Navigation > Slice` to fly through your tomogram.
1. In `Visualization > Surface display > Load model` attach a density to the annotations.

![Overlay of annotations over a tomogram slice](https://github.com/user-attachments/assets/afa17f98-62f9-4cb7-a3eb-69d024a1e2cf "ATP annotations tomo_1963.")
