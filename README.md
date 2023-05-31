![logo](logo/logo1.png "Logo")
# Stochastic Optoacoustic Numerical Breast Phantom (SOA-NBP)

- Author:
  - Seonyeong Park (University of Illinois at Urbana-Champaign, sp33@illinois.edu)
  - Umberto Villa (Washington University in St. Louis)
  - Fu Li (University of Illinois at Urbana-Champaign)
  - Refik Mert Cam (University of Illinois at Urbana-Champaign)
  - Alexander A. Oraevsky (TomoWave Laboratories, Inc., Houston, Texas)
  - Mark A. Anastasio (University of Illinois at Urbana-Champaign, maa@illinois.edu)
- License: GNU General Public License version 3 (GPLv3)
- Version: 1.0.0

## Introduction
Stochastic Optoacoustic Numerical Breast Phantom (SOA-NBP) is a software framework to stochastically generate three-dimensional (3D) distributions of the **functional**, **optical**, and **acousitc** properties of breasts and lesions for use in computational studies of **optical**, **acoustic**, and **optoacoustic (OA) imaging**, also known as **photoacoustic imaging**. The functional, optical, and acoustic numerical breast phatnoms (NBPs) are seperately established via assignmnet of the specific properties of breasts to each tissue type in the anatomical NBPs. 

Generation of the anatomical NBPs was accomplished by extending the breast phantoms developed by the U.S. Food and Drug Administration [[VICTRE], [VICTRE breast phantom](https://breastphantom.readthedocs.io/en/latest/)]. As these were designed for use in mammography applications, substantial modifications were made to improve blood vasculature modeling for use in optical and OA imaging. The numerical lesion phantoms (NLPs) were modeled to include viable tumor cells only or a combination of viable tumor cells, necrotic core, and peripheral angiogenesis region. The details of the method are in [[Park2023]].


## Example data
The following three example datasets (a total of 84 NBP sets) are available from the Harvard dataverse:
- [Dataset1](https://doi.org/10.7910/DVN/1ZF0OW): 40 sets of NBPs in _natural_ shapes with _four different-sized lesions, that are composed solely of a viable tumor cell region_;
- [Dataset2](https://doi.org/10.7910/DVN/AQZE3H): 40 sets of NBPs in _hemispherical_ shapes with _four different-sized lesions, that are composed solely of a viable tumor cell region_;
- [Dataset3](https://doi.org/10.7910/DVN/OZRVX6): Four sets of NBPs in _natural_ shapes with _one lesion with a necrotic core and a peripheral angiogenesis region and the other without_.

Each NBP set consists of
- A tissue label map (`anatomical NBP`);
- Functional properties and chromophore concentrations maps (`functional NBPs`);
- Optical properties maps (optical absorption and scattering coefficients, scattering anisotropy, and refractive indexes) at multiple illumination wavelengths (`optical NBPs`);
- Acoustic properties (speed of sound, density, and acoustic attenuation) maps (`acoustic NBPs`);
- Simulated multi-wavelength `optical fluence distributions`;
- Simulated multi-wavelength `induced initial pressure distributions`;
- Simulated multi-wavelength `acoustic measurements`.

Further details of the NBPs, virtual OAT imaging system, and virtual data acquisition are in [[Park2023]].

The example data can be downloaded using the following command:
```
wget https://dataverse.harvard.edu/api/access/datafile/6988734 -O ./A40210923l_label.mat
wget https://dataverse.harvard.edu/api/access/datafile/6988732 -O ./A40210923l_func.mat
wget https://dataverse.harvard.edu/api/access/datafile/6988733 -O ./A40210923l_opt.mat
wget https://dataverse.harvard.edu/api/access/datafile/6988731 -O ./A40210923l_acou.mat
wget https://dataverse.harvard.edu/api/access/datafile/6988742 -O ./A40210923l_phi.mat
wget https://dataverse.harvard.edu/api/access/datafile/6988741 -O ./A40210923l_p0.mat
wget https://dataverse.harvard.edu/api/access/datafile/6988740 -O ./A40210923l_p.mat
```


## Citation
If you use our codes, methods to generate anatomical, functional, optical, and acoustic NBPs and NLPs, and/or the example data in your research, the authors of this software would like you to cite our paper and/or conference proceedings in your related publications.

```
@article{Park2023,
  author = {Seonyeong Park and Umberto Villa and Fu Li, Refik Mert Cam and Alexander A. Oraevsky and Mark A. Anastasio},
  title = {{Stochastic three-dimensional numerical phantoms to enable computational studies in quantitative optoacoustic computed tomography of breast cancer}},
  volume = {28},
  journal = {Journal of Biomedical Optics},
  number = {NO},
  publisher = {SPIE},
  pages = {P -- P},
  year = {2023},
  doi = {10.1117/DOI_NUMBER},
  URL = {https://doi.org/10.1117/DOI_NUMBER}
}
```
```
@inproceedings{Park2020,
  author = {Seonyeong Park and Umberto Villa and Richard Su and Alexander Oraevsky and Frank J. Brooks and Mark A. Anastasio},
  title = {{Realistic three-dimensional optoacoustic tomography imaging trials using the VICTRE breast phantom of FDA (Conference Presentation)}},
  volume = {11240},
  booktitle = {Photons Plus Ultrasound: Imaging and Sensing 2020},
  editor = {Alexander A. Oraevsky and Lihong V. Wang},
  organization = {International Society for Optics and Photonics},
  publisher = {SPIE},
  year = {2020},
  doi = {10.1117/12.2552380},
  URL = {https://doi.org/10.1117/12.2552380}
}
```

## Reference
- [[Park2023]] Seonyeong Park, Umberto Villa, Fu Li, Refik Mert Cam, Alexander A. Oraevsky, Mark A. Anastasio, "Stochastic three-dimensional numerical phantoms to enable computational studies in quantitative optoacoustic computed tomography of breast cancer," _J. Biomed. Opt._ 28(NO) ARTICLE_NO (DD MONTH 2023) https://doi.org/10.1117/DOI_NUMBER

- [[Park2020]] Seonyeong Park, Umberto Villa, Richard Su, Alexander Oraevsky, Frank J. Brooks, Mark A. Anastasio, "Realistic three-dimensional optoacoustic tomography imaging trials using the VICTRE breast phantom of FDA (Conference Presentation)," _Proc. SPIE 11240, Photons Plus Ultrasound: Imaging and Sensing 2020_, 112401H (6 March 2020); https://doi.org/10.1117/12.2552380

- [[Li2022]] Fu Li, Umberto Villa, Seonyeong Park, Mark A. Anastasio, "3-D Stochastic numerical breast phantoms for enabling virtual imaging trials of ultrasound computed tomography," _IEEE Transactions on Ultrasonics, Ferroelectrics, and Frequency Control_, vol. 69, no. 1, pp. 135-146, Jan. 2022, https://doi.org/10.1109/TUFFC.2021.3112544

- [[Modified VICTRE](https://github.com/comp-imaging-sci/breast-phantom-oat)] BreastPhantom: modified branch for OAT virtual imaging studies

- [[VICTRE]] Virtual Imaging Clinical Trials for Regulatory Evaluation project

- [[VICTRE breast phantom](https://breastphantom.readthedocs.io/en/latest/)] VICTRE breast phantom

[Park2023]: <https://doi.org/10.1117/DOI_NUMBER>
[Park2020]: <https://doi.org/10.1117/12.2552380>
[Li2022]: <https://doi.org/10.1109/TUFFC.2021.3112544>
[Modified VICTRE]: <https://github.com/comp-imaging-sci/breast-phantom-oat>
[VICTRE]: <https://github.com/DIDSR/VICTRE>
