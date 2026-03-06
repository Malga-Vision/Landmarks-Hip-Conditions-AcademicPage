# Automated Landmark Detection for Hip Conditions: Cross-Modality Validation

This is the academic project page for the ISBI 2026 accepted paper:

**Automated Landmark Detection for assessing hip conditions: A Cross-Modality Validation of MRI versus X-ray**

## Paper Details

- **Venue**: ISBI 2026 (Accepted)
- **Authors**: Roberto Di Via, Vito Paolo Pastore, Francesca Odone, Sión Glyn-Jones, Irina Voiculescu
- **Affiliations**: MaLGa-DIBRIS, University of Genoa | Oxford University

## Links

- [Paper (arXiv)](https://arxiv.org/abs/2601.18555)
- [Code (GitHub)](https://github.com/Malga-Vision/Landmarks-Hip-Conditions)

## Abstract

Many clinical screening decisions are based on angle measurements. In particular, FemoroAcetabular Impingement (FAI) screening relies on angles traditionally measured on X-rays. However, assessing the height and span of the impingement area requires also a 3D view through an MRI scan. The two modalities inform the surgeon on different aspects of the condition.

In this work, we conduct a matched-cohort validation study (89 patients, paired MRI/X-ray) using standard heatmap regression architectures to assess cross-modality clinical equivalence. We show that MRI achieves equivalent localisation and diagnostic accuracy for cam-type impingement. Our method demonstrates clinical feasibility for FAI assessment in coronal views of 3D MRI volumes, opening the possibility for volumetric analysis through placing further landmarks.

## Key Results

- **Equivalent landmark localisation accuracy**: MRI (2.98 mm) vs X-ray (3.02 mm)
- **Identical diagnostic accuracy**: 87.5% for cam-type impingement detection
- **First cross-modality validation** of automated hip landmark detection between X-ray and MRI

## Method

We formulate FAI angle computation as a landmark detection problem. For each hip, we localise four annotated anatomical keypoints: femoral head centre (FHC), neck-axis point (NA), lateral acetabular edge (LAE), and lateral cam point (LCP). We employ UNet++ with a ResNet18 encoder (ImageNet-initialised) trained with heatmap regression.

## Website

This page is built using the [Academic Project Page Template](https://github.com/anonymity99/academic-page-template) and is hosted on GitHub Pages.

## License

<a rel="license" href="http://creativecommons.org/licenses/by-sa/4.0/"><img alt="Creative Commons License" style="border-width:0" src="https://i.creativecommons.org/l/by-sa/4.0/88x31.png" /></a><br />This work is licensed under a <a rel="license" href="http://creativecommons.org/licenses/by-sa/4.0/">Creative Commons Attribution-ShareAlike 4.0 International License</a>.
