# Automated Threat Detection in X-ray Imagery for Advanced Security Applications

## Overview 
<p align="justify">
Potential threats concealed within the baggage has become one of the prime security concern all over the world. Manual recognition of these threats is a time consuming task and also subject to human errors caused by fatigue work schedules or due to less experience. Here, we aim to develop a framework which can autonomously recognize such threats especially under extreme occlusion, clutter and concealment. The project is fully sponsored by the Center for Cyber-Physical Systems, Khalifa University, United Arab Emirates.
</p>

## Team Members
1. Prof. Dr. Ernesto Damiani (Khalifa University, United Arab Emirates) [Profile](https://scholar.google.com/citations?user=aC7ZsHAAAAAJ&hl=en)
2. Prof. Dr. Naoufel Werghi (Khalifa University, United Arab Emirates) [Profile](https://scholar.google.com/citations?hl=en&user=G_2Xpm0AAAAJ)
3. Dr. Taimur Hassan (Khalifa University, United Arab Emirates) [Profile](https://scholar.google.com/citations?hl=en&user=11mwy0YAAAAJ)

## External Collaborators
1. Prof. Dr. Mohammad Bennamoun (University of Western Australia, Australia) [Profile](https://scholar.google.com/citations?user=ylX5MEAAAAAJ&hl=en)
2. Prof. Dr. Salman Khan (Mohamed bin Zayed University of Artificial Intelligence, United Arab Emirates) [Profile](https://scholar.google.com/citations?hl=en&user=M59O9lkAAAAJ)
3. Dr. Samet Akcay (Durham University, United Kingdom) [Profile](https://scholar.google.com/citations?hl=en&user=SVpL2VMAAAAJ)

## Approaches

<b>Cascaded Structure Tensor Framework for Recognizing Highly Cluttered Baggage Threats</b>

<p align="justify">
Manual screening of the baggage items is an extremely cumbersome task which is also subjected to human errors. Many researchers have developed computer-aided screening systems to replace manual baggage threat recognition process. However, majority of the times, these systems lack the capacity to recognize concealed, cluttered and overlapping baggage items mainly due to the texture-less nature of the X-ray scans or through region-based searches. To cater this, we present a Cascaded Structure Tensor (CST) framework as shown in Figure 1. CST is a contour-driven detection framework that intelligently extracts each object by iteratively picking their transitional information from different orientations and uses only a single feed-forward convolutional neural network for recognizing them. Furthermore, the CST is inherently robust against imbalanced nature of the baggage threats since it is trained on balanced set of the baggage item proposals rather than imbalanced set of X-ray scans.
</p>

![CST Block Diagram](/images/CST_BD.jpg) 
Figure 1: Block Diagram of the CST Framework

<p align="justify">
Moreover, CST has been thoroughly evaluated on two publicly available datasets, namely, GDXray and SIXray, containing a cumulative of 1,067,381 grayscale and colored X-ray scans. In addition to this, CST framework outperforms the state-of-the-art solutions by achieving the mean average precision score of 0.9343 on GDXray and 0.9595 on SIXray for recognizing the highly cluttered and overlapping suspicious items.  
</p>

<b> Dissemination </b>

1. Taimur Hassan, Samet Akcay, Mohammed Bennamoun, Salman Khan, and Naoufel Werghi, "Cascaded Structure Tensor Framework for Robust Identification of Heavily Occluded Baggage Items from X-ray Scans", Submitted in IEEE Transactions on Image Processing, May 2020. [Paper](https://arxiv.org/abs/2004.06780), Source Code (To be Released Soon)

2. Taimur Hassan, Meriem Bettayeb, Samet Akcay, Mohammed Bennamoun, Salman Khan, and Naoufel Werghi, "Detecting Prohibited Items in X-ray Images: A Contour Proposal Learning Approach", Accepted in 27th IEEE International Conference on Image Processing (ICIP), May 2020. [URL](https://cmsworkshops.com/ICIP2020/Papers/ViewPaper.asp?PaperNum=2238)

## Applicability of Proposed Frameworks in Other Domains

<p align="justify">
While the prime emphasis of the developed approaches is for recognizing the baggage threats under extreme occlusion. Nevertheless, they are equally applicable to other domains as well. Here, we have applied the developed frameworks for solving medical imaging problems as discussed below:
</p>

<b>RAG-FW: A Hybrid Convolutional Framework for Diagnosing and Grading Retinopathy</b>

<p align="justify">
The identification of retinal lesions plays a vital role in accurately classifying and grading retinopathy. Many researchers have presented studies on optical coherence tomography (OCT) based retinal image analysis over the past. However, to the best of our knowledge, there is no framework yet available that can extract retinal lesions from multi-vendor OCT scans and utilize them for the intuitive severity grading of the human retina. To cater this lack, we propose a deep retinal analysis and grading framework (RAG-FW). RAG-FW is a hybrid convolutional framework that extracts multiple retinal lesions from OCT scans and utilizes them for lesion-influenced grading of retinopathy as per the clinical standards. RAG-FW has been rigorously tested on 43,613 scans from five highly complex publicly available datasets, containing multi-vendor scans, where it achieved the mean intersection-over-union score of 0.8055 for extracting the retinal lesions and the accuracy of 98.70% for the correct severity grading of retinopathy.
</p>

![RAG-FW](/images/Picture3.PNG) 
Figure 2: Block Diagram of the Proposed RAG-FW Framework

<b> Dissemination </b>

1. Taimur Hassan, Muhammad Usman Akram, Naoufel Werghi, Muhammad Noman Nazir, "RAG-FW: A hybrid convolutional framework for the automated extraction of retinal lesions and lesion-influenced grading of human retinal pathology", IEEE Journal of Biomedical and Health Informatics, March 2020. [Paper](https://ieeexplore.ieee.org/document/9049083), [Source Code](http://biomisa.org/index.php/downloads/)

2. Muhammad Usman Akram, Shahzad Akhbar, Taimur Hassan, Sajid Gul Khawaja, Ubaidullah Yasin, Imran Basit, "Data on fundus images for vessels segmentation, detection of hypertensive retinopathy, diabetic retinopathy and papilledema", Elsevier Data in Brief, February 2020. [Paper](https://www.sciencedirect.com/science/article/pii/S2352340920301761)

3. Taimur Hassan, Muhammad Usman Akram, Imran Basit, "Analysis of optical coherence tomography images using deep convolutional neural network for maculopathy grading", Diabetes and Retinopathy, May 2020.

4. Taimur Hassan, Muhammad Usman Akram, Naoufel Werghi, "Exploiting the Transferability of Deep Learning Systems Across Multi-modal Retinal Scans for Extracting Retinopathy Lesions", Accepted in 20th IEEE International Conference on BioInformatics And BioEngineering (BIBE), August 2020 [Paper](https://arxiv.org/abs/2006.02662), [Source Code](http://biomisa.org/index.php/downloads/) 

<b>Clinically Verified Hybrid Deep Learning System for Retinal Ganglion Cells Aware Grading of Glaucomatous Progression</b>

<p align="justify">
Glaucoma is the second leading cause of irreversible blindness worldwide. With the advent of spectral-domain optical coherence tomography (SD-OCT), glaucomatous progression can be easily monitored by analyzing the degradation of retinal ganglion cells (RGCs). Many researchers have worked on diagnosing glaucoma by measuring the cup-to-disc ratio from the fused fundus and SD-OCT imagery. However, to the best of our knowledge, there is no literature available which robustly measures the pathological variations of ganglion cell bodies, dendrites, and axons within ganglion cell complex (GCC) region to grade the severity of glaucoma. The paper presents a novel strategy encompassing a hybrid convolutional network that extracts the retinal nerve fiber layer (RNFL), ganglion cell with the inner plexiform layer (GC-IPL) and GCC regions, allowing thus a quantitative screening of glaucomatous subjects. Furthermore, the severity of glaucoma in screened cases is objectively graded by analyzing the RGC atrophy through RNFL, GC-IPL, and GCC thickness profiles. The proposed framework has been rigorously tested on publicly available Armed Forces Institute of Ophthalmology (AFIO) dataset (containing highly annotated optic nerve head SD-OCT scans), where it achieved the $F_1$ score of 0.9577 for diagnosing glaucoma, a mean dice coefficient score of 0.8697 for extracting the RGCs and an accuracy of 0.9117 for grading glaucomatous progression. Also, the performance of the proposed framework has been clinically verified with the markings of four expert ophthalmologists, achieving a statistically significant Pearson correlation coefficient of 0.9236.

</p>

![RAG-FW](/images/Picture10.png) 
Figure 3: Block Diagram of the Proposed Glaucomatous Grading Framework

<b> Dissemination </b>

<p align="justify">
1. Hina Raja, Taimur Hassan, Muhammad Usman Akram, Naoufel Werghi, "Clinically Verified Hybrid Deep Learning System for Retinal Ganglion Cells Aware Grading of Glaucomatous Progression", Submitted in IEEE Transactions on Biomedical Engineering, June 2020. 
</p>

## Publications

<b>Accepted/ Published</b>
  
1. Taimur Hassan, Meriem Bettayeb, Samet Akcay, Mohammed Bennamoun, Salman Khan, and Naoufel Werghi, "Detecting Prohibited Items in X-ray Images: A Contour Proposal Learning Approach", Accepted in 27th IEEE International Conference on Image Processing (ICIP), May 2020. [URL](https://cmsworkshops.com/ICIP2020/Papers/ViewPaper.asp?PaperNum=2238)

2. Taimur Hassan, Muhammad Usman Akram, Naoufel Werghi, Muhammad Noman Nazir, "RAG-FW: A hybrid convolutional framework for the automated extraction of retinal lesions and lesion-influenced grading of human retinal pathology", IEEE Journal of Biomedical and Health Informatics, March 2020. [Paper](https://ieeexplore.ieee.org/document/9049083), [Source Code](http://biomisa.org/index.php/downloads/)

3. Muhammad Usman Akram, Shahzad Akhbar, Taimur Hassan, Sajid Gul Khawaja, Ubaidullah Yasin, Imran Basit, "Data on fundus images for vessels segmentation, detection of hypertensive retinopathy, diabetic retinopathy and papilledema", Elsevier Data in Brief, February 2020. [Paper](https://www.sciencedirect.com/science/article/pii/S2352340920301761), [Dataset](https://data.mendeley.com/datasets/3csr652p9y/2)

4. Taimur Hassan, Muhammad Usman Akram, Imran Basit, "Analysis of optical coherence tomography images using deep convolutional neural network for maculopathy grading", Diabetes and Retinopathy, May 2020.

5. Taimur Hassan, Muhammad Usman Akram, Naoufel Werghi, "Exploiting the Transferability of Deep Learning Systems Across Multi-modal Retinal Scans for Extracting Retinopathy Lesions", Accepted in 20th IEEE International Conference on BioInformatics And BioEngineering (BIBE), August 2020. [Paper](https://arxiv.org/abs/2006.02662), [Source Code](http://biomisa.org/index.php/downloads/) 

<b>Under Review</b>
  
1. Taimur Hassan, Samet Akcay, Mohammed Bennamoun, Salman Khan, and Naoufel Werghi, "Cascaded Structure Tensor Framework for Robust Identification of Heavily Occluded Baggage Items from X-ray Scans", Submitted in IEEE Transactions on Image Processing, May 2020. [Paper](https://arxiv.org/abs/2004.06780)

2. Taimur Hassan, Samet Akcay, Mohammed Bennamoun, Salman Khan, and Naoufel Werghi, "Incremental Instance Segmentation Framework for Recognizing Extremely Cluttered Baggage Threats", Submitted in IEEE Transactions on Circuits and Systems for Video Technology, August 2020. 

3. Taimur Hassan, Samet Akcay, Mohammed Bennamoun, Salman Khan, and Naoufel Werghi, "A Novel Incremental Learning Driven Instance Segmentation Framework to Recognize Highly Cluttered Instances of the Contraband Items", Submitted in IEEE Transactions on Systems, Man, and Cybernetics: Systems, June 2020. 

4. Taimur Hassan, Samet Akcay, Mohammed Bennamoun, Salman Khan, and Naoufel Werghi, "Trainable Structure Tensors for Autonomous Baggage Threat Detection Under Extreme Occlusion", Submitted in Asian Conference on Computer Vision (ACCV), July 2020. 

5. Hina Raja, Taimur Hassan, Muhammad Usman Akram, Naoufel Werghi, "Clinically Verified Hybrid Deep Learning System for Retinal Ganglion Cells Aware Grading of Glaucomatous Progression", Submitted in IEEE Transactions on Biomedical Engineering, June 2020. 

## Acknowledgement

This work is supported by a research fund from CIRA, Khalifa University Ref: CIRA-2019-047.
