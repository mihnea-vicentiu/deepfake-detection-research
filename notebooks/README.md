# Notebooks

The notebooks are grouped by research task and numbered by method. Outputs are intentionally preserved as a record of the original experiment runs.

## Cross-Generator Detection

- `cross_generator_detection/01_xception_scratch.ipynb`: trains `xception41` from scratch for binary real/fake detection across generators.
- `cross_generator_detection/02_xception_imagenet_finetuning.ipynb`: fine-tunes an ImageNet-pretrained `xception41` model.
- `cross_generator_detection/03_clip_sam_linear_probe.ipynb`: evaluates frozen CLIP and SAM feature extractors with linear classifiers.

## Model Attribution

- `model_attribution/01_xception_scratch.ipynb`: trains `xception41` from scratch for generator attribution.
- `model_attribution/02_xception_imagenet_finetuning.ipynb`: fine-tunes an ImageNet-pretrained `xception41` model for attribution.
- `model_attribution/03_clip_sam_linear_probe.ipynb`: evaluates CLIP and SAM feature extraction for attribution.

## Local Artifacts

Datasets, checkpoints, and generated model outputs should be kept outside version control, for example under `data/`, `checkpoints/`, or `outputs/`.
