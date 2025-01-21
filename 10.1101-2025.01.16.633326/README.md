# Comprehensive segmentation of 25 macromolecules and organelles across the full dataset # 

These segmentations were generated using [Ais](www.github.com/bionanopatterning/Ais) and [Pom](www.github.com/bionanopatternin/Pom) as a part of a project to explore scaling up data analyses in cellular cryoET. Segmentation was performed in two steps: first, segmenting various macromolecules based on density volumes as the input, followed by a second segmentation of many different organelles and other subcellular niches using both density volumes and the macromolecule segmentations as the input. We segmented 25 different features across asll 1829 tomograms and used these results to test three analysis strategies for use in large scale cellular cryoET studies: 1) automated curation and selection of data-subsets, 2) context-aware particle picking, and 3) area-selective template matching. These are described in detail in our preprint: [Scaling data analyses in cellular cryoET using comprehensive segmentation](https://doi.org/10.1101/2025.01.16.633326)

The segmentation results can be explored [online](cryopom.streamlit.app) and have been uploaded to the CryoET Data Portal, under deposition ID [10314](https://cryoetdataportal.czscience.com/depositions/10314).

A copy of the 'dataset summary', listing the composition of all tomograms, can be found in 'summary.xlsx'. 

Further reading
----
Comprehensive segmentation at scale: www.github.com/bionanopatterning/Pom \
Streamlining tomogram segmentation: www.github.com/bionanopatterning/Ais \
