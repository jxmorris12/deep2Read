---
layout: post
title: Basic16- DNN to be Scalable 
desc: 2017-team
tags:
- 0Basics
- 2Structures
categories: 2017Reads
---

| Presenter | Papers | Paper URL|  Our Slides |
| -----: | -------------------------------------: | :----- | :----- |
|  scalable  | Sanjiv Kumar (Columbia EECS 6898), Lecture: Introduction to large-scale machine learning 2010 [^1]| [PDF](http://www.sanjivk.com/EECS6898/) | |
| data scalable | Alex Smola - Berkeley SML: Scalable Machine Learning:  Syllabus 2012 [^2]  | [PDF 2014](http://alex.smola.org/teaching/berkeley2012/syllabus.html) + [PDF](http://alex.smola.org/teaching/aaai2014/AAAI2014.pdf)|  |
| Binary | Binarized Neural Networks: Training Deep Neural Networks with Weights and Activations Constrained to +1 or -1 | | | 
| Model | Binary embeddings with structured hashed projections [^3] | [PDF](https://arxiv.org/abs/1511.05212) | [PDF]({{site.baseurl}}/MoreTalksTeam/Un17/Tobin-BinaryEmbedding.pdf) |
| Model |  Deep Compression: Compressing Deep Neural Networks (ICLR 2016) [^4]| [PDF](https://arxiv.org/abs/1510.00149) |  [PDF]({{site.baseurl}}/MoreTalksTeam/Un17/Muthu-Compression.pdf) | 


####  Syllabus from Sanjiv Kuman Course 

```
+ Randomized Algorithms
+ Matrix Approximations I (low-rank approximation, decomposition)
+ Matrix Approximations II (sparse matrices, matrix completion)
+ Approximate Nearest Neighbor Search I (trees)
+ Approximate Nearest Neighbor Search II (hashes)
+ Fast Optimization (first-order methods)
+ Kernel Methods I (fast training)
+ Kernel Methods II (fast testing)
+ Dimensionality Reduction (linear and nonlinear methods)
+ Sparse Methods/Streaming (sparse coding...)
```


####  Syllabus from Smola Course 

###### SML: Systems
+ Hardware: Processor, RAM, buses, GPU, disk, SSD, network, switches, racks, server centers / Bandwidth, latency and faults
+ Basic parallelization paradigms:  Trees, stars, rings, queues / Hashing (consistent, proportional) / Distributed hash tables and P2P 
+ Storage: RAID / Google File System / HadoopFS / Distributed (key, value) storage
+ Processing:  MapReduce / Dryad / S4 / stream processing
+ Structured access beyond SQL:  BigTable / Cassandra

###### SML: Data Streams
+ Random subsets: Hash functions / Approximate moments / Alon-Matias-Szegedy sketch
+ Heavy hitter detection: Lossy counting / Space saving
+ Randomized statistics: Flajolet counter / Bloom filter and logarithmic randomized techniques / CountMin sketch

###### SML: optimization: 
+ Batch methods:  Distributed subgradient / Bundle methods
+ Online methods: Unconstrained subgradient / Gradient projections / Parallel optimization
+ Efficient Kernel algorithms: Dual space (using α) / Reduced dimensionality (low rank expanions) / Function space (using fast Kα) / Primal space (hashing & random kitchen sinks)






[^3]: <sub><sup> Deep Compression: Compressing Deep Neural Networks (ICLR 2016) / Song Han, Huizi Mao, William J. Dally / conference paper at ICLR 2016 (oral) / Neural networks are both computationally intensive and memory intensive, making them difficult to deploy on embedded systems with limited hardware resources. To address this limitation, we introduce "deep compression", a three stage pipeline: pruning, trained quantization and Huffman coding, that work together to reduce the storage requirement of neural networks by 35x to 49x without affecting their accuracy. Our method first prunes the network by learning only the important connections. Next, we quantize the weights to enforce weight sharing, finally, we apply Huffman coding. After the first two steps we retrain the network to fine tune the remaining connections and the quantized centroids. Pruning, reduces the number of connections by 9x to 13x; Quantization then reduces the number of bits that represent each connection from 32 to 5. On the ImageNet dataset, our method reduced the storage required by AlexNet by 35x, from 240MB to 6.9MB, without loss of accuracy. Our method reduced the size of VGG-16 by 49x from 552MB to 11.3MB, again with no loss of accuracy. This allows fitting the model into on-chip SRAM cache rather than off-chip DRAM memory. Our compression method also facilitates the use of complex neural networks in mobile applications where application size and download bandwidth are constrained. Benchmarked on CPU, GPU and mobile GPU, compressed network has 3x to 4x layerwise speedup and 3x to 7x better energy efficiency. </sup></sub>



[^4]: <sub><sup> Binary embeddings with structured hashed projections /Anna Choromanska, Krzysztof Choromanski, Mariusz Bojarski, Tony Jebara, Sanjiv Kumar, Yann LeCun (Submitted on 16 Nov 2015 (v1), last revised 1 Jul 2016 (this version, v5))/ We consider the hashing mechanism for constructing binary embeddings, that involves pseudo-random projections followed by nonlinear (sign function) mappings. The pseudo-random projection is described by a matrix, where not all entries are independent random variables but instead a fixed "budget of randomness" is distributed across the matrix. Such matrices can be efficiently stored in sub-quadratic or even linear space, provide reduction in randomness usage (i.e. number of required random values), and very often lead to computational speed ups. We prove several theoretical results showing that projections via various structured matrices followed by nonlinear mappings accurately preserve the angular distance between input high-dimensional vectors. To the best of our knowledge, these results are the first that give theoretical ground for the use of general structured matrices in the nonlinear setting. In particular, they generalize previous extensions of the Johnson-Lindenstrauss lemma and prove the plausibility of the approach that was so far only heuristically confirmed for some special structured matrices. Consequently, we show that many structured matrices can be used as an efficient information compression mechanism. Our findings build a better understanding of certain deep architectures, which contain randomly weighted and untrained layers, and yet achieve high performance on different learning tasks. We empirically verify our theoretical findings and show the dependence of learning via structured hashed projections on the performance of neural network as well as nearest neighbor classifier. </sup></sub>