# Automated Landmark Detection for Hip Conditions: Cross-Modality Validation

This is the [academic project page](https://malga-vision.github.io/Landmarks-Hip-Conditions-AcademicPage/) for the ISBI 2026 accepted paper:

**Automated Landmark Detection for assessing hip conditions: A Cross-Modality Validation of MRI versus X-ray**

## Paper Details

- **Venue**: ISBI 2026 (Accepted)
- **Authors**: Roberto Di Via, Vito Paolo Pastore, Francesca Odone, Siôn Glyn-Jones, Irina Voiculescu
- **Affiliations**: MaLGa-DIBRIS, University of Genoa | Oxford University

## Links

- [Paper (arXiv)](https://arxiv.org/abs/2601.18555)
- [Code (GitHub)](https://github.com/Malga-Vision/Landmarks-Hip-Conditions)

## Abstract

Many clinical screening decisions are based on angle measurements. In particular, FemoroAcetabular Impingement (FAI) screening relies on angles traditionally measured on X-rays. However, assessing the height and span of the impingement area requires also a 3D view through an MRI scan. The two modalities inform the surgeon on different aspects of the condition.

In this work, we conduct a matched-cohort validation study (89 patients, paired MRI/X-ray) using standard heatmap regression architectures to assess cross-modality clinical equivalence. Seen that landmark detection has been proven effective on X-rays, we show that MRI also achieves equivalent localisation and diagnostic accuracy for cam-type impingement. Our method demonstrates clinical feasibility for FAI assessment in coronal views of 3D MRI volumes, opening the possibility for volumetric analysis through placing further landmarks. These results support integrating automated FAI assessment into routine MRI workflows.

## Key Results

- **Equivalent landmark localisation accuracy**: MRI (2.98 mm) vs X-ray (3.02 mm)
- **Identical diagnostic accuracy**: 87.5% for cam-type impingement detection
- **First cross-modality validation** of automated hip landmark detection between X-ray and MRI

## Method

We formulate FAI angle computation as a landmark detection problem. For each hip, we localise four annotated anatomical keypoints: femoral head centre (FHC), neck-axis point (NA), lateral acetabular edge (LAE), and lateral cam point (LCP). We employ UNet++ with a ResNet18 encoder (ImageNet-initialised) trained with heatmap regression.

## About this page

Static page built with the [MaLGa academic page template](https://github.com/Malga-Vision/malga-academic-page-template): no build step, no third-party scripts. Preview it locally with `python -m http.server` and open http://localhost:8000.

Before pushing, run `python tools/page_guard.py`. The Pages workflow runs the same checks on every push and publishes the page only when they pass.

## Citation

If you use this work, please cite:

```bibtex
@inproceedings{divia2026hip,
  title={Automated Landmark Detection for Assessing Hip Conditions: A Cross-Modality Validation of {MRI} versus {X-ray}},
  author={Di Via, Roberto and Pastore, Vito Paolo and Odone, Francesca and Glyn-Jones, Si{\^o}n and Voiculescu, Irina},
  booktitle={2026 IEEE 23rd International Symposium on Biomedical Imaging (ISBI)},
  pages={1--4},
  year={2026},
  publisher={IEEE},
  doi={10.1109/ISBI61048.2026.11515938}
}
```
