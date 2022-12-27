# Mobile Freeze-Net with Attention-based Loss Function for Covid-19 Detection from an Imbalanced CXR Dataset

by Santanu Roy, Rahul Khurana

This paper has been presented as a Poster presentation in the 38th ACM/SIGAPP Symposium On Applied Computing.

In this paper, we have worked in a new direction, that is, alleviating the class imbalance problem from CXR dataset by using novel loss function. We chose a challengable CXR dataset consisting of 4 classes namely COVID, Normal, Lung Opacity and Viral Pneumonia. The real problem in this dataset is not only the class imbalance, but also huge inter and intra class variance. Hence we come up with a new strategy my modifying bias weights in WCCE based on statistical properties of images in that class.

## Methodology

![alt text](https://github.com/RahulKhurana-16/MobileFreezeNet/blob/main/images/Model1.drawio%20(8).png)



## Abstract

In this paper, we present a novel framework, that is, Mobile FreezeNet along with Attention-based Loss Function, for Covid-19 detection from a Chest X-Ray (CXR) dataset. First, we have observed that the employed CXR dataset has higher class imbalance. We have implemented several pretrained CNN models VGG-16, ResNet-50, Mobile-NetV2, Inception-V3 etc. and existing Covid Detection models like Covid-Lite, Covid-Net on this dataset. However, all those models are fraught with class imbalance problem, thus, have not produced very effective results. In this paper, we have worked on two novel directions. First, we have proposed a Mobile Freeze-Net, in which we freeze first 50% layers of Mobile NetV2 model empirically and then train only the last 50% layers of the model. Freezing 50% of layers during training of Mobile-Net V2, has significantly reduced the computational complexity of the network and consequently, removed the class imbalance problem a bit automatically. Thereafter, we have incorporated an Attention-based Loss function which gives more attention towards a class, having poor performance in the Mobile Freeze-Net. The attention or bias weights of Weighted CCE loss function is chosen from the statistical inference of the dataset itself. In order to compute such statistics (like inter and intra-class variance) for each class, we have employed a MonteCarlo method. By utilizing Mobile freeze-Net, we have achieved testing accuracy, F1 score, precision and recall of 93%, 94%, 93% and 94% respectively. This is approximately 3-4% improvement compared to 100% finetuning of Mobile-Net V2. Furthermore, we have achieved approximate 1-2% improvement of Mobile Freeze-Net, after incorporating Attention-based Loss function. For the validity of the proposed framework, we have conducted the experiments with 10-fold cross validation. All these experimental results suggest that our proposed framework has alleviated the class imbalance problem considerably.
