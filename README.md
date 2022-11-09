# ViSeH
## Overview
This projection includes source codes and some examples of ViSeH.
## Training
### Offline training
### Online training
## Testing
## Example
To facilitate understanding of the mechanism of ViSeH, we provide some examples. Including [pretrained models](./model_save/resnet18), a [sub-hierarchy](./hierarchy), and several [samples](./data_food101_demo) from the Ingredient-101 dataset.

Here is one of the case: predicting an image with ground-truth label [1] by the global model (Visual backbone) produces a wrong Top-1 prediction, and the predits of ground-truth is at Top-4. By introducing the VSHC and MMGF, the final output is correct.

> Sample 0, Ground Truth label: 1

> Top-1 Class prediction: Global model: [20], VSHC: [1], MMGF: [1] | final prediction: [1]

> Top-2 Class prediction: Global model: [77], VSHC: [1], MMGF: [50]

> Top-3 Class prediction: Global model: [38], VSHC: [77], MMGF: [20]

> Top-4 Class prediction: Global model: [1], VSHC: [1], MMGF: [23]

> Top-5 Class prediction: Global model: [42], VSHC: [1], MMGF: [77]
