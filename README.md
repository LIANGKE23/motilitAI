# MotilitAI

<img src="./grabs.png" width="500">

With motilitAI, human semen samples from the ![VISEM dataset](https://datasets.simula.no/visem/) can be automatically assessed in respect to sperm motility. Several regression models are trained to
automatically predict the percentage (0 to 100) of progressive, non-progressive, and immotile spermatozoa in a given sample. The videos are adopted for unsupervised tracking and two different feature extraction methods, in particular custom movement statistics (cms) and mean squared displacement features (msd). We train Support Vector Regressors (SVR), Multilayer Perceptron (MLP) models, Convolutional Neural Networks (CNNs), and Recurrent Neural Networks (RNNs) on the extracted features. Best results are achieved using a linear SVR on an aggregated and quantised representation of individual displacement features of each sperm cell.

## Citing
If you use motilitAI in your research work, you are kindly asked to acknowledge the use of motilitAI in your publications.
> S. Ottl, S. Amiriparian, M. Gerczuk and B. Schuller, "A Machine Learning Framework for Automatic Prediction of Human Semen Motility", 2021. [https://arxiv.org/abs/2109.08049](https://arxiv.org/abs/2109.08049)

```
@article{ottl2021machine,
  title={A Machine Learning Framework for Automatic Prediction of Human Semen Motility},
  author={Ottl, Sandra and Amiriparian, Shahin and Gerczuk, Maurice and Schuller, Björn},
  journal={arXiv preprint arXiv:2109.08049},
  year={2021}
}

```

## Installation

Create a virtual environment, e.g. with conda:
```bash
conda create -n optical-flow-visem
conda activate optical-flow-visem
```

### Dependencies
There is an `environment.yml` file with all dependencies.

## Usage
WIP

### Prediction Models
There are two Machine Learning approaches, one using ensemble mean squared displacement (emsd) features to train different models, and one with Bags-of-Words (BoWs) created from either custom movement statistics (cms) or individual mean squared displacement (imsd) features.
```
models/emsd-prediction-models.py
models/bow-prediction-models.py 
```
