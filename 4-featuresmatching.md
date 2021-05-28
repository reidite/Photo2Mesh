# Features Matching

![](.gitbook/assets/matcher_result2.jpg)

The objective of this step is to match all features between candidate image pairs. Firstly, we perform photometric matches between the set of descriptors from 2 input images. For each feature in image A, we obtain a list of candidate features in image B and then remove all the bad candidates.

## References

```text
@article{article,
author = {Lowe, David},
year = {2004},
month = {11},
pages = {91-},
title = {Distinctive Image Features from Scale-Invariant Keypoints},
volume = {60},
journal = {International Journal of Computer Vision},
doi = {10.1023/B:VISI.0000029664.99615.94}
}
```

```text
@inproceedings{inproceedings,
author = {Muja, Marius and Lowe, David},
year = {2009},
month = {01},
pages = {331-340},
title = {Fast Approximate Nearest Neighbors with Automatic Algorithm Configuration.},
volume = {1},
journal = {VISAPP 2009 - Proceedings of the 4th International Conference on Computer Vision Theory and Applications}
}
```

