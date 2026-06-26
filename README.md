# Deepfake Image Detection Research

This repository contains academic experiments for detecting manipulated face images and attributing them to the generative process that produced them. The work focuses on local image manipulations and evaluates how well different visual representations generalize across manipulation generators.

## Authors

- Buca Mihnea Vicentiu
- Capatina Razvan Nicolae
- Luculescu Teodor

## Research Tasks

### Cross-Generator Deepfake Detection

The first task evaluates whether a detector trained on images from one generator can detect manipulations produced by another generator. This setup measures cross-domain generalization rather than only in-domain accuracy.

The experiments compare:

- `xception41` trained from scratch
- `xception41` initialized with ImageNet-pretrained weights and fine-tuned
- Frozen CLIP and SAM representations with a trained linear classifier

### Model Attribution

The second task treats generator identification as a multiclass classification problem. Given an input image, the model predicts one of the following classes: `real`, `lama`, `ldm`, `pluralistic`, or `repaint`.

The experiments report overall accuracy, per-class accuracy, and t-SNE visualizations of learned or extracted features.

## Repository Structure

```text
.
|-- docs/
|   `-- poster.pdf
|-- notebooks/
|   |-- cross_generator_detection/
|   |   |-- 01_xception_scratch.ipynb
|   |   |-- 02_xception_imagenet_finetuning.ipynb
|   |   `-- 03_clip_sam_linear_probe.ipynb
|   `-- model_attribution/
|       |-- 01_xception_scratch.ipynb
|       |-- 02_xception_imagenet_finetuning.ipynb
|       `-- 03_clip_sam_linear_probe.ipynb
`-- README.md
```

## Data And Artifacts

The notebooks expect a local dataset containing real images and manipulated images generated with LAMA, LDM, Pluralistic, and Repaint. Large datasets, checkpoints, generated results, and model weights are intentionally not committed to the repository.

Recommended local layout:

```text
data/
`-- deepfake_local_data/
    |-- celebhq_real_data/
    |-- lama/
    |-- ldm/
    |-- pluralistic/
    `-- repaint/
```

Notebook outputs are kept in version control as experiment evidence. Re-run paths may still need to be adapted to your local or notebook-hosted environment.

## Documentation

- [`docs/poster.pdf`](docs/poster.pdf) summarizes the experiment setup and results.
- [`notebooks/README.md`](notebooks/README.md) describes the notebook organization and execution order.
