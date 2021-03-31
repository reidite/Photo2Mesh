
# Photogrammetry Methodology
<p align="center">
<img alt="ubuntu" src="https://img.shields.io/badge/ubuntu-%3E%3D18.04-blueviolet?style=for-the-badge&logo=ubuntu">
<img alt="python" src="https://img.shields.io/badge/python-%3E%3D3.6-blue?style=for-the-badge&logo=python">
<img alt="numpy" src="https://img.shields.io/badge/numpy-%3E%3D1.19-skyblue?style=for-the-badge&logo=numpy">
<img alt="scipy" src="https://img.shields.io/badge/scipy-%3E%3D1.60-lightblue?style=for-the-badge&logo=scipy">
</p>
Photogrammetry is the science of making measurements from photographs. It infers the geometry of a scene from a set of unordered photographs or videos. Photography is the projection of a 3D scene onto a 2D plane, losing depth information. The goal of photogrammetry is to reverse this process.

# Method
## Natural Feature Extraction
The objective of this step is to extract distinctive groups of pixels that are, to some extent, invariant to changing camera viewpoints during image acquisition. Hence, a feature in the scene should have similar feature descriptions in all images.
### References

- David G. Lowe. [Distinctive image features from scale-invariant keypoints](https://people.eecs.berkeley.edu/~malik/cs294/lowe-ijcv04.pdf). IJCV 2004.
  ```
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
- Ives Rey Otero, Mauricio Delbracio. [Anatomy of the SIFT Method](https://www.ipol.im/pub/art/2014/82/article.pdf). IPOL 2014.
  ```
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
- Guoshen Yu, Jean-Michel Morel. [ASIFT: An Algorithm for Fully Affine Invariant Comparison](https://www.ipol.im/pub/art/2011/my-asift/article_lr.pdf). IPOL 2011.
  ```
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
- Pablo F. Alcantarilla, Jesus Nuevo, Adrien Bartoli. [Fast explicit diffusion for accelerated features in nonlinear scale spaces](http://www.bmva.org/bmvc/2013/Papers/paper0013/paper0013.pdf). BMVC 2013.
  ```
  @inproceedings{Alcantarilla2013,
  author = {Fernández Alcantarilla, Pablo},
  year = {2013},
  month = {09},
  pages = {},
  title = {Fast Explicit Diffusion for Accelerated Features in Nonlinear Scale Spaces},
  doi = {10.5244/C.27.13}
  }
- Yali Li, Shengjin Wang, Qi Tian, Xiaoqing Ding. [A survey of recent advances in visual feature detection](https://dl.acm.org/doi/10.1016/j.neucom.2014.08.003). NEUROC 2015.
  ```
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
- Andrea Vedaldi, Brian Fulkerson. [VLFeat - An open and portable library of computer vision algorithms](https://www.robots.ox.ac.uk/~vedaldi/assets/pubs/vedaldi10vlfeat.pdf). ACMM 2008.
  ```
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
## Image Matching
The objective of this part is to find images that are looking to the same areas of the scene. For that, we use the image retrieval techniques to find images that share some content without the cost of resolving all feature matches in details. The ambition is to simplify the image in a compact image descriptor which allows to compute the distance between all images descriptors efficiently.
### References

- David Nister, Henrik Stewenius. [Scalable Recognition with a Vocabulary Tree](https://my.eng.utah.edu/~cs6320/cv_files/ImageMatching.pdf). CVPR 2006.
  ```
  @inproceedings{Nister2006,
  author = {Nistér, David and Stewénius, Henrik},
  year = {2006},
  month = {02},
  pages = {2161 - 2168},
  title = {Scalable Recognition with a Vocabulary Tree},
  volume = {2},
  isbn = {0-7695-2597-0},
  journal = {Proceedings of the IEEE Computer Society Conference on Computer  Vision and Pattern Recognition},
  doi = {10.1109/CVPR.2006.264}
  }
  ```
- Matthew Brown, Richard Szeliski, Simon Winder. [Multi-Image Matching using Multi-Scale Oriented Patches Matthew](http://matthewalunbrown.com/papers/cvpr05.pdf). CVPR 2005.
  ```
  @inproceedings{Brown2005,
  author = {Brown, M. and Szeliski, R. and Winder, Simon},
  year = {2005},
  month = {07},
  pages = {510- 517 vol. 1},
  title = {Multi-image matching using multi-scale oriented patches},
  volume = {1},
  isbn = {0-7695-2372-2},
  journal = {Proceedings of the IEEE Computer Society Conference on Computer  Vision and Pattern Recognition},
  doi = {10.1109/CVPR.2005.235}
  }
  ```
## Features Matching
The objective of this step is to match all features between candidate image pairs.
## Structure From Motion
The objective of this step is to understand the geometric relationship behind all the observations provided by the input images, and infer the rigid scene structure (3D points) with the pose (position and orientation) and internal calibration of all cameras. The Incremental pipeline is a growing reconstruction process. It first computes an initial two-view reconstruction that is iteratively extended by adding new views.
## Depth Maps Estimation
The objective of this step is to retrieve the depth value of each pixel.

## Meshing
The objective of this step is to create a dense geometric surface representation of the scene.

## Texturing
The objective of this step is to texture the generated mesh.

## Localization
Based on the SFM results, we can perform camera localization and retrieve the motion of an animated camera in the scene of the 3D reconstruction.

## Camera Calibration

Becoming a super hero is a fairly straight forward process:

```
$ give me super-powers
```

Once you're strong enough, save the world:

```bash
# Ain't no code for that yet, sorry
echo 'You got to trust me on this, I saved the world'
```



