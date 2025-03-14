# We will release the code soon!! #

# MD-BERT: Action Recognition in Dark Videos via Dynamic Multi-Stream Fusion and Temporal Modeling

![My Image](assets/IJCNN-25-Arch.png)

This page contains all the Datasets and Code bases (experiments and evaluations) involved in experimenting and establishing our newly proposed **MD-BERT or MultiDark-BERT** framework for video action recognition in the Dark.

The official repository of the paper with supplementary: [MD-BERT](https://arxiv.org/pdf/2502.03724) | ![Visitor Count](https://visitor-badge.laobi.icu/badge?page_id=HrishavBakulBarua.DarkBERT)




## About the project

This project is a carried out in [Monash University, Malaysia campus](https://www.monash.edu.my/).

Project Members -                                                                                                                                                                                                                                                                      
[Sharana Dharshikgan Suresh Dass](https://www.linkedin.com/in/sharana-dharshikgan-suresh-dass-361167191/?originalSubdomain=my) [(Monash University, Malaysia)](https://www.monash.edu.my/)                                                                                             
[Hrishav Bakul Barua](https://www.researchgate.net/profile/Hrishav-Barua)  [(Monash University, Australia and TCS Research, Kolkata, India)](https://www.tcs.com/what-we-do/research),                                                                                                         
[Ganesh Krishnasami](https://research.monash.edu/en/persons/ganesh-krishnasamy) [(Monash University, Malaysia)](https://www.monash.edu.my/)                                                                                                                                         
[Raveendran Paramesran](https://scholar.google.com.my/citations?user=NIbyoq0AAAAJ&hl=en) [(Monash University, Malaysia)](https://www.monash.edu.my/)                                                                                                                                   
[Raphaël C.-W. Phan](https://scholar.google.com/citations?user=wR84XY1kACcC&hl=en) [(Monash University, Malaysia)](https://www.monash.edu.my/).   

### Funding details
This work is supported by the [`Global Research Excellence Scholarship`](https://www.monash.edu.my/student-services/financial-assistance/postgraduate-scholarships/merit-scholarships), Monash University, Malaysia. This research is also supported, in part, by the prestigious [`Global Excellence and Mobility Scholarship (GEMS)`](https://www.monash.edu.my/research/support-and-scholarships/gems-scholarship), Monash University (Malaysia & Melbourne, Australia).


## Overview

Action recognition in dark, low-light (under-exposed) or noisy videos is a challenging task due to visibility degradation, which can hinder critical spatiotemporal details. This paper proposes MD-BERT, a novel multi-stream approach that integrates complementary pre-processing techniques such as gamma correction and histogram equalization alongside raw dark frames to address these challenges. We introduce the Dynamic Feature Fusion (DFF) module, extending existing atten- tional fusion methods to a three-stream setting, thereby capturing fine-grained and global contextual information across different brightness and contrast enhancements. The fused spatiotemporal features are then processed by a BERT-based (Bidirectional Encoder Representations from Transformers) temporal model, which leverages its bidirectional self-attention to effectively cap- ture long-range dependencies and contextual relationships across frames. Extensive experiments on the ARID V1.0 and ARID V1.5 dark video datasets show that MD-BERT outperforms existing methods, establishing a new state-of-the-art performance. Ablation studies further highlight the individual contributions of each input stream and the effectiveness of the proposed DFF and BERT modules.

### The Dynamic Feature Fusion (DFF) module proposed in our Architecture

![My Image](assets/DFF.png)

### Dataset samples

We use gamma correction and histogram equalization alongside raw dark frames as input to our pipeline. Visual illustration of Gamma enhanced images and histogram equalised images based 5 different classes of ARID dataset.

![My Image](assets/dataset.png)


### Histograms of dataset

verage histograms for (a) Dark frames, (b) Gamma-enhanced frames (γ = 2.5), and (c) Histogram-equalized frames. The dark frame histogram (left) illustrates the dominance of low-intensity values, reflecting the inherent challenges of low-light videos. The gamma-enhanced histogram (middle) shifts pixel intensities towards higher brightness, effectively enhancing visibility in dark regions. The histogram-equalized frame (right) shows a broader distribution of intensity values, improving contrast by redistributing intensities.

![My Image](assets/histograms.png)

## Our work utilizes the following:

### <ins>Basic Neural Network and DL models</ins>

`ICLR 2015` | `VGG-TS` - Very Deep Convolutional Networks for Large-Scale Image Recognition | [Code](https://github.com/Prabhu204/Very-Deep-Convolutional-Networks-for-Large-Scale-Image-Recognition)

`ECCV 2016` | `TSN` - Temporal Segment Networks: Towards Good Practices for Deep Action Recognition | [Code](https://github.com/Ruiyang-061X/TSN)

`CVPR 2017` | `I3D-RGB`, `I3D Two-stream` - Quo Vadis, Action Recognition? A New Model and the Kinetics Dataset | [Code](https://github.com/piergiaj/pytorch-i3d)

`ICCV 2017` | `Pseudo-3D-199` - Learning Spatio-Temporal Representation with Pseudo-3D Residual Networks | [Code](https://github.com/ZhaofanQiu/pseudo-3d-residual-networks)

`CVPR 2018` | `R(2+1)D` -  A closer look at spatiotemporal convolutions for action recognition | [Code](https://github.com/leftthomas/R2Plus1D-C3D)

`CVPR 2018` | `3D-ResNet-18`, `3D-ResNet-50`, `3D-ResNet-101` - Can Spatiotemporal 3D CNNs Retrace the History of 2D CNNs and ImageNet? | [Code](https://github.com/kenshohara/3D-ResNets-PyTorch)

`NAACL 2019` | `BERT` - BERT: Pre-training of Deep Bidirectional Transformers for Language Understanding | [Code](https://github.com/google-research/bert)


### <ins>State-of-the-art learning models for action/activity recognition in the dark</ins>

`CVPRW 2021` | `DarkLight-ResNeXt-101`, `DarkLight-R(2+1)D-34` - DarkLight Networks for Action Recognition in the Dark | [Code](https://github.com/Ticuby/Darklight-Pytorch)

`CVPRW 2021` | `MRAN` - Delta Sampling R-BERT for Limited Data and Low-Light Action Recognition | [Code](https://openaccess.thecvf.com/content/CVPR2021W/UG2/papers/Hira_Delta_Sampling_R-BERT_for_Limited_Data_and_Low-Light_Action_Recognition_CVPRW_2021_paper.pdf)

`IEEE TAI 2022` | `R(2+1)D-GCN+BERT` - Action Recognition in Dark Videos using Spatio-temporal Features and Bidirectional Encoder Representations from Transformers | [Code](https://www.isical.ac.in/~ash/Action_Recognition_in_Dark_Videos_using_Spatio-temporal_Features_and_Bidirectional_Encoder_Representations_from_Transformers.pdf)

`AAAI 2023` | `SCI + R(2+1)D-GCN` - Two-Streams: Dark and Light Networks with Graph Convolution for Action Recognition from Dark Videos | [Code](https://ojs.aaai.org/index.php/AAAI/article/view/27030)

`IEEE TIP 2023` | `DTCM` - DTCM: Joint Optimization of Dark Enhancement and Action Recognition in Videos | [Code](https://www.researchgate.net/publication/371698911_DTCM_Joint_Optimization_of_Dark_Enhancement_and_Action_Recognition_in_Videos)


### <ins>Action recognition datasets for dark videos</ins>

`DL-HAR 2020` | `ARID V1.0` & `ARID V1.5` | ARID: A New Dataset for Recognizing Action in the Dark | [Link1](https://github.com/xuyu0010/ARID_v1); [Link2](https://xuyu0010.github.io/arid.html)

`ACCV 2024` | `ELLAR` | An Action Recognition Dataset for Extremely Low-Light Conditions with Dual Gamma Adaptive Modulation | [Link](https://sites.google.com/view/knu-ellar/)


## Experiments and Results

![My Image](assets/results_1.png)

![My Image](assets/results_2.png)

For more details and experimental results please check out the paper!!

##  Citation 

If you find our work (i.e. the code, the theory/concept, or the dataset) useful for your research or development activities, please consider citing our work as follows:

~~~
@article{dass2025md,
  title={MD-BERT: Action Recognition in Dark Videos via Dynamic Multi-Stream Fusion and Temporal Modeling},
  author={Dass, Sharana Dharshikgan Suresh and Barua, Hrishav Bakul and Krishnasamy, Ganesh and Paramesran, Raveendran and Phan, Raphael C-W},
  journal={arXiv preprint arXiv:2502.03724},
  year={2025}
}
~~~


## License and Copyright


~~~
----------------------------------------------------------------------------------------
Copyright 2024 | All the authors and contributors of this repository as mentioned above.
----------------------------------------------------------------------------------------

~~~

Please check the [License](LICENSE) Agreement.


