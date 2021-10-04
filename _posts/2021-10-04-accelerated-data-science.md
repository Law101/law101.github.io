---
title: "Welcome to Jekyll!"
date: 2021-10-04T9:57:30+01:00
categories:
  - NVIDIA RAPIDS
tags:
  - accelerated-data-science
  - RAPIDS API
---

# Accelerating End-to-End Data Science Workflows with Rapids: Introduction

Handling traditional data science workflows on CPU has gained much popularity in recent years, and it has become a starting point for exploring and manipulating data quickly. But there are some limitations; the set of tools involved in carrying out the CPU-powered operations on data are not efficient due to rapid increase in data size, high latency in getting computational results during analysis and modeling of large data. Likewise, we have seen a dramatic boost in the performance of complex and computational intensive machine learning models with blazing speed, accelerated by Graphical Processing Unit (GPU). This has been made possible with NVIDIA leading the forefront of HPC Manufacturing and other devices which can speed up data science and AI-driven processes.

The conventional way of using GPU to accelerate processes involve offloading data periodically to the GPU for compute-intense operations and later transferred back to the CPU, this approach can be time-consuming especially when data is constantly been manipulated and transformed.

![Traditional Model](/assets/images/trad-model.png)

In contrast, the RAPIDS model allows data loading directly to the GPU early in the data science process so that standard data manipulations, transformations, and other operations can be performed end-to-end on the GPU.

![Rapids Model](/assets/images/rapids-model.png)

**What is RAPIDS?**

RAPIDS is a suite of open-source software libraries and APIs that enable the execution of end-to-end data science and analytics pipelines entirely on GPUs including support for multi-GPU deployment, multi-node, accelerated processing, and training on large dataset sizes. RAPIDS utilizes NVIDIA CUDA - a low-level compute framework for parallel computing, to interact with the GPU.

The wide range of APIs and Libraries available in RAPIDS include:

- [cuDF](https://github.com/rapidsai/cudf)
    - cuDF is a Python GPU DataFrame library (built on the Apache Arrow columnar memory format) for loading, joining, aggregating, filtering, and otherwise manipulating data. cuDF uses a similar interface to Pandas so that Python data scientists can use it with very little ramp-up. ***It can handle large data especially when pandas fail***.
- cuML
    - cuML is a suite of libraries that implement machine learning algorithms and mathematical primitives functions that share compatible APIs with other RAPIDS projects. It follows the sckit-learn convention of model objects with .fit .predict/.transform with rapidly growing subset of algorithms:
        - XGBoost, DBSCAN, Logistic Regression, K-Nearest Neighbors, K-means
- cuGraph
    - cuGraph is a GPU accelerated graph analytics library, with functionality like NetworkX, which is seamlessly integrated into the RAPIDS data science platform.
- cuXFilter (pronounced as 'coo-cross-filter')
    - cuxfilter acts as a connector library, which provides the connections between different open-source (Bokeh, DataShader), and proprietary visualization libraries and a GPU dataframe without much hassle. This also allows the user to use charts from different libraries in a single dashboard, while also providing the interaction.
- CLX (pronounced as 'clicks')
    - Cyber Log Accelerators (CLX), provides a collection of RAPIDS examples for security analysts, data scientists, and engineers to quickly get started applying RAPIDS and GPU acceleration to real-world cybersecurity use cases.
- cuSpatial
    - cuSpatial is a GPU accelerated C++/Python library for accelerating GIS workflows including point-in-polygon, spatial join, coordinate systems, shape primitives, distances, and trajectory analysis.
- cuSignal
    - cuSignal leverages CuPy, Numba, and the RAPIDS ecosystem for GPU accelerated signal processing. In some cases, cuSignal is a direct port of Scipy Signal to leverage GPU compute resources via CuPy but also contains Numba CUDA kernels for additional speedups for selected functions.
- cuCIM
    - The RAPIDS cuCIM is an extensible toolkit designed to provide GPU accelerated I/O, computer vision & image processing primitives for N-Dimensional images with a focus on biomedical imaging.
- RAPIDS Memory Manager (RMM)
    - RAPIDS Memory Manager (RMM) is a central place for all device memory allocations in cuDF (C++ and Python) and other RAPIDS libraries. In addition, it is a replacement allocator for CUDA Device Memory (and CUDA Managed Memory) and a pool allocator to make CUDA device memory allocation/deallocation faster and asynchronous.

**Integrations with RAPIDS**

RAPIDS supports a wide array of other standalone open-source libraries and frameworks with seamless integration for GPU-accelerated data analytics and machine learning. 

*RAPIDS + Dask*

*RAPIDS + Spark*

RAPIDS + Plotly Dash

RAPIDS + BlazingSQL

RAPIDS + XGBoost

RAPIDS + HPO

RAPIDS + HPC

RAPIDS + Cloud

*RAPIDS + Nvidia Merlin*

**Installation on Colab**

Install RAPIDS on Google Colab by following the instruction in this notebook;

[https://colab.research.google.com/drive/1rY7Ln6rEE1pOlfSHCYOVaqt8OvDO35J0#forceEdit=true&offline=true&sandboxMode=true](https://colab.research.google.com/drive/1rY7Ln6rEE1pOlfSHCYOVaqt8OvDO35J0#forceEdit=true&offline=true&sandboxMode=true)

**References**

[https://rapids.ai/index.html](https://rapids.ai/index.html)

[Accelerating End-to-End Data Science Workflows](https://courses.nvidia.com/courses/course-v1:DLI+S-DS-01+V1/about)