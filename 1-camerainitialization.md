---
description: >-
  This chapter describes numerical methods for estimating the camera projection
  matrix from corresponding 3D space and image entities. This computation of the
  camera matrix is known as resectioning.
---

# Camera Initialization

## Basic equations

The goal of this section is to compute the projection matrix that goes from world 3D coordinates to 2D image coordinates. The simplest such correspondence is that between a 3D point $$X$$ __and its image $$x$$ __under the unknown camera mapping and thus given sufficiently many correspondences $$X_i \leftrightarrow x_i$$ the camera matrix $$P$$ may be determined.

We assume a number of point correspondences $$X_i \leftrightarrow x_i$$ between 3D points $$X_i$$ and 2D image points $$x_i$$ are given. We are required to find a camera matrix $$P$$, namely a $$3 \times 4$$ matrix such that $$x_i = PX_i$$ for all $$i$$. For each correspondence $$X_i \leftrightarrow x_i$$ we derive a relationship:



## Geometric error

## Restricted camera estimation

## Radial distortion

## Closure

