# Natural Feature Extraction

![](.gitbook/assets/download.jpeg)

The objective of this step is to extract distinctive groups of pixels that are, to some extent, invariant to changing camera viewpoints during image acquisition. Hence, a feature in the scene should have similar feature descriptions in all images.

## Scale-Invariant Feature Transform

The most well-known feature detection method is the SIFT \(Scale-invariant feature transform\) algorithm. The initial goal of SIFT is to extract discriminative patches in a first image that can be compared to discriminative patches of a second image irrespective of rotation, translation, and scale.

![The limitations of HCD method](.gitbook/assets/sift_scale_invariant.jpg)

In 2004, D.Lowe came up with a new algorithm SIFT which extracts keypoints and computes their descriptors. 

### Scale-space Extrema Detection

The first stage of computation searches over all scales and image locations. It is implemented efficiently by using a different-of-Gaussian function to identify potential interest points that are invariant to scale and orientation.

![ For each octave of scale space, the initial image is repeatedly convolved with Gaussians to produce the set of scale space images shown on the left.](.gitbook/assets/sift_dog.jpg)

### Keypoint Localization

At each candidate location, a detailed model is fit to determine location and scale. Keypoints are selected based on measures of their stability.

### Orientation Assignment

One or more orientations are assigned to each keypoint location based on local image gradient directions. All future operations are performed on image data that has been transformed relative to the assigned orientation, scale, and location for each feature, thereby providing invariance to these transformations.

### Keypoint Descriptor

The local image gradients are measured at the selected scale in the region around each keypoint. There are transformed into a representation that allows for significant levels of local shape distortion and change in illumination.

### Keypoint Matching

Keypoints between two images are matched by identifying their nearest neighbors. But in some cases, the second closest match may be very near to the first. It may happen due to noise or some other reason. In that case,  the ratio of closest-distance to second-closest distance is taken. If it is greater than 0.8, they are rejected. It eliminates around 90% of false matches while discards only 5% of correct matches, as per the paper.

## References

* David G. Lowe. [Distinctive image features from scale-invariant keypoints](https://people.eecs.berkeley.edu/~malik/cs294/lowe-ijcv04.pdf). IJCV 2004.

  ```text
  @article{Lowe2004,
  author = {Lowe, David},
  year = {2004},
  month = {11},
  pages = {91-110},
  title = {Distinctive Image Features from Scale-Invariant Keypoints},
  volume = {60},
  journal = {International Journal of Computer Vision},
  doi = {10.1023/B%3AVISI.0000029664.99615.94}
  }
  ```

* Ives Rey Otero, Mauricio Delbracio. [Anatomy of the SIFT Method](https://www.ipol.im/pub/art/2014/82/article.pdf). IPOL 2014.

  ```text
  @phdthesis{Otero2014,
  author = {Otero, Ives},
  year = {2015},
  month = {09},
  pages = {},
  title = {Anatomy of the SIFT method},
  volume = {4},
  journal = {Image Processing On Line},
  doi = {10.5201/ipol.2014.82}
  }
  ```

* Guoshen Yu, Jean-Michel Morel. [ASIFT: An Algorithm for Fully Affine Invariant Comparison](https://www.ipol.im/pub/art/2011/my-asift/article_lr.pdf). IPOL 2011.

  ```text
  @article{Yu2011,
  author = {Yu, Guoshen and Morel, Jean-Michel},
  year = {2011},
  month = {02},
  pages = {},
  title = {ASIFT: An Algorithm for Fully Affine Invariant Comparison},
  volume = {1},
  journal = {Image Processing On Line},
  doi = {10.5201/ipol.2011.my-asift}
  }
  ```

* Pablo F. Alcantarilla, Jesus Nuevo, Adrien Bartoli. [Fast explicit diffusion for accelerated features in nonlinear scale spaces](http://www.bmva.org/bmvc/2013/Papers/paper0013/paper0013.pdf). BMVC 2013.

> ```text
> @inproceedings{Alcantarilla2013,
> author = {Fern??ndez Alcantarilla, Pablo},
> year = {2013},
> month = {09},
> pages = {},
> title = {Fast Explicit Diffusion for Accelerated Features in Nonlinear Scale Spaces},
> doi = {10.5244/C.27.13}
> }
> ```

* Yali Li, Shengjin Wang, Qi Tian, Xiaoqing Ding. [A survey of recent advances in visual feature detection](https://dl.acm.org/doi/10.1016/j.neucom.2014.08.003). NEUROC 2015.

```text
@article{Li2015,
author = {Li, Yali and Wang, Shengjin and Tian, Qi and Ding, Xiaoqing},
year = {2015},
month = {02},
pages = {736-751},
title = {A survey of recent advances in visual feature detection},
volume = {149},
journal = {Neurocomputing},
doi = {10.1016/j.neucom.2014.08.003}
}
```



* Andrea Vedaldi, Brian Fulkerson. [VLFeat - An open and portable library of computer vision algorithms](https://www.robots.ox.ac.uk/~vedaldi/assets/pubs/vedaldi10vlfeat.pdf). ACMM 2008.

```text
@inproceedings{VLFEAT2008,
author = {Vedaldi, Andrea and Fulkerson, Brian},
year = {2010},
month = {10},
pages = {1469-1472},
title = {VLFeat: An open and portable library of computer vision algorithms},
volume = {3},
journal = {MM'10 - Proceedings of the ACM Multimedia 2010 International Conference},
doi = {10.1145/1873951.1874249}
}
```

