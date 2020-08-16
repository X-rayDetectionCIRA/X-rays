## Overview 
<p align="justify">
Potential threats concealed within the baggage has become one of the prime security concern all over the world. Manual recognition of these threats is a time consuming task and also subject to human errors caused by fatigue work schedules or due to less experience. Here, we aim to develop a framework which can autonomously recognize such threats especially under extreme occlusion, clutter and concealment. The project is fully sponsored by the Center for Cyber-Physical Systems, Khalifa University, United Arab Emirates.
</p>

## Team Members
1. Prof. Dr. Mohammad Bennamoun (University of Western Australia, Australia) [Profile](https://scholar.google.com/citations?user=ylX5MEAAAAAJ&hl=en)
2. Prof. Dr. Naoufel Werghi (Khalifa University, United Arab Emirates) [Profile](https://scholar.google.com/citations?hl=en&user=G_2Xpm0AAAAJ)
3. Prof. Dr. Salman Khan (Mohamed bin Zayed University of Artificial Intelligence, UAE) [Profile](https://scholar.google.com/citations?hl=en&user=M59O9lkAAAAJ)
4. Dr. Samet Akcay (Durham University, United Kingdom) [Profile](https://scholar.google.com/citations?hl=en&user=SVpL2VMAAAAJ)
5. Dr. Taimur Hassan (Khalifa University, United Arab Emirates) [Profile](https://scholar.google.com/citations?hl=en&user=11mwy0YAAAAJ)
6. Engr. Tayaba Abbasi (Khalifa University, United Arab Emirates) [Profile](https://scholar.google.com/citations?hl=en&user=TlNyfb4AAAAJ)
7. Engr. Muhammad Shafay (Khalifa University, United Arab Emirates)

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

<b>Incremental Instance Segmentation via Regression</b>

<p align="justify">
Many researchers have developed autonomous baggage screening systems by employing upon state-of-the-art object detectors. However, these frameworks are inherently limited towards recognizing extremely cluttered and occluded items (since they are based on region-based detection schemes). Semantic segmentation networks, due to their pixel-wise recognition ability, can identify baggage threats even in extreme clutter. However, semantic segmentation network cannot differentiate between different instances of the same item (e.g. a gun overlapped on top of another gun). Through postprocessing steps like Connected Component Analysis, isolated instances of the same items generated through semantic segmentation can be recognized. However, for occluded instances, it outputs a single blob. To cater this, we propose a novel strategy whereby we modify the existing encoder-decoder, scene parsing and fully convolutional networks designed for semantic segmentation to perform instance-aware segmentation using incremental learning and regression (as shown in Figure 2).
</p>

![Regression Instance Segmentation Block Diagram](/images/block.jpg) 
Figure 2: Block Diagram of the Proposed Regression Based Incremental Instance Segmentation Framework 

<p align="justify">
First, the model E<sub>1</sub> is trained for semantic segmentation, i.e to extract different isolated and overlapped objects (e.g. a knife overlaid on the gun). To differentiate between overlapped instances of the same item (e.g. a knife on top of another knife), we incrementally update E<sub>1</sub> in each iteration by adding new item instance classes (given small set of training examples) such that a model trained in j<sup>th</sup> iteration model E<sub>j</sub> can recognize up to ‘j’ instances of each item. In the testing phase, the input scan is first fed to the trained E<sub>1</sub> model to obtain masks of the different detected items (isolated and overlapped). The corresponding patches in the original scan are passed into the regressor to determine the maximum number, k, of overlapped instances in the scan. The number k is used to select the appropriate instance segmentation model (E<sub>k</sub>).
</p>

<b>Dissemination</b>

1. Taimur Hassan, Samet Akcay, Mohammed Bennamoun, Salman Khan, and Naoufel Werghi, "Incremental Instance Segmentation Framework for Recognizing Extremely Cluttered Baggage Threats", Submitted in IEEE Transactions on Circuits and Systems for Video Technology, August 2020. [Source Code](https://github.com/taimurhassan/inc-instance-seg)

<b>Incremental Learning Driven Instance Segmentation</b>

<p align="justify">
In the previous approach, the regressor model selects the accurate instance of the encoder-decoder model for instance segmentation. However, the use of the regression model is an additional overhead within the complete framework which can be easily avoided. Here, we propose a new instance segmentation approach in which we incrementally evolve the conventional encoder-decoder, scene parsing and fully convolutional networks to perform instance-aware segmentation based upon Bayesian inference. At each iteration, the network learns new classes of the item instances while simultaneously retaining its previously acquired knowledge based upon the proposed incremental learning loss function, which penalizes the network (in each iteration) to learn the mutual relationship and inter-dependencies between different knowledge representations through Bayes Rule. The block diagram of the incremental learning driven instance segmentation is shown in Figure 3.
</p>

![Instance Segmentation Block Diagram](/images/Figure3.jpg) 
Figure 3: Block Diagram of the Proposed Incremental Learning Driven Instance Segmentation Framework 

<b> Dissemination </b>

<p align="justify">
1. Taimur Hassan, Samet Akcay, Mohammed Bennamoun, Salman Khan, and Naoufel Werghi, "A Novel Incremental Learning Driven Instance Segmentation Framework to Recognize Highly Cluttered Instances of the Contraband Items", Submitted in IEEE Transactions on Systems, Man, and Cybernetics: Systems, June 2020. 
</p>

<b>Trainable Structure Tensors for Autonomous Baggage Threat Detection Under Extreme Occlusion</b>

<p align="justify">
Here, we present a novel instance detection (and instance segmentation) approach based on trainable structure tensor scheme to highlight the contours of the occluded and cluttered contraband items obtained from multiple predominant orientations w.r.t the scan gradients. The block diagram of the proposed scheme is shown in Figure 4. First of all, the input scan is passed through the structure tensor module. Afterward, the resultant tensor (showcasing the transitional patterns of the baggage content) is passed through the encoder-decoder network that only retains the contours of the threatening items while suppressing the rest of the baggage content. Apart from this, the backbone encoder-decoder outputs the contours of the suspicious items and from each item contour, the corresponding bounding box and the mask are generated highlighting the detected item. Here, it should be noticed that the use of the encoder-decoder backbone within the proposed framework not only aids in extracting the contours of the contraband items while suppressing the unwanted boundaries. But it also helps in recognizing to which item they belong to. In addition to this, the proposed framework has been rigorously tested on four publicly available X-ray datasets where it outperforms the state-of-the-art frameworks in terms of mean average precision scores. Furthermore, to the best of our knowledge, it is the only framework that has been rigorously tested on combined grayscale and colored scans obtained from four different types of X-ray scanners.
</p>

![Trainable Tensor Block Diagram](/images/Picture1.png) 
Figure 4: Block Diagram of the Proposed Trainable Tensor Driven Instance Segmentation Framework 

<b> Dissemination </b>

<p align="justify">
1. Taimur Hassan, Samet Akcay, Mohammed Bennamoun, Salman Khan, and Naoufel Werghi, "Trainable Structure Tensors for Autonomous Baggage Threat Detection Under Extreme Occlusion", Submitted in Asian Conference on Computer Vision (ACCV), July 2020. 
</p>

<b>Tensor Pooling Driven Instance Segmentation</b>

<p align="justify">
Screening baggage to identify potential threats is a difficult task even from expert security staff. Towards this end, researchers have developed autonomous systems capable of screening suspicious items from the X-ray scans. However, these frameworks are limited towards detecting baggage threats subject to high clutter, concealment and extreme occlusion. Here, we present a novel instance segmentation framework that analyzes the predominant orientations of the contraband items at multiple scales and utilizes them for recognizing baggage threats in a high cluttered scenario. The block diagram of the proposed framework is shown in Figure 5. At first, the input scan is passed to the tensor pooling module which generates the multi-scale tensor containing the contours of the baggage items. Afterward, the generated tensor is passed to the asymmetric encoder-decoder backbone that segments and recognize the contours of the contraband item while suppressing the rest of the baggage content. For each detected contour, the corresponding bounding box and mask is generated (using minimum bounding rectangle and inward interpolation techniques) to localize the detected contraband items. 
</p>

![Trainable Tensor Block Diagram](/images/Picture2.png) 
Figure 5: Block Diagram of the Proposed Tensor Pooling Driven Instance Segmentation Framework 

<p align="justify">
The proposed framework has been thoroughly validated on the three publicly available large-scale baggage X-ray datasets, namely, GDXray, SIXray, and the OPIXray, achieving the mean average precision score of 0.8748, 0.7866, and 0.7503, respectively.
</p>

<b> Dissemination </b>

<p align="justify">
1. Taimur Hassan, Bilal Hassan, Samet Akcay, Mohammed Bennamoun, Salman Khan, and Naoufel Werghi, "Tensor Pooling Driven Instance Segmentation for Baggage Threat Recognition Under Extreme Occlusion", To be submitted in IEEE Transactions on Multimedia, August 2020. 
</p>

## Applicability of Proposed Frameworks in Other Domains

<p align="justify">
While the prime emphasis of the developed approaches is for recognizing the baggage threats under extreme occlusion. Nevertheless, they are equally applicable to other domains as well. Here, we have applied the developed frameworks for solving medical imaging problems as discussed below:
</p>

<b>RAG-FW: A Hybrid Convolutional Framework for Diagnosing and Grading Retinopathy</b>

<p align="justify">
The identification of retinal lesions plays a vital role in accurately classifying and grading retinopathy. Many researchers have presented studies on optical coherence tomography (OCT) based retinal image analysis over the past. However, to the best of our knowledge, there is no framework yet available that can extract retinal lesions from multi-vendor OCT scans and utilize them for the intuitive severity grading of the human retina. To cater this lack, we propose a deep retinal analysis and grading framework (RAG-FW). RAG-FW is a hybrid convolutional framework that extracts multiple retinal lesions from OCT scans and utilizes them for lesion-influenced grading of retinopathy as per the clinical standards. RAG-FW has been rigorously tested on 43,613 scans from five highly complex publicly available datasets, containing multi-vendor scans, where it achieved the mean intersection-over-union score of 0.8055 for extracting the retinal lesions and the accuracy of 98.70% for the correct severity grading of retinopathy.
</p>

![RAG-FW](/images/Picture3.PNG) 
Figure 5: Block Diagram of the Proposed RAG-FW Framework

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
Figure 6: Block Diagram of the Proposed Glaucomatous Grading Framework

<b> Dissemination </b>

<p align="justify">
1. Hina Raja, Taimur Hassan, Muhammad Usman Akram, Naoufel Werghi, "Clinically Verified Hybrid Deep Learning System for Retinal Ganglion Cells Aware Grading of Glaucomatous Progression", Submitted in IEEE Transactions on Biomedical Engineering, June 2020. 
</p>

## Demos

For demos videos, please contact us at taimur.hassan@ku.ac.ae

## Publications

<b>Accepted/ Published</b>
  
1. Taimur Hassan, Meriem Bettayeb, Samet Akcay, Mohammed Bennamoun, Salman Khan, and Naoufel Werghi, "Detecting Prohibited Items in X-ray Images: A Contour Proposal Learning Approach", Accepted in 27th IEEE International Conference on Image Processing (ICIP), May 2020.

2. Taimur Hassan, Muhammad Usman Akram, Naoufel Werghi, Muhammad Noman Nazir, "RAG-FW: A hybrid convolutional framework for the automated extraction of retinal lesions and lesion-influenced grading of human retinal pathology", IEEE Journal of Biomedical and Health Informatics, March 2020. 

3. Muhammad Usman Akram, Shahzad Akhbar, Taimur Hassan, Sajid Gul Khawaja, Ubaidullah Yasin, Imran Basit, "Data on fundus images for vessels segmentation, detection of hypertensive retinopathy, diabetic retinopathy and papilledema", Elsevier Data in Brief, February 2020. 

4. Taimur Hassan, Muhammad Usman Akram, Imran Basit, "Analysis of optical coherence tomography images using deep convolutional neural network for maculopathy grading", Diabetes and Retinopathy, May 2020.

5. Taimur Hassan, Muhammad Usman Akram, Naoufel Werghi, "Exploiting the Transferability of Deep Learning Systems Across Multi-modal Retinal Scans for Extracting Retinopathy Lesions", Accepted in 20th IEEE International Conference on BioInformatics And BioEngineering (BIBE), August 2020.

<b>Under Review</b>
  
1. Taimur Hassan, Samet Akcay, Mohammed Bennamoun, Salman Khan, and Naoufel Werghi, "Cascaded Structure Tensor Framework for Robust Identification of Heavily Occluded Baggage Items from X-ray Scans", Submitted in IEEE Transactions on Image Processing, May 2020.

3. Taimur Hassan, Samet Akcay, Mohammed Bennamoun, Salman Khan, and Naoufel Werghi, "Incremental Instance Segmentation Framework for Recognizing Extremely Cluttered Baggage Threats", Submitted in IEEE Transactions on Circuits and Systems for Video Technology, August 2020.

3. Taimur Hassan, Samet Akcay, Mohammed Bennamoun, Salman Khan, and Naoufel Werghi, "A Novel Incremental Learning Driven Instance Segmentation Framework to Recognize Highly Cluttered Instances of the Contraband Items", Submitted in IEEE Transactions on Systems, Man, and Cybernetics: Systems, June 2020. 

4. Taimur Hassan, Samet Akcay, Mohammed Bennamoun, Salman Khan, and Naoufel Werghi, "Trainable Structure Tensors for Autonomous Baggage Threat Detection Under Extreme Occlusion", Submitted in Asian Conference on Computer Vision (ACCV), July 2020. 

5. Hina Raja, Taimur Hassan, Muhammad Usman Akram, Naoufel Werghi, "Clinically Verified Hybrid Deep Learning System for Retinal Ganglion Cells Aware Grading of Glaucomatous Progression", Submitted in IEEE Transactions on Biomedical Engineering, June 2020. 
