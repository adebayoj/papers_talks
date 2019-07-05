DP + {Fairness, Interpretability}
=====================
This set of notes will be about a bunch of papers that
look at satisfying differential privacy at the same time as
fairness properties, and or interpretability.



### DP + Fairness (Badasaryan & Shmatikov, 2019 and Jagielski et. al. 2019)

#### Badasaryan & Shmatikov, 2019

Main figure of the paper showing different model accuracies on 
different datasets.

Take home message: minority (possibly outlier) portions of the dataset show worse accuracy when you train with differential privacy.

Face classification has 29,500 images for lighter skin color
and 500 images for darker skin color (deliberate imbalance).
In the age classification portion, the 72 groups are the intersection
of age, gender, and skin color. It is not clear if the imbalance is 
maintained for the age classification results (I assume it is.)
In the sentiment classification, they sample 60,000 standard american english tweets, and 1000 tweets labeled African American english.
The model used here is an LSTM.

Tested models: Resnet-18, Inception-V3 (27M parameters), two layer bi-directional lstm (4.7m parameters).

<img src="https://raw.githubusercontent.com/adebayoj/papers/master/figures/dp_reading_group_summer_2019/main_figure_badasaryan_shmatikov.png" width="800"> 


The image below shows different hyperparameters on the MNIST
dataset. Clipping seems to have an especially detrimental
effect for the minority class when training is done with
DP.

<img src="https://raw.githubusercontent.com/adebayoj/papers/master/figures/dp_reading_group_summer_2019/hyperparams_bs_fairness.png" width="800"> 

 

### Interpretability & CNNS.
<img src="https://raw.githubusercontent.com/adebayoj/sanity_checks_saliency/master/doc/figures/saliency_methods_and_edge_detector.png" width="700">


### DP + Interpretability (Harder, 2019)
