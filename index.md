## Welcome 

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

<b>Cascaded Structure Tensor Framework for Recognizing Highly Cluttered Contraband Items </b>

In the last two decades, baggage scanning has globally become one of the prime aviation security concerns. Manual screening of the baggage items is tedious, error-prone, and compromise privacy. Hence, many researchers have developed X-ray imagery-based autonomous systems to address these shortcomings. But such system lacks the capcacity to recognize concealed, cluttered and overlapping objects found at one of the times in the real-world. To cater this, we present a Cascaded Structure Tensor (CST) framework. The block diagram of the proposed CST framework is shown below. CST is a contour-driven detection framework that intelligently extracts each object by iteratively picking their transitional information from different orientations and uses only a single feed-forward convolutional neural network for recognizing them. 
![CST Block Diagram](/images/CST_BD.jpg)

CST has been rigorously tested on two publicly available GDXray and SIXray datasets containing a cumulative of 1,067,381 grayscale and colored X-ray scans. Furthermore, it outperforms state-of-the-art solutions by achieving the mean average precision score of 0.9343 on GDXray and 0.9595 on SIXray for recognizing the highly cluttered and overlapping suspicious items.  

<b> Publications </b>
1. Taimur Hassan, Samet Akcay, Mohammed Bennamoun, Salman Khan, and Naoufel Werghi, "Cascaded Structure Tensor Framework for Robust Identification of Heavily Occluded Baggage Items from X-ray Scans", Submitted in IEEE Transactions on Image Processing, 2020. [Paper](https://arxiv.org/abs/2004.06780)

2. Taimur Hassan, Meriem Bettayeb, Samet Akcay, Mohammed Bennamoun, Salman Khan, and Naoufel Werghi, "Detecting Prohibited Items in X-ray Images: A Contour Proposal Learning Approach", 27th IEEE International Conference on Image Processing (ICIP), 2020. [URL](https://cmsworkshops.com/ICIP2020/Papers/ViewPaper.asp?PaperNum=2238)
