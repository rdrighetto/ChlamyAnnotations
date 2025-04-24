# chlamydataset2relion5
Python script to import pre-processed results from the Chlamy dataset ([EMPIAR-11830](https://www.ebi.ac.uk/empiar/EMPIAR-11830/)) into [Relion-5](https://relion.readthedocs.io/en/release-5.0/STA_tutorial/index.html)

# Dependencies
A standard `python3` environment with [numpy](https://numpy.org/) and [starfile](https://github.com/teamtomo/starfile) suffices.

# Usage instructions

1. Clone this repo:
   
```bash
git clone git@github.com:Chromatin-Structure-Rhythms-Lab/ChlamyAnnotations.git
```
   
2. Download the desired tomogram folders contained in the [chlamy_visual_proteomics](https://ftp.ebi.ac.uk/empiar/world_availability/11830/data/chlamy_visual_proteomics/) directory from [EMPIAR-11830](https://www.ebi.ac.uk/empiar/EMPIAR-11830/). Example:

```bash
mkdir EMPIAR-11830

cd EMPIAR-11830

wget -r -N -np -nH --cut-dirs=4 --reject "*.eer" ftp://ftp.ebi.ac.uk/empiar/world_availability/11830/data/chlamy_visual_proteomics/01082023_BrnoKrios_Arctis_WebUI_Position_8/
```

3. **OPTIONAL:** Download the [ctf3d](https://ftp.ebi.ac.uk/empiar/world_availability/11830/data/ctf3d_bin4/) and [cryo-CARE](https://ftp.ebi.ac.uk/empiar/world_availability/11830/data/cryocare_bin4/) denoised tomograms (see example above)

4. Run the script:

```bash
cd ChlamyAnnotations/chlamydataset2relion5/

python chlamydataset2relion5.py /path/to/chlamy_visual_proteomics/ --output_dir /path/to/relion5/project/ --correspondence_star tomolist_num_dir.star --ctf3d /path/to/bin4_ctf3d/ --cryocare /path/to/bin4_cryocare/`
```

**Tip:** the `tomolist_num_dir.star` file is provided in this repo for convenience. Alternatively, it can also be [downloaded](https://ftp.ebi.ac.uk/empiar/world_availability/11830/data/chlamy_visual_proteomics/tomolist_num_dir.star) from EMPIAR.

5. **Profit!** the generated `/path/to/relion5/project/tomograms.star` can be used as a direct entry in Relion-5 jobs.

   **NOTE:** make sure you launch Relion-5 in tomography mode, i.e. by running `relion --tomo &`

6. **OPTIONAL:** for a sanity check, it's a good idea to have Relion reconstruct at least one imported tomogram and make sure it matches the deposited ctf3d or cryo-CARE bin4 tomogram:
![image](https://github.com/user-attachments/assets/a37b6556-b14c-4951-b92a-87bc2094c1b8)


# Acknowledgments
This script is almost entirely derived from [aretomo3torelion5](https://github.com/Phaips/aretomo3torelion5/) from [@Phaips](https://github.com/Phaips) 🚀

# References
If the Chlamy dataset is useful to you, please cite the corresponding manuscript:

* R. Kelley et al., “Towards community-driven visual proteomics with large-scale cryo-electron tomography of Chlamydomonas reinhardtii,” Dec. 28, 2024, bioRxiv. https://doi.org/10.1101/2024.12.28.630444

# See also
* Repository of particle annotations: https://github.com/Chromatin-Structure-Rhythms-Lab/ChlamyAnnotations
* Annotation spreadsheet on Zenodo: https://zenodo.org/records/13941456
* Voxel-dense annotations from [Pom](https://pom-cryoet.readthedocs.io/): https://cryopom.streamlit.app/
* Chlamy dataset at the [CZII data portal](https://cryoetdataportal.czscience.com/): https://cryoetdataportal.czscience.com/datasets/10302

