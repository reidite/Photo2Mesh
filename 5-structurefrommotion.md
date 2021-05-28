# Structure From Motion

![](.gitbook/assets/teaser.png)

The objective of this step is to understand the geometric relationship behind all the observations provided by the input images and infer the rigid scene structure \(3D points\) with the pose \(position and orientation\) and internal calibration of all cameras. The Incremental pipeline is a growing reconstruction process. It first computes an initial two-view reconstruction that is iteratively extended by adding new views.

## References

```text
@inproceedings{inproceedings,
author = {Cheng, Jian and Leng, Cong and Wu, Jiaxiang and Cui, Hainan and Lu, Hanqing},
year = {2014},
month = {06},
pages = {},
title = {Fast and Accurate Image Matching with Cascade Hashing for 3D Reconstruction},
journal = {Computer Vision and Pattern Recognition},
doi = {10.1109/CVPR.2014.8}
}
```

```text
@incollection{FISCHLER1987726,
title = {Random Sample Consensus: A Paradigm for Model Fitting with Applications to Image Analysis and Automated Cartography},
editor = {Martin A. Fischler and Oscar Firschein},
booktitle = {Readings in Computer Vision},
publisher = {Morgan Kaufmann},
address = {San Francisco (CA)},
pages = {726-740},
year = {1987},
isbn = {978-0-08-051581-6},
doi = {https://doi.org/10.1016/B978-0-08-051581-6.50070-2},
url = {https://www.sciencedirect.com/science/article/pii/B9780080515816500702},
author = {Martin A. Fischler and Robert C. Bolles},
abstract = {A new paradigm, Random Sample Consensus (RANSAC), for fitting a model to experimental data is introduced, RANSAC is capable of interpreting/ smoothing data containing a significant percentage of gross errors, and is thus ideally suited for applications in automated image analysis where interpretation is based on the data provided by error-prone feature detectors. A major portion of this paper describes the application of RANSAC to the Location Determination Problem (LDP): Given an image depicting a set of landmarks with known locations, determine that point in space from which the image was obtained. In response to a RANSAC requirement, new results are derived on the minimum number of landmarks needed to obtain a solution, and algorithms are presented for computing these minimum-landmark solutions in closed form. These results provide the basis for an automatic system that can solve the LDP under difficult viewing and analysis conditions. Implementation details and computational examples are also presented.}
}
```

```text
@inproceedings{inproceedings,
author = {Moulon, Pierre and Monasse, Pascal and Marlet, Renaud and others,},
year = {2013},
month = {12},
pages = {},
title = {Global Fusion of Relative Motions for Robust, Accurate and Scalable Structure from Motion},
journal = {Proceedings of the IEEE International Conference on Computer Vision},
doi = {10.1109/ICCV.2013.403}
}
```

```text
@inproceedings{inproceedings,
author = {Moulon, Pierre and Monasse, Pascal and Marlet, Renaud},
year = {2012},
month = {10},
pages = {},
title = {Adaptive Structure from Motion with a Contrario Model Estimation},
isbn = {978-3-642-37446-3},
journal = {11th Asian Conference on Computer Vision - ACCV},
doi = {10.1007/978-3-642-37447-0_20}
}
```

```text
@article{article,
author = {Moisan, Lionel and Moulon, Pierre and Monasse, Pascal},
year = {2012},
month = {05},
pages = {},
title = {Automatic Homographic Registration of a Pair of Images, with A Contrario Elimination of Outliers},
volume = {2},
journal = {IPOL},
doi = {10.5201/ipol.2012.mmm-oh}
}
```

```text
@inproceedings{inproceedings,
author = {Moulon, Pierre and Monasse, Pascal},
year = {2012},
month = {12},
pages = {},
title = {Unordered feature tracking made fast and easy},
doi = {10.13140/2.1.3743.3287}
}
```

```text
@inproceedings{inproceedings,
author = {Kneip, Laurent and Scaramuzza, Davide and Siegwart, Roland},
year = {2011},
month = {06},
pages = {2969-2976},
title = {A novel parametrization of the perspective-three-point problem for a direct computation of absolute camera position and orientation},
journal = {Proceedings of the IEEE Computer Society Conference on Computer Vision and Pattern Recognition},
doi = {10.1109/CVPR.2011.5995464}
}
```

```text
@article{article,
author = {Lepetit, Vincent and Moreno-Noguer, Francesc and Fua, Pascal},
year = {2009},
month = {02},
pages = {},
title = {EPnP: An accurate O(n) solution to the PnP problem},
volume = {81},
journal = {International Journal of Computer Vision},
doi = {10.1007/s11263-008-0152-6}
}
```

```text

```

