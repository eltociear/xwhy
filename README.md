<p align="left"> </p>

 <a href="https://opensource.org/licenses/MIT"><img src="https://img.shields.io/badge/License-MIT-yellow.svg" alt="License: MIT">
 <a href="https://standardjs.com"><img src="https://img.shields.io/badge/code_style-standard-brightgreen.svg" alt="Standard - \Python Style Guide"></a> 
 
# X-Why
XWhy: eXplain Why with SMILE -- Statistical Model-agnostic Interpretability with Local Explanations
 
<p align="center">
 <img src="https://github.com/koo-ec/xwhy/blob/main/docs/graphics/XWhy_Logo_v1.png" alt="XWhy, SMILE, Explainability, Interpretability, XAI, machine learning explainability, responsible ai"> </p>



## Installation
```
pip install xwhy
```

## Simple Example
```
import xwhy
import xgboost

# train an XGBoost model
X, y = xwhy.datasets.boston()
model = xgboost.XGBRegressor().fit(X, y)

# explain the model's predictions using xwhy
# (same syntax works for LightGBM, CatBoost, scikit-learn, transformers, Spark, etc.)
explainer = xwhy.Explainer(model)
xwhy_values = explainer(X)

# visualize the first prediction's explanation
xwhy.plots.waterfall(xwhy_values[0])

```
 
## Citations
It would be appreciated a citation to our paper as follows if you use X-Why for your research:
```
@article{Aslansefat2021Xwhy,
   author  = {{Aslansefat}, Koorosh and {Hashemian}, Mojgan and {Martin}, Walker and {Papadopoulos}, Yiannis},
   title   = "{SMILE: Statistical Model-agnostic Interpretability with Local Explanations}",
   journal = {arXiv e-prints},
   year    = {2021},
   url     = {https://arxiv.org/abs/...},
   eprint  = {},
}
```
 
## Acknowledgment
This project is supported by the [Secure and Safe Multi-Robot Systems (SESAME)](https://www.sesame-project.org) H2020 Project under Grant Agreement 101017258.

## Contribution 
If you are interested in contributing to this project, please check the [contribution guidelines](https://github.com/koo-ec/xwhy/blob/main/docs/contribute/contributing.md).
