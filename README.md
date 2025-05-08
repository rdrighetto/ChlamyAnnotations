# Towards community-driven visual proteomics with large-scale cryo-electron tomography of *Chlamydomonas reinhardtii*

This is an accompanying repository to the work [doi:10.1101/2024.12.28.630444](https://doi.org/10.1101/2024.12.28.630444) and the dataset of 1829 cryo-electron tomograms presented within. This repository serves as a central location for exchnage of additional resources and community contributions related to this dataset. The intended audience includes researchers and practitioners in cryo-electron tomography, structural biology, and visual proteomics. It is designed for those interested in exploring large-scale cryo-ET datasets, developing new analysis tools, or contributing annotations and resources to advance the field. Students and educators in related disciplines may also find the repository valuable for learning and teaching. Licensing information can be found in [LICENSE](LICENSE).


## Dataset of 1829 cryo-electron tomograms

The tomograms are available for download from [EMPIAR-11830](https://www.ebi.ac.uk/empiar/EMPIAR-11830/) and [CZI-10302](https://cryoetdataportal.czscience.com/datasets/10302). 
Parameters of data acquisition are listed in Section **Cryo-ET data acquisition** of the article.

Available sets: 
* Tilt-series in `EER` format & Metadata (26.8TB)
* Reconstructions (bin4) denoised with cryo-CARE (3.6TB) - These files are not 3D CTF-corrected
* Reconstructions (bin4) 3D CTF-corrected with IMOD (1.8TB) - These files are not cryo-CARE denoised


## How to contribute?

We welcome contributions from the community to enhance the utility of this dataset. Read how you can get involved in [CONTRIBUTING.md](CONTRIBUTING.md). We look forward to seeing your contributions!

## Resources (original or contributed)

----

### Particle annotations of ATPase, Microtubule, Nucleosome, Clathrin, Photosystem II, Rubisco, Ribosome

**Article:** Towards community-driven visual proteomics with large-scale cryo-electron tomography of *Chlamydomonas reinhardtii* \
**Authors:** Kelley, R., Khavnekar, S., Righetto, R.D., Heebner, J., Obr, M., Zhang, X., Chakraborty, S., Tagiltsev, G., Michael, A.K., van Dorst, S., Waltz, F., McCafferty, C.L., Lamm, L., Zufferey, S., Van der Stappen, P., van den Hoek, H., Wietrzynski, W., Harar, P., Wan, W., Briggs, J.A.G., Plitzko, J.M., Engel, B.D., Kotecha, A. \
**DOI:** [10.1101/2024.12.28.630444](https://doi.org/10.1101/2024.12.28.630444) \
**REPO:** [github.com/Chromatin-Structure-Rhythms-Lab/ChlamyAnnotations](https://github.com/Chromatin-Structure-Rhythms-Lab/ChlamyAnnotations) \
**Subfolder in this repository:** [10.1101-2024.12.28.630444](10.1101-2024.12.28.630444) \
**Data source & version:** EMPIAR (as of 28.02.2025)

----

### Manual tomogram annotation spreadsheet

**Article:** Towards community-driven visual proteomics with large-scale cryo-electron tomography of *Chlamydomonas reinhardtii* \
**Authors:** Kelley, R., Khavnekar, S., Righetto, R.D., Heebner, J., Obr, M., Zhang, X., Chakraborty, S., Tagiltsev, G., Michael, A.K., van Dorst, S., Waltz, F., McCafferty, C.L., Lamm, L., Zufferey, S., Van der Stappen, P., van den Hoek, H., Wietrzynski, W., Harar, P., Wan, W., Briggs, J.A.G., Plitzko, J.M., Engel, B.D., Kotecha, A. \
**DOI:** [10.1101/2024.12.28.630444](https://doi.org/10.5281/zenodo.13941456) \
**REPO:** [github.com/Chromatin-Structure-Rhythms-Lab/ChlamyAnnotations](https://github.com/Chromatin-Structure-Rhythms-Lab/ChlamyAnnotations) \
**Subfolder in this repository:** [10.5281-zenodo.13941456/](10.5281-zenodo.13941456/)

----

### Comprehensive segmentation of 25 macromolecules and organelles across the full dataset

**Paper:** Scaling data analyses in cellular cryoET using comprehensive segmentation \
**Authors:** Last, M.G.F., Voortman, L.M. and Sharp, T.H. \
**DOI:** [10.1101/2025.01.16.633326](https://doi.org/10.1101/2025.01.16.633326) \
**REPO:** [github.com/bionanopatterning/Pom](https://www.github.com/bionanopatterning/Pom) \
**APP:** https://cryopom.streamlit.app \
**Segmented features:** cytoplasm, mitochondrion, nuclear envelope, nucleoplasm, pyrenoid tube, thylakoid, vesicle, Golgi, pyrenoid, stroma, lipid droplet, endoplasmic reticulum, nuclear pore complex, starch granule, cilum, intermediate-filament rich areas, cell wall, chloroplast outer membrane, dense layer, membrane, ribosome, ATP synthase, RuBisCo, TRiC, proteasome. \
**Subfolder in this repository:** [10.1101-2025.01.16.633326](10.1101-2025.01.16.633326) \
**Data source & version:** [CryoET Data Portal deposition 10314](https://cryoetdataportal.czscience.com/depositions/10314)

----

### chlamydataset2relion5: script to import EMPIAR-11830 data into RELION-5 for subtomogram averaging

**Authors:** Righetto, R.D. & Van der Stappen, P. \
**REPO:** [github.com/Chromatin-Structure-Rhythms-Lab/ChlamyAnnotations](https://github.com/Chromatin-Structure-Rhythms-Lab/ChlamyAnnotations) \
**Subfolder in this repository:** [chlamydataset2relion5](chlamydataset2relion5)

----

### TomoGuide – a cryo-electron tomography processing workflow tutorial

**Authors:** Van der Stappen, Philippe & Waltz, Florent \
**DOI:** [10.5281/zenodo.15358525](https://doi.org/10.5281/zenodo.15358525) \
**REPO:** [github.com/TomoGuide/TomoGuide.github.io](https://github.com/TomoGuide/TomoGuide.github.io) \
**Subfolder in this repository:** [10.5281-zenodo.15358525](10.5281-zenodo.15358525)

----

