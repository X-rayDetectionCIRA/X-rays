## Overview 

Potential threats concealed within the baggage has become one of the prime security concern all over the world. Manual recognition of these threats is a time consuming task and also subject to human errors caused by fatigue work schedules or due to less experience. Here, we aim to develop a framework which can autonomously recognize such threats especially under extreme occlusion, clutter and concealment. The project is fully sponsored by the Center for Cyber-Physical Systems, Khalifa University, United Arab Emirates.

## Team Members
1. Prof. Dr. Mohammad Bennamoun (University of Western Australia, Australia) [Profile](https://scholar.google.com/citations?user=ylX5MEAAAAAJ&hl=en)
2. Prof. Dr. Naoufel Werghi (Khalifa University, United Arab Emirates) [Profile](https://scholar.google.com/citations?hl=en&user=G_2Xpm0AAAAJ)
3. Prof. Dr. Salman Khan (Mohamed bin Zayed University of Artificial Intelligence, United Arab Emirates) [Profile](https://scholar.google.com/citations?hl=en&user=M59O9lkAAAAJ)
4. Dr. Samet Akcay (Durham University, United Kingdom) [Profile](https://scholar.google.com/citations?hl=en&user=SVpL2VMAAAAJ)
5. Dr. Taimur Hassan (Khalifa University, United Arab Emirates) [Profile](https://scholar.google.com/citations?hl=en&user=11mwy0YAAAAJ)
6. Tayaba Abbasi (Khalifa University, United Arab Emirates) [Profile](https://scholar.google.com/citations?hl=en&user=TlNyfb4AAAAJ)
7. Muhammad Shafay (Khalifa University, United Arab Emirates)

## Approaches

<b>Cascaded Structure Tensor Framework for Recognizing Highly Cluttered Baggage Threats</b>

Manual screening of the baggage items is an extremely cumbersome task which is also subjected to human errors. Many researchers have developed computer-aided screening systems to replace manual baggage threat recognition process. However, majority of the times, these systems lack the capacity to recognize concealed, cluttered and overlapping baggage items mainly due to the texture-less nature of the X-ray scans or through region-based searches. To cater this, we present a Cascaded Structure Tensor (CST) framework as shown in Figure 1. CST is a contour-driven detection framework that intelligently extracts each object by iteratively picking their transitional information from different orientations and uses only a single feed-forward convolutional neural network for recognizing them. Furthermore, the CST is inherently robust against imbalanced nature of the baggage threats since it is trained on balanced set of the baggage item proposals rather than imbalanced set of X-ray scans.

![CST Block Diagram](/images/CST_BD.jpg) 
Figure 1: Block Diagram of the CST Framework

Moreover, CST has been thoroughly evaluated on two publicly available datasets, namely, GDXray and SIXray, containing a cumulative of 1,067,381 grayscale and colored X-ray scans. In addition to this, CST framework outperforms the state-of-the-art solutions by achieving the mean average precision score of 0.9343 on GDXray and 0.9595 on SIXray for recognizing the highly cluttered and overlapping suspicious items.  

<b> Publications </b>
1. Taimur Hassan, Samet Akcay, Mohammed Bennamoun, Salman Khan, and Naoufel Werghi, "Cascaded Structure Tensor Framework for Robust Identification of Heavily Occluded Baggage Items from X-ray Scans", Submitted in IEEE Transactions on Image Processing, 2020. [Paper](https://arxiv.org/abs/2004.06780), Source Code (To be Released Soon)

2. Taimur Hassan, Meriem Bettayeb, Samet Akcay, Mohammed Bennamoun, Salman Khan, and Naoufel Werghi, "Detecting Prohibited Items in X-ray Images: A Contour Proposal Learning Approach", Accepted in 27th IEEE International Conference on Image Processing (ICIP), 2020. [URL](https://cmsworkshops.com/ICIP2020/Papers/ViewPaper.asp?PaperNum=2238)

for Recognizing Baggage Threats Under Extreme Occlusion
<b>Instance Segmentation via Incremental and Regression Learning</b>

Many researchers have developed autonomous baggage screening systems by employing upon state-of-the-art object detectors. However, these frameworks are inherently limited towards recognizing extremely cluttered and occluded items (since they are based on region-based detection schemes). Semantic segmentation networks, due to their pixel-wise recognition ability, can identify baggage threats even in extreme clutter. However, semantic segmentation network cannot differentiate between different instances of the same item (e.g. a gun overlapped on top of another gun). Through postprocessing steps like Connected Component Analysis, isolated instances of the same items generated through semantic segmentation can be recognized. However, for occluded instances, it outputs a single blob. To cater this, we propose a novel strategy whereby we modify the existing encoder-decoder, scene parsing and fully convolutional networks designed for semantic segmentation to perform instance-aware segmentation using incremental learning and regression (as shown in Figure 2).

