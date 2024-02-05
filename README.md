# Suicide-rates
Suicide is a complex phenomenon that finds its root in multiple economical, social and individual causes. This scourge impacts very few people but every society experiences it, at different levels. 

Gaining a better understanding of the causes of suicides could make it easier for authorities to provide help for those who seek it, estimate the risk of suicide in an area but also help future work on this topic.

In this repository we share a study where we use real world data gathered since the 70s all around the globe to propose a model describing the suicide rate in a population depending on some economical parameters, such as the [Human Development Index](https://en.wikipedia.org/wiki/Human_Development_Index), the [Gross Domestic Product](https://en.wikipedia.org/wiki/Gross_domestic_product) but also the gender wage gap.

## How to run
The whole study is contained in the [Jupyter notebook](./notebook.ipynb), that should already be executed to allow you to read the study from your browser without running the notebook locally.

However if you wish to reproduce the results and/or contribute to this study by modifying or adding to this notebook, you will need to [install Python](https://www.python.org/downloads/) (>=3.11) and [Jupyter](https://jupyter.org/install). You can then clone this repository:
```bash
git clone https://github.com/brayevalerien/Suicide-rates
```
The notebook requires `scipy` and `scikit-learn` that you might need to install using `ip`:
```bash
pip install scipy==1.11.3 scikit-learn==1.3.1
```
You can then configure the global variables in the first code cell and run the whole notebook to get the results.

## Results
### Model
After a lengthy exploration of the data, we chose to consider the year, the country GDP, GDP per capita, HDI and gender wage gap in the country to model the suicide rate in said country. This lead us to try five models and settle on a **random forest classifier**, which got an **MSE of 16.43** on the test set after being trained on 422 observations (and tested on 182 observations).

### Complementary analysis
We also studied the effect of gender inequalities on the ratio between male suicide and female suicide. We leave linking the results of this complementary analysis with the modeling of the absolute suicide rate to future work.

### Conclusions
After applying our model we found that the economical variables describing the GDP and the HDI of the country are the main factor of suicide. By working on those factors it could be expected to see the suicide rate in the country drop by a small amount. However, we also want to underline that taking only 5 socio-economical variables as we did is not enough to accurately model the suicide rate in a region, but our model is fast and easy to implement due to the fact that obtaining the required values to run it is fairly simple. 

## Contributing
Feel free to open issues or pull requests. Although this study is mostly finished, we will happily read your work and add it to this repository if it fits our requirements.

---
*Disclaimer:* although we tried our best to make this study accurate, reproductible and valid, it is still a student project and we cannot guarantee that all our results are right. Make sure to double check before using our work for any application. If you find any mistake, please [open an issue on github](https://github.com/brayevalerien/Suicide-rates/issues) or email us at [valerien.braye@telecom-sudparis.eu](mailto:valerien.braye@telecom-sudparis.eu).