# ENTP

This repository is the official implementation of "Fast and Accurate Element-Level Streaming CP Decomposition for Higher-Order Tensors" (submitted to ICDM 2025).

## Abstract

How can we efficiently and accurately analyze a tensor in an element-level streaming setting? An element-level streaming setting involves updating tensors in smaller portions at each time step, such as individual elements or groups of entries. This setting is particularly advantageous when a tensor has two or more temporal axes to capture periodic patterns, as it allows for a higher-order representation of temporal data and higher data stream frequency at the same time. However, existing online tensor decomposition methods are limited to conventional streaming settings, where updates occur only at the level of slices, or subtensors over time.

In this paper, we propose ENTP (Element-Level Streaming CP Decomposition), a fast and accurate method specifically designed for tensor decomposition in an element-level streaming setting. ENTP efficiently updates only the relevant factor matrices when new elements are introduced, thereby avoiding unnecessary computational overhead. Extensive experiments show that ENTP achieves up to $28\times$ speed-up compared to existing online tensor decomposition methods, while excelling in accuracy as well. Additionally, we demonstrate that ENTP delivers strong predictive performance on real-world datasets.

## Prerequisites

Our code requires Tensor Toolbox (available at https://gitlab.com/tensors/tensor_toolbox).

## Datasets

The datasets are available at [VicRoads](https://github.com/florinsch/BigTrafficData), [PEMS](https://www.timeseriesclassification.com/), and [Electricity](https://archive.ics.uci.edu/dataset/321/electricityloaddiagrams20112014).

| Dataset     | Total Size (order 3)         | Total Size (order 4)                 | Update Size |
| ----------- | ---------------------------- | ------------------------------------ | ----------- |
| VicRoads    | $1084 \times 96 \times 2030$ | $1084 \times 96 \times 7 \times 290$ | $1084$      |
| PEMS        | $963 \times 144 \times 448$  | $963 \times 144 \times 7 \times 64$  | $963$       |
| Electricity | $370 \times 96 \times 1092$  | $370 \times 96 \times 7 \times 156$  | $370$       |
