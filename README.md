# Introduction
This repository is used in our paper:  
  
[**Jointly Learning Aspect-Focused and Inter-Aspect Relations with Graph Convolutional Networks for Aspect Sentiment Analysis**](https://www.aclweb.org/anthology/2020.coling-main.13/)
<br>
Bin Liang, Rongdi Yin, Lin Gui<sup>\*</sup>, Jiachen Du, Ruifeng Xu<sup>\*</sup>. *Proceedings of COLING 2020*
  
Please cite our paper and kindly give a star for this repository if you use this code.

## Requirements

* Python 3.6
* PyTorch 1.0.0
* SpaCy 2.0.18
* numpy 1.15.4

## Usage

* Install [SpaCy](https://spacy.io/) package and language models with
```bash
pip install spacy
```
and
```bash
python -m spacy download en
```
* Generate aspect-focused graph with
```bash
python generate_graph_for_aspect.py
```
* Generate inter-aspect graph with
```bash
python generate_position_con_graph.py
```

## Training
* Train with command, optional arguments could be found in [train.py](/train.py) \& [train_bert.py](/train_bert.py)


* Run intergcn: ```./run_intergcn.sh```

* Run afgcn: ```./run_afgcn.sh```



* Run intergcn_bert: ```./run_intergcn_bert.sh```

* Run afgcn_bert: ```./run_afgcn_bert.sh```



## Citation

The BibTex of the citation is as follow:

```bibtex
@inproceedings{liang-etal-2020-jointly,
    title = "Jointly Learning Aspect-Focused and Inter-Aspect Relations with Graph Convolutional Networks for Aspect Sentiment Analysis",
    author = "Liang, Bin  and
      Yin, Rongdi  and
      Gui, Lin  and
      Du, Jiachen  and
      Xu, Ruifeng",
    booktitle = "Proceedings of the 28th International Conference on Computational Linguistics",
    month = dec,
    year = "2020",
    address = "Barcelona, Spain (Online)",
    publisher = "International Committee on Computational Linguistics",
    url = "https://www.aclweb.org/anthology/2020.coling-main.13",
    pages = "150--161",
    abstract = "In this paper, we explore a novel solution of constructing a heterogeneous graph for each instance by leveraging aspect-focused and inter-aspect contextual dependencies for the specific aspect and propose an Interactive Graph Convolutional Networks (InterGCN) model for aspect sentiment analysis. Specifically, an ordinary dependency graph is first constructed for each sentence over the dependency tree. Then we refine the graph by considering the syntactical dependencies between contextual words and aspect-specific words to derive the aspect-focused graph. Subsequently, the aspect-focused graph and the corresponding embedding matrix are fed into the aspect-focused GCN to capture the key aspect and contextual words. Besides, to interactively extract the inter-aspect relations for the specific aspect, an inter-aspect GCN is adopted to model the representations learned by aspect-focused GCN based on the inter-aspect graph which is constructed by the relative dependencies between the aspect words and other aspects. Hence, the model can be aware of the significant contextual and aspect words when interactively learning the sentiment features for a specific aspect. Experimental results on four benchmark datasets illustrate that our proposed model outperforms state-of-the-art methods and substantially boosts the performance in comparison with BERT.",
}
```


## Credits

* The code of this repository partly relies on [ASGCN](https://github.com/GeneZC/ASGCN) \& [ABSA-PyTorch](https://github.com/songyouwei/ABSA-PyTorch). 
* Here, I would like to express my gratitude to the authors of the [ASGCN](https://github.com/GeneZC/ASGCN) \& [ABSA-PyTorch](https://github.com/songyouwei/ABSA-PyTorch) repositories.


## Poster

A poster of our work is as follow:

<img src="/poster/poster.png" width = "90%" />
