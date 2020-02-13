# Cassava desease classification

Cassava plant is an important source of food in the world. 
This plant is vulnerable to a number of viruses.

In this project, we fine tune the pretrained Inception V3 deep CNN trained on ImageNet 
to identify the type of disease that a given plant is infected with. 

## Data

The data used for training our CNN model is based on the [Kaggle Cassava Disease Challenge](https://www.kaggle.com/c/cassava-disease/overview).

## Model

The core of the archituecture of our CNN model is the [Inception_V3](https://arxiv.org/abs/1512.00567) deep CNN model, which was trained on the [Imagnet data](www.image-net.org). We drop the last fully connected layers of Inception and replace them with a fully connect layer of 512 hidden units and lastly a softmax layer for the multi-lable classification task. 

Note that the data set itself is highly imbalanced, with two of the classes, CMD & CBSD, dominating the examples. 
One could tackle the imbalanced nature of the data by using weights in the cost functions. Such weights will make the model pay more attention to the under-represented examples. In our work we have not used any weight which is evident in our model evaluation analysis in the code. 

## Reference

```
@misc{mwebaze2019icassava,
    title={iCassava 2019Fine-Grained Visual Categorization Challenge},
    author={Ernest Mwebaze and Timnit Gebru and Andrea Frome and Solomon Nsumba and Jeremy Tusubira},
    year={2019},
    eprint={1908.02900},
    archivePrefix={arXiv},
    primaryClass={cs.CV}
}
```

## Licence

[MIT](https://opensource.org/licenses/MIT)
