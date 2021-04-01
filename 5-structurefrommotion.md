# Structure From Motion

The objective of this step is to understand the geometric relationship behind all the observations provided by the input images, and infer the rigid scene structure \(3D points\) with the pose \(position and orientation\) and internal calibration of all cameras. The Incremental pipeline is a growing reconstruction process. It first computes an initial two-view reconstruction that is iteratively extended by adding new views.

