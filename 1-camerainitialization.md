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

<img src="https://latex.codecogs.com/svg.image?\begin{bmatrix}&space;0^T&space;&&space;&space;-w_i\textbf{X}_{i}^{T}&&space;y_i\textbf{X}_{i}^{T}&space;\\&space;w_i\textbf{X}_{i}^{T}&&space;0^T&space;&&space;-x_i\textbf{X}_{i}^{T}&space;\\&space;-y_i\textbf{X}_{i}^{T}&&space;x_i\textbf{X}_{i}^{T}&space;&&space;0^T&space;\\\end{bmatrix}\begin{pmatrix}&space;\textbf{P}^1\\&space;\textbf{P}^2\\&space;\textbf{P}^3\\\end{pmatrix}&space;=&space;0" title="\begin{bmatrix} 0^T & -w_i\textbf{X}_{i}^{T}& y_i\textbf{X}_{i}^{T} \\ w_i\textbf{X}_{i}^{T}& 0^T & -x_i\textbf{X}_{i}^{T} \\ -y_i\textbf{X}_{i}^{T}& x_i\textbf{X}_{i}^{T} & 0^T \\\end{bmatrix}\begin{pmatrix} \textbf{P}^1\\ \textbf{P}^2\\ \textbf{P}^3\\\end{pmatrix} = 0" />

## Geometric error

## Restricted camera estimation

## Radial distortion

## Closure

