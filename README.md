# SKS-Net
  This is an official implementation of SKS-Net proposed by our paper "SKS-Net: Semi-supervised Sparse Koch Snowflake Encoding Network for
Large-scale Semantic Point Cloud Segmentation (CVPR 2024)."

# New Features
  We have limited resources for maintaining and updating the code. However, we have added a few new features since the original release that are inspired by some of the excellent work many other researchers have been doing on 3DGS. We will be adding other features within the ability of our resources.

**Update of October 2024**: We integrated training speed acceleration and made it compatible with depth regularization, anti-aliasing and exposure compensation. We have enhanced the SIBR real time viewer by correcting bugs and adding features in the Top View that allows visualization of input and user cameras.

**Update of Spring 2024**: Orange Labs has kindly added OpenXR support for VR viewing.

# Roadmap
  Please note that the code release is currently in alpha. We intend to provide fixes for issues that are experienced by users, due to difficulties with setups and/or environments that we did not test on. The below steps were successfully tested on Windows and Ubuntu 22. We appreciate the documentation of issues by users and will try to address them. Furthermore, there are several points that we will integrate in the coming weeks:

  Datasets: We will add links for large-scale datasets that are currently undergoing auditing.
  Windows binaries: Once we have sufficiently tested them, we will add pre-compiled binaries for the viewers on Windows.
  Direct conversion of legacy 3DGS models: we are testing the conversion of scenes trained with vanilla 3DGS to hierarchical models. Once the quality is assured and we have concluded testing, we will document the necessary steps to do so.
  Streaming from disk: currently, data is streamed on-demand to the GPU, however, the viewed dataset must fit into memory. This can become prohibitive in the hierarchy merger and real-time viewer. We will adapt the code to allow dynamic streaming from disk soon.
  Reduce real-time viewer resource usage: the storage configuration for the real-time viewer is unoptimized, and so is the speed. Users can define a VRAM budget for the scene, but it is not used as efficiently as it could be. We will iterate towards making sure that higher quality settings can be achieved with lower budgets and better framerates. We will try to make the budget so that it effectively limits the total application VRAM, including framebuffer structs.

# Step-by-step Tutorial 
## Cloning the repo.
  Make sure to clone the repo using --recursive:
  ```
  git clone https://github.com/graphdeco-inria/hierarchical-3d-gaussians.git --recursive
  cd hierarchical-3d-gaussians
```
