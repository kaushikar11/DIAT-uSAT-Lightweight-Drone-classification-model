# DIAT-LightCSPDNet

A compact Cross-Stage Partial Network for micro-Doppler-based small unmanned aerial vehicle (SUAV) detection and classification.

## Methodology and Approach

The work targets efficient SUAV classification from micro-Doppler (m-D) time–frequency signatures under limited compute. The approach builds on a Cross-Stage Partially Deformable Network (CSPDNet) and reduces its cost via **feature map partitioning** and **depth-wise separable convolutions**, yielding a lightweight model suitable for real-time use on resource-constrained hardware. Training and evaluation use the X-band DIAT-μSAT dataset with field-measured m-D data, extended to 10 SUAV classes. The resulting trade-off between accuracy and efficiency is intended for deployment in scenarios where both classification reliability and low resource usage matter.

## Repository Contents

- **`LightCSPDNet/`** — Proposed DIAT-LightCSPDNet model: training/evaluation notebook and `results/` (checkpoints, confusion matrix, ROC/PR curves, training history, evaluation metrics).
- **`Other models and outputs/`** — Baseline and comparison experiments:
  - **CSPDNet/** — Full CSPDNet (DIAT) implementation and results.
  - **DenseNet, ResNeXt, Wide-ResNet/** — DenseNet-121, ResNeXt-50, Wide ResNet-50 on the same task.
  - **EfficientNet/**, **Inception-V3/**, **MobileNetV2/**, **ResNet/**, **ShuffleNet/**, **SqueezeNet/** — Additional CNN baselines, each with a notebook and corresponding `results/` (checkpoints, metrics, plots).

Each subfolder contains a Jupyter notebook for reproduction and a `results/` directory with saved models and evaluation outputs.
