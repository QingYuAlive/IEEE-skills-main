# IEEE Corpus Evidence Index
Generated from all PDFs in `IEEE-skills-main/ieee_corpus/` using `pdfplumber` text extraction. Snippets preserve local line numbers from extracted text.

## A_Multidataset_Characterization_of_Window-Based_Hyperparameters_for_Deep_CNN-Driven_sEMG_Pattern_Recognition
- Extracted chars: 65525

### Opening / abstract evidence
- ===== PAGE 1 =====
- IEEE TRANSACTIONS ON HUMAN-MACHINE SYSTEMS, VOL. 54, NO. 1, FEBRUARY 2024 131
- A Multidataset Characterization of Window-Based
- Hyperparameters for Deep CNN-Driven
- sEMG Pattern Recognition
- Frank Kulwa , Student Member, IEEE, Haoshi Zhang , Oluwarotimi Williams Samuel , Senior Member, IEEE,
- Mojisola Grace Asogbon , Member, IEEE, Erik Scheme , Senior Member, IEEE,
- Rami Khushaba , Senior Member, IEEE, Alistair A. McEwan , and Guanglin Li , Senior Member, IEEE
- Abstract—The control performance of myoelectric prostheses (window length and overlap) employed for the construction of raw
- would not only depend on the feature extraction and classification two-dimensional (2-D) surface electromyogram (sEMG) signals on
- algorithms but also on interactions of dynamic window-based hy- the performance of CNNs when used for motion intent decoding.
- perparameters (WBHP) used to construct input signals. However, Moreover,weexaminedtherelationshipbetweenthewindowlength
- the relationship between these hyperparameters and how they of the 2-D sEMG and three commonly used CNN kernel sizes.
- influence the performance of the convolutional neural networks To ensure high confidence in the findings, we implemented three
- (CNNs) during motor intent decoding has not been studied. There- CNNs, which are variants of the existing models, and a newly
- fore, we investigated the impact of various combinations of WBHP proposed CNN model. Experimental analysis was conducted using
- threedistinctbenchmarkdatabases,twofromupperlimbamputees
- and one from able-bodied subjects. The results demonstrate that
- Manuscript received 3 August 2023; accepted 27 October 2023. Date of
- the performance of the CNNs improved as the overlap between
- publication 14 December 2023; date of current version 26 January 2024.
- This work was supported in part by the Key-Area Research and Development consecutively generated 2-D signals increased, with 75% over-
- Program of Guangdong Province under Grant 2020B0909020004, in part by lap yielding the optimal improvement by 12.62% accuracy and
- the National Natural Science Foundation of China under Grant #62150410439, 39.60% F1-score compared to no overlap. Moreover, the CNNs
- in part by Guangdong Basic and Applied Research Foundation under Grant performance was better for kernel size of seven than three and
- #2023A1515011478, in part by the Science and Technology Program of Guang- five across the databases. For the first time, we have established
- dong Province under Grant #2022A0505090007, in part by the Ministry of with multiple evidence that WBHP would substantially impact the
- Science and Technology, Shenzhen under Grant #QN2022032013L, and in
- decoding outcome and computational complexity of deep neural
- part by the ANSO Scholarship for Young Talented Students, “The Belt and
- networks, and we anticipate that this may spur positive advance-
- Road” Innovative Talent Exchange Program for Foreign Experts under Grant
- ment in myoelectric control and related fields.
- DL2022024002L and Jinan 5150 Program for Talents Introduction. This article
- was recommended by Associate Editor X. Hu. (Frank Kulwa and Haoshi
- Index Terms—Convolution neural network (CNN), prostheses,
- Zhang contributed equally to this work.) (Corresponding authors: Oluwarotimi
- surface electromyogram (sEMG) signal, upper limb, window
- Williams Samuel; Guanglin Li.)
- This work involved human subjects or animals in its research. Approval length, window overlap.
- of all ethical and experimental procedures and protocols was granted by the
- Institutional Review Board of Shenzhen Institutes of Advanced Technology,
- ChineseAcademyofSciencesunderApplicationNo.SIAT-IRB-221115-H0626.
- I. INTRODUCTION
- Frank Kulwa and Haoshi Zhang are with the CAS Key Laboratory of Human- T HE inability of amputees to carry out basic and complex

### Section, table, and figure headings detected
- L47: I. INTRODUCTION
- L125: A. Description of the EMG Databases Utilized
- L156: Fig. 2. Framework for the construction of 2-D signals. The relationship
- L158: Fig. 1. Electrode location and experiment setup on the amputee during sEMG exploited for constructing 2-D sEMG representation of size JxW is depicted in
- L161: TABLE I
- L198: C. Convolution Neural Networks
- L225: Fig. 3. Proposed multiscale convolution neural network (MS-CNN). D repre-
- L281: TABLE II TABLE III
- L310: A. Analyzing the Impact of Window Length and Overlap on
- L314: D. Experimental Setups
- L351: Fig. 5. Classification accuracy of Model1, Model2, Model3, and Model4, when they are applied to DB1. (a) Each subpart in the graphs contains results of all
- L355: TABLE IV
- L387: Fig. 6. Classification accuracy of Model1, Model2, Model3, and Model4, when they are applied to DB2. (a) Each subpart in the graphs contains results of all
- L392: Fig. 7. Classification (in accuracy) of Model1, Model2, Model3, and Model4, when they are applied to DB3. (a) Each subpart in the graphs contains results of
- L396: TABLE V
- L409: TABLE VI
- L411: Fig. 8. Classification performance of Model1, Model2, and Model3 while varying the network kernels (3, 5, and 7) at different 2-D signal lengths (W) of 25, 50,
- L445: C. Analysis of Individual Limb MI Across Window Overlaps
- L455: Fig. 9. Confusion matrices for Model1 on classification performance across
- L501: TABLE VII IV. DISCUSSION
- L516: TABLE VIII the generated 2-D signals on the performance of the CNNs. In
- L526: Fig. 9(b)(for DB2), and Fig. 9(c)(for DB3). The classification
- L530: TABLE IX
- L560: Table IX) are within the acceptable range. Therefore, when con- peak performance attained by kernel = 7. This implied that
- L614: Fig. 5(b)], in DB2 [see Fig. 6(b)] for all overlaps except overlap [2] S. Pancholi and A. M. Joshi, “Electromyography-based hand gesture

### Evidence snippets: math_formalization

```text
L88: However, such engineered features are computed based on sta- on the network’s performance as small size kernels are good
L89: tistical approaches that sometimes fail to capture relationships in mining fine features, which could be missed by large size
L90: across sEMG channels, leading to the loss of underlying motor kernels and vice versa. Therefore, it is important to look at their
L91: information [7]. To address this issue, deep learning methods influence in EMG decoding tasks.
L92: have been proposed for automatic feature learning and can be In an attempt to fill the abovementioned research gaps, this
```

```text
L95: [13]. tions of windowing parameters on the decoding performance
L96: The sEMG-based gesture classification task can be modeled of CNNs. Besides, the CNN models employed are simple and
L97: as a 2-D signal recognition problem using convolutional neural low memory enabling practical deployment in upper limb pros-
L98: networks (CNNs), where the input signal to the CNNs has a size theses. Also, we explored the effects of varying kernel sizes on
L99: of J × W (length x width). Many techniques have been used the classification performance of different CNN models. The ex-
```

```text
L118: coding, which may be necessary in developing time-efficient 4) We proposed a novel variant of CNN model characterized
L119: and intuitive deep learning driven prosthetic control schemes. by low computational complexity with simple yet robust,
L120: Recent research has confirmed that 2-D signals’ temporal and accurate decoding performance.
L121: and spatial information can be used by CNN to extract long
L122: and short-term patterns present in sEMG recordings [17], [19],
```

```text
L243: layer. Because the networks are trained from scratch, we have the concatenation layer without dimension reshaping while
L244: applied weights initialization in both Model2 and Model3 to al- max-pooling is applied to extract the most essential joint
L245: low quick convergence and optimization of the networks [37]. It features. The second multiscale block (Block 2) has a similar
L246: should be noted that the classification in both networks (Model2 operation to Block 1.
L247: and Model3) is performed using a Softmax layer. The subsequent Block 3 contains two point-wise 1 × 1 con-
```

```text
L264: are the multiscale block 1 and block 2 composed of dilated lated convolution filters are an easy approach to generating
L265: convolution layers at different scales (dilation rates) to enable an a CNN with large filters such as 5 × 5, 7 × 7. while keeping
L266: exponential increase of large receptive fields without loss of out- the parameters similar to 2 × 2 or 3 × 3 kernels. A dilated
L267: put resolution [40]. The input to the network is fed to block1 via convolution with an enlargement rate of d places d − 1 zeros
L268: two means including the upper and lower paths with each having in between successive filter values, which results in enlarging
```

```text
L288: in internal covariant shift within the network [43]. To resolve tistical significance of the proposed method, a nonparametric
L289: this issue, batch normalization layers were introduced after Friedman’s test was conducted followed by Dunn’s post hoc
L290: each convolution block, and the exponential linear unit (ELU) test. The definitions for the metrics are indicated in
L291: activation function was leveraged afterwards in requisite layers. TP + TN
L292: Thus, the ELU activation function is expressed mathematically, Accuracy = (2)
```

```text
L317: work performance (in our preliminary/pilot experiments of find- CNNs. For each experiment, the W was kept constant while
L318: ing the optimal hyperparameters for the models) compared to varying the V and vice versa. And the corresponding signals
L319: the stochastic gradient descent optimizer [46], all the described were used to train the built CNNs described in Section II-C. For
L320: models were trained using Adam Optimizer with a learning instance, 2-D signals obtained from W of 175 ms and an overlap
L321: rate of 0.0001. It should also be noted that at least one subject of “75% of W” were employed to train and test a CNN with
```

```text
L323: for the models during preliminary experiments. Besides, due of W and V across kernel sizes on the CNNs was examined.
L324: to its superior performance in multiclass tasks, the categorical Meanwhile, the experiments were carried out for each of the
L325: cross-entropy [47] was utilized as the loss function. The number databases described in Section II-A and the obtained results are
L326: of epochs for each model was set depending on the character- presented as follows. Table III summarizes the overall analyses
L327: istics of the dataset in each database, as indicated in Table II. per subject. Because the results for all three kernels (3, 5, and 7)
```

```text
L414: window lengths in DB3.
L415: every model is realized when the size of kernels increases from impact in the performance of CNNs especially in Model2 and
L416: 3, 5 to 7. The observation in this database shows that the use Model3 where the graphs show a positive gradient with the
L417: of large-size kernels improves the CNN’s performance signif- increase in window lengths for all window sizes (from 25 ms
L418: icantly (with p<0.05 in all models) regardless of the window to 200 ms) in Model2, and from 100 ms to 200 ms in Model2 at
```

```text
L699: pp. 1–5. activation by sparse regularization,” in Proc. Int. Joint Conf. Neural Netw.,
L700: [23] P. Gulati, Q. Hu, and S. F. Atashzar, “Toward deep generalization of 2017, pp. 2684–2691.
L701: peripheral EMG-Based Human-Robot interfacing: A hybrid explainable [45] D. P. Kingma and J. L. Ba, “Adam: A method for stochastic optimization,”
L702: solution for NeuroRobotic systems,” IEEE Robot. Automat. Lett., vol. 6, in Proc. Int. Conf. Learn. Representations, 2015, pp. 1–13.
L703: no. 2, pp. 2650–2657, Apr. 2021. [46] S. Ruder, “An overview of gradient descent optimization algorithms,”
```

```text
L703: no. 2, pp. 2650–2657, Apr. 2021. [46] S. Ruder, “An overview of gradient descent optimization algorithms,”
L704: [24] M. G. Asogbon et al., “Appropriate feature set and window parameters 2016, arXiv:1609.04747.
L705: selection for efficient motion intent characterization towards intelligently [47] Z. Zhang and M. Sabuncu, “Generalized cross entropy loss for training
L706: smart EMG-PR system,” Symmetry, vol. 12, no. 10, 2020, Art. no. 1710. deep neural networks with noisy labels,” in Proc. Adv. Neural Inf. Process.
L707: [25] T. Farrell and R. F. Weir, “Analysis window induced controller de- Syst., 2018, Art. no. 31.
```

### Evidence snippets: architecture

```text
L5: IEEE TRANSACTIONS ON HUMAN-MACHINE SYSTEMS, VOL. 54, NO. 1, FEBRUARY 2024 131
L6: A Multidataset Characterization of Window-Based
L7: Hyperparameters for Deep CNN-Driven
L8: sEMG Pattern Recognition
L9: Frank Kulwa , Student Member, IEEE, Haoshi Zhang , Oluwarotimi Williams Samuel , Senior Member, IEEE,
```

```text
L12: Abstract—The control performance of myoelectric prostheses (window length and overlap) employed for the construction of raw
L13: would not only depend on the feature extraction and classification two-dimensional (2-D) surface electromyogram (sEMG) signals on
L14: algorithms but also on interactions of dynamic window-based hy- the performance of CNNs when used for motion intent decoding.
L15: perparameters (WBHP) used to construct input signals. However, Moreover,weexaminedtherelationshipbetweenthewindowlength
L16: the relationship between these hyperparameters and how they of the 2-D sEMG and three commonly used CNN kernel sizes.
```

```text
L15: perparameters (WBHP) used to construct input signals. However, Moreover,weexaminedtherelationshipbetweenthewindowlength
L16: the relationship between these hyperparameters and how they of the 2-D sEMG and three commonly used CNN kernel sizes.
L17: influence the performance of the convolutional neural networks To ensure high confidence in the findings, we implemented three
L18: (CNNs) during motor intent decoding has not been studied. There- CNNs, which are variants of the existing models, and a newly
L19: fore, we investigated the impact of various combinations of WBHP proposed CNN model. Experimental analysis was conducted using
```

```text
L25: This work was supported in part by the Key-Area Research and Development consecutively generated 2-D signals increased, with 75% over-
L26: Program of Guangdong Province under Grant 2020B0909020004, in part by lap yielding the optimal improvement by 12.62% accuracy and
L27: the National Natural Science Foundation of China under Grant #62150410439, 39.60% F1-score compared to no overlap. Moreover, the CNNs
L28: in part by Guangdong Basic and Applied Research Foundation under Grant performance was better for kernel size of seven than three and
L29: #2023A1515011478, in part by the Science and Technology Program of Guang- five across the databases. For the first time, we have established
```

```text
L32: decoding outcome and computational complexity of deep neural
L33: part by the ANSO Scholarship for Young Talented Students, “The Belt and
L34: networks, and we anticipate that this may spur positive advance-
L35: Road” Innovative Talent Exchange Program for Foreign Experts under Grant
L36: ment in myoelectric control and related fields.
```

```text
L87: 132 IEEE TRANSACTIONS ON HUMAN-MACHINE SYSTEMS, VOL. 54, NO. 1, FEBRUARY 2024
L88: However, such engineered features are computed based on sta- on the network’s performance as small size kernels are good
L89: tistical approaches that sometimes fail to capture relationships in mining fine features, which could be missed by large size
L90: across sEMG channels, leading to the loss of underlying motor kernels and vice versa. Therefore, it is important to look at their
```

```text
L94: for adequate extraction of relevant features across channels [9], structed from raw sEMG recordings using varied combina-
L95: [13]. tions of windowing parameters on the decoding performance
L96: The sEMG-based gesture classification task can be modeled of CNNs. Besides, the CNN models employed are simple and
L97: as a 2-D signal recognition problem using convolutional neural low memory enabling practical deployment in upper limb pros-
L98: networks (CNNs), where the input signal to the CNNs has a size theses. Also, we explored the effects of varying kernel sizes on
```

```text
L95: [13]. tions of windowing parameters on the decoding performance
L96: The sEMG-based gesture classification task can be modeled of CNNs. Besides, the CNN models employed are simple and
L97: as a 2-D signal recognition problem using convolutional neural low memory enabling practical deployment in upper limb pros-
L98: networks (CNNs), where the input signal to the CNNs has a size theses. Also, we explored the effects of varying kernel sizes on
L99: of J × W (length x width). Many techniques have been used the classification performance of different CNN models. The ex-
```

```text
L109: the signal width is equal to the number of electrodes and the deep learning driven prostheses control scheme, this study
L110: length matches the segmentation window length). However, the explored the impact of the raw 2-D signals’ window length
L111: use of spectrogram, scalogram and 2-D from engineered features and overlap on the performance of CNNs.
L112: impose extra preprocessing time. While the raw EMG as input 2) We explore the effects of receptive window for different
L113: to CNNs represents a seamless and direct approach, several configurations of CNNs and how they influence the feature
```

```text
L111: use of spectrogram, scalogram and 2-D from engineered features and overlap on the performance of CNNs.
L112: impose extra preprocessing time. While the raw EMG as input 2) We explore the effects of receptive window for different
L113: to CNNs represents a seamless and direct approach, several configurations of CNNs and how they influence the feature
L114: studies have leveraged this option towards attaining fairly decent learning on the raw 2-D signal.
L115: classification performance [16], [18]. This partly motivated us to 3) To aid the optimal selection of window parameters, we
```

```text
L119: and intuitive deep learning driven prosthetic control schemes. by low computational complexity with simple yet robust,
L120: Recent research has confirmed that 2-D signals’ temporal and accurate decoding performance.
L121: and spatial information can be used by CNN to extract long
L122: and short-term patterns present in sEMG recordings [17], [19],
L123: [20]. With respect to sparse and high-density surface EMG II. MATERIAL AND METHODS
```

```text
L135: terms of window length and overlap would yield the requisite was placed on the extensor digitorum communis muscle at
L136: 2-D signals for optimal movement intent decoding (in terms the height of the radio-humeral joint and others were equally
L137: of accuracy and robustness) in CNNs-based pattern recognition spaced clockwise. Eight isotonic and isometric hand gestures
L138: schemes for multifunctional prostheses. Notably, previous stud- were involved, and were the subset of NinaPro database (DB3)
L139: ies have reiterated that variation in window-based hyperparame- [30]. There were 10 repetitions of each motion, each held for 3
```

### Evidence snippets: experiment_defense

```text
L5: IEEE TRANSACTIONS ON HUMAN-MACHINE SYSTEMS, VOL. 54, NO. 1, FEBRUARY 2024 131
L6: A Multidataset Characterization of Window-Based
L7: Hyperparameters for Deep CNN-Driven
L8: sEMG Pattern Recognition
```

```text
L18: (CNNs) during motor intent decoding has not been studied. There- CNNs, which are variants of the existing models, and a newly
L19: fore, we investigated the impact of various combinations of WBHP proposed CNN model. Experimental analysis was conducted using
L20: threedistinctbenchmarkdatabases,twofromupperlimbamputees
L21: and one from able-bodied subjects. The results demonstrate that
L22: Manuscript received 3 August 2023; accepted 27 October 2023. Date of
```

```text
L24: publication 14 December 2023; date of current version 26 January 2024.
L25: This work was supported in part by the Key-Area Research and Development consecutively generated 2-D signals increased, with 75% over-
L26: Program of Guangdong Province under Grant 2020B0909020004, in part by lap yielding the optimal improvement by 12.62% accuracy and
L27: the National Natural Science Foundation of China under Grant #62150410439, 39.60% F1-score compared to no overlap. Moreover, the CNNs
L28: in part by Guangdong Basic and Applied Research Foundation under Grant performance was better for kernel size of seven than three and
```

```text
L48: Frank Kulwa and Haoshi Zhang are with the CAS Key Laboratory of Human- T HE inability of amputees to carry out basic and complex
L49: Machine Intelligence-Synergy Systems, Shenzhen Institute of Artificial Intelli-
L50: arm related tasks reduces their quality of life, which may be
L51: gence and Robotics for Society, Shenzhen Institute of Advanced Technology,
L52: Chinese Academy of Sciences, Shenzhen 518055, China, and also with the psychologically distressing. To restore limb functionality in am-
```

```text
L89: tistical approaches that sometimes fail to capture relationships in mining fine features, which could be missed by large size
L90: across sEMG channels, leading to the loss of underlying motor kernels and vice versa. Therefore, it is important to look at their
L91: information [7]. To address this issue, deep learning methods influence in EMG decoding tasks.
L92: have been proposed for automatic feature learning and can be In an attempt to fill the abovementioned research gaps, this
L93: directly applied to raw two-dimensional (2-D) sEMG signals article thoroughly investigated the impact of 2-D signals con-
```

```text
L135: terms of window length and overlap would yield the requisite was placed on the extensor digitorum communis muscle at
L136: 2-D signals for optimal movement intent decoding (in terms the height of the radio-humeral joint and others were equally
L137: of accuracy and robustness) in CNNs-based pattern recognition spaced clockwise. Eight isotonic and isometric hand gestures
L138: schemes for multifunctional prostheses. Notably, previous stud- were involved, and were the subset of NinaPro database (DB3)
L139: ies have reiterated that variation in window-based hyperparame- [30]. There were 10 repetitions of each motion, each held for 3
```

```text
L146: remains an open research question to the best of the authors’ filter of 20–380 Hz.
L147: knowledge. Database 2 (DB2): This database was acquired in-house from
L148: Convolution kernels act as the feature extraction phase for the four transhumeral amputees. The dataset was collected using
L149: CNN in which the network automatically learn low- and high- the HD-sEMG system (Refa 128 model, TMS International,
L150: level features [28]. The size of the kernel has a great influence Netherlands) with 32 monopolar electrodes and an amplifier
```

```text
L153: ===== PAGE 3 =====
L155: KULWA et al.: MULTIDATASET CHARACTERIZATION OF WBHP FOR DEEP CNN-DRIVEN SEMG PATTERN RECOGNITION 133
L156: Fig. 2. Framework for the construction of 2-D signals. The relationship
L157: between window length (W) and overlap (V) of any successive data segment
```

```text
L183: supination, wrist pronation, no movement, hand close, and hand leakage (a key challenge in building machine learning models).
L184: open (HO). Meanwhile, each motion was held for about 5 s Before training, a Z-score normalization method was applied
L185: with a 5 s rest between two consecutive tasks. Each gesture to the training set to ease the CNN’s learning process [32]. For
L186: was repeated 5 times. The data was sampled at 1024 Hz while the testing set normalization, the mean value to subtract and
L187: 50 Hz notch filter and band pass filter with cut-off frequencies the standard deviation to divide as obtained from the training
```

```text
L259: possible. Moreover, inspired by the dilated convolution kernel 2-Dfilterstoextendthestandardconvolutionlayer. Fig.4depicts
L260: concept [39], we have utilized them as core layers to achieve the the conceptual representation of a typical dilation process in
L261: multiscale task. The architecture of the proposed network herein the context of the proposed MS-CNN. In order to optimize
L262: referred to as Model4 is presented in Fig. 3. the number of network parameters, traditional CNNs exploit
L263: The essential functional layers in the MS-CNN (see Fig. 3) convolution with small filters (2 × 2 or 3 × 3). However, di-
```

```text
L278: ===== PAGE 5 =====
L280: KULWA et al.: MULTIDATASET CHARACTERIZATION OF WBHP FOR DEEP CNN-DRIVEN SEMG PATTERN RECOGNITION 135
L281: TABLE II TABLE III
L282: NUMBER OF EPOCHS FOR EACH MODEL AND DATABASE EXPERIMENTAL ANALYSES PERFORMED FOR THE THREE PARAMETERS FOR
```

```text
L290: each convolution block, and the exponential linear unit (ELU) test. The definitions for the metrics are indicated in
L291: activation function was leveraged afterwards in requisite layers. TP + TN
L292: Thus, the ELU activation function is expressed mathematically, Accuracy = (2)
L293: TP + FP + TN + FN
L294: as shown in
```

### Evidence snippets: visualization

```text
L155: KULWA et al.: MULTIDATASET CHARACTERIZATION OF WBHP FOR DEEP CNN-DRIVEN SEMG PATTERN RECOGNITION 133
L156: Fig. 2. Framework for the construction of 2-D signals. The relationship
L157: between window length (W) and overlap (V) of any successive data segment
L158: Fig. 1. Electrode location and experiment setup on the amputee during sEMG exploited for constructing 2-D sEMG representation of size JxW is depicted in
```

```text
L174: gain of 26.55. The electrodes were positioned on biceps brachii recommendations [24]. It is worth noting that, in this article,
L175: and triceps brachii of the individuals’ residual limbs in a matrix we denote the overlap as V. For instance, the overlap of 25% of
L176: of 4 × 8, as indicated in Fig. 1. Prior to the data collection, W is denoted as 0.25V, 50% of W is 0.50 V. A description of the
L177: the subjects were given written informed consent and they constructed 2-D signals based on combinations of windowing
L178: providedpermissionforthepublicationoftheirdataforscientific parameters is indicated in Fig. 2.
```

```text
L176: of 4 × 8, as indicated in Fig. 1. Prior to the data collection, W is denoted as 0.25V, 50% of W is 0.50 V. A description of the
L177: the subjects were given written informed consent and they constructed 2-D signals based on combinations of windowing
L178: providedpermissionforthepublicationoftheirdataforscientific parameters is indicated in Fig. 2.
L179: and educational purposes. During data acquisition, a computer Subsequently, the 2-D signals were partitioned into training
L180: screen was placed in front of the participants and a picture of and test sets. Where a five-fold cross validation protocol was
```

```text
L223: not prone to overfitting [35]. Thus, the Model2 consists of three
L224: convolution blocks each having 80, 100, and 120 nodes with
L225: Fig. 3. Proposed multiscale convolution neural network (MS-CNN). D repre-
L226: similar values of kernel sizes, respectively. Succeeding each
L227: sents the dilation rate.
```

```text
L238: convolution layers with 2-D convolution layers and discarded
L239: the dropout layers after each convolution except after the fully
L240: connected layer. Each convolution is followed by a batch nor- Fig. 4. Conceptualization of dilation: The convolution kernel (L) = 3 × 3 and
L241: malization and max-pooling layer of 2 × 2. Similar to Model2, its dilated filters when dilation rate (D) = 1, 2, and 3.
L242: feature reduction is achieved by using the global max-pooling
```

```text
L257: performance by learning both fine and large-grained patterns 1) Dilated Convolution Layer for Multiscale and Memory
L258: from the signal while keeping the network parameters as low as Efficiency: Dilated convolution layer is a layer that uses larger
L259: possible. Moreover, inspired by the dilated convolution kernel 2-Dfilterstoextendthestandardconvolutionlayer. Fig.4depicts
L260: concept [39], we have utilized them as core layers to achieve the the conceptual representation of a typical dilation process in
L261: multiscale task. The architecture of the proposed network herein the context of the proposed MS-CNN. In order to optimize
```

```text
L330: the effects of the studied parameters (overlap, window length, combination of window parameters (W versus V) across kernel
L331: and kernel sizes) to be observed. sizes and subjects for the different CNNs for Database 1 (DB1)
L332: To analyze the impact of kernel size on the performance of are presented in Fig. 5 in accuracy and Table IV in F1-score.
L333: the CNNs per time, the same size of the kernel was applied to all Analyzing the results in [see Fig. 5(a)], it can be seen that
L334: convolution layers of the models. Hence, we utilized kernel sizes the accuracy in every CNN improves when the percentage of
```

```text
L349: 136 IEEE TRANSACTIONS ON HUMAN-MACHINE SYSTEMS, VOL. 54, NO. 1, FEBRUARY 2024
L350: (a) (b)
L351: Fig. 5. Classification accuracy of Model1, Model2, Model3, and Model4, when they are applied to DB1. (a) Each subpart in the graphs contains results of all
L352: models at the same window length and varied overlaps 0 V, 0.25 V, 0.50 V, and 0.75 V, which are equivalent to 75% of W, 50% of W, 25% of W, and 0% of W.
L353: Note: Window length (W) unit is in millisecond (ms). (b) Average classification results across window lengths. (a) The classification accuracy for every window
```

```text
L360: show that the model’s performance improved by increasing the The effect of each model’s kernel size on different 2-D
L361: percentage of overlap at constant window length. Similarly, the sEMG signals constructed using varied windowing parameters
L362: average results displayed in Fig. 5(b)(accuracy) and Table IV was investigated in this section. The experiments were carried
L363: (F1-score), show that the overlap of 75% (0.75 V) achieved out by varying kernel sizes (3, 5, and 7) while keeping each
L364: much better classification results for upper limb MI decoding window length constant and the networks were configured to
```

```text
L371: mance of all the networks increases with an increase in overlap Thus, the F1-score results for three models at different kernel
L372: at a fixed window size per time with statistical significance sizes when 2-D signals were generated from DB1, DB2, and
L373: of p = 4.0x10−6, 3.0x10−6, 3.0x10−6, 7.9x10−5 for model1, DB3 are presented in Fig. 8.
L374: model2, model3, and model4 in DB2, respectively. While Based on analysis of the results for DB1 presented in Fig. 8(a),
L375: p = 3.62x10−4, 2.4x10−5, 2.8 x10−5, 8.26x10−3 were observed in general, the kernel size of 7 yields better classification per-
```

```text
L385: KULWA et al.: MULTIDATASET CHARACTERIZATION OF WBHP FOR DEEP CNN-DRIVEN SEMG PATTERN RECOGNITION 137
L386: (a) (b)
L387: Fig. 6. Classification accuracy of Model1, Model2, Model3, and Model4, when they are applied to DB2. (a) Each subpart in the graphs contains results of all
L388: models at the same window length and varied overlaps 0 V, 0.25 V, 0.50 V, and 0.75 V, which are equivalent to 75% of W, 50% of W, 25% of W, and 0% of W. Note:
L389: Window length (W) unit is in millisecond (ms). (b) Average classification results across window lengths. (a) Classification accuracy of every window length at
```

```text
L401: the statistical analysis between kernel 3 and 7 show a significant Model1, and from 25 to 75 ms for Model2 and Model3.
L402: improvement of p = 0.9.92x10−4, 1.30x10−3, and 1.83x10−2. By closely analyzing the variation of kernel sizes and window
L403: Although the impact is realized when varying kernel sizes, there lengths for DB2 in Fig. 8(b), an increase in the performance of
L404: Authorized licensed use limited to: University of Science & Technology of China. Downloaded on July 05,2026 at 09:59:05 UTC from IEEE Xplore. Restrictions apply.
```

### Closing evidence
- intertemporal structure of the upper-limb sEMG: Comparisons between tions,” 2015, arXiv:1511.07122.
- an LSTM network and cross-sectional myoelectric pattern recognition [40] S. Bai, J. Z. Kolter, and V. Koltun, “An empirical evaluation of generic
- methods,” in Proc. IEEE 41st Annu. Int. Conf. Eng. Med. Biol. Soc., 2019, convolutional and recurrent networks for sequence modeling,” 2018,
- pp. 6611–6615. arXiv:1803.01271.
- [20] E. Rahimian, S. Zabihi, A. Asif, D. Farina, S. F. Atashzar, and [41] P. H. Chen and C. Y. Lee, “UAVNet: An efficient obstacel detection model
- A. Mohammadi, “FS-HGR: Few-shot learning for hand gesture recog- for UAV with autonomous flight,” in Proc. Int. Conf. Intell. Auton. Syst.,
- nition via electromyography,” IEEE Trans. Neural Syst. Rehabil. Eng., 2018, pp. 217–220.
- vol. 29, pp. 1004–1015, 2021. [42] X. Zhang, Y. Zou, and W. Shi, “Dilated convolution neural network with
- [21] M. Atzori, M. Cognolato, and H. Müller, “Deep learning with convolu- LeakyReLU for environmental sound classification,” in Proc. 22nd Int.
- tional neural networks applied to electromyography data: A resource for Conf. Digit. Signal Process., 2017, pp. 1–5.
- the classification of movements for prosthetic hands,” Front. Neurorobot., [43] M. J. Hasan, D. Shon, K. Im, H. K. Choi, D. S. Yoo, and J. M. Kim,
- vol. 10, 2016, Art. no. 9. “Sleep state classification using power spectral density and residual neural
- [22] E. Rahimian, S. Zabihi, S. F. Atashzar, A. Asif, and A. Mohammadi, network with multichannel EEG signals,” Appl. Sci., vol. 10, no. 21, 2020,
- “Semg-based hand gesture recognition via dilated convolutional neu- Art. no. 7639.
- ral networks,” in Proc. IEEE Glob. Conf. Signal Inf. Process., 2019, [44] H. Ide and T. Kurita, “Improvement of learning for CNN with ReLU
- pp. 1–5. activation by sparse regularization,” in Proc. Int. Joint Conf. Neural Netw.,
- [23] P. Gulati, Q. Hu, and S. F. Atashzar, “Toward deep generalization of 2017, pp. 2684–2691.
- peripheral EMG-Based Human-Robot interfacing: A hybrid explainable [45] D. P. Kingma and J. L. Ba, “Adam: A method for stochastic optimization,”
- solution for NeuroRobotic systems,” IEEE Robot. Automat. Lett., vol. 6, in Proc. Int. Conf. Learn. Representations, 2015, pp. 1–13.
- no. 2, pp. 2650–2657, Apr. 2021. [46] S. Ruder, “An overview of gradient descent optimization algorithms,”
- [24] M. G. Asogbon et al., “Appropriate feature set and window parameters 2016, arXiv:1609.04747.
- selection for efficient motion intent characterization towards intelligently [47] Z. Zhang and M. Sabuncu, “Generalized cross entropy loss for training
- smart EMG-PR system,” Symmetry, vol. 12, no. 10, 2020, Art. no. 1710. deep neural networks with noisy labels,” in Proc. Adv. Neural Inf. Process.
- [25] T. Farrell and R. F. Weir, “Analysis window induced controller de- Syst., 2018, Art. no. 31.
- lay for multifunctional prostheses,” in Proc. Myoelectric Symp., 2008, [48] U. Côté-Allard et al., “Deep learning for electromyographic hand gesture
- Art. no. 20125. signal classification using transfer learning,” IEEE Trans. Neural Syst.
- [26] L.H.Smith,L.J.Hargrove,B.A.Lock,andT.A.Kuiken,“Determiningthe Rehabil. Eng., vol. 27, no. 4, pp. 760–771, Apr. 2019.
- optimal window length for pattern recognition-based myoelectric control: [49] A. Stango, F. Negro, and D. Farina, “Spatial correlation of high-density
- Balancing the competing effects of classification error and controller EMG signals provides features robust to electrode number and shift in
- delay,”IEEETrans.NeuralSyst.Rehabil.Eng.,vol.19,no.2,pp. 186–192, pattern recognition for myocontrol,” IEEE Trans. Neural Syst. Rehabil.
- Apr. 2011. Eng., vol. 23, no. 2, pp. 189–198, Mar. 2015.
- [27] E. N. Kamavuako, E. J. Scheme, and K. B. Englehart, “Determination of [50] O. W. Samuel et al., “Intelligent EMG pattern recognition control method
- optimum threshold values for EMG time domain features; a multi-dataset for upper-limb multifunctional prostheses: Advances, current challenges,
- investigation,” J. Neural Eng., vol. 13, no. 4, 2016, Art. no. 0460. and future prospects,” IEEE Access, vol. 7, pp. 10150–10165, 2019.
- Authorized licensed use limited to: University of Science & Technology of China. Downloaded on July 05,2026 at 09:59:05 UTC from IEEE Xplore. Restrictions apply.

## A_Multimodal_Multilevel_Converged_Attention_Network_for_Hand_Gesture_Recognition_With_Hybrid_
- Extracted chars: 54829

### Opening / abstract evidence
- ===== PAGE 1 =====
- IEEE TRANSACTIONS ON CYBERNETICS, VOL. 53, NO. 12, DECEMBER 2023 7723
- A Multimodal Multilevel Converged Attention
- Network for Hand Gesture Recognition With
- Hybrid sEMG and A-Mode Ultrasound Sensing
- Sheng Wei , Yue Zhang, and Honghai Liu , Fellow, IEEE
- Abstract—Gesture recognition based on surface electromyogra- I. INTRODUCTION
- phy (sEMG) has been widely used in the field of human–machine THE HAND is the most flexible limb in the human body. It
- interaction (HMI). However, sEMG has limitations, such as low
- can assist humans in most life behaviors. Hand gestures,
- signal-to-noise ratio and insensitivity to fine finger movements,
- so we consider adding A-mode ultrasound (AUS) to enhance as an intuitive and convenient human expression, can express a
- the recognition impact. To explore the influence of multisource variety of meanings. With the development of human–machine
- sensing data on gesture recognition and better integrate the fea- interaction (HMI), HMI methods based on gesture recogni-
- tures of different modules. We proposed a multimodal multilevel
- tion have gained widespread attention. However, the result of
- converged attention network (MMCANet) model for multisource
- gesture recognition is strongly affected by the original sig-
- signals composed of sEMG and AUS. The proposed model
- extracts the hidden features of the AUS signal with a con- nal, so it is especially critical to choose a suitable signal.
- volutional neural network (CNN). Meanwhile, a CNN-LSTM The human body carries a large amount of information, and
- (long-short memory network) hybrid structure extracts some bio-signals are a great treasure for obtaining the state of the
- spatial-temporal features from the sEMG signal. Then, two
- human body. With the continuous development of the bio-
- types of CNN features from AUS and sEMG are spliced and
- signal decoding technology, researchers are extracting and
- transmitted to a transformer encoder to fuse the information
- and interact with sEMG features to produce hybrid features. analyzing human bio-signals to characterize them as con-
- Finally, the classification results are output employing fully con- trol signals to accomplish gesture interaction. The bio-electric
- nected layers. Attention mechanisms are used to adjust the signals have received a lot of attention include electromyog-
- weights of feature channels. We compared MMCANet’s feature
- raphy (EMG) [1], [2], [3], electroencephalography (EEG) [4],
- extraction and classification performance with that of manually
- electrooculography (EOG) [5], etc. In addition, near-infrared
- extracted sEMG-AUS features using four traditional machine-
- spectroscopy (NIRS) [6], force myography (FMG) [7], inertial
- learning (ML) algorithms. The recognition accuracy increased by
- at least 5.15%. In addition, we tried deep learning (DL) methods measurement unit (IMU) [8], and ultrasound (US) sensing [9],
- with CNN on single modals. The experimental results showed that etc. They have been used in wearable sensing solutions.
- the proposed model improved 14.31% and 3.80% over the CNN The surface EMG (sEMG) signal is the most accessible and
- method with single sEMG and AUS, respectively. Compared with
- simplest physiological signal, and it is the principal noninva-
- some state-of-the-art fusion techniques, our method also achieved
- sive method to determine the upper limb bio-electric signals.
- better results.

### Section, table, and figure headings detected
- L126: A. Networks
- L159: Fig. 1. Structure of transformer encoder.
- L160: Fig. 2. Twenty gestures in the dataset [15].
- L222: Fig. 5. Structure of AUS CNN network.
- L223: TABLE I
- L225: Fig. 3. Picture of the sEMG and AUS fusion device.
- L231: Fig. 4. Position of the probes. the normalization operation is employed.
- L232: D. Experiment Setup
- L268: C. Data Preprocessing
- L286: TABLE II
- L288: Fig. 6. Structure of sEMG CNN-LSTM network.
- L289: TABLE III
- L292: TABLE IV
- L294: Fig. 7. Time-frequency diagrams of two adjacent. (a) sEMG and (b) AUS
- L296: Fig. 8. Multimodal fusion structure of RDFKM.
- L316: Fig. 9. Structure of MMCANet. Every ConvBlocks’ configurations are in Table VI.
- L317: TABLE V TABLE VII
- L325: TABLE VI multilevel spatial-temporal fusion feature of sEMG and AUS
- L333: E. Details of Traditional Methods
- L348: III. RESULT AND DISCUSSION
- L359: TABLE VIII
- L408: Fig. 10. Average recognition rate of SVM classifier and DL methods for sEMG, AUS, and hybrid features.
- L464: Fig. 11. Results of 20 gestures average recognition accuracy for sEMG-CNN-LSTM, AUS-CNN, and sEMG-AUS-MMCANet.
- L466: Fig. 12. Projections of different features on 2-D space by tSNE. (a) sEMG.
- L468: Fig. 13. Two methods of four-fold cross-validation.
- L501: TABLE X
- L510: H. Future Work
- L538: IV. CONCLUSION

### Evidence snippets: math_formalization

```text
L134: chronously showed a significant improvement over a single extraction methods [14].
L135: modality. Zeng et al. [22] proposed a convolutional neu- 2) LSTM: LSTM is a variant of recurrent neural network
L136: ral network (CNN)-based sEMG and AUS feature fusion (RNN), mainly to figure out the gradient disappearance and
L137: architecture (EU-Net), which surpassed the method of the gradient explosion problems during the long sequences train-
L138: ML algorithm with the manual designed features. In [23], ing. It is a kind of neural network containing LSTM blocks,
```

```text
L135: modality. Zeng et al. [22] proposed a convolutional neu- 2) LSTM: LSTM is a variant of recurrent neural network
L136: ral network (CNN)-based sEMG and AUS feature fusion (RNN), mainly to figure out the gradient disappearance and
L137: architecture (EU-Net), which surpassed the method of the gradient explosion problems during the long sequences train-
L138: ML algorithm with the manual designed features. In [23], ing. It is a kind of neural network containing LSTM blocks,
L139: researchers proposed a regularized deep fusion of kernel and the LSTM block includes forget gate, input gate, and
```

```text
L159: Fig. 1. Structure of transformer encoder.
L160: Fig. 2. Twenty gestures in the dataset [15].
L161: HighwayNet. They introduced shortcuts to reduce gradient
L162: (mRMR) algorithm [38]. Intermediate fusion is converting
L163: disappearance and enhanced information fusion between
```

```text
L240: networks, the batch size was 50. The early stopping method
L241: skin with alcohol pads where the probes will place. Two of
L242: would stop training when the training loss no longer decreases.
L243: the probes were attached to the ulnar carpal flexor and ulnar
L244: The specific setup of the experiments will show in later sec-
```

```text
L350: A. Experiment 1: Different Fusion Methods
L351: module is embedded between CNN and LSTM.
L352: Further fusion operations were considered to avoid the loss Experimental results comparing different fusion methods
L353: of the sEMG signal’s spatial information. We first joined the showed that, for the multimodal fusion of AUS and sEMG,
L354: Authorized licensed use limited to: University of Science & Technology of China. Downloaded on July 05,2026 at 10:00:00 UTC from IEEE Xplore. Restrictions apply.
```

```text
L489: hensively illustrate the bio-electric signal state and muscle test set, dividing the first four trials into four folds, of which
L490: morphology in different dimensions. Therefore, the hybrid fea- three folds were used for training and others for validation.
L491: tures can obtain higher accuracy in gesture recognition. As The training would stop early according to the loss of valida-
L492: shown in Fig. 12, the sEMG, AUS, and hybrid characteristics tion set. The second method was to divide all eight trials into
L493: were projected to two dimensions for the visualization. The four folds, three folds for training and one fold for testing,
```

```text
L512: From the outcomes of method (a), we can see that the
L513: of relevant public datasets, this study uses our collection of
L514: accuracy trend of early stop using the validation set loss was
L515: sEMG-AUS datasets and therefore lacks comparisons with
L516: almost the same as that of early stop using the training set
```

```text
L554: From the experimental results, it can be seen from the com- the recognition accuracy of the MMCANet improved by at
L555: parison between Baseline and Method 1, that the improvement least 5.15% and 1.97%. The improvement in accuracy over
L556: of the number and type of features can improve the recogni- other strategies confirms the effectiveness of our method. As
L557: tion accuracy because more features and dimensions can better well as the advance, compared with sEMG and AUS alone,
L558: represent the contents and characteristics of the data. From the recognition rate improved by over 3.80%, demonstrating
```

### Evidence snippets: architecture

```text
L5: IEEE TRANSACTIONS ON CYBERNETICS, VOL. 53, NO. 12, DECEMBER 2023 7723
L6: A Multimodal Multilevel Converged Attention
L7: Network for Hand Gesture Recognition With
L8: Hybrid sEMG and A-Mode Ultrasound Sensing
```

```text
L17: sensing data on gesture recognition and better integrate the fea- interaction (HMI), HMI methods based on gesture recogni-
L18: tures of different modules. We proposed a multimodal multilevel
L19: tion have gained widespread attention. However, the result of
L20: converged attention network (MMCANet) model for multisource
L21: gesture recognition is strongly affected by the original sig-
```

```text
L23: extracts the hidden features of the AUS signal with a con- nal, so it is especially critical to choose a suitable signal.
L24: volutional neural network (CNN). Meanwhile, a CNN-LSTM The human body carries a large amount of information, and
L25: (long-short memory network) hybrid structure extracts some bio-signals are a great treasure for obtaining the state of the
L26: spatial-temporal features from the sEMG signal. Then, two
L27: human body. With the continuous development of the bio-
```

```text
L31: and interact with sEMG features to produce hybrid features. analyzing human bio-signals to characterize them as con-
L32: Finally, the classification results are output employing fully con- trol signals to accomplish gesture interaction. The bio-electric
L33: nected layers. Attention mechanisms are used to adjust the signals have received a lot of attention include electromyog-
L34: weights of feature channels. We compared MMCANet’s feature
L35: raphy (EMG) [1], [2], [3], electroencephalography (EEG) [4],
```

```text
L40: learning (ML) algorithms. The recognition accuracy increased by
L41: at least 5.15%. In addition, we tried deep learning (DL) methods measurement unit (IMU) [8], and ultrasound (US) sensing [9],
L42: with CNN on single modals. The experimental results showed that etc. They have been used in wearable sensing solutions.
L43: the proposed model improved 14.31% and 3.80% over the CNN The surface EMG (sEMG) signal is the most accessible and
L44: method with single sEMG and AUS, respectively. Compared with
```

```text
L48: better results.
L49: When transmitting the nerve excitation impulse to the mus-
L50: Index Terms—A-mode ultrasound (AUS), attention mecha-
L51: cle, we can obtain the sEMG signals through the surface
L52: nism, gesture recognition, hybrid features, multimodal, surface
```

```text
L71: counterpart techniques. In [14], researchers used a convolu-
L72: Sheng Wei and Yue Zhang are with the Department of Computer
L73: Science, Zhejiang University of Technology, Hangzhou 310013, China tion neural network to extract sEMG features, called CNNFeat,
L74: (e-mail: 2112012098@zjut.edu.cn; 1111712013@zjut.edu.cn). and the results showed that the combination of CNNFeats and
L75: Honghai Liu is with the State Key Laboratory of Robotics and Systems,
```

```text
L90: 7724 IEEE TRANSACTIONS ON CYBERNETICS, VOL. 53, NO. 12, DECEMBER 2023
L91: and susceptible to interference from noise. To overcome this CNN can extract the characteristics of hierarchy and space
L92: shortcoming, A-mode US (AUS) is introduced as the pio- well [25]. LSTM can make good use of the temporal features
L93: neering study to resolve the decoding effect in [15]. AUS of sequences [26].
```

```text
L96: time and amplitude of sound waves to detect the echo of extraction and fusion using a deep-learning-based approach to
L97: sound waves, with high axial resolution and positioning accu- enhance feature extraction and exploit the relationship between
L98: racy [16]. AUS can obtain the subtle changes of deep muscles features. In this article, we adopted CNN with LSTM networks
L99: and has enormous advantages over sEMG in recognizing sub- to extract deeper traits and intrinsic connections to multimodal
L100: tle gestures. It is also less likely to be affected by muscle data and find effective ways of multimodal feature fusion.
```

```text
L104: obtain forearm muscle information by multiple single-element nels. At the same time, to better integrate the information
L105: AUS sensors, and average recognition accuracy can achieve of different modalities, we chose the more advanced trans-
L106: 96% for six movements, including five finger flexion motions former encoder module to extract the fusion traits. We also
L107: and a resting state. Yang et al. [18] implemented the decoding compared our method with concatenating features and two
L108: of synchronized and proportional wrist/hand kinematics using state-of-the-art fusion methods and obtained a higher decoding
```

```text
L124: of AUS in gesture recognition and discrete force estima-
L125: tions and then combined them with the strength of sEMG
L126: A. Networks
L127: in continuous force estimation to achieve multilevel scaled
L128: gesture control. Boyd and Liu [21] used AUS signals as a 1) CNN: CNN is a feed-forward neural network, usually
```

```text
L127: in continuous force estimation to achieve multilevel scaled
L128: gesture control. Boyd and Liu [21] used AUS signals as a 1) CNN: CNN is a feed-forward neural network, usually
L129: complement to sEMG signals, and it could provide power- consisting of one or more convolution and fully connected
L130: ful improvements in the decoding of fine finger movements layers. The receptive field was introduced into CNN to mimic
L131: and large arm movements. Xia et al. [15] used feature extrac- the pattern the human brain processes information [27]. So,
```

### Evidence snippets: experiment_defense

```text
L38: extracted sEMG-AUS features using four traditional machine-
L39: spectroscopy (NIRS) [6], force myography (FMG) [7], inertial
L40: learning (ML) algorithms. The recognition accuracy increased by
L41: at least 5.15%. In addition, we tried deep learning (DL) methods measurement unit (IMU) [8], and ultrasound (US) sensing [9],
L42: with CNN on single modals. The experimental results showed that etc. They have been used in wearable sensing solutions.
```

```text
L74: (e-mail: 2112012098@zjut.edu.cn; 1111712013@zjut.edu.cn). and the results showed that the combination of CNNFeats and
L75: Honghai Liu is with the State Key Laboratory of Robotics and Systems,
L76: manual features can further improve the accuracy of traditional
L77: Harbin Institute of Technology Shenzhen, Shenzhen 518055, China, and
L78: also with the School of Computing, University of Portsmouth, PO1 3HE classifiers.
```

```text
L103: ies on gesture recognition. In [17], a method was proposed to weights. It can better explore the relationship between chan-
L104: obtain forearm muscle information by multiple single-element nels. At the same time, to better integrate the information
L105: AUS sensors, and average recognition accuracy can achieve of different modalities, we chose the more advanced trans-
L106: 96% for six movements, including five finger flexion motions former encoder module to extract the fusion traits. We also
L107: and a resting state. Yang et al. [18] implemented the decoding compared our method with concatenating features and two
```

```text
L139: researchers proposed a regularized deep fusion of kernel and the LSTM block includes forget gate, input gate, and
L140: machine (RDFKM) approach to merge multimodal physiolog- output gate. The forget gate, which is the key to achieving
L141: ical signals. The above study shows that multimodal gesture the long-term memory task, is the most critical part of each
L142: recognition can complement the strength of different modali- LSTM block [28]. The LSTM network can capture the tem-
L143: ties to improve performance [24], and indicates the possibility poral dependence of time series and has achieved a series of
```

```text
L158: WEI et al.: MMCANet FOR HAND GESTURE RECOGNITION 7725
L159: Fig. 1. Structure of transformer encoder.
L160: Fig. 2. Twenty gestures in the dataset [15].
L161: HighwayNet. They introduced shortcuts to reduce gradient
L162: (mRMR) algorithm [38]. Intermediate fusion is converting
```

```text
L185: gate mechanism in RNNs, generating corresponding weights
L186: for each feature channel, and representing the correlation
L187: between channels. Finally, the significance of each channel B. Dataset
L188: is adjusted by multiplication operation, and the channel focus In this article, the dataset for the experiment contains a syn-
L189: module is implemented to improve the focus on critical fea- chronized sEMG signal and AUS signal, where the sEMG and
```

```text
L192: 6) Transformer Encoder: The transformer structure is com- are from the multimodal signal. The selection of motions in
L193: posed of encoders and decoders. The encoder is divided into this experiment is based on the NinaPro database [39]. The
L194: two modules, the multihead attention layer and the feed- 20 gestures in this dataset were shown in Fig. 2. It includes
L195: forward neural-network layer, as shown in Fig. 1. Further split, six wrist movements: 1) wrist flexion (WF); 2) wrist exten-
L196: the multihead attention layer can be divided into the atten- sion (WE); 3) wrist radial deviation (WRD); 4) wrist ulnar
```

```text
L204: attention mechanism and powerful coding ability, it can fuse 12) ring and little finger flexion (RLF); and 13) pinch (PH)
L205: information from different modules [36]. and a rest state (RS).
L206: 7) Multimodal Fusion: In multimodal tasks, how effi- The experimental data are acquired by a four-channel sEMG
L207: ciently fusing multiple features from various modalities is the and AUS fusion device (Elonxi Ltd, www.elonxi.cn), as shown
L208: key to improving model performance. Generally, the fusion in Fig. 3. The device consists of four-unit modules with one
```

```text
L236: sEMG, AUS, and fusion signals. We designed different
L237: AUS probe in advance). We placed the armband on the fore-
L238: network models for the three datasets in this article. For all the
L239: arm of the subject. Before that, we should clean the subjects’
L240: networks, the batch size was 50. The early stopping method
```

```text
L244: The specific setup of the experiments will show in later sec-
L245: carpal extensor muscles. While the other two were attached
L246: tions. For the datasets, the first four out of eight trials for
L247: to the radial carpal flexor and radial carpal flexor muscles, as
L248: each subject were the training set, and the data from the last
```

```text
L257: 20 types of actions. The above process was completed once
L258: In all figures of the network structure, the first number
L259: and called one action group. The experiment was repeated
L260: before @ means the channel number of this layer, and a × b
L261: for eight groups. For each gesture action, the middle 3 s of
```

```text
L302: optimizer was Adam, and the initial learning rate was 0.01. 4) Some State-of-the-Art Fusion Methods: To prove the
L303: 3) Other Famous Backbones (AlexNet and DenseNet): We superiority and effectiveness of our method, we compared it
L304: chose the well-known AlexNet and DenseNet as a comparison. with the state-of-the-art method EU-Net based on sEMG and
L305: Since these two networks were for image classification and AUS fusion [22], whose network parameters were shown in
L306: sEMG and AUS data are multichannel signal data. We tried Table V. Also, we compared it with an advanced multimodal
```

### Evidence snippets: visualization

```text
L158: WEI et al.: MMCANet FOR HAND GESTURE RECOGNITION 7725
L159: Fig. 1. Structure of transformer encoder.
L160: Fig. 2. Twenty gestures in the dataset [15].
L161: HighwayNet. They introduced shortcuts to reduce gradient
```

```text
L192: 6) Transformer Encoder: The transformer structure is com- are from the multimodal signal. The selection of motions in
L193: posed of encoders and decoders. The encoder is divided into this experiment is based on the NinaPro database [39]. The
L194: two modules, the multihead attention layer and the feed- 20 gestures in this dataset were shown in Fig. 2. It includes
L195: forward neural-network layer, as shown in Fig. 1. Further split, six wrist movements: 1) wrist flexion (WF); 2) wrist exten-
L196: the multihead attention layer can be divided into the atten- sion (WE); 3) wrist radial deviation (WRD); 4) wrist ulnar
```

```text
L206: 7) Multimodal Fusion: In multimodal tasks, how effi- The experimental data are acquired by a four-channel sEMG
L207: ciently fusing multiple features from various modalities is the and AUS fusion device (Elonxi Ltd, www.elonxi.cn), as shown
L208: key to improving model performance. Generally, the fusion in Fig. 3. The device consists of four-unit modules with one
L209: methods of multimodal features are categorized into three AUS probe and two sEMG electrodes fixed on each module,
L210: types: 1) front-end fusion; 2) intermediate fusion; and 3) back- and it can obtain both sEMG and AUS signals from the same
```

```text
L221: 7726 IEEE TRANSACTIONS ON CYBERNETICS, VOL. 53, NO. 12, DECEMBER 2023
L222: Fig. 5. Structure of AUS CNN network.
L223: TABLE I
L224: AUS-CNN ARCHITECTURES
```

```text
L223: TABLE I
L224: AUS-CNN ARCHITECTURES
L225: Fig. 3. Picture of the sEMG and AUS fusion device.
L226: a band-pass filter for noise reduction for the sEMG signal. To
L227: ensure the synchronization with the AUS signal, the window
```

```text
L247: to the radial carpal flexor and radial carpal flexor muscles, as
L248: each subject were the training set, and the data from the last
L249: shown in Fig. 4. The experiment was carried out following
L250: four trials were the test set. The network weight initialization
L251: the Declaration of Helsinki. In the experiment, the duration
```

```text
L264: figure stands for the ConvBlock, the structure of a ConvBlock
L265: number of 20 types of gestures in the database was balanced.
L266: was shown in Fig. 5. In this table, in and out are in_channel
L267: and out_channel, k, s, and p means kernel_size, padding, and
L268: C. Data Preprocessing
```

```text
L274: and damping during the propagation of AUS. In band-pass data size of 4 × 100 × 10 for each sample to feed into the
L275: filtering, we used a Gaussian filter with the center frequency network for training. The network structure consists of five
L276: positioned at the center of the passband, and it can filter out the layers, as shown in Fig. 5. The AUS-CNN architectures are in
L277: nonlinear propagation and the noise in the circuit. The Hilbert Table I. Adam was the optimizer, and the initial learning rate
L278: transform was used to perform envelope extraction. The log was 0.001.
```

```text
L286: TABLE II
L287: SEMG-CNN-LSTM ARCHITECTURES
L288: Fig. 6. Structure of sEMG CNN-LSTM network.
L289: TABLE III
L290: ALEXNET ARCHITECTURES
```

```text
L292: TABLE IV
L293: DENSENET ARCHITECTURES
L294: Fig. 7. Time-frequency diagrams of two adjacent. (a) sEMG and (b) AUS
L295: signal samples.
L296: Fig. 8. Multimodal fusion structure of RDFKM.
```

```text
L298: and converted it into a shape of 300 × 4. Then the data was
L299: sent to the network for training. The entire network consisted
L300: of seven layers, as shown in Fig. 6, and the parameters of signal samples are shown in Fig. 7. The network structure
L301: the sEMG CNN-LSTM Network are shown in Table II. The parameters are shown in Tables III and IV.
L302: optimizer was Adam, and the initial learning rate was 0.01. 4) Some State-of-the-Art Fusion Methods: To prove the
```

```text
L307: two input methods: one is to use the signal data as input and fusion method RDFKM [23]. Since the input signals are dif-
L308: the other is to transform the signal data into a time-frequency ferent, the structure of the multimodal fusion in RDFKM
L309: map of size 227 × 227 by continue wavelet transform (CWT). was reconstructed for comparison, as illustrated in Fig. 8. The
L310: The time-frequency diagrams of two adjacent sEMG and AUS feature dimension was 64, the same as the original paper.
L311: Authorized licensed use limited to: University of Science & Technology of China. Downloaded on July 05,2026 at 10:00:00 UTC from IEEE Xplore. Restrictions apply.
```

### Closing evidence
- no. 6, pp. 1199–1208, Jun. 2018.
- (Healthcom), 2016, pp. 360–365.
- [18] X. Yang, Y. Zhou, and H. Liu, “Wearable ultrasound-based decoding
- of simultaneous wrist/hand kinematics,” IEEE Trans. Ind. Electron.,
- vol. 68, no. 9, pp. 8667–8675, Sep. 2021.
- [19] J. He, H. Luo, J. Jia, J. T. W. Yeow, and N. Jiang, “Wrist and finger Sheng Wei received the B.S. degree in software
- gesture recognition with single-element ultrasound signals: A compari- engineering from the University of South China,
- son with single-channel surface electromyogram,” IEEE Trans. Biomed. Hengyang, China, in 2019. He is currently pursu-
- Eng., vol. 66, no. 5, pp. 1277–1284, May 2019. ing the M.S. degree with the Zhejiang University of
- [20] X. C. Yang, J. P. Yan, and H. H. Liu, “Comparative analysis of wear- Technology, Hangzhou, China.
- able a-mode ultrasound and sEMG for muscle-computer interface,” IEEE His research interests include biological signal
- Trans. Biomed. Eng., vol. 67, no. 9, pp. 2434–2442, Sep. 2020. processing, human–computer interaction, and deep
- learning.
- [21] P. Boyd and H. H. Liu, “A-mode ultrasound driven sensor fusion for hand
- gesture recognition,” in Proc. Int. Joint Conf. Neural Netw. (IJCNN),
- 2020, pp. 1–6.
- Authorized licensed use limited to: University of Science & Technology of China. Downloaded on July 05,2026 at 10:00:00 UTC from IEEE Xplore. Restrictions apply.
- ===== PAGE 12 =====
- 7734 IEEE TRANSACTIONS ON CYBERNETICS, VOL. 53, NO. 12, DECEMBER 2023
- Yue Zhang received the M.S. degree in com- Honghai Liu (Fellow, IEEE) received the Ph.D.
- puter science and technology from the Zhejiang degree from King’s College, University London,
- University of Technology, Hengyang, China, in London, U.K., in 2003.
- 2017, where he is currently pursuing the Ph.D. He is a Chair Professor with the State Key
- degree with the Department of Computer science. Laboratory of Robotics and Systems, Harbin
- His research interests include intelligent system, Institute of Technology, Shenzhen, China, and
- biological signal processing, human–computer also with the School of Computing, University of
- interaction, and adaptive learning methods. Portsmouth, Portsmouth, U.K. He is interested in
- intelligent sensing, biomechatronics, pattern recog-
- nition, intelligent video analytics, intelligent robotics
- and their practical applications with an emphasis on
- approaches that could make contribution to the intelligent connection of per-
- ception to action using contextual information.
- Prof. Liu is an Associate Editor for IEEE TRANSACTIONS ON INDUSTRIAL
- ELECTRONICS and IEEE TRANSACTIONS ON INDUSTRIAL INFORMATICS.
- Authorized licensed use limited to: University of Science & Technology of China. Downloaded on July 05,2026 at 10:00:00 UTC from IEEE Xplore. Restrictions apply.

## Contrast-Assisted_Domain-Specificity-Removal_Network_for_Semi-Supervised_Generalization_Fault
- Extracted chars: 62211

### Opening / abstract evidence
- ===== PAGE 1 =====
- IEEE TRANSACTIONS ON NEURAL NETWORKS AND LEARNING SYSTEMS, VOL. 36, NO. 3, MARCH 2025 5403
- Contrast-Assisted Domain-Specificity-Removal
- Network for Semi-Supervised Generalization
- Fault Diagnosis
- Qiuyu Song , Xingxing Jiang , Jie Liu , Member, IEEE, Juanjuan Shi , and Zhongkui Zhu
- Abstract—Unknown domain shift caused by the unavail- past few years [1], [2], [3], [4]. For example, Yang et al. [5]
- ability of target domain during training phase degrades the recently proposed a digital twin-driven fault diagnosis method,
- performance of intelligent fault diagnosis models in practical
- which can better evaluate the reliability of industrial systems
- applications. Domain generalization (DG)-based methods have
- and is extremely effective for composite faults. Furthermore,
- recently emerged to alleviate the influence of domain shift and
- improve the generalization ability of models toward invisible due to the widespread application of rotating machinery in
- working conditions. However, most existing studies are con- industrial systems, implementing reliable condition monitor-
- ducted on multiple fully labeled source domains. Meanwhile, ing and fault diagnosis of rotating machinery, especially
- domain-specific information related to the variations of working
- safety-critical assets such as bearings and gears, is essen-
- conditions is often neglected during model training. Therefore,
- tial [6], [7], [8]. With appealing capabilities of mining implicit
- in order to realize reliable generalization fault diagnosis based on
- partially labeled source domains, this article proposes a contrast- fault-related features automatically and characterizing internal
- assisted domain-specificity-removal network (CDSRN) to extract information in industrial big data through layer-by-layer learn-
- transferable features from domain-specificity-removal perspec- ing, intelligent fault diagnosis methods based on deep learning
- tive. Concretely, a domain-specific feature removal branch is
- (DL) have made significant progress and shown promising
- designed to disentangle domain-invariant features and domain-
- application prospects [9], [10].
- specific features, thus excavating generalized information only in
- domain-invariance dimension. Simultaneously, proxy-contrastive Nevertheless, the diagnostic performance of traditional
- representation enhancement module is embedded to facilitate DL-based methods usually severely degrades under different
- the fault class-discriminative and domain-discriminative feature operating conditions. The basic premise of most DL-based
- learning, thereby assisting the model in further improvement
- fault diagnosis methods is that the training and testing data are
- of generalization capability. Experimental studies confirm the
- collected under the same working conditions, thus following
- effectiveness and competitiveness of the proposed CDSRN in
- semi-supervised generalization fault diagnosis. the same data distribution. However, this basic premise is
- difficult to hold in many real engineering scenarios [11].
- Index Terms—Adversarial training, contrastive learning, intel-
- To overcome this issue, domain adaption (DA) is developed
- ligent fault diagnosis, rotating machinery, semi-supervised
- domain generalization (DG), unseen target domain. based on the idea of transfer learning to realize reliable fault
- diagnosis under varying working conditions [12]. DA aims
- I. INTRODUCTION to transfer diagnosis knowledge from the training data, i.e.,

### Section, table, and figure headings detected
- L108: A. Supervised DG-Based Fault Diagnosis
- L130: 1) A domain-specific feature removal branch is established aged along with adversarial learning between the feature
- L138: 2) A proxy-contrastive representation enhancement module intelligent fault diagnosis under unseen working conditions via
- L193: A. Motivation of CDSRN Idea for Diagnosis
- L200: A. Problem Definition for Semi-Supervised DG-Based Fault Furthermore, confronted with unavailable target domains in
- L203: Fig. 1 illustrates the problem definition for semi-supervised
- L238: B. Domain-Specific Information in Machinery Fault
- L249: Fig. 1. Illustration of semi-supervised DG-based fault diagnosis.
- L267: Fig. 2. Diagram of domain-specific information and domain-invariant
- L273: D. The basic optimization objective for the fault classifier C
- L449: B. Method Overview and Network Architecture
- L459: Fig. 3. Schematic of the motivation of CDSRN.
- L636: Fig. 4. Overview of the proposed CDSRN.
- L771: TABLE I Algorithm 1 CDSRN
- L818: Table I lists the details of the proposed architecture. θq ←θq−1−µ λ D + GS,adv + cos +λ dpcl
- L841: C. Network Training and Objective Optimization PI Pf
- L865: TABLE II
- L867: Fig. 5. Test rigs in (a) SU and (b) PU.
- L868: A. Datasets Description
- L876: TABLE III
- L912: Table II. Each fault class contains 100 samples with a length
- L921: B. Experimental Settings
- L943: C. Results and Analysis of Comparative Experiments
- L949: Fig. 6. Confusion matrices in task T2 by (a) M1, (b) M2, (c) M3, (d) M4,
- L956: 2) In the experiment of SU Wheel Set bearing dataset, there
- L965: Fig. 7. Confusion matrices in task Q4 by (a) M1, (b) M2, (c) M3, (d) M4,
- L987: Fig. 7, almost all methods can accurately diagnose the health semi-supervised DG-based fault diagnosis.
- L998: TABLE IV
- L1000: TABLE V
- L1002: TABLE VI
- L1004: Fig. 9 shows the feature clustering results in task T2 by proposed CDSRN can learn more domain-invariant features on
- L1021: Fig. 10(c) is unsatisfactory. Instead, as shown in Fig. 10(f), the
- L1028: Fig. 10. Feature visualization in task Q4 by (a) M1, (b) M2, (c) M3, (d) M4,
- L1029: Fig. 9. Feature visualization in task T2 by (a) M1, (b) M2, (c) M3, (d) M4,
- L1039: D. Ablation Study
- L1040: Fig. 11. Critical difference diagrams of post hoc Friedman test based on
- L1060: E. Discussion
- L1070: TABLE VII
- L1072: Fig. 13. Diagnosis performance of different learning rates for CDSRN.
- L1073: Fig. 14. PAD of (a) source domains and (b) source domains and target
- L1079: Fig. 12. Sensitivity analysis of the coefficient λ1 and λ2 in (a) task T2 and
- L1091: Fig. 13 illustrates the diagnosis performance with different below the diagonal, indicating that the proposed CDSRN

### Evidence snippets: math_formalization

```text
L28: tive. Concretely, a domain-specific feature removal branch is
L29: (DL) have made significant progress and shown promising
L30: designed to disentangle domain-invariant features and domain-
L31: application prospects [9], [10].
L32: specific features, thus excavating generalized information only in
```

```text
L36: learning, thereby assisting the model in further improvement
L37: fault diagnosis methods is that the training and testing data are
L38: of generalization capability. Experimental studies confirm the
L39: collected under the same working conditions, thus following
L40: effectiveness and competitiveness of the proposed CDSRN in
```

```text
L78: seek to achieve the final goal of learning common knowl-
L79: jie_liu@hust.edu.cn).
L80: Digital Object Identifier 10.1109/TNNLS.2024.3383467 edge among source domains by distilling the domain-invariant
L81: 2162-237X © 2024 IEEE. Personal use is permitted, but republication/redistribution requires IEEE permission.
L82: See https://www.ieee.org/publications/rights/index.html for more information.
```

```text
L98: principle of working condition-dominant information and Section II. Section III introduces the preliminary knowledge.
L99: fault-dominant information, which are, respectively, termed A detailed illustration of the proposed CDSRN is presented
L100: domain-specific information and domain-invariant informa- in Section IV. In Section V, experimental studies, including
L101: tion in our work. Wang et al. [19] designed multiple result analyses and discussions based on two bearing datasets,
L102: domain-specific auxiliary classifiers to learn domain-specific are carried out to validate the performance of the proposed
```

```text
L116: CDSRN utilizes partially labeled source domains for model sis, and finally gain the representation of the general diagnosis
L117: training. Based on the preliminary framework of domain structure through Karcher Mean. Yang et al. [16] introduced
L118: adversarial neural network (DANN) [21], a domain-specific the center loss to the traditional convolutional neural network
L119: feature removal branch is exquisitely affiliated to provide (CNN) to improve the generalization ability of network on
L120: clear guidance for the network to learn domain-invariant unseen operating conditions. Meta-learning and domain mixup
```

```text
L130: 1) A domain-specific feature removal branch is established aged along with adversarial learning between the feature
L131: to give the network explicit guidance to exploit transfer- extractor and the domain classifier. Li et al. [24] proposed
L132: able domain-invariant features. Specifically, an auxiliary an adversarial domain-augmented generalization method with
L133: network branch is designed to extract domain-specific domain augmentation via convex combination of data and
L134: features excluding fault-category information by adver- feature-label pairs. Li et al. [25] proposed a DG method for
```

```text
L140: tation learning. On the one hand, fault-class-proxy- and strategy of sample adaptive screening and weighting.
L141: contrastive learning enhances the discriminability of Nevertheless, most of the existing supervised DG-based fault
L142: domain-invariant features by promoting intraclass aggre- diagnosis methods are based on the assumption that the col-
L143: gation and interclass separation. On the other hand, lected data contain sufficient label information. However, due
L144: domain-proxy-contrastive learning enhances the domain- to the expensive cost of acquiring label information, unlabeled
```

```text
L152: B. Semi-Supervised DG-Based Fault Diagnosis follows [17]:
L153: To the best of our knowledge, unsupervised learning cur-
L154: rently cannot deal with the problem of DG-based fault
L155: x(t) = δ(t) ∗ fδ (t) + d(t) ∗ f
L156: d
```

```text
L167: handle unlabeled data. Therefore, to make full utilize of large the transmission path effects of δ(t), d(t), and n(t), respec-
L168: amount of unlabeled data in DG, semi-supervised learning is a tively. It can be observed from (1) that the first term is the
L169: promising tool for fault diagnosis. It can utilize a small portion target fault-dominant information (domain-invariant informa-
L170: of labeled data and a large amount of unlabeled data for model tion) δ(t) coupled by working condition-dominant information
L171: training and achieve good performance with limited labels. (domain-specific information). The second and third terms
```

```text
L178: where f is a nonparametric function and x and x mean
L179: consisting of entropy-based sample purification strategy and x f d
L180: the domain-invariant information and domain-specific infor-
L181: low-rank decomposition method to realize DG-based fault
L182: mation, respectively. Hence, given that the final goal of
```

```text
L190: based on class boundary feature detection. Ren et al. [29]
L191: proposed a semi-supervised DG model for intelligent fault IV. PROPOSED METHOD
L192: diagnosis, termed domain-invariant feature fusion networks
L193: A. Motivation of CDSRN Idea for Diagnosis
L194: (DIFFN). However, these two methods ignore consideration
```

```text
L198: it is promising to develop semi-supervised intelligent fault
L199: III. PRELIMINARY diagnosis methods to address the limitedly labeled samples.
L200: A. Problem Definition for Semi-Supervised DG-Based Fault Furthermore, confronted with unavailable target domains in
L201: Diagnosis practical scenarios, the key to enhancing the generalization
L202: performance of the fault diagnosis model is to excavate
```

### Evidence snippets: architecture

```text
L3: ===== PAGE 1 =====
L5: IEEE TRANSACTIONS ON NEURAL NETWORKS AND LEARNING SYSTEMS, VOL. 36, NO. 3, MARCH 2025 5403
L6: Contrast-Assisted Domain-Specificity-Removal
L7: Network for Semi-Supervised Generalization
```

```text
L24: in order to realize reliable generalization fault diagnosis based on
L25: partially labeled source domains, this article proposes a contrast- fault-related features automatically and characterizing internal
L26: assisted domain-specificity-removal network (CDSRN) to extract information in industrial big data through layer-by-layer learn-
L27: transferable features from domain-specificity-removal perspec- ing, intelligent fault diagnosis methods based on deep learning
L28: tive. Concretely, a domain-specific feature removal branch is
```

```text
L49: RELIABILITY of industrial systems has always been a source domain, to the testing data, i.e., target domain, thereby
L50: eliminating the discrepancies of data distribution and achieving
L51: major concern and attracted increasing attention during
L52: satisfactory diagnosis result in the target domain.
L53: Unfortunately, given that rotating machinery often operates
```

```text
L85: ===== PAGE 2 =====
L87: 5404 IEEE TRANSACTIONS ON NEURAL NETWORKS AND LEARNING SYSTEMS, VOL. 36, NO. 3, MARCH 2025
L88: features in a straightforward way [15], [16]. Despite show- 3) A novel and complete method called CDSRN com-
L89: ing promising performance, these studies neglect the private bining domain-specific feature removal branch and
```

```text
L90: knowledge of each source domain, which is related to the proxy-contrastive representation enhancement module is
L91: variations of working conditions, thus failing to explicitly proposed for semi-supervised intelligent fault diagnosis
L92: inform the deep neural networks that private knowledge of toward unseen working conditions. Its reliable ability of
L93: each source domain should be removed. Ignoring the clear generalization fault diagnosis based on partially anno-
L94: guidance of removing private knowledge from the network tated data is verified through experimental studies based
```

```text
L100: domain-specific information and domain-invariant informa- in Section IV. In Section V, experimental studies, including
L101: tion in our work. Wang et al. [19] designed multiple result analyses and discussions based on two bearing datasets,
L102: domain-specific auxiliary classifiers to learn domain-specific are carried out to validate the performance of the proposed
L103: features from each source domain and remove the learned CDSRN. Finally, Section VI concludes this article.
L104: domain-specific features by a convolutional autoencoder mod-
```

```text
L110: diagnosis scenarios owing to the expensive cost of expert Supervised DG-based fault diagnosis methods can train the
L111: annotation [20]. model without accessing the target domain, which has attracted
L112: Aiming to solve the above issues, a novel contrast-assisted the attention of many scholars in recent years. For example,
L113: domain-specificity-removal network (CDSRN) is proposed Zheng et al. [15] proposed to learn the discriminant structures
L114: in this article for semi-supervised intelligent fault diagnosis of source domains based on Grassmann manifold, preserve
```

```text
L111: annotation [20]. model without accessing the target domain, which has attracted
L112: Aiming to solve the above issues, a novel contrast-assisted the attention of many scholars in recent years. For example,
L113: domain-specificity-removal network (CDSRN) is proposed Zheng et al. [15] proposed to learn the discriminant structures
L114: in this article for semi-supervised intelligent fault diagnosis of source domains based on Grassmann manifold, preserve
L115: toward unseen working conditions. Specifically, the proposed within-class local structure by local Fisher discriminant analy-
```

```text
L129: of this work are as follows. of feature normalization and adaptive weight were lever-
L130: 1) A domain-specific feature removal branch is established aged along with adversarial learning between the feature
L131: to give the network explicit guidance to exploit transfer- extractor and the domain classifier. Li et al. [24] proposed
L132: able domain-invariant features. Specifically, an auxiliary an adversarial domain-augmented generalization method with
L133: network branch is designed to extract domain-specific domain augmentation via convex combination of data and
```

```text
L172: Up to now, there are still few studies on semi-supervised DG are actually both working condition-dominant information
L173: problem for machinery fault diagnosis. Liao et al. [20] utilized (domain-specific information). Therefore, as shown in Fig. 2,
L174: the Wasserstein generative adversarial network and pseudo (1) can be transformed into
L175: label-based semi-supervised learning for training but did not
L176: consider the quality changes of pseudo labels during training. x(t) = f x (cid:0) x f , x d (cid:1) (2)
```

```text
L175: label-based semi-supervised learning for training but did not
L176: consider the quality changes of pseudo labels during training. x(t) = f x (cid:0) x f , x d (cid:1) (2)
L177: Zhao and Shen [27] proposed a mutual-assistance network
L178: where f is a nonparametric function and x and x mean
L179: consisting of entropy-based sample purification strategy and x f d
```

```text
L187: determined on validated tasks, which is lack of adaptability. f d
L188: is of great significance.
L189: Li et al. [28] proposed an adversarial DG network (ADGN)
L190: based on class boundary feature detection. Ren et al. [29]
L191: proposed a semi-supervised DG model for intelligent fault IV. PROPOSED METHOD
```

### Evidence snippets: experiment_defense

```text
L64: (Corresponding author: Xingxing Jiang.)
L65: Qiuyu Song, Juanjuan Shi, and Zhongkui Zhu are with the historical monitoring data can be obtained for training, while
L66: School of Rail Transportation, Soochow University, Suzhou 215131, the testing tasks are unseen, leading to the obstacle of unseen
L67: China (e-mail: qysongjob@stu.suda.edu.cn; jshi091@suda.edu.cn;
L68: distribution domain shift [14]. Thus, domain generalization
```

```text
L93: each source domain should be removed. Ignoring the clear generalization fault diagnosis based on partially anno-
L94: guidance of removing private knowledge from the network tated data is verified through experimental studies based
L95: may influence the learning efficacy. Some emerging DG-based on our laboratory wheel set bearing dataset and the
L96: fault diagnosis works have shown interest in this perspec- public rolling bearing dataset.
L97: tive. Jia et al. [17] and Li et al. [18] illustrated the causal The rest of this article starts with the related work in
```

```text
L99: fault-dominant information, which are, respectively, termed A detailed illustration of the proposed CDSRN is presented
L100: domain-specific information and domain-invariant informa- in Section IV. In Section V, experimental studies, including
L101: tion in our work. Wang et al. [19] designed multiple result analyses and discussions based on two bearing datasets,
L102: domain-specific auxiliary classifiers to learn domain-specific are carried out to validate the performance of the proposed
L103: features from each source domain and remove the learned CDSRN. Finally, Section VI concludes this article.
```

```text
L185: the optimal selection ratio of pseudo-labeled samples must be
L186: x , extracting and removing domain-specific information x
L187: determined on validated tasks, which is lack of adaptability. f d
L188: is of great significance.
L189: Li et al. [28] proposed an adversarial DG network (ADGN)
```

```text
L221: specific information. It motivates the idea of CDSRN to take
L222: m m m m,i i=1 the domain-specific information related to the variations of
L223: A typical semi-supervised DG-based fault diagnosis task aims
L224: working conditions into account. In addition, the discrim-
L225: to generalize a diagnostic model learned from one fully labeled
```

```text
L854: (11) V. EXPERIMENTAL STUDY
L855: In this section, experiments are conducted on two bear-
L856: where λ and λ are two coefficients to balance the losses. The ing datasets (including laboratory and public datasets) to
L857: 1 2
L858: Adam optimizer is utilized to update the network parameters. demonstrate the effectiveness and superiority of the proposed
```

```text
L864: 5410 IEEE TRANSACTIONS ON NEURAL NETWORKS AND LEARNING SYSTEMS, VOL. 36, NO. 3, MARCH 2025
L865: TABLE II
L866: DOMAINS BUILT ON THE TWO ROLLING BEARING DATASETS
L867: Fig. 5. Test rigs in (a) SU and (b) PU.
L868: A. Datasets Description
```

```text
L876: TABLE III
L877: diameter acting as a stand-in for the rail and a smaller wheel
L878: GENERALIZATION DIAGNOSIS TASKS BUILT ON THE TWO ROLLING BEAR-
L879: set with a 200 mm diameter representing the train wheels. One ING DATASETS
L880: side of the small wheel set is home to the NJ208E test bearing,
```

```text
L882: vibration signals with a 32 768-Hz sampling frequency. Cracks
L883: with a width of 0.4 mm were manually produced on a range of
L884: bearing rolling surfaces. This dataset includes eight different
L885: health states of the tested bearing: one normal state (N); three
L886: single fault states, including inner race fault (I), outer race
```

```text
L890: and inner race and ball faults (OIB), which are labeled using
L891: numbers 0–7.
L892: 2) PU Rolling Bearing Dataset: The utilization of PU
L893: rolling bearing dataset aims to prove the universality of the
L894: proposed method for diagnosing rolling bearing faults. This
```

```text
L906: According to four working conditions, four domains of SU
L907: DG-based fault diagnosis method.
L908: Wheel Set bearing dataset and PU rolling bearing dataset can
L909: 3) M3: As a state-of-the-art DG method, PCL [22] is used in
L910: be denoted as S1–S4 and C1–C4, respectively, as presented in
```

```text
L912: Table II. Each fault class contains 100 samples with a length
L913: source domains in this comparative experiment.
L914: of 4096. Thus, generalization diagnosis tasks are constructed
L915: 4) M4: DIFFN [29] is a state-of-the-art semi-supervised DG
L916: in Table III. Note that only the first source domain emphasized
```

### Evidence snippets: visualization

```text
L171: training and achieve good performance with limited labels. (domain-specific information). The second and third terms
L172: Up to now, there are still few studies on semi-supervised DG are actually both working condition-dominant information
L173: problem for machinery fault diagnosis. Liao et al. [20] utilized (domain-specific information). Therefore, as shown in Fig. 2,
L174: the Wasserstein generative adversarial network and pseudo (1) can be transformed into
L175: label-based semi-supervised learning for training but did not
```

```text
L201: Diagnosis practical scenarios, the key to enhancing the generalization
L202: performance of the fault diagnosis model is to excavate
L203: Fig. 1 illustrates the problem definition for semi-supervised
L204: common knowledge independent of data distributions from the
L205: DG-based fault diagnosis. The distribution of historical moni-
```

```text
L227: source domains D m s = {(xs m,i , d m,i )} i n = s m 1 , m = 2, 3, . . . , M enhance representation learning from the perspective of class
L228: to an unseen unlabeled target domain Dt with nt samples discriminability.
L229: Xt = {x i t} i n = t 1 , where y 1 s ,i and d m,i denote the labels of K Fig. 3 exhibits the overall schematic of the motivation
L230: machine health states and M domains, respectively. It should of CDSRN. Generally, CDSRN attempts to obtain the ulti-
L231: be noted that this work focuses on the problem of domain mate generalized features only in the domain-invariance
```

```text
L248: 5406 IEEE TRANSACTIONS ON NEURAL NETWORKS AND LEARNING SYSTEMS, VOL. 36, NO. 3, MARCH 2025
L249: Fig. 1. Illustration of semi-supervised DG-based fault diagnosis.
L250: generalization capability when source domains are partially
L251: labeled. Fig. 4 shows the network architecture of the pro-
```

```text
L265: I
L266: domain classifier D constitute the preliminary framework of
L267: Fig. 2. Diagram of domain-specific information and domain-invariant
L268: information in machinery fault signal. the proposed CDSRN. The domain-invariant features can be
L269: obtained coarsely by the adversarial training between the
```

```text
L458: SONG et al.: CDSRN FOR SEMI-SUPERVISED GENERALIZATION FAULT DIAGNOSIS 5407
L459: Fig. 3. Schematic of the motivation of CDSRN.
L460: domain-invariant feature extractor G and domain classifier where θ is the parameter of domain-specific feature extrac-
L461: I GS
```

```text
L635: 5408 IEEE TRANSACTIONS ON NEURAL NETWORKS AND LEARNING SYSTEMS, VOL. 36, NO. 3, MARCH 2025
L636: Fig. 4. Overview of the proposed CDSRN.
L637: Part 1 (Fault-Class-Proxy-Contrastive Learning): Fault- feature projection head P and a domain-proxy projection
L638: S
```

```text
L865: TABLE II
L866: DOMAINS BUILT ON THE TWO ROLLING BEARING DATASETS
L867: Fig. 5. Test rigs in (a) SU and (b) PU.
L868: A. Datasets Description
L869: 1) SU Wheel Set Bearing Dataset: SU Wheel Set bearing
```

```text
L872: in simulated rail vehicle operation scenarios. The wheel set
L873: bearing test rig established by our own laboratory of Soochow
L874: University (SU) is displayed in Fig. 5(a) [29]. The wheel rail
L875: simulation part consists of a massive wheel set with a 280 mm
L876: TABLE III
```

```text
L894: proposed method for diagnosing rolling bearing faults. This
L895: public dataset is provided by Paderborn University (PU) [31]
L896: and the test rig is shown in Fig. 5(b). Four types of health
L897: states, including normal state (N), inner race fault (I), outer
L898: race fault (O), and compound faults containing I and O (IO),
```

```text
L947: presented in Table IV. Some observations and conclusions can
L948: be drawn as follows.
L949: Fig. 6. Confusion matrices in task T2 by (a) M1, (b) M2, (c) M3, (d) M4,
L950: 1) M1 only obtains an average diagnosis accuracy of (e) M5, and (f) CDSRN.
L951: 74.39% and 80.34% in the two experiments, respectively,
```

```text
L963: be attributed to the abilities of M2, M3, M4, and M5 to learn
L964: domain-common knowledge among source domains.
L965: Fig. 7. Confusion matrices in task Q4 by (a) M1, (b) M2, (c) M3, (d) M4,
L966: 3) The final average accuracy of the proposed CDSRN (e) M5, and (f) CDSRN.
L967: method reaches the highest average accuracy of 97.73%
```

### Closing evidence
- She is currently a Professor with the School of
- Rail Transportation, Soochow University, Suzhou,
- Jiangsu, China. Her research interests include rotat-
- ing machinery condition monitoring, vibration con-
- Qiuyu Song received the B.E. degree in vehi-
- trol, and digital signal processing.
- cle engineering from Soochow University, Suzhou,
- China, in 2020. She is currently pursuing the Ph.D.
- degree with the School of Rail Transportation, Soo-
- chow University.
- Her research interests include adaptive sig-
- nal decomposition, health monitoring of rotating
- machines, and intelligent fault diagnosis.
- Zhongkui Zhu received the B.S. degree in automo-
- bile and tractor (automobile) and the M.S. degree
- Xingxing Jiang received the B.E. and Ph.D. degrees
- in vehicle engineering from Hefei Polytechnic Uni-
- in vehicle engineering from Nanjing University of
- versity, Hefei, Anhui, China, in 1997 and 2002,
- Aeronautics and Astronautics (NUAA), Nanjing,
- respectively, and the Ph.D. degree in instrument sci-
- China, in 2012 and 2016, respectively.
- ence and technology from the University of Science
- He is currently a Professor with the School of Rail
- and Technology of China, Hefei, in 2005.
- Transportation, Soochow University, Suzhou, China.
- He is currently a Professor with the School of
- His research interests include machinery intelli-
- Rail Transportation, Soochow University, Suzhou,
- gent fault diagnosis, health monitoring of rotating
- Jiangsu, China. His research interests include vehicle
- machines, and adaptive signal decomposition.
- system dynamics and control, vibration measure-
- ment, and signal processing.
- Authorized licensed use limited to: University of Science & Technology of China. Downloaded on July 05,2026 at 10:03:23 UTC from IEEE Xplore. Restrictions apply.

## Domain_Perturbation_With_Uncertainty_for_Bearing_Fault_Diagnosis_Under_Unseen_Conditions
- Extracted chars: 57576

### Opening / abstract evidence
- ===== PAGE 1 =====
- 4956 IEEE TRANSACTIONS ON CYBERNETICS, VOL. 55, NO. 10, OCTOBER 2025
- Domain Perturbation With Uncertainty for Bearing
- Fault Diagnosis Under Unseen Conditions
- Yongyi Chen , Dan Zhang , Senior Member, IEEE, Ruqiang Yan , Fellow, IEEE, Min Xie , Fellow, IEEE,
- and Qi Xuan , Senior Member, IEEE
- Abstract—Domain adaptation (DA) techniques are becoming long been discovered that the success of DL heavily relies on
- increasingly proficient in cross-domain fault diagnosis tasks. the assumption that training and testing data follow indepen-
- However, DA-based methods are not always applicable due to
- dent and identical distributions [5], [6]. Unfortunately, in real
- the target domain data is not always accessible. Although there
- industrial scenarios, this assumption is difficult to hold. Due
- have been some interesting domain generalization methods for
- fault diagnosis under unseen conditions, most of them can only to the interference of operating conditions and environmental
- be used to mine the fault features on source domain distributions, noise, it is impossible to ensure that the data collected at
- and the improvement of model generalization performance is every moment has the same data distribution. In this case,
- limited. To solve this problem, the multiplicative noise Gaussian
- the diagnosis network obtained by fitting the source domain
- perturbation strategy and the additive noise linear fusion strategy
- data could fail on data from new domains [7]. To reduce the
- are proposed to capture fault information beyond source domain
- distributions. The former is used to randomly perturb feature performance loss of diagnosis networks caused by domain
- statistics of multisource domains to simulate the uncertainty of shift, domain adaptation (DA) technology is introduced into
- domain shift, while the latter is used to perform the additive noise fault diagnosis in some researches [8]. DA technology aims
- linear operation on feature statistics of multiple source domains
- to make the model adapt and learn based on the target
- to ensure the authenticity of the generated feature styles. Further,
- domain data received, so as to generalize the fault knowledge
- the feature statistics generated by both strategies are mixed with
- random convex weights to obtain new feature styles, achieving the learned in the source domain to the target domain. The
- best compromise between reliability and diversity. The network most common DA technique is unsupervised DA (UDA).
- can learn more fault information from features with diversified Recent UDA methods can be divided into two categories, i.e.,
- styles. Extensive experimental results on both public and real
- adversarial learning (AL) and reconstruction learning (RL).
- datasets verify the effectiveness of our approach.
- The former is used to align the marginal distribution (or
- Index Terms—Deep learning (DL), domain generalization conditional distribution) of the data from both domains using
- (DG), fault diagnosis, feature styles, unseen conditions.
- the distance function, and the latter is used to realize the
- domain-invariant feature learning by reconstructing the target
- I. INTRODUCTION domain data.
- DEEP learning (DL) has demonstrated remarkable ability The assumption that the label spaces of the source and
- target domains are aligned needs to be satisfied in the UDA
- in fault diagnosis, which is proven to be effective in
- method. In reality, however, it is difficult to ensure that

### Section, table, and figure headings detected
- L115: II. METHODOLOGY
- L117: A. Overall Framework
- L123: 1) In most existing DG methods, new learning mecha- efficient way to improve the generalization ability of the
- L144: 1) The multiplicative noise Gaussian perturbation (MNGP) improve the diversity of fault knowledge learned by the
- L192: Fig. 1. Overall flow of the proposed method. distribution range of feature statistics. Once the target domain
- L232: Fig. 2. Overview of DGNSU.
- L346: TABLE I Algorithm 1 Training Procedures of DGNSU
- L385: Table I. 64 samples are sampled from two source domain B B b b
- L400: A. Dataset Description
- L433: B. Comparisons With State-of-the-Art
- L452: 2) MAGNet and ADAG are very similar methods for
- L462: Fig. 3. Experimental setup of ZJUT dataset. on the ZJUT dataset. This may be because the sample
- L464: TABLE II
- L469: 3) Unlike ADAG and MAGNet, which use Mixup to
- L471: TABLE III
- L493: 1) Compared with DL-based methods (MF-DRCN), DG- existing approaches based on Mixup and style gener-
- L505: C. Further Analyses
- L515: TABLE IV
- L517: TABLE V
- L519: TABLE VI
- L521: Fig. 4. Sensitivity analysis of parameters in DGNSU. (a) ωˆ 1 and ωˆ 2. (b) ω˜ 1
- L522: Table VI summarizes the average generalization performance and ω˜ 2.
- L561: Fig. 5. Diversity analysis of feature styles. (a) C1 + C3. (b) C5 + C6. the features of various health state bearings.
- L562: IV. CONCLUSION
- L579: Fig. 6. Results of visualizing the features extracted by the penultimate

### Evidence snippets: math_formalization

```text
L9: and Qi Xuan , Senior Member, IEEE
L10: Abstract—Domain adaptation (DA) techniques are becoming long been discovered that the success of DL heavily relies on
L11: increasingly proficient in cross-domain fault diagnosis tasks. the assumption that training and testing data follow indepen-
L12: However, DA-based methods are not always applicable due to
L13: dent and identical distributions [5], [6]. Unfortunately, in real
```

```text
L18: be used to mine the fault features on source domain distributions, noise, it is impossible to ensure that the data collected at
L19: and the improvement of model generalization performance is every moment has the same data distribution. In this case,
L20: limited. To solve this problem, the multiplicative noise Gaussian
L21: the diagnosis network obtained by fitting the source domain
L22: perturbation strategy and the additive noise linear fusion strategy
```

```text
L23: data could fail on data from new domains [7]. To reduce the
L24: are proposed to capture fault information beyond source domain
L25: distributions. The former is used to randomly perturb feature performance loss of diagnosis networks caused by domain
L26: statistics of multisource domains to simulate the uncertainty of shift, domain adaptation (DA) technology is introduced into
L27: domain shift, while the latter is used to perform the additive noise fault diagnosis in some researches [8]. DA technology aims
```

```text
L41: (DG), fault diagnosis, feature styles, unseen conditions.
L42: the distance function, and the latter is used to realize the
L43: domain-invariant feature learning by reconstructing the target
L44: I. INTRODUCTION domain data.
L45: DEEP learning (DL) has demonstrated remarkable ability The assumption that the label spaces of the source and
```

```text
L59: contains private classes [9], which has received wide attention
L60: under Grant 11201023 and Grant 11202224. This article was recommended
L61: by Associate Editor R.-E. Precup. (Corresponding author: Dan Zhang.) recently. Common methods to solve the PDA problem include
L62: Yongyi Chen and Dan Zhang are with the Department of Automation, common sample weighting [10], [11], [12] and multiclassifier
L63: Zhejiang University of Technology, Hangzhou 310023, China (e-mail:
```

```text
L65: 2111903247@zjut.edu.cn; danzhang@zjut.edu.cn).
L66: Ruqiang Yan is with the School of Mechanical Engineering, Xi’an Jiaotong of samples with outlier classes on DA. Unlike PDA, the
L67: University, Xi’an 710049, China (e-mail: yanruqiang@xjtu.edu.cn). purpose of OSDA is to solve the problem of private classes in
L68: Min Xie is with the Department of Systems Engineering and Engineering
L69: the target domain. Recent OSDA studies [15], [16], [17] have
```

```text
L99: of DA is cumbersome, and it is impossible to quickly optimize some random interference.
L100: the model based on the real-time changes of the target domain. 3) The feature statistics generated by MNGP and ANLF
L101: Therefore, the problem of domain generalization (DG), aiming strategies are mixed with random convex weights to
L102: to improve the robustness of the network on various unseen generate new feature styles, which achieves the best
L103: target domains, becomes quite important. In DG, only existing compromise between reliability and diversity. The diag-
```

```text
L104: source domain data can be used without accessing target nosis network is trained to reduce domain perturbations
L105: domain data to train a robust model so that the model caused by features with new styles, which could promote
L106: performs well on unseen domains. In [21], [22], and [23], AL the network encode better domain-invariant features.
L107: was introduced as a bridge to establish a smooth adaptation The remainder of this article is organised as follows. In
L108: from multisource domains to unseen domains. In [24], [25], Section II, the proposed DGNSU and the key components are
```

```text
L112: to learn fault features beyond source domain distributions.
L113: In [31], [32], [33], and [34], multiple classifiers were used to
L114: learn domain-invariant features in multisource domain data,
L115: II. METHODOLOGY
L116: including multiclassifier ensemble [31], [32], multiclassifier
```

```text
L123: 1) In most existing DG methods, new learning mecha- efficient way to improve the generalization ability of the
L124: nisms are usually designed to align multisource domain DG model on the unseen domain data is to let the network
L125: distributions to guide models to learn domain-invariant learn more fault feature styles under limited source domain
L126: features. However, this common practice causes the data. For this purpose, a novel fault diagnosis network, i.e.,
L127: diagnosis model to overfit the feature styles of the exist- DGNSU, is developed to enable the model to learn more styles
```

```text
L204: domain features into that of target domain features is required to reduce the domain perturbations and encode
L205: (cid:2) (cid:3)
L206: (cid:4) (cid:5) x − μ(F ) (cid:4) (cid:5) better domain-invariant features during training, so as to
L207: AdaIN(F ) = σ F x + μ F . (2) improve the generalization performance of the network for
L208: x y σ(F ) y
```

```text
L422: 2) CWRU Dataset: In the Case Western Reserve University
L423: (CWRU) public dataset [47], bearing damage occurs at three 17: Extract the fault features of F new by the encoder.
L424: different locations, i.e., OF, IF, and BF. There are three fault 18: Use RMSprop optimization algorithm to train
L425: DGNSU by minimizing the cross-entropy loss func-
L426: diameters for different locations, i.e., 0.1778 (L2), 0.3556
```

### Evidence snippets: architecture

```text
L19: and the improvement of model generalization performance is every moment has the same data distribution. In this case,
L20: limited. To solve this problem, the multiplicative noise Gaussian
L21: the diagnosis network obtained by fitting the source domain
L22: perturbation strategy and the additive noise linear fusion strategy
L23: data could fail on data from new domains [7]. To reduce the
```

```text
L23: data could fail on data from new domains [7]. To reduce the
L24: are proposed to capture fault information beyond source domain
L25: distributions. The former is used to randomly perturb feature performance loss of diagnosis networks caused by domain
L26: statistics of multisource domains to simulate the uncertainty of shift, domain adaptation (DA) technology is introduced into
L27: domain shift, while the latter is used to perform the additive noise fault diagnosis in some researches [8]. DA technology aims
```

```text
L32: the feature statistics generated by both strategies are mixed with
L33: random convex weights to obtain new feature styles, achieving the learned in the source domain to the target domain. The
L34: best compromise between reliability and diversity. The network most common DA technique is unsupervised DA (UDA).
L35: can learn more fault information from features with diversified Recent UDA methods can be divided into two categories, i.e.,
L36: styles. Extensive experimental results on both public and real
```

```text
L57: the Key Research and Development Programs of Zhejiang Province under (UniDA). PDA is a scenario where only the source domain
L58: Grant 2023C01224; and in part by the Research Grant Council of Hong Kong
L59: contains private classes [9], which has received wide attention
L60: under Grant 11201023 and Grant 11202224. This article was recommended
L61: by Associate Editor R.-E. Precup. (Corresponding author: Dan Zhang.) recently. Common methods to solve the PDA problem include
```

```text
L89: CHEN et al.: DOMAIN PERTURBATION WITH UNCERTAINTY FOR BEARING FAULT DIAGNOSIS 4957
L90: PDA, and the application scenarios are limited. UniDA, as a so that the fault information learned by the diagnosis
L91: more challenging scenario, allows both domains to have their network is more diversified.
L92: own private classes, broadening the application of DA-based 2) The additive noise linear fusion (ANLF) strategy is
L93: diagnosis methods, such as [18], [19], and [20]. developed to compensate for the authenticity risk caused
```

```text
L100: the model based on the real-time changes of the target domain. 3) The feature statistics generated by MNGP and ANLF
L101: Therefore, the problem of domain generalization (DG), aiming strategies are mixed with random convex weights to
L102: to improve the robustness of the network on various unseen generate new feature styles, which achieves the best
L103: target domains, becomes quite important. In DG, only existing compromise between reliability and diversity. The diag-
L104: source domain data can be used without accessing target nosis network is trained to reduce domain perturbations
```

```text
L104: source domain data can be used without accessing target nosis network is trained to reduce domain perturbations
L105: domain data to train a robust model so that the model caused by features with new styles, which could promote
L106: performs well on unseen domains. In [21], [22], and [23], AL the network encode better domain-invariant features.
L107: was introduced as a bridge to establish a smooth adaptation The remainder of this article is organised as follows. In
L108: from multisource domains to unseen domains. In [24], [25], Section II, the proposed DGNSU and the key components are
```

```text
L111: was performed on the source domain and augmented domain are drawn in Section IV.
L112: to learn fault features beyond source domain distributions.
L113: In [31], [32], [33], and [34], multiple classifiers were used to
L114: learn domain-invariant features in multisource domain data,
L115: II. METHODOLOGY
```

```text
L122: these methods suffer from two major limitations. given the target domain data. Intuitively, the most direct and
L123: 1) In most existing DG methods, new learning mecha- efficient way to improve the generalization ability of the
L124: nisms are usually designed to align multisource domain DG model on the unseen domain data is to let the network
L125: distributions to guide models to learn domain-invariant learn more fault feature styles under limited source domain
L126: features. However, this common practice causes the data. For this purpose, a novel fault diagnosis network, i.e.,
```

```text
L131: domain data when the domain gap is large. 1) Two new datasets are first constructed by alternating
L132: 2) Although data-augmentation-based methods (e.g., [28] combinations of labeled multisource domain data as
L133: and [30]) can enable the network to learn more styles the network input, and then network bottom features
L134: of fault features, the augmented data is only a linear of the input data are extracted to capture their style
L135: combination or linear transformation of multisource information.
```

```text
L138: makes the model unable to learn potential domain shifts generate new feature styles that are different from the
L139: in unseen conditions. original styles in source domains.
L140: In this article, our architecture, DG network with statistical 3) Finally, new styles are applied to the style-normalized
L141: uncertainty (DGNSU), is designed to be an efficient architec- features to generate features with new styles by adaptive
L142: ture for improving the performance of the diagnosis model instance normalization (AdaIN). The generated features
```

```text
L143: over unseen conditions. Our main contributions are as follows. are fed into the encoder for fault feature extraction to
L144: 1) The multiplicative noise Gaussian perturbation (MNGP) improve the diversity of fault knowledge learned by the
L145: strategy is designed to model potential domain shift for diagnosis network.
L146: the uncertainty and randomness of unseen conditions. In Remark 1: Instance-normalization (IN) is used to normalize
L147: the MNGP strategy, new styles that do not exist in source feature F according to the mean and standard deviation
```

### Evidence snippets: experiment_defense

```text
L9: and Qi Xuan , Senior Member, IEEE
L10: Abstract—Domain adaptation (DA) techniques are becoming long been discovered that the success of DL heavily relies on
L11: increasingly proficient in cross-domain fault diagnosis tasks. the assumption that training and testing data follow indepen-
L12: However, DA-based methods are not always applicable due to
L13: dent and identical distributions [5], [6]. Unfortunately, in real
```

```text
L36: styles. Extensive experimental results on both public and real
L37: adversarial learning (AL) and reconstruction learning (RL).
L38: datasets verify the effectiveness of our approach.
L39: The former is used to align the marginal distribution (or
L40: Index Terms—Deep learning (DL), domain generalization conditional distribution) of the data from both domains using
```

```text
L47: in fault diagnosis, which is proven to be effective in
L48: method. In reality, however, it is difficult to ensure that
L49: many fault diagnosis tasks [1], [2], [3], [4]. However, it has
L50: the label space of the target domain is consistent with that
L51: Received 2 May 2025; accepted 14 June 2025. Date of publication of the source domain, and it is also impossible to know
```

```text
L129: the diagnosis knowledge learned from the multisource DGNSU comprises the steps listed as follows (see Fig. 1 for
L130: domain data can be effectively generalized to the unseen details).
L131: domain data when the domain gap is large. 1) Two new datasets are first constructed by alternating
L132: 2) Although data-augmentation-based methods (e.g., [28] combinations of labeled multisource domain data as
L133: and [30]) can enable the network to learn more styles the network input, and then network bottom features
```

```text
L138: makes the model unable to learn potential domain shifts generate new feature styles that are different from the
L139: in unseen conditions. original styles in source domains.
L140: In this article, our architecture, DG network with statistical 3) Finally, new styles are applied to the style-normalized
L141: uncertainty (DGNSU), is designed to be an efficient architec- features to generate features with new styles by adaptive
L142: ture for improving the performance of the diagnosis model instance normalization (AdaIN). The generated features
```

```text
L145: strategy is designed to model potential domain shift for diagnosis network.
L146: the uncertainty and randomness of unseen conditions. In Remark 1: Instance-normalization (IN) is used to normalize
L147: the MNGP strategy, new styles that do not exist in source feature F according to the mean and standard deviation
L148: x
L149: domains are randomly generated from a range that is of F and perform affine transformations. At this stage, F
```

```text
L208: x y σ(F ) y
L209: x unseen conditions. In the MNGP strategy, the channel-wise
L210: feature mean and standard deviation of each instance feature
L211: B. Uncertainty Estimation of Domain Shift F α and F β ∈ RC×W in a mini-batch are calculated to
L212: b b
```

```text
L237: where μ(F) ∈ RC and σ(F) ∈ RC represent the channel-wise B B b B b B
L238: b=1
L239: feature mean and standard deviation computed within each (cid:4) (cid:5) (cid:6)B (cid:7) (cid:7) (cid:8) (cid:8)(cid:7) (cid:7) (cid:8) (cid:8)
L240: channel of F, respectively. Similar to the feature generation σσ 2 = 1 σ F β − μσ σ F β − μσ T . (10)
L241: process of AdaIN in (2), μ(F α) and σ(F α) are applied to B B b B b B
```

```text
L277: ¨β the source domain features. Specifically, Gaussian white noise
L278: feature statistics of F can better characterize the changes in
L279: b with mean 0 and standard deviation 1 is added to the source
L280: data distribution caused by domain shift α ¯ α
L281: domain feature F to obtain F , which aims to ensure the
```

```text
L398: σ 2 according to Eqs.
L399: (17)-(20);
L400: A. Dataset Description
L401: 10: Build Gaussian distributions N μ and N σ for two style
L402: We tested the performance of the proposed method on both β
```

```text
L402: We tested the performance of the proposed method on both β
L403: vectors of F ;
L404: real and public datasets. In each dataset, 2450 samples were b
L405: used for training and 1200 samples were used for testing. Each 11: Sample randomly a pair of style vectors μˆ s and σˆ s
L406: according to Eqs. (21) and (22);
```

```text
L407: vibration signal sample was preprocessed by power spectrum ¯ α β
L408: estimation method, and each sample contains 2048 data points. 12: Obtain F b by adding additive no (cid:4) ise (cid:5) to F (cid:4)b ; (cid:5)
L409: 1) ZJUT Dataset: As shown in Fig. 3, the real dataset 13: Calculate the feature statistics (μ F ¯ b α , σ F ¯ b α ) of F b β
L410: came from Zhejiang University of Technology (ZJUT). The
L411: according(cid:4) to (cid:5)Eqs. (23(cid:4)) a(cid:5)nd (24);
```

### Evidence snippets: visualization

```text
L72: Qi Xuan is with the Institute of Cyberspace Security, College of shared and outlier classes by introducing a weighted learning
L73: Information Engineering, Zhejiang University of Technology, Hangzhou
L74: mechanism. The feature distributions between samples of
L75: 310023, China, and also with the Binjiang Institute of Artificial Intelligence,
L76: Zhejiang University of Technology, Hangzhou 310056, China (e-mail: classes shared across domains can be more effectively aligned
```

```text
L127: diagnosis model to overfit the feature styles of the exist- DGNSU, is developed to enable the model to learn more styles
L128: ing source domain. Especially, there is no guarantee that of fault features under limited source domain data. Overall,
L129: the diagnosis knowledge learned from the multisource DGNSU comprises the steps listed as follows (see Fig. 1 for
L130: domain data can be effectively generalized to the unseen details).
L131: domain data when the domain gap is large. 1) Two new datasets are first constructed by alternating
```

```text
L171: the both source domains, X1 = {Dm, Dn} and X2 = {Dn, Dm}
L172: are constructed by alternating combinations of source domains
L173: Dm and Dn. As shown in Fig. 2, X1 and X2 are obtained by
L174: exchanging the positions of Dm and Dn and are shuffled using
L175: the same shuffling operation. At this stage, samples at the
```

```text
L190: as the determined values for the diagnosis network to learn,
L191: the network can only learn fault information within the given
L192: Fig. 1. Overall flow of the proposed method. distribution range of feature statistics. Once the target domain
L193: has a large domain shift compared with the source domain,
L194: the fault knowledge learned by the network will be difficult
```

```text
L231: CHEN et al.: DOMAIN PERTURBATION WITH UNCERTAINTY FOR BEARING FAULT DIAGNOSIS 4959
L232: Fig. 2. Overview of DGNSU.
L233: (cid:9)
L234: σ (cid:7) F b β (cid:8) = (cid:10) (cid:10) (cid:11) W 1 w (cid:6)W =1 (cid:7) F b β ,w − μ (cid:7) F b β (cid:8)(cid:8) 2 (6) μσ B = B 1 (cid:6) b= B 1 σ (cid:7) F b β (cid:8) (8)
```

```text
L251: uncertainty and randomness of the feature style vectors sim-
L252: of feature statistics is used to guide the generation of new ulated by N μ and N σ, nonlinear perturbations are introduced
L253: feature styles. As shown in Fig. 2, the mean and variance of
L254: feature statistics μ(F β) and σ(F β) for all instance features in into the uncertainty estimation of fe β ature stat ¨ is β tics. Particularly,
L255: b b multiplicative noise is added to F to get F and the feature
```

```text
L332: due to the introduction of two nonlinear operations in the allowing the network to learn more styles of fault features.
L333: sampling process of feature style vectors. Some new styles The entire framework of the proposed DGNSU is presented
L334: may be very different from those of source domain data, which in Fig. 2. Features with new styles generated by MNGP and
L335: brings the risk of authenticity. If there is no restriction in the ANLF strategies are used to update the feature extractor
L336: generated random styles, the learning of the diagnosis network and classifier, avoiding network fitting to specific domain
```

```text
L407: vibration signal sample was preprocessed by power spectrum ¯ α β
L408: estimation method, and each sample contains 2048 data points. 12: Obtain F b by adding additive no (cid:4) ise (cid:5) to F (cid:4)b ; (cid:5)
L409: 1) ZJUT Dataset: As shown in Fig. 3, the real dataset 13: Calculate the feature statistics (μ F ¯ b α , σ F ¯ b α ) of F b β
L410: came from Zhejiang University of Technology (ZJUT). The
L411: according(cid:4) to (cid:5)Eqs. (23(cid:4)) a(cid:5)nd (24);
```

```text
L460: average accuracy of MAGNet (93.70% ) is lower than
L461: ADAG (94.12% ) but higher than ADIG in all DG tasks
L462: Fig. 3. Experimental setup of ZJUT dataset. on the ZJUT dataset. This may be because the sample
L463: weighting mechanism restricts the learning weights of
L464: TABLE II
```

```text
L519: TABLE VI
L520: ABLATION EXPERIMENT
L521: Fig. 4. Sensitivity analysis of parameters in DGNSU. (a) ωˆ 1 and ωˆ 2. (b) ω˜ 1
L522: Table VI summarizes the average generalization performance and ω˜ 2.
L523: of each ablation schemes on C1+C2, C1+C3, C1+C4,
```

```text
L534: it difficult for the network to learn fault features beyond weights ωˆ and ωˆ on diagnosis results is studied, as shown
L535: 1 2
L536: source domain distributions, and the performance improve- in Fig. 4(a). It can be observed that DGNSU is very sensitive
L537: ment is limited compared with the baseline (A4). Similarly, to weights ωˆ and ωˆ . The weight ωˆ assigned to nonlinear
L538: 1 2 2
```

```text
L541: with new styles have a larger domain shift than the source of new styles. The ability of the network to resist domain
L542: domain features. As a result, noise information is introduced, disturbance can be improved by introducing a proper amount
L543: which makes the network unable to effectively learn domain- of nonlinear noise. In Fig. 4(b), we show the fusion parameters
L544: invariant representations. We further analyze the complexity in the ANLF strategy. It can be concluded that the weights of
L545: involved in integrating MNGP and ANLF strategies into the source features and additive noise features should be balanced
```

### Closing evidence
- to 2014, also with the National University of
- Singapore, Singapore, from 2016 to 2017, and also
- with the City University of Hong Kong, Hong Kong,
- from 2017 to 2019. His current research interests are
- in the areas of unmanned systems and AI application in industries.
- Dr. Zhang is an Associate Editor of the IEEE TRANSACTIONS ON
- INSTRUMENTATION AND MEASUREMENT, SIGNAL, IMAGE AND VIDEO
- PROCESSING, IET Electronics Letters, ISA Transactions, International
- Journal of Control, Automation, and Systems, Cyber–Physical Systems, and
- an Area Editor of International Journal of Uncertainty, Fuzziness and
- Knowledge-Based Systems.
- Ruqiang Yan (Fellow, IEEE) received the M.S.
- degree in precision instrument and machinery from
- the University of Science and Technology of China,
- Hefei, China, in 2002, and the Ph.D. degree in
- mechanical engineering from the University of
- Massachusetts at Amherst, Amherst, MA, USA, in
- 2007.
- He was a Guest Researcher with the National Qi Xuan (Senior Member, IEEE) received the B.S.
- Institute of Standards and Technology, Gaithersburg, and Ph.D. degrees in control theory and engineering
- MD, USA, from 2006 to 2008 and a Professor with from Zhejiang University, Hangzhou, China, in 2003
- the School of Instrument Science and Engineering, and 2008, respectively.
- Southeast University, Nanjing, China, from 2009 to 2018. He joined the He was a Postdoctoral Researcher with the
- School of Mechanical Engineering, Xi’an Jiaotong University, Xi’an, China, Department of Information Science and Electronic
- in 2018. His research interests include data analytics, AI, and energy-efficient Engineering, Zhejiang University from 2008 to
- sensing and sensor networks for the condition monitoring and health diagnosis 2010, and a Research Assistant with the Department
- of large-scale, complex, and dynamical systems. of Electronic Engineering, City University of Hong
- Dr. Yan’s honors and awards include the IEEE Instrumentation and Kong, Hong Kong, SAR, China, in 2010 and 2017.
- Measurement Society Technical Award in 2019 and the Outstanding Service From 2012 to 2014, he was a Postdoctoral Fellow
- Award in 2022, and multiple best paper awards, such as the Andrew P. with the Department of Computer Science, University of California at Davis,
- Sage Best Transactions Paper Award. He served as an Editor-in-Chief for the Davis, CA, USA. He is currently a Professor with the College of Information
- IEEE TRANSACTIONS ON INSTRUMENTATION AND MEASUREMENT, and is Engineering, Zhejiang University of Technology, Hangzhou. His current
- currently an Associate Editor-in-Chief for Chinese Journal of Mechanical research interests include network-based algorithms design, social networks,
- Engineering. He is a Fellow of ASME in 2019. data mining, cyberspace security, machine learning, and computer vision.
- Authorized licensed use limited to: University of Science & Technology of China. Downloaded on July 05,2026 at 10:05:07 UTC from IEEE Xplore. Restrictions apply.

## Extended_Invariant_Risk_Minimization_for_Machine_Fault_Diagnosis_With_Label_Noise_and_Data_Sh
- Extracted chars: 87649

### Opening / abstract evidence
- ===== PAGE 1 =====
- 15476 IEEE TRANSACTIONS ON NEURAL NETWORKS AND LEARNING SYSTEMS, VOL. 36, NO. 8, AUGUST 2025
- Extended Invariant Risk Minimization for Machine
- Fault Diagnosis With Label Noise and Data Shift
- Zhenling Mo, Zijun Zhang , Senior Member, IEEE, Qiang Miao , Senior Member, IEEE,
- and Kwok-Leung Tsui
- Abstract—Incorrect labels as well as the discrepancy between conditions [6], [7]. In practice, NLs and data distribution
- training and test domain data distributions can significantly shifts are inevitable in machine fault diagnosis. To enhance
- affect the effectiveness of supervised data-driven models in
- the practical value of data-driven models for machine fault
- machine fault diagnosis applications. Such a challenge can be
- diagnosis, it is imperative to develop a fault diagnosis model
- characterized as the noisy label-domain generalization (NL-DG)
- problem. In this article, the extended invariant risk minimization that is both tolerant to label noise (LN) and capable of
- (EIRM) is developed, which incorporates flat minima seeking to generalizing across domains.
- address the NL-DG challenge. The ability of handling NL-DG is In existing literature of the machine learning community,
- realized by shifting the gradient penalty base from the dummy
- addressing LNs focused on LN robust learning [8] while
- classifier to the entire model. EIRM is shown to be closely related
- tackling data distribution shifts was regarded as one major
- to locating a flat minimum, which is crucial for label noise (LN)
- robustness and model generalization. Explorations on function task in domain generalization (DG) [9]. A significant focus
- smoothness and algorithm convergence are offered to understand of recent studies in LN robust learning is designing robust
- EIRM from the theoretical aspect. An efficient implementation risk functions [8]. The designed function is considered robust
- of EIRM is also developed to construct the fault diagnosis
- in the sense that the global minima are unchanged even if
- model. The EIRM-based fault diagnosis method is compared with
- some portions of labels are corrupted [10]. One technique
- strong benchmarks on multiple NL-DG tasks using actuator and
- gearbox fault datasets. Results indicate that the EIRM-based enabling such robustness is the symmetric condition [10].
- method on average is more effective than the benchmarks. The Inspired by the symmetric condition, different symmetric
- code is available at https://github.com/mozhenling/doge-eirm. robust risk functions were studied, such as the mean absolute
- Index Terms—Domain generalization (DG), fault diagnosis, error risk function [10], the symmetric cross-entropy (SCE)
- flat minimum, invariant learning, label noise (LN) robustness. risk function [11], and the normalized risk function [12].
- In general, robust risk functions can facilitate training
- I. INTRODUCTION
- various risk minimization-based data-driven models in a
- INDUSTRIAL machine fault diagnosis can be challeng- straightforward plug-in approach to tackle LNs. However,
- ing since the presence of noisy labels (NLs) and data relying solely on designing the robust risk function may not
- distribution shifts can greatly diminish the performance of sufficiently address the challenges imposed by DG. To realize
- many data-driven methods [1], [2]. Incorrect machine fault DG, one popular direction is to learn invariant features [13].
- labels are often introduced due to the similarity among fault The invariant features are informative about the labels and
- patterns [3], less experienced labelers [4], or improper data shared across domains, which can enable model generalization
- management [5]. In addition, data distribution shifts are often beyond training domains [14]. A notable approach in learning
- induced by data collected under different machine operation invariant features is invariant risk minimization (IRM) [15].

### Section, table, and figure headings detected
- L39: I. INTRODUCTION
- L110: II. PRELIMINARIES
- L253: C. Notations
- L286: III. METHODOLOGY
- L292: A. Brief of IRM
- L353: Fig. 1. Fault diagnosis model training based on EIRM and 1-D LeNet.
- L364: C. EIRM-Based Fault Diagnosis Model
- L365: A. Smoothness of the Vanilla Risk Function
- L536: 1) The extended risk function enables the vanilla risk func-
- L543: 2) The coefficients of upper bounds in (25) and (28) range
- L554: 3) Compared to the vanilla function, the extended risk
- L566: 4) Finally, it should be mentioned that the main purpose of
- L585: A. Benchmark Method dataset contains data reflecting three health conditions of a
- L603: Fig. 1) based on two training domains and then test the trained
- L615: TABLE I
- L617: TABLE II
- L621: D. Result Analysis
- L626: 1) All models generally perform better on the gearbox
- L628: Fig. 3. Test rig of the gearbox. the complexity of the actuator’s two motion profiles,
- L651: A. Proof of Corollary 1
- L669: B. Proof of Corollary 2
- L697: C. Proof of Lemma 2

### Evidence snippets: math_formalization

```text
L5: 15476 IEEE TRANSACTIONS ON NEURAL NETWORKS AND LEARNING SYSTEMS, VOL. 36, NO. 8, AUGUST 2025
L6: Extended Invariant Risk Minimization for Machine
L7: Fault Diagnosis With Label Noise and Data Shift
L8: Zhenling Mo, Zijun Zhang , Senior Member, IEEE, Qiang Miao , Senior Member, IEEE,
```

```text
L15: diagnosis, it is imperative to develop a fault diagnosis model
L16: characterized as the noisy label-domain generalization (NL-DG)
L17: problem. In this article, the extended invariant risk minimization that is both tolerant to label noise (LN) and capable of
L18: (EIRM) is developed, which incorporates flat minima seeking to generalizing across domains.
L19: address the NL-DG challenge. The ability of handling NL-DG is In existing literature of the machine learning community,
```

```text
L25: robustness and model generalization. Explorations on function task in domain generalization (DG) [9]. A significant focus
L26: smoothness and algorithm convergence are offered to understand of recent studies in LN robust learning is designing robust
L27: EIRM from the theoretical aspect. An efficient implementation risk functions [8]. The designed function is considered robust
L28: of EIRM is also developed to construct the fault diagnosis
L29: in the sense that the global minima are unchanged even if
```

```text
L31: some portions of labels are corrupted [10]. One technique
L32: strong benchmarks on multiple NL-DG tasks using actuator and
L33: gearbox fault datasets. Results indicate that the EIRM-based enabling such robustness is the symmetric condition [10].
L34: method on average is more effective than the benchmarks. The Inspired by the symmetric condition, different symmetric
L35: code is available at https://github.com/mozhenling/doge-eirm. robust risk functions were studied, such as the mean absolute
```

```text
L42: ing since the presence of noisy labels (NLs) and data relying solely on designing the robust risk function may not
L43: distribution shifts can greatly diminish the performance of sufficiently address the challenges imposed by DG. To realize
L44: many data-driven methods [1], [2]. Incorrect machine fault DG, one popular direction is to learn invariant features [13].
L45: labels are often introduced due to the similarity among fault The invariant features are informative about the labels and
L46: patterns [3], less experienced labelers [4], or improper data shared across domains, which can enable model generalization
```

```text
L47: management [5]. In addition, data distribution shifts are often beyond training domains [14]. A notable approach in learning
L48: induced by data collected under different machine operation invariant features is invariant risk minimization (IRM) [15].
L49: The key idea of IRM is penalizing a dummy classifier to
L50: Received 14 May 2024; revised 12 October 2024; accepted 13 January
L51: be simultaneously optimal on multiple training domains.
```

```text
L59: Technology Fund Project under Grant ITS/034/22MS, in part by Guangdong demand in-depth investigations.
L60: Provincial Basic and Applied Basic Research - Offshore Wind Power Joint
L61: First, how can IRM be extended to take both LN and
L62: Fund Project under Grant 2022A1515240066, in part by Guangdong Province
L63: Technological Project under Grant 2023A0505030014, and in part by InnoHK DG settings into account? Previous methods, such as IRM
```

```text
L69: (e-mail: zijzhang@cityu.edu.hk). tions. Thus, a new method for handling both LN and DG
L70: Qiang Miao is with the College of Electrical Engineering, Sichuan Univer-
L71: problems is imperative.
L72: sity, Chengdu, Sichuan 610017, China.
L73: Kwok-Leung Tsui was with the Grado Department of Industrial and Systems Next, what is the design of a practical risk function
```

```text
L76: nosis applications? Frameworks for addressing LN and DG
L77: University of Texas at Arlington, Arlington, TX 76019 USA.
L78: Digital Object Identifier 10.1109/TNNLS.2025.3531214 problems individually have been presented [8], [9]. Among
L79: 2162-237X © 2025 IEEE. All rights reserved, including rights for text and data mining, and training of artificial intelligence
L80: and similar technologies. Personal use is permitted, but republication/redistribution requires IEEE permission.
```

```text
L84: ===== PAGE 2 =====
L86: MO et al.: EXTENDED IRM FOR MACHINE FAULT DIAGNOSIS WITH LABEL NOISE AND DATA SHIFT 15477
L87: reported frameworks for LN and DG problems, new develop- proposed EIRM, which, to the best of our knowledge,
L88: ments often happen in the risk function design. Discussions were not studied previously.
```

```text
L87: reported frameworks for LN and DG problems, new develop- proposed EIRM, which, to the best of our knowledge,
L88: ments often happen in the risk function design. Discussions were not studied previously.
L89: in risk functions for NL-DG problems in data-driven machine From the application aspect, they are given as follows.
L90: fault diagnosis are scarce and it is valuable to develop one for 1) To verify the advantage of EIRM, extensive NL-DG
L91: ease of use under such a real application. tasks are designed using gearbox and actuator fault
```

```text
L98: Thus, it is crucial to obtain insights from both theoretical and The remaining part of this work is organized as follows.
L99: experimental aspects for a method developed for machine fault Section II distinguishes our study from previous studies, spec-
L100: diagnosis considering NL-DG. ifies the problem setting concerned, and details the frequent
L101: To address the abovementioned questions, recent theoretical notations in this work. Section III begins with the formulations
L102: and empirical findings regarding LN robustness and DG in of IRM and elaborates on the derivations of EIRM and the
```

### Evidence snippets: architecture

```text
L3: ===== PAGE 1 =====
L5: 15476 IEEE TRANSACTIONS ON NEURAL NETWORKS AND LEARNING SYSTEMS, VOL. 36, NO. 8, AUGUST 2025
L6: Extended Invariant Risk Minimization for Machine
L7: Fault Diagnosis With Label Noise and Data Shift
```

```text
L20: realized by shifting the gradient penalty base from the dummy
L21: addressing LNs focused on LN robust learning [8] while
L22: classifier to the entire model. EIRM is shown to be closely related
L23: tackling data distribution shifts was regarded as one major
L24: to locating a flat minimum, which is crucial for label noise (LN)
```

```text
L47: management [5]. In addition, data distribution shifts are often beyond training domains [14]. A notable approach in learning
L48: induced by data collected under different machine operation invariant features is invariant risk minimization (IRM) [15].
L49: The key idea of IRM is penalizing a dummy classifier to
L50: Received 14 May 2024; revised 12 October 2024; accepted 13 January
L51: be simultaneously optimal on multiple training domains.
```

```text
L153: ===== PAGE 3 =====
L155: 15478 IEEE TRANSACTIONS ON NEURAL NETWORKS AND LEARNING SYSTEMS, VOL. 36, NO. 8, AUGUST 2025
L156: of the practical risk function includes an approximation to is that we not only leverage the power of flat minima but
L157: gradient penalty of the whole model, which was not considered also rely on invariant feature learning based on the framework
```

```text
L167: tigated [13], [14], [15], [30]. One representative work of invari- ness, the infinite iteration number, and the Polyak–Lojasiewicz
L168: ant feature learning is IRM, which elicits invariant features via condition [52], [53], [54], [55]. In particular, the conditions
L169: forcing the dummy classifier to be optimal on multiple training required for analyzing global convergence are often stricter
L170: domains. The idea of IRM then generated a surge of follow-up than those for local convergence as shown in a bunch of past
L171: studies under different settings. For instance, the idea of studies on global convergence, such as [55], [56], and [57].
```

```text
L185: bridge learning invariance with flat minima optimization. Our cal aspect, well matches machine fault diagnosis tasks depicted
L186: study is then significantly different from the existing studies in the later section of case studies. This work considers a
L187: on IRM and its variants by filling these two gaps. general model f as a composition of a feature extractor g
L188: 3) Flat Minima: In training network models, converging to and a classifier/predictor h, i.e., f = h ◦g. The general model
L189: a “flat” minimum often enabled models to possess better gen- f is parametrized by θ ∈ Rd, which contains d independent
```

```text
L299: ===== PAGE 5 =====
L301: 15480 IEEE TRANSACTIONS ON NEURAL NETWORKS AND LEARNING SYSTEMS, VOL. 36, NO. 8, AUGUST 2025
L302: Note that θ′ = θ + γ ∇R(θ) is the steepest ascent. By plug- Algorithm 1 One Epoch of Gradient Update of EIRM
L303: ging it into (6), we obtain the following: 1. Begin the epoch
```

```text
L354: (11)
L355: from [59] and employed in this study. The 1-D LetNet is a
L356: Finally, the proposed EIRM is based on (10). To compute 1-D variant of the celebrated LetNet-5 network. Training the
L357: its gradient in (11), we only need to obtain Re(θ), compute fault diagnosis model is illustrated in Fig. 1.
L358: ∇Re(θ), update parameter θ′ = θ + γ ∇Re(θ) after a backup,
```

```text
L367: sis task, we leverage EIRM as the objective function and First, let us leave the domain variable e aside and consider
L368: apply the optimization process in Algorithm 1 to train a 1-D the setting of one domain. Then, we attempt to characterize
L369: convolutional neural network (1-D CNN) to classify faults. different levels of “smoothness” of the vanilla risk function
L370: The selection of 1-D CNN as the data-driven model is due R based on the Lipschitz continuity. The definitions based
L371: to its popularity in fault diagnosis applications [58], [59]. on Lipschitz continuity to capture function smoothness are
```

```text
L456: ===== PAGE 7 =====
L458: 15482 IEEE TRANSACTIONS ON NEURAL NETWORKS AND LEARNING SYSTEMS, VOL. 36, NO. 8, AUGUST 2025
L459: C. Convergence Based on the Extended Risk Function flat minima. To this end, the global convergence analysis is
L460: significant and valuable to understand the characteristics of
```

```text
L477: convergence and local convergence of the GD algorithm based exist some other conditions for enabling global convergence in
L478: on the gradient of the extended risk function. recent literature, such as special initializations [50] and special
L479: Theorem 1 (Global Convergence): If the extended risk neural network models [56]. However, these studies offered
L480: function R ˜ has the global optimal value R ˜ (θ∗) and satisfies the little knowledge on linking global convergence with seeking
L481: Polyak–Lojasiewicz condition with the finite positive constant flat minima. In addition to the global convergence analysis, the
```

```text
L612: ===== PAGE 9 =====
L614: 15484 IEEE TRANSACTIONS ON NEURAL NETWORKS AND LEARNING SYSTEMS, VOL. 36, NO. 8, AUGUST 2025
L615: TABLE I
L616: FAULT CLASSIFICATION RESULTS BASED ON THE ACTUATOR AND GEARBOX DATASETS WITH SYMMETRIC LNS
```

### Evidence snippets: experiment_defense

```text
L23: tackling data distribution shifts was regarded as one major
L24: to locating a flat minimum, which is crucial for label noise (LN)
L25: robustness and model generalization. Explorations on function task in domain generalization (DG) [9]. A significant focus
L26: smoothness and algorithm convergence are offered to understand of recent studies in LN robust learning is designing robust
L27: EIRM from the theoretical aspect. An efficient implementation risk functions [8]. The designed function is considered robust
```

```text
L31: some portions of labels are corrupted [10]. One technique
L32: strong benchmarks on multiple NL-DG tasks using actuator and
L33: gearbox fault datasets. Results indicate that the EIRM-based enabling such robustness is the symmetric condition [10].
L34: method on average is more effective than the benchmarks. The Inspired by the symmetric condition, different symmetric
L35: code is available at https://github.com/mozhenling/doge-eirm. robust risk functions were studied, such as the mean absolute
```

```text
L56: NL-DG problems, especially serving machine fault diagnosis
L57: Fund Project under Grant 11213124, in part by Collaborative Research Fund
L58: Project under Grant C1049-24GF, in part by Hong Kong ITC Innovation and tasks, remains unexplored and several critical questions
L59: Technology Fund Project under Grant ITS/034/22MS, in part by Guangdong demand in-depth investigations.
L60: Provincial Basic and Applied Basic Research - Offshore Wind Power Joint
```

```text
L89: in risk functions for NL-DG problems in data-driven machine From the application aspect, they are given as follows.
L90: fault diagnosis are scarce and it is valuable to develop one for 1) To verify the advantage of EIRM, extensive NL-DG
L91: ease of use under such a real application. tasks are designed using gearbox and actuator fault
L92: Moreover, what is theoretical and experimental evidence datasets. EIRM is then compared with 15 strong bench-
L93: supporting the developed methodology for machine fault diag- marks on designed tasks. Based on average classification
```

```text
L95: the understanding of the developed method. Meanwhile, benchmark methods. Quantitatively, EIRM also achieves
L96: experimental results of benchmarking with the state-of-the-art an improvement of more than 4% compared to the
L97: methods can validate the effectiveness of the proposed method. majority of the benchmark methods.
L98: Thus, it is crucial to obtain insights from both theoretical and The remaining part of this work is organized as follows.
L99: experimental aspects for a method developed for machine fault Section II distinguishes our study from previous studies, spec-
```

```text
L104: as follows. One recent theoretical finding presented that under retical insights of EIRM via studying the function smoothness
L105: the correct label dominant condition, the correct label-based and convergence properties. Section V presents experimental
L106: loss was smaller than the incorrect label-based loss [16]. Such studies based on actuator and gear datasets. Section VI offers
L107: a finding implied that the incorrect label could lead to a the conclusion.
L108: perturbation of the loss. Thus, finding flat minima during
```

```text
L183: on labels were ignored. Second, rare attempts were made B. Problem Description
L184: by IRM-related studies to methodologically and theoretically We first start with a general problem, which, from the practi-
L185: bridge learning invariance with flat minima optimization. Our cal aspect, well matches machine fault diagnosis tasks depicted
L186: study is then significantly different from the existing studies in the later section of case studies. This work considers a
L187: on IRM and its variants by filling these two gaps. general model f as a composition of a feature extractor g
```

```text
L264: The element of θ is indexed by the subscript. For efficient since it requires the computation of the Hessian
L265: instance, the ith element is presented as θ i . matrix. One simple solution is to sacrifice a certain level of
L266: 3) ∇R(θ) is the gradient of R with respect to θ, while computational accuracy for a higher efficiency.
L267: the Hessian is ∇2R(θ). For simplicity, the gradient and For convenience, let us ignore the domain variable e and
L268: the Hessian can be further denoted as ∇R and ∇2R, consider the approximation on one domain. Then, let us
```

```text
L283: 7) λ, γ , and µ are positive finite scalars. to the question is the steepest direction under a constraint
L284: ∥v∥ ≤ ρ and ρ ∈ R. To proceed further, let us consider the
L285: Cauchy–Schwarz inequality as follows:
L286: III. METHODOLOGY
L287: In this section, the formulation of IRM is first briefed. Next, (cid:13) (cid:13)∇R(θ)T v (cid:13) (cid:13) ≤ ∥∇R(θ)∥∥v∥ (5)
```

```text
L287: In this section, the formulation of IRM is first briefed. Next, (cid:13) (cid:13)∇R(θ)T v (cid:13) (cid:13) ≤ ∥∇R(θ)∥∥v∥ (5)
L288: the step-by-step development of EIRM from IRM is elaborated
L289: and the EIRM for machine fault diagnosis tasks is presented. where the equality holds when v∗ = ξ∇R(θ) and ξ ∈ R. Note
L290: that ∥v∗∥ ≤ ρ ⇒ ξ = ρ(1/∥∇R(θ)∥), which implies that
L291: v∗ = ρ(∇R(θ)/∥∇R(θ)∥). Thus, the steepest direction is just
```

```text
L365: A. Smoothness of the Vanilla Risk Function
L366: In developing a data-driven model for the fault diagno-
L367: sis task, we leverage EIRM as the objective function and First, let us leave the domain variable e aside and consider
L368: apply the optimization process in Algorithm 1 to train a 1-D the setting of one domain. Then, we attempt to characterize
L369: convolutional neural network (1-D CNN) to classify faults. different levels of “smoothness” of the vanilla risk function
```

```text
L545: conditions outlined in Theorems 1 and 2, the current Fig. 2. Test rig of the linear electromechanical actuator.
L546: risk difference goes to zero as t approaches infinity. The
L547: we only introduce the essential information for task design.
L548: global and local convergences of the GD algorithm are
L549: The data were collected under three loading conditions, 20 kgf
```

### Evidence snippets: visualization

```text
L351: tr e∈D
L352: tr
L353: Fig. 1. Fault diagnosis model training based on EIRM and 1-D LeNet.
L354: (11)
L355: from [59] and employed in this study. The 1-D LetNet is a
```

```text
L543: 2) The coefficients of upper bounds in (25) and (28) range
L544: between zero and one. This indicates that under the
L545: conditions outlined in Theorems 1 and 2, the current Fig. 2. Test rig of the linear electromechanical actuator.
L546: risk difference goes to zero as t approaches infinity. The
L547: we only introduce the essential information for task design.
```

```text
L586: The compared methods encompass a variety of risk func- gearbox: normal condition (labeled as 0), missing tooth of sun
L587: tions, including the ERM based on the standard CE [21], gear (labeled as 1), and missing tooth of planet gear (labeled
L588: the SCE [11], the normalized CE (NCE) [12], the JSD as 2). The test rig is shown in Fig. 3. For complete information
L589: [20], the ANL [22], the generalized label smoothing (GLS) of the data collection, please refer to [32]. Next, we provide
L590: [24], the asymmetric unhinged loss (AUL) [23], and the pre- only the key information necessary to illustrate the task design.
```

```text
L600: A total of 15 methods, most proposed in recent years, serve as C. Experiment Implementation
L601: benchmarks. Each method is applied to train the 1-D LeNet In each fault classification task, we separately apply EIRM
L602: (Fig. 1) to classify faults in the experiments. and the benchmark methods to train the 1-D LeNet (shown in
L603: Fig. 1) based on two training domains and then test the trained
L604: B. Machine Fault Diagnosis Task model on one test domain.
```

```text
L626: 1) All models generally perform better on the gearbox
L627: dataset than the actuator dataset. This likely results from
L628: Fig. 3. Test rig of the gearbox. the complexity of the actuator’s two motion profiles,
L629: the trapezoidal and the sinusoidal, as detailed in [62],
L630: 20×, with each search averaged over three random seeds of which are more complex than the simple constant speed
```

### Closing evidence
- Jun. 2022, pp. 639–668.
- fault diagnosis, and health assessment.
- [55] Z. Charles and D. Papailiopoulos, “Stability and generalization of
- Dr. Miao has been a Senior Member of the IEEE Reliability Society
- learning algorithms that converge to global optima,” in Proc. 35th Int.
- since 2012. He served as an IEEE RS AdCom Member from 2019 to
- Conf. Mach. Learn., Jul. 2017, pp. 745–754.
- 2021 and the IEEE RS Vice President from 2020 to 2021. He is the
- [56] S. S. Du, J. D. Lee, H. Li, L. Wang, and X. Zhai, “Gradient descent Associate Editor-in-Chief of IEEE TRANSACTIONS ON INSTRUMENTATION
- finds global minima of deep neural networks,” in Proc. 36th Int. Conf. AND MEASUREMENT and an Associate Editor of IEEE TRANSACTIONS ON
- Mach. Learn., May 2019, pp. 1675–1685. RELIABILITY. He serves as an Editorial Board Member for Chinese Journal
- [57] A. J. Arnulf Jentzen and A. R. Adrian Riekert, “On the exis- of Aeronautics.
- tence of global minima and convergence analyses for gradient
- descent methods in the training of deep neural networks,” J. Mach.
- Learn., vol. 1, no. 2, pp. 141–246, Jan. 2022, doi: 10.4208/jml. Kwok-Leung Tsui received the Ph.D. degree
- 220114a. in statistics from the University of Wisconsin–
- [58] S. Li, T. Li, C. Sun, X. Chen, and R. Yan, “WPConvNet: An interpretable Madison, Madison, WI, USA, in 1986.
- wavelet packet kernel-constrained convolutional network for noise- He is currently a Professor with the Department of
- robust fault diagnosis,” IEEE Trans. Neural Netw. Learn. Syst., vol. Manufacturing, Systems, and Industrial Engineering,
- 35, no. 10, pp. 14974–14988, Oct. 2024, doi: 10.1109/TNNLS.2023. The University of Texas at Arlington, Arlington,
- 3282599. TX, USA. His current research interests include data
- [59] Z. Mo, Z. Zhang, and K.-L. Tsui, “The variational kernel-based science and data analytics, surveillance in healthcare
- 1-D convolutional neural network for machinery fault diagno- and public health, personalized health monitoring,
- sis,” IEEE Trans. Instrum. Meas., vol. 70, pp. 1–10, 2021, doi: prognostics and systems health management, cali-
- 10.1109/TIM.2021.3105252. bration and validation of computer models, process
- [60] T. Nguyen, K. Do, B. Duong, and T. Nguyen, “Domain generalization control and monitoring, and robust design and Taguchi methods.
- via risk distribution matching,” in Proc. IEEE/CVF Winter Conf. Appl. Dr. Tsui was elected as a Council Member of the International Statisti-
- Comput. Vis., Jan. 2024, pp. 2790–2799. cal Institute and U.S. Representative of the ISO Technical Committee on
- [61] M. Yang et al., “Invariant learning via probability of sufficient and Statistical Methods. He is a fellow of American Statistical Association,
- necessary causes,” in Proc. Adv. Neural Inf. Process. Syst., vol. 36, American Society for Quality, the International Society of Engineering Asset
- Dec. 2023, pp. 79832–79857. Management, and Hong Kong Institution of Engineers. He was a recipient
- [62] C. Ruiz-Carcel and A. Starr, “Data-based detection and diagnosis of of the National Science Foundation Young Investigator Award. He was the
- faults in linear actuators,” IEEE Trans. Instrum. Meas., vol. 67, no. 9, Chair of the INFORMS Section on Quality, Statistics, and Reliability, and the
- pp. 2035–2047, Sep. 2018. Founding Chair of the INFORMS Section on Data Mining.
- Authorized licensed use limited to: University of Science & Technology of China. Downloaded on July 05,2026 at 10:04:47 UTC from IEEE Xplore. Restrictions apply.

## Learning_Motor_Cues_in_Brain-Muscle_Modulation
- Extracted chars: 65120

### Opening / abstract evidence
- ===== PAGE 1 =====
- 86 IEEE TRANSACTIONS ON CYBERNETICS, VOL. 55, NO. 1, JANUARY 2025
- Learning Motor Cues in Brain-Muscle Modulation
- Tian-Yu Xiang , Student Member, IEEE, Xiao-Hu Zhou , Member, IEEE, Xiao-Liang Xie , Member, IEEE,
- Shi-Qi Liu , Mei-Jiang Gui , Graduate Student Member, IEEE, Hao Li , Graduate Student Member, IEEE,
- De-Xing Huang , Graduate Student Member, IEEE, Xiu-Ling Liu , Member, IEEE,
- and Zeng-Guang Hou , Fellow, IEEE
- Abstract—Current studies for brain-muscle modulation often data-driven approach for the neuroscience community, offering
- analyze selected properties in electrophysiological signals, leading a comprehensive perspective of brain-muscular modulation.
- to a partial understanding. This article proposes a cross-
- Index Terms—Brain-muscle modulation, generative model,
- modal generative model that converts brain activities measured
- motor analysis.
- by electroencephalography (EEG) to corresponding muscular
- responses recorded by electromyography (EMG). Examining the
- generation process in the model highlights how the motor cue,
- representing implicit motor information hidden within brain I. INTRODUCTION
- activities, modulates the interaction between brain and muscle
- MUSCLE contractions are driven by motor cues that
- systems. The proposed model employs a two-stage generation
- process to bridge the semantic gap in cross-modal signals. represent implicit motor information of brain activities.
- Initially, the shared movement-related information between EEG These cues, originating from brain neurons, are transmitted via
- and EMG signals is extracted using a contrastive learning frame- motor nerves to activate muscle movements. Investigating the
- work. These shared representations act as conditional vectors
- neural pathways and motor cues is critical for understanding
- in the subsequent EMG generation stage based on generative
- brain-muscle modulation. These insights have wide-ranging
- adversarial networks (GANs). Experiments on a self-collected
- multimodal electrophysiological signal data set show the algo- implications, including the development of treatments for
- rithm’s superiority over existing time series generative methods neuromuscular disorders [1], [2], the enhancement of motor
- in cross-modal EMG generation. Further insights derived from learning protocols [3], and advancements in prosthetics and
- the model’s inference process underscore the brain’s strategy
- exoskeleton equipment [4]. To investigate the motor cues
- for muscle control during movements. This research provides a
- in brain-muscular modulation, it’s important to record the
- corresponding activities.
- Received 1 February 2024; revised 28 March 2024 and 16 May 2024; Electroencephalography (EEG) and electromyography
- accepted 31 May 2024. Date of publication 18 October 2024; date of
- (EMG), as noninvasive electrophysiological signals, are
- current version 20 December 2024. This work was supported in part by
- the National Key Research and Development Program of China under Grant well-suited for recording brain and muscle activities. EEG
- 2023YFC2415100; in part by the National Natural Science Foundation of records the electrical activities of neurons [5], offering
- China under Grant 62373351, Grant 62222316, Grant U20A20224, Grant
- insights into how the brain governs muscle systems [6], [7].
- 62303463, Grant 82327801, and Grant 62073325; in part by the Youth

### Section, table, and figure headings detected
- L99: A. Contrastive Learning for Electrophysiological Signals
- L144: 1) A data-driven analysis pipeline is proposed using a conditional latent variables to synthesize corresponding EMG
- L148: C. Brain-Muscle Modulation Analysis via
- L153: 2) A novel two-stage algorithm is introduced to synthesize
- L165: 3) Experimental results from the self-collected multimodal
- L176: III. METHOD
- L184: Fig. 1. Overview of the training process. The training process involves two stages: representation learning (left) and EMG generation (right).
- L185: TABLE I
- L189: Fig. 2. Inference process for generating EMG from EEG signals.
- L329: TABLE III Algorithm 2 Training Scheme for Generator
- L391: A. Data Collection
- L410: TABLE IV
- L412: Fig. 3. Data collection paradigm.
- L413: B. Training Detail
- L458: TABLE V
- L461: Fig. 4. Visualization of the synthetic EMG generated by different methods and real EMG after PCA. (a) T-force [19]. (b) P-force [20]. (c) RCGAN [22].
- L463: D. Experimental Results generator in synthesizing EMG signals with more pronounced
- L479: E. Ablation Study
- L504: TABLE VI
- L507: Fig. 5. Comparison between real EMG and synthetic EMG generated by different methods (x-axis: time (s) and y-axis: normalized amplitude). Root mean
- L521: V. BRAIN-MUSCULAR MODULATION ANALYSIS
- L530: Fig. 6. It can be found that the proposed algorithm achieves ther explored by examining the generation process from
- L538: Fig. 6. Comparison between real EMG and synthetic EMG generated by different methods in the spectral domain (x-axis: frequency (Hz) and y-axis:
- L593: Fig. 7. Visualization of I of different EMG channels for different movements by topographic maps: (a) Wrist rotation, (b) hand extension, and (c) elbow
- L595: TABLE VII
- L600: Fig. 8. Visualization of Pearson correlation coefficients of I between different
- L603: VI. DISCUSSION
- L604: A. Role of the Shared EEG-EMG Representations
- L688: VII. CONCLUSION

### Evidence snippets: math_formalization

```text
L208: A. Representation Learning (cid:2) (cid:3)
L209: zi = p ri (3)
L210: The primary objective of this stage is to derive shared B B (cid:2) B (cid:3)
L211: representations, which are parts of motor cues, from the zi = p ri (4)
L212: M M M
```

```text
L227: brain activities are measured by EEG, while the muscular choice is particularly pertinent in cross-modal representation
L228: movements are recorded via EMG. The backbone encoder learning, where EEG and corresponding EMG are treated
L229: in this research is a modified version of EEGNet [45], as a positive pair. The primary objective is to enhance the
L230: which retains only the feature extraction stage and omits similarity between the latent of these positive pairs, utilizing
L231: the classification head (shown in Table I). The adaptation the InfoNCE loss (l ) function
```

```text
L251: 5: z B = p B (f B (X B )).
L252: 6: z M = p M (f M (X M )).
L253: 7: Calculate loss L c by (5)-(7).
L254: 8: Update parameters of f B/M and p B/M with adamW
L255: algorithm based on L .
```

```text
L269: the l norm of the vector. The contrastive representation ditional dependencies. This strategy enables simultaneous
L270: 2
L271: learning’s overall loss function is computed as the average of consideration of various temporal scales, essential for captur-
L272: the cross InfoNCE loss over the samples in a batch ing both long-term and short-term dependencies in EMG.
L273: ⎛ ⎞
```

```text
L278: j=1
L279: smoothness of the generated EMG signals.
L280: where N is the batch size. This loss function aims to enhance The final substep, labeled g , integrates multiscale distri-
L281: 4
L282: the similarity between muscular movements and corresponding butions with 1 × 1 convolutions. This stage completes the
```

```text
L307: The first substep (g ) is a two-layer multilayer perception. The discriminator’s training is inspired by the idea of
L308: 1
L309: Wasserstein GANs (WGANs) with gradient penalty, as
L310: This step facilitates a nonlinear transformation, mapping the
L311: detailed in [42] and [48]. WGAN, characterized by its con-
```

```text
L320: function within the 1-Lipschitz space. To satisfy this require-
L321: estimation. This relationship is mathematically represented as
L322: (cid:8) (cid:9) ment, a gradient penalty is applied to ensure the L2 norm of the
L323: r2(t) ∼ P r2(t) | r1(t − l/2),r1(t − l/2 + 1),...,r1(t + l/2 − 1) (10) discriminator’s gradients remains close to unity. The associated
L324: Authorized licensed use limited to: University of Science & Technology of China. Downloaded on July 05,2026 at 10:00:54 UTC from IEEE Xplore. Restrictions apply.
```

```text
L343: 8: while k < K and L D > t do
L344: 9: Calculate L D using (11) and (12).
L345: loss function is formulated as 10: Update parameters of D based on L D and k+=1.
L346: (cid:18) (cid:8) (cid:9)(cid:19)
L347: L = E[D(X )] − E D X ˆ + λgp (11) 11: end while
```

```text
L359: ˆ threshold t. The training of the discriminator is halted either
L360: where X are samples drawn from the distribution of the real
L361: EMG signals (X ) and the generated EMG signals (X ˆ ), and when its loss function falls below this threshold or when
L362: ∇ represents the M gradients of D of the input data. M it reaches the specified maximum update limit (K). Such a
L363: strategy ensures a balanced interplay between the discriminator
```

```text
L367: training process.
L368: synthesized EMG accurately reflects the movement patterns.
L369: The classification loss (L ) is computed using the cross-
L370: clf
L371: entropy loss function C. Inference Process
```

```text
L379: classifier’s prediction, and m represents the movement types.
L380: The generator’s primary responsibility is to synthesize EMG X ˆ M = G ◦ f B (X B ). (15)
L381: signals from EEG representations. The loss function for the
L382: The procedure begins by extracting movement-related rep-
L383: generator, L , is formulated as
```

```text
L386: L = L X , X ˆ + E D X ˆ + L (14) used to synthesize the corresponding EMG signals.
L387: G r M M M clf
L388: where the first term (L ) signifies the reconstruction loss based
L389: r IV. EXPERIMENTS
L390: on the mean square error, serving as a metric to evaluate the
```

### Evidence snippets: architecture

```text
L29: in the subsequent EMG generation stage based on generative
L30: brain-muscle modulation. These insights have wide-ranging
L31: adversarial networks (GANs). Experiments on a self-collected
L32: multimodal electrophysiological signal data set show the algo- implications, including the development of treatments for
L33: rithm’s superiority over existing time series generative methods neuromuscular disorders [1], [2], the enhancement of motor
```

```text
L78: China, and also with the Joint Laboratory of Intelligence Science and
L79: Technology, Institute of Systems Engineering, Macau University of Science series generation: 1) autoregressive models [18], [19], [20]
L80: and Technology, Taipa, Macau, China (e-mail: zengguang.hou@ia.ac.cn). and 2) generative adversarial networks (GANs) [21], [22].
L81: Color versions of one or more figures in this article are available at
L82: Autoregressive models treat the generation process as a series
```

```text
L92: from prior to current states. On the other hand, GAN aims method for analyzing brain-muscle modulation are delineated
L93: to directly learn the distributions that govern entire sequences in Section V. Section VI carries out a discussion on the role
L94: by two adversarially trained neural networks. Despite the of shared EEG-EMG representations and future works. This
L95: inherent challenges in capturing entire distributions, GAN has article culminates with conclusions in Section VII.
L96: become increasingly popular in time-series generation. This is
```

```text
L128: related information embedded in brain activities, in
L129: brain-muscle modulation by synthesizing muscular movements
L130: measured by EMG based on corresponding EEG. The B. Generative Adversarial Network for Electrophysiological
L131: synthesis process is divided into two phases: 1) extracting Signals
L132: shared representations from EEG and EMG signals; 2) GAN [39] models the underlying distributions of datasets
```

```text
L184: Fig. 1. Overview of the training process. The training process involves two stages: representation learning (left) and EMG generation (right).
L185: TABLE I
L186: DESIGN OF EEG/EMG ENCODER AND PROJECTOR STRUCTURE.
L187: THE DIFFERENCE CONFIGURATION BETWEEN EEG AND EMG ARE
L188: WRITTEN IN EEG/EMG
```

```text
L197: training in two stages, as illustrated in Fig. 1. This two-stage
L198: approach is designed to condition the GAN with high-quality
L199: representations, which bolsters the stability of the generator’s
L200: training phase and the fidelity of its output. The inference
L201: process, delineated in Fig. 2, is straightforward. The EEG
```

```text
L203: signals serve as the sole inputs and are subsequently processed
L204: linear projector, inspired by SimCLR [32], is applied to
L205: through an encoder and generator to the EMG signals.
L206: enhance the representation quality. This projector transforms
L207: the representations into a latent space, defined as
```

```text
L213: brain and muscular activities based on the contrastive learning
L214: where zi denotes the latent for the ith brain/muscular signal.
L215: paradigm. To achieve this, an encoder is employed to extract B/M
L216: spatial–temporal representations from the electrophysiological The function p B/M implemented as a two-layer multilayer
L217: perceptron, serves as a projector for the signals to map the
```

```text
L222: M M M
L223: variation requires extracting unique characteristics inherent in
L224: where f B/M denotes the encoder for brain/muscular signals, brain and muscle activities within each trial. Consequently,
L225: Xi B/M represents the ith brain/muscular signal in a batch, and instance discrimination, commonly utilized in the contrastive
L226: ri B/M is the corresponding representation. In this study, the learning framework [32], is employed as the proxy task. This
```

```text
L226: ri B/M is the corresponding representation. In this study, the learning framework [32], is employed as the proxy task. This
L227: brain activities are measured by EEG, while the muscular choice is particularly pertinent in cross-modal representation
L228: movements are recorded via EMG. The backbone encoder learning, where EEG and corresponding EMG are treated
L229: in this research is a modified version of EEGNet [45], as a positive pair. The primary objective is to enhance the
L230: which retains only the feature extraction stage and omits similarity between the latent of these positive pairs, utilizing
```

```text
L241: XIANG et al.: LEARNING MOTOR CUES IN BRAIN-MUSCLE MODULATION 89
L242: Algorithm 1 Training Scheme for Representation Learning TABLE II
L243: DESIGN OF GENERATOR STRUCTURE
L244: Require: X , X , N, E (raw EEG/EMG signals, batch size,
L245: B M
```

```text
L274: The third substep, denoted as g , is designed as a 1-D
L275: (cid:15)N 3
L276: L = 1 ⎝ lj ⎠ (7) CNN to refine the generated distribution. This refinement is
L277: c N c essential for reducing high-frequency noise and enhancing the
L278: j=1
```

### Evidence snippets: experiment_defense

```text
L67: ited perspectives. This study proposes a novel approach by
L68: Xiu-Ling Liu is with the College of Electronic Information Engineering and
L69: the Hebei Key Laboratory of Digital Medical Engineering, Hebei University, using the generation of EMG from EEG as a proxy task,
L70: Baoding 071000, China. for considering multiple signal properties simultaneously. This
L71: Zeng-Guang Hou is with the State Key Laboratory of Multimodal Artificial
```

```text
L114: for machine learning algorithms and improving performance
L115: them into a shared space [33], [34], [35], [36], [37]. It has
L116: in downstream tasks. Most literature focuses on generating
L117: been predominantly applied across different subjects [33],
L118: single-modal signals, yet a significant challenge persists in
```

```text
L121: electrophysiological signals. This technique has also been
L122: signal modalities. Addressing this challenge requires repre-
L123: validated under cross-sessions [34] and datasets [36]. However,
L124: senting multimodal signals in a shared space before synthesis.
L125: its effectiveness in creating shared representations for cross-
```

```text
L130: measured by EMG based on corresponding EEG. The B. Generative Adversarial Network for Electrophysiological
L131: synthesis process is divided into two phases: 1) extracting Signals
L132: shared representations from EEG and EMG signals; 2) GAN [39] models the underlying distributions of datasets
L133: synthesizing EMG signals based on the derived EEG to synthesize data. GAN aims to train a generator that can
L134: representations. In the first phase, a contrastive learning effectively deceive the discriminator. This structure has been
```

```text
L165: 3) Experimental results from the self-collected multimodal
L166: temporal domains [14], [15]. However, these methods often
L167: electrophysiological signal datasets demonstrate that the
L168: depend on select signal properties, which may not fully capture
L169: proposed algorithm can generate EMG signals from
```

```text
L224: where f B/M denotes the encoder for brain/muscular signals, brain and muscle activities within each trial. Consequently,
L225: Xi B/M represents the ith brain/muscular signal in a batch, and instance discrimination, commonly utilized in the contrastive
L226: ri B/M is the corresponding representation. In this study, the learning framework [32], is employed as the proxy task. This
L227: brain activities are measured by EEG, while the muscular choice is particularly pertinent in cross-modal representation
L228: movements are recorded via EMG. The backbone encoder learning, where EEG and corresponding EMG are treated
```

```text
L301: and g denote the substeps of the composite function G.
L302: 4
L303: layer contains one unit for binary tasks and four units for
L304: The detailed configuration of G is illustrated in Table II.
L305: The output of each g is denoted as rj for j = 1, 2, 3. multiclass tasks.
```

```text
L303: layer contains one unit for binary tasks and four units for
L304: The detailed configuration of G is illustrated in Table II.
L305: The output of each g is denoted as rj for j = 1, 2, 3. multiclass tasks.
L306: j
L307: The first substep (g ) is a two-layer multilayer perception. The discriminator’s training is inspired by the idea of
```

```text
L391: A. Data Collection
L392: fidelity between the synthesized and original EMG signals.
L393: The second term encapsulates the adversarial training process The dataset is collected in our previous work [17], com-
L394: between the generator and the discriminator, indicating the prising 4000 multimodal electrophysiological signals from
L395: generator’s attempts to deceive the discriminator. The third 10 participants. The collection process is shown in Fig. 3. EEG
```

```text
L400: more frequently in each iteration, adhering to the strategy The experimental protocol included four motors executed
L401: recommended in [42]. An early termination mechanism is by the right hand/arm: 1) wrist rotation; 2) hand extension;
L402: incorporated to prevent the discriminator from becoming 3) elbow flexion; and 4) rest. These tasks were chosen due to
L403: overly proficient or weak which may lead to the collapse of their distinct motor patterns and relevance to daily activities.
L404: the generator. This mechanism is designed by a predefined Each participant executed each task around 100 times.
```

```text
L420: the remaining 80% used for training. The model was distinctly optimizer is employed during the representation learning
L421: constructed for each EMG channel in the training phase. This stage to counteract potential overfitting issues in smaller-scale
L422: decision was driven by the inherent variability in muscle datasets [51]. The Adam optimizer is utilized in the EMG
L423: activities across different channels for identical movements. generation stage [52], following the approach recommended
L424: Opting for a multichannel approach in such a scenario could by Gulrajani et al. [48]. The detailed hyperparameters can be
```

```text
L447: to emphasize the signal components within the low- and ing maximum mean discrepancy (MMD) and dynamic time
L448: middle-frequency ranges. This procedure aims to retain critical warping (DTW). MMD measures the distributional distance
L449: motor information while facilitating model training stabiliza- between datasets using a kernel function. DTW aligns two
L450: tion by removing high-frequency noise. Before the training sequences through time stretching or compression, and then
L451: phase, both EEG and EMG signals undergo normalization to quantifies their similarity using Euclidean distance to measure
```

### Evidence snippets: visualization

```text
L107: tive and negative pairs to create a representation space where
L108: the challenges of limited scale and low-signal-to-noise ratios
L109: similar pairs cluster together and dissimilar ones are apart.
L110: inherent in bio-signals. GAN generates high-quality synthetic
L111: In electrophysiological signal analysis, contrastive learning
```

```text
L183: 88 IEEE TRANSACTIONS ON CYBERNETICS, VOL. 55, NO. 1, JANUARY 2025
L184: Fig. 1. Overview of the training process. The training process involves two stages: representation learning (left) and EMG generation (right).
L185: TABLE I
L186: DESIGN OF EEG/EMG ENCODER AND PROJECTOR STRUCTURE.
```

```text
L187: THE DIFFERENCE CONFIGURATION BETWEEN EEG AND EMG ARE
L188: WRITTEN IN EEG/EMG
L189: Fig. 2. Inference process for generating EMG from EEG signals.
L190: by EEG. Two stages are involved in the proposed pipeline:
L191: 1) representation learning and 2) EMG generation. The model
```

```text
L195: are designed to generate EMG, leveraging the representations
L196: derived earlier as conditional vectors. The pipeline undergoes
L197: training in two stages, as illustrated in Fig. 1. This two-stage
L198: approach is designed to condition the GAN with high-quality
L199: representations, which bolsters the stability of the generator’s
```

```text
L199: representations, which bolsters the stability of the generator’s
L200: training phase and the fidelity of its output. The inference
L201: process, delineated in Fig. 2, is straightforward. The EEG
L202: After acquiring the spatial–temporal representations, a non-
L203: signals serve as the sole inputs and are subsequently processed
```

```text
L373: While the training procedure is intricate, the inference
L374: L = − y log yˆ (13)
L375: clf c c process is more straightforward. As depicted in Fig. 2, only
L376: m
L377: the encoder for brain activities and the generator are utilized
```

```text
L393: The second term encapsulates the adversarial training process The dataset is collected in our previous work [17], com-
L394: between the generator and the discriminator, indicating the prising 4000 multimodal electrophysiological signals from
L395: generator’s attempts to deceive the discriminator. The third 10 participants. The collection process is shown in Fig. 3. EEG
L396: term plays a crucial role in incorporating movement-related data were measured by a 32-channel Emotiv Epoc Flex EEG
L397: information into the synthesized signals. head cap with a frequency of 128 Hz. Simultaneously, EMG
```

```text
L410: TABLE IV
L411: HYPERPARAMETER OF THE PROPOSED PIPELINE
L412: Fig. 3. Data collection paradigm.
L413: B. Training Detail
L414: 1) Experimental Setup: A 5-s time window of EEG and
```

```text
L459: COMPARISON BETWEEN THE PROPOSED METHOD AND OTHER METHODS IN EMG GENERATION. ↑: HIGHER IS BETTER AND ↓: LOWER IS BETTER
L460: (a) (b) (c) (d) (e)
L461: Fig. 4. Visualization of the synthetic EMG generated by different methods and real EMG after PCA. (a) T-force [19]. (b) P-force [20]. (c) RCGAN [22].
L462: (d) TimeGAN [21]. (e) Ours.
L463: D. Experimental Results generator in synthesizing EMG signals with more pronounced
```

```text
L488: based methods, focusing on learning the entire probability 3) the multiscale CNN within the generator.
L489: distribution, offer a more reliable solution. This is corroborated Quantitative results are shown in Table VI. The findings
L490: by Fig. 4, showing that plots (c)–(e), representing GAN-based indicate that integrating all components yields optimal EMG
L491: methods, produce a closer synthetic EMG signal distribution signal generation performance across various metrics and
L492: to the actual signals. experimental setups. Each component contributes uniquely
```

```text
L505: ABLATION STUDY ON EMG GENERATION TASK. W/O IS THE ABBREVIATION OF WITHOUT. ↑: HIGHER IS BETTER AND ↓: LOWER IS BETTER
L506: (a) (b) (c) (d) (e)
L507: Fig. 5. Comparison between real EMG and synthetic EMG generated by different methods (x-axis: time (s) and y-axis: normalized amplitude). Root mean
L508: square error (RMSR) between the synthesis EMG and the ground truth is displayed at the left top corner. (a) Real EMG. (b) W/o classifier. (c) W/o EMG.
L509: (d) W/o multi CNN. (e) Ours.
```

```text
L513: The multiscale CNN contributes to the overall performance algorithm closely align with the ground truth. This align-
L514: of the proposed model. This enhancement is particularly ment demonstrates that the EMG signals synthesized by the
L515: evident in Fig. 5, where the detailed features of the EMG proposed algorithm closely replicate the intensity profile of
L516: signal are refined by integrating the multiscale CNN into real EMG signals across the frequency spectrum.
L517: the generator. In essence, the collective integration of these
```

### Closing evidence
- From May 1997 to June 1999, he was
- Chinese Academy of Sciences.
- a Postdoctoral Research Fellow with the Key
- He is also with the University of Chinese
- Laboratory of Systems and Control, Institute of
- Academy of Sciences, Beijing. His research interests
- Systems Science, Chinese Academy of Sciences,
- include surgical robotics and tactile perception.
- Beijing. He was a Research Assistant with The Hong Kong Polytechnic
- University, Hong Kong, from May 2000 to January 2001. From July 1999 to
- May 2004, he was an Associate Professor with the Institute of Automation,
- Chinese Academy of Sciences, and has been a Full Professor since June 2004.
- From September 2003 to October 2004, he was a Visiting Professor with the
- Intelligent Systems Research Laboratory, College of Engineering, University
- of Saskatchewan, Saskatoon, SK, Canada. He is a Professor with the State
- Hao Li (Graduate Student Member, IEEE) received
- Key Laboratory of Multimodal Artificial Intelligence Systems, Institute of
- the B.E. degree in automation from Tsinghua
- Automation, Chinese Academy of Sciences. His research interests include
- University, Beijing, China, in 2020. He is currently
- neural networks, robotics, and intelligent systems.
- pursuing the Ph.D. degree in control theory and
- Prof. Hou was an Associate Editor of the IEEE Computational Intelligence
- control engineering with the Institute of Automation,
- Magazine and the IEEE Transactions on Neural Networks, and the Chair of
- Chinese Academy of Sciences, Beijing.
- Neural Network Technical Committee of Computational Intelligence Society.
- He is also with the University of Chinese
- He is currently the Vice-President of Asia Pacific Neural Network Society. He
- Academy of Sciences, Beijing. His research interests
- is an Associate Editor of the IEEE TRANSACTIONS ON CYBERNETICS and
- include surgical robotics and reinforcement learning.
- Control Theory and Applications and an Editorial Board Member of Neural
- Networks.
- Authorized licensed use limited to: University of Science & Technology of China. Downloaded on July 05,2026 at 10:00:54 UTC from IEEE Xplore. Restrictions apply.

## Multisource_Domain_Separation_Network_for_Industrial_Intelligent_Monitoring_in_Unseen_Conditi
- Extracted chars: 52844

### Opening / abstract evidence
- ===== PAGE 1 =====
- This article has been accepted for inclusion in a future issue of this journal. Content is final as presented, with the exception of pagination.
- IEEE TRANSACTIONS ON CYBERNETICS 1
- Multisource Domain Separation Network for
- Industrial Intelligent Monitoring in
- Unseen Conditions
- Zidi Jia , Member, IEEE, Lei Ren , Senior Member, IEEE, Zuo-Jun Max Shen, Member, IEEE,
- and Laurence T. Yang , Fellow, IEEE
- Abstract—Industrial time-series prediction is one of the crucial time-series prediction, multisource domain separation network
- tasks of industrial artificial intelligence, which has been exten- (MS-DSN), supervised contrastive similarity.
- sively adopted in intelligent monitoring. However, continuous
- variations in the working conditions of industrial processes
- I. INTRODUCTION
- lead to continuous changing in monitoring data, resulting in
- distribution shift. Industrial time-series prediction models may RECENTLY, the advancements in artificial intelligence
- not be able to maintain satisfactory accuracy. Domain general- technology have made data-driven methods popular in
- ization (DG) methods can effectively improve the robustness and
- Industrial Internet of Things (IIoT) [1]. These methods only
- generalization of the models for unseen or dynamic distribution
- need to obtain information from monitoring data and can
- data. However, existing methods have drawbacks limit their
- applicability in practice. First, most DG methods are designed realize better performance, thus they have been extensively
- for classification tasks and lack a general framework for regres- studied [2]. The widespread application of advanced artificial
- sion tasks. Second, extracting domain-invariance may obscure intelligence technology has led to significant breakthroughs
- task-relevant information, thereby degrading the prediction pre-
- in many area of industrial manufacturing, such as predictive
- cision. Third, DG methods are generally sensitive to extremely
- maintenance [3], product life-cycle management [4], and smart
- distributed data, potentially compromising the robustness. To
- address these issues, a multisource domain separation network grids [5]. Industrial time-series prediction is a critical com-
- (MS-DSN) is proposed. First, by constructing a DSN to separate ponent of these issues [6], and holds great importance for
- the features into domain-private and -shared spaces, domain- ensuring safe, stable, and efficient industrial production [7].
- specific information can be filtered while domain-invariant
- Deep learning models are commonly employed to analysis
- features are preserved. Second, a supervised contrastive loss is
- industrial time-series [8]. While these methods generally per-
- defined to preserve the domain invariant information related to
- the label changing tendency in the domain-shared space. Finally, form well in controlled experimental settings, the presence
- a directional risk extrapolation (DREx) method is proposed to of numerous uncertainties in complex industrial environments
- represents the extreme distributed data. Experiments on two hinders their widespread practical application.
- datasets, CMAPSS and N-CMAPSS, verify the effectiveness of
- Industrial process conditions in IIoT are increasingly com-
- our method.
- plex and varying. It may lead to variations in the distribution
- Index Terms—Directional risk extrapolation (DREx), domain of collected monitoring data, referred to as a distribution

### Section, table, and figure headings detected
- L16: I. INTRODUCTION
- L117: A. Industrial Time-Series Prediction
- L157: Fig. 1. Overall framework of MS-DSN. Autoencoders are used for representation learning in private space and shared space, respectively.
- L183: III. METHODOLOGY
- L185: A. Multisource DSN
- L211: Fig. 2. Topology of the neural network structure of MS-DSN. tures HP and HS , domain-private features could be removed
- L248: Fig. 1 shows the framework of the proposed MS-DSN and compute the reconstruct loss L reconstruct by Eq.(5)
- L272: B. Supervised Contrastive Similarity
- L282: Fig. 3. Structure of the module for each domain.
- L379: TABLE I
- L390: TABLE II
- L427: A. Monitoring Data of Aircraft Turbofan Engines
- L441: TABLE III the form of
- L455: C. Baseline Models
- L456: TABLE IV This part provides a brief introduction to the baseline mod-
- L476: B. Experimental Setting
- L485: D. Experimental Results
- L522: Fig. 5. Visualization of the RUL prediction results of FD004 test engine #248 by each method in case 1. The shaded region indicates the error margin
- L524: TABLE V
- L547: TABLE VI
- L549: Fig. 7. Visualization of the domain shared representation of MS-DSN and
- L556: Fig. 6. Case 1 visualization of domain-shared features and domain-private
- L567: Fig. 6 shows the t-SNE visualization of domain-private three components are verified.
- L583: G. Sensitivity Analysis
- L592: F. Ablation Studies
- L602: TABLE VII
- L623: Fig. 8. Experimental results with different weights of individual loss for case [6] H. Jiang, S. Zhang, W. Yang, X. Peng, and W. Zhong, “Integration of

### Evidence snippets: math_formalization

```text
L34: (MS-DSN) is proposed. First, by constructing a DSN to separate ponent of these issues [6], and holds great importance for
L35: the features into domain-private and -shared spaces, domain- ensuring safe, stable, and efficient industrial production [7].
L36: specific information can be filtered while domain-invariant
L37: Deep learning models are commonly employed to analysis
L38: features are preserved. Second, a supervised contrastive loss is
```

```text
L53: Received 27 May 2025; revised 24 September 2025; accepted 29 September
L54: 2025. This work was supported in part by the National Key Research a challenge to the independent and identically distributed data
L55: and Development Program of China under Grant 2023YFB3308000 and in assumption required by most models. Conventional time-series
L56: part by the National Science Foundation of China (NSFC) under Project
L57: prediction methods may not be able to adapt to sudden changes
```

```text
L87: handle data uncertainty in DA even without access to source (MS-DSN) is proposed for solving the challenge of predicting
L88: data. Jia et al. [14] proposed a DA method based on contrastive industrial time-series in unseen scenarios. The primary contri-
L89: learning for domain-invariant prediction across domains, by butions can be outlined as.
L90: representing the relationship between feature distribution and 1) A model-agnostic DG structure for industrial time-series
L91: label changes. These methods eliminate the impact of domain prediction in varying and unseen condition, denoted as
```

```text
L114: network for mechanical fault diagnosis, guided by adversarial
L115: mutual information. Xia et al. [20] proposed a depth sensing II. RELATED WORKS
L116: adversarial DA method that uses perceptual loss to force the
L117: A. Industrial Time-Series Prediction
L118: target domain and source domain to have the same distribution,
```

```text
L121: still many issues that need to be addressed. time-series prediction is a core task in intelligent monitoring.
L122: First, to the best of our knowledge, most of the solutions to Time-series prediction methods based on deep learning are a
L123: distribution shift so far are aimed at classification problems. promising technology for extracting and analyzing spatiotem-
L124: Cross-domain methods for prediction and regression issues poral correlations between features in industrial time-series.
L125: have not yet received much attention, especially in industrial These methods can identify and analyze these correlations,
```

```text
L135: particularly when the target data is not accessible. Therefore, and low-value intensive, and is highly dynamic. Traditional
L136: studying general DG methods that can be applied to various methods struggle to effectively deal with the complexity and
L137: issues is also a thorny problem that needs to be solved urgently. dynamic characteristics of industrial time data. Therefore,
L138: Third, DG models may be sensitive to extreme distribution highly generalized, robust, and evolvable models are needed.
L139: changes, resulting in satisfactory robustness not always being
```

```text
L149: that vary with working conditions can be considered noise. prediction function f:X → Y within the hypothesis space
L150: Therefore, the method described in this article is based on the through empirical risk minimization (ERM) applied to the
L151: strategy of invariant risk minimization (IRM). training set D. However, when the training and test sets do not
L153: ===== PAGE 3 =====
```

```text
L156: JIA et al.: MULTISOURCE DSN FOR INDUSTRIAL INTELLIGENT MONITORING IN UNSEEN CONDITIONS 3
L157: Fig. 1. Overall framework of MS-DSN. Autoencoders are used for representation learning in private space and shared space, respectively.
L158: obey the assumption of independent and identical distributed, to standardize the alignment of features in different domains,
L159: ERM is less robust and difficult to generalize, despite its such as IRM [24]. Krueger et al. [25] advocate for feature
L160: high computational efficiency. Therefore, DG is proposed and invariance by minimizing the extrapolation risk among source
```

```text
L164: domains, Sk ∼ Pk , obeying different distributions Pk , the conditions may change very frequently, which can lead to
L165: XY XY
L166: objective of DG is to acquire a robust and generalizable predic- changes in the distribution of monitoring signals. Therefore,
L167: tion function f from S through minimizing the expected error DG methods are required to improve the robustness of the
L168: on any unseen target domain T , where the joint distribution monitoring model, with the IRM method being the most
```

```text
L170: XY XY
L171: Although there have been many related studies, most of
L172: f = arg min E L (f (x) , y) . (1)
L173: (x,y)∈T them are used for classification tasks (such as fault diagnosis),
L174: and only consider aligning the features of the overall source
```

```text
L182: Domain adversarial training stands as a widely employed
L183: III. METHODOLOGY
L184: technique for acquiring domain-invariant representations, with
L185: A. Multisource DSN
L186: the domain adversarial neural network [23] serving as the most
```

```text
L186: the domain adversarial neural network [23] serving as the most
L187: frequently utilized method in this context. Explicit alignment Inspired by domain-separated networks [26] for DA, this
L188: is a more direct approach, directly utilizing specific constraints article applies domain-private components and domain-shared
L190: ===== PAGE 4 =====
```

### Evidence snippets: architecture

```text
L5: This article has been accepted for inclusion in a future issue of this journal. Content is final as presented, with the exception of pagination.
L6: IEEE TRANSACTIONS ON CYBERNETICS 1
L7: Multisource Domain Separation Network for
L8: Industrial Intelligent Monitoring in
L9: Unseen Conditions
```

```text
L10: Zidi Jia , Member, IEEE, Lei Ren , Senior Member, IEEE, Zuo-Jun Max Shen, Member, IEEE,
L11: and Laurence T. Yang , Fellow, IEEE
L12: Abstract—Industrial time-series prediction is one of the crucial time-series prediction, multisource domain separation network
L13: tasks of industrial artificial intelligence, which has been exten- (MS-DSN), supervised contrastive similarity.
L14: sively adopted in intelligent monitoring. However, continuous
```

```text
L31: maintenance [3], product life-cycle management [4], and smart
L32: distributed data, potentially compromising the robustness. To
L33: address these issues, a multisource domain separation network grids [5]. Industrial time-series prediction is a critical com-
L34: (MS-DSN) is proposed. First, by constructing a DSN to separate ponent of these issues [6], and holds great importance for
L35: the features into domain-private and -shared spaces, domain- ensuring safe, stable, and efficient industrial production [7].
```

```text
L84: This article has been accepted for inclusion in a future issue of this journal. Content is final as presented, with the exception of pagination.
L85: 2 IEEE TRANSACTIONS ON CYBERNETICS
L86: networks based on fuzzy rules, utilizing fuzzy systems to In this article, a multisource domain separation network
L87: handle data uncertainty in DA even without access to source (MS-DSN) is proposed for solving the challenge of predicting
L88: data. Jia et al. [14] proposed a DA method based on contrastive industrial time-series in unseen scenarios. The primary contri-
```

```text
L112: For instance, Zhao and Shen [19] introduced a single-DG
L113: conclusion is drawn in Section V.
L114: network for mechanical fault diagnosis, guided by adversarial
L115: mutual information. Xia et al. [20] proposed a depth sensing II. RELATED WORKS
L116: adversarial DA method that uses perceptual loss to force the
```

```text
L123: distribution shift so far are aimed at classification problems. promising technology for extracting and analyzing spatiotem-
L124: Cross-domain methods for prediction and regression issues poral correlations between features in industrial time-series.
L125: have not yet received much attention, especially in industrial These methods can identify and analyze these correlations,
L126: scenarios. Many current studies on cross-domain learning providing a powerful means of understanding the complex
L127: methods rely on techniques such as pseudo-label [21] or dis- relationships between different features of temporal data [7].
```

```text
L155: This article has been accepted for inclusion in a future issue of this journal. Content is final as presented, with the exception of pagination.
L156: JIA et al.: MULTISOURCE DSN FOR INDUSTRIAL INTELLIGENT MONITORING IN UNSEEN CONDITIONS 3
L157: Fig. 1. Overall framework of MS-DSN. Autoencoders are used for representation learning in private space and shared space, respectively.
L158: obey the assumption of independent and identical distributed, to standardize the alignment of features in different domains,
L159: ERM is less robust and difficult to generalize, despite its such as IRM [24]. Krueger et al. [25] advocate for feature
```

```text
L184: technique for acquiring domain-invariant representations, with
L185: A. Multisource DSN
L186: the domain adversarial neural network [23] serving as the most
L187: frequently utilized method in this context. Explicit alignment Inspired by domain-separated networks [26] for DA, this
L188: is a more direct approach, directly utilizing specific constraints article applies domain-private components and domain-shared
```

```text
L192: This article has been accepted for inclusion in a future issue of this journal. Content is final as presented, with the exception of pagination.
L193: 4 IEEE TRANSACTIONS ON CYBERNETICS
L194: information as possible is extracted by the encoders. During
L195: model training, the data X (k = 1, . . . , K) of the kth source
L196: k
```

```text
L209: k
L210: the diversity between domain-private and -shared hidden fea-
L211: Fig. 2. Topology of the neural network structure of MS-DSN. tures HP and HS , domain-private features could be removed
L212: k k
L213: from HS and consistency could be maintained. Besides, the
```

```text
L222: introduces the concepts of domain-private and domain-shared minimizing risk extrapolation to reduce the sensitivity of the
L223: spaces. For each domain, these two spaces are conjugate to model to a wide range of extreme distribution changes. The
L224: each other and together they contain all the information in that trained domain shared encoder and shared predictor are models
L225: domain. The domain-private space is unique to each domain, with high generalization ability to data distribution shifts.
L226: while the domain-shared space is shared by all domains. Algorithm 1 shows the flow of the proposed MS-DSN.
```

```text
L229: is hypothesized that information relevant to the downstream
L230: monitoring task is contained within the domain-shared space. Input: Source data Dk = {X k,i , y k,i }n i= k 1 , k = 1, . . ., K,
L231: By identifying a shared subspace that is orthogonal to the pri- Initialized shared encoder ES ,
L232: vate subspace, the method can separate unique domain-specific Initialized private encoders EP, k = 1, . . ., K,
L233: k
```

### Evidence snippets: experiment_defense

```text
L11: and Laurence T. Yang , Fellow, IEEE
L12: Abstract—Industrial time-series prediction is one of the crucial time-series prediction, multisource domain separation network
L13: tasks of industrial artificial intelligence, which has been exten- (MS-DSN), supervised contrastive similarity.
L14: sively adopted in intelligent monitoring. However, continuous
L15: variations in the working conditions of industrial processes
```

```text
L17: lead to continuous changing in monitoring data, resulting in
L18: distribution shift. Industrial time-series prediction models may RECENTLY, the advancements in artificial intelligence
L19: not be able to maintain satisfactory accuracy. Domain general- technology have made data-driven methods popular in
L20: ization (DG) methods can effectively improve the robustness and
L21: Industrial Internet of Things (IIoT) [1]. These methods only
```

```text
L24: data. However, existing methods have drawbacks limit their
L25: applicability in practice. First, most DG methods are designed realize better performance, thus they have been extensively
L26: for classification tasks and lack a general framework for regres- studied [2]. The widespread application of advanced artificial
L27: sion tasks. Second, extracting domain-invariance may obscure intelligence technology has led to significant breakthroughs
L28: task-relevant information, thereby degrading the prediction pre-
```

```text
L42: a directional risk extrapolation (DREx) method is proposed to of numerous uncertainties in complex industrial environments
L43: represents the extreme distributed data. Experiments on two hinders their widespread practical application.
L44: datasets, CMAPSS and N-CMAPSS, verify the effectiveness of
L45: Industrial process conditions in IIoT are increasingly com-
L46: our method.
```

```text
L50: shift [9]. For instance, in a flexible manufacturing process,
L51: the operational state of production equipment continually
L52: fluctuates in response to varying manufacturing tasks. It poses
L53: Received 27 May 2025; revised 24 September 2025; accepted 29 September
L54: 2025. This work was supported in part by the National Key Research a challenge to the independent and identically distributed data
```

```text
L119: which is used for fault diagnosis of industrial robot bearings Since most of the data collected in industrial intelligent
L120: under different conditions. Despite recent progress, there are monitoring systems are sensor signals and control signals,
L121: still many issues that need to be addressed. time-series prediction is a core task in intelligent monitoring.
L122: First, to the best of our knowledge, most of the solutions to Time-series prediction methods based on deep learning are a
L123: distribution shift so far are aimed at classification problems. promising technology for extracting and analyzing spatiotem-
```

```text
L127: methods rely on techniques such as pseudo-label [21] or dis- relationships between different features of temporal data [7].
L128: tribution assumptions [22]. However, assessing the reliability As demand for flexibility in industrial tasks continues to
L129: of relevant metrics for these techniques in regression tasks can grow, manufacturing on mixed production lines involving mul-
L130: be challenging. Second, basic distribution alignment is likely tiple, constantly changing processes is becoming increasingly
L131: to obscure specific information related to downstream tasks. common. Consequently, the distribution of monitoring data
```

```text
L141: solve the problem of industrial time-series prediction under DG enables the model to maintain high robustness when
L142: varying and unseen working conditions. As the targets of processing more widely distributed data by learning invariant
L143: industrial monitoring tasks are typically fixed, these tasks knowledge across various domains. Let X represent the data
L144: can be considered invariant. This means that the distribution and Y denote its corresponding labels. A domain, denoted
L145: of features related to the predicted targets in the monitoring as D = {(x , y )}n , consists of data sampled from a joint
```

```text
L160: high computational efficiency. Therefore, DG is proposed and invariance by minimizing the extrapolation risk among source
L161: applied. domains, effectively diminishing the variance of the source
L162: Given a training set S = {Sk}K containing K source domain risk. In industrial intelligent monitoring tasks, working
L163: k=1
L164: domains, Sk ∼ Pk , obeying different distributions Pk , the conditions may change very frequently, which can lead to
```

```text
L171: Although there have been many related studies, most of
L172: f = arg min E L (f (x) , y) . (1)
L173: (x,y)∈T them are used for classification tasks (such as fault diagnosis),
L174: and only consider aligning the features of the overall source
L175: Numerous DG methods have been proposed, broadly
```

```text
L228: Algorithm 1 Algorithm of Training MS-DSN
L229: is hypothesized that information relevant to the downstream
L230: monitoring task is contained within the domain-shared space. Input: Source data Dk = {X k,i , y k,i }n i= k 1 , k = 1, . . ., K,
L231: By identifying a shared subspace that is orthogonal to the pri- Initialized shared encoder ES ,
L232: vate subspace, the method can separate unique domain-specific Initialized private encoders EP, k = 1, . . ., K,
```

```text
L234: information and generate more meaningful representations for Initialized private decoders DP, k = 1, . . ., K,
L235: k
L236: downstream tasks. In this case, modeling of the downstream Initialized predictor P.
L237: tasks can be performed in the domain-shared space to achieve Output: Trained shared encoder ES ,
L238: high generalization. Trained predictor P.
```

### Evidence snippets: visualization

```text
L88: data. Jia et al. [14] proposed a DA method based on contrastive industrial time-series in unseen scenarios. The primary contri-
L89: learning for domain-invariant prediction across domains, by butions can be outlined as.
L90: representing the relationship between feature distribution and 1) A model-agnostic DG structure for industrial time-series
L91: label changes. These methods eliminate the impact of domain prediction in varying and unseen condition, denoted as
L92: shift by discovering domain-invariant knowledge between MS-DSN, is put forth in this proposal. In MS-DSN,
```

```text
L155: This article has been accepted for inclusion in a future issue of this journal. Content is final as presented, with the exception of pagination.
L156: JIA et al.: MULTISOURCE DSN FOR INDUSTRIAL INTELLIGENT MONITORING IN UNSEEN CONDITIONS 3
L157: Fig. 1. Overall framework of MS-DSN. Autoencoders are used for representation learning in private space and shared space, respectively.
L158: obey the assumption of independent and identical distributed, to standardize the alignment of features in different domains,
L159: ERM is less robust and difficult to generalize, despite its such as IRM [24]. Krueger et al. [25] advocate for feature
```

```text
L209: k
L210: the diversity between domain-private and -shared hidden fea-
L211: Fig. 2. Topology of the neural network structure of MS-DSN. tures HP and HS , domain-private features could be removed
L212: k k
L213: from HS and consistency could be maintained. Besides, the
```

```text
L246: of domain-IRM, it is not applicable to heterogeneous DG L task by Eq.(12)
L247: tasks. 6: Reconstruct X k : Xˆ k = D k P(concat(hS k , h k P)), k = 1, . . ., K,
L248: Fig. 1 shows the framework of the proposed MS-DSN and compute the reconstruct loss L reconstruct by Eq.(5)
L249: method. We believe that MS-DSN is applicable to a variety of 7: Compute the loss of diversities L diversity of h k P and hS k ,
L250: DG tasks. Without losing generalization, we choose regres- k = 1, . . ., K, by Eq.(4)
```

```text
L251: sion task as downstream task. Assume there are K source 8: Compute the loss of similarity L similarity of {hS k }, k =
L252: domains, S 1, . . . , S K. The topology of the neural network 1, . . ., K, by Eq.(7)
L253: structure of MS-DSN is shown in Fig. 2. The model consists 9: Update ES with L ES = L diversity + L similarity + L task +
L254: of a encoder layer and a decoder layer, with 1 domain L recontrust
L255: shared encoder, 1 domain shared predictor, K domain private 10: Update E k P, k = 1, . . ., K with L EP = L diversity +
```

```text
L280: information (just like domain adversarial neural network) may
L281: lead to losing valuable information. Besides, these methods
L282: Fig. 3. Structure of the module for each domain.
L283: are effective in classification tasks, especially the alignment of
L284: data distribution boundaries has significant benefits for the DG
```

```text
L328: predictor. The module corresponding to the kth domain is
L329: unnecessary computation, batch normalization is performed
L330: shown in Fig. 3. To induce the model to produce such a split
L331: on hS before L ’s computing. The loss function can be
L332: representation, we define diversity loss, L , to encourage similarity
```

```text
L374: particular, in our approach, both measures of DSN structure
L375: and similarity loss reduce the information contained in the
L376: extracted features, which may cause domain-specific informa- Fig. 4. Simplified diagram of the aircraft turbofan engine.
L377: tion for many downstream tasks to be filtered as well. At the
L378: same time, such prediction risk only considers the scale of the
```

```text
L427: A. Monitoring Data of Aircraft Turbofan Engines
L428: datasets DS01-DS07 were chosen. Each sub-dataset represents
L429: As shown in Fig. 4, aero-engines monitoring data are used different working conditions, leading to variations in the
L430: in the experiment for RUL prediction. This dataset contains distribution of collected data. The specific selection of training
L431: run-to-failure data of aero-engines. The RUL of an engine is and test sets is detailed in Table III. This task poses a more
```

```text
L506: (RMSE) and score metric. RMSE is defined as
L507: The results of the comparative experiments on CMAPSS are
L508: v shown in Table V and Fig. 5. It can be found that the perfor-
L509: u n
L510: RMSE = u t 1 n X (cid:0) yˆ j − y j (cid:1)2 . (13) mance of the proposed MS-DSN is better than all competing
```

```text
L520: This article has been accepted for inclusion in a future issue of this journal. Content is final as presented, with the exception of pagination.
L521: 8 IEEE TRANSACTIONS ON CYBERNETICS
L522: Fig. 5. Visualization of the RUL prediction results of FD004 test engine #248 by each method in case 1. The shaded region indicates the error margin
L523: between the prediction and the actual RUL values. (a) DANN. (b) CORAL. (c) Mixup. (d) VREx. (e) RSC. (f) MS-DSN.
L524: TABLE V
```

```text
L547: TABLE VI
L548: PERFORMANCE COMPARISONS AMONG MS-DSN AND SEVERAL STATE-OF-THE-ART METHODS ON N-CMAPSS
L549: Fig. 7. Visualization of the domain shared representation of MS-DSN and
L550: the latent representation of DANN encoder. (a) MS-DSN. (b) DANN.
L551: SCS,” “w/o DREx,” and “DANN1,” respectively. In particular,
```

### Closing evidence
- ment, data-driven optimization algorithms and applications, energy systems,
- CMAPSS dataset for prognostics,” in Proc. IEEE Int. Conf. Ind. Eng.
- and transportation system planning and optimization.
- Eng. Manage. (IEEM), Dec. 2021, pp. 1114–1121.
- [31] B. Sun and K. Saenko, “Deep coral: Correlation alignment for deep
- domain adaptation,” in Proc. Comput. Vis. Workshops (ECCV). Amster-
- dam, The Netherlands: Springer, Oct. 2016, pp. 443–450.
- [32] H. Zhang, M. Cisse, Y. N. Dauphin, and D. Lopez-Paz, “Mixup: Beyond
- empirical risk minimization,” in Proc. Int. Conf. Learn. Represent., 2018,
- pp. 1–13.
- [33] Z. Huang, H. Wang, E. P. Xing, and D. Huang, “Self-challenging
- improves cross-domain generalization,” in Proc. 16th Eur. Conf. Com-
- put. Vision (ECCV). Glasgow, U.K.: Springer, Aug. 2020, pp. 124–140.
- Laurence T. Yang (Fellow, IEEE) received the
- B.E. degree in computer science and technology
- from Tsinghua University, Beijing, China, in 1992,
- Zidi Jia (Member, IEEE) received the Ph.D. degree
- and the Ph.D. degree in computer science from
- in pattern recognition and intelligent systems from
- the University of Victoria, Victoria, BC, Canada, in
- the School of Automation Science and Electrical
- 2006.
- Engineering, Beihang University, Beijing, China, in
- He is a Professor with the Department of
- 2025.
- Computer Science, St. Francis Xavier University,
- He is currently a Post-Doctoral Fellow with Bei-
- Antigonish, NS, Canada. His research was supported
- hang University. His research interests include deep
- by the National Sciences and Engineering Research
- learning, domain generalization, Industrial Internet
- Council, Canada (NSERC), and the Canada Founda-
- of Things, and industrial process monitoring.
- tion for Innovation (CFI). His research interests include parallel and distributed
- computing, embedded and ubiquitous/pervasive computing, and big data.

## Self-Supervised_Time_Series_Representation_Learning_via_Cross_Reconstruction_Transformer
- Extracted chars: 59120

### Opening / abstract evidence
- ===== PAGE 1 =====
- IEEE TRANSACTIONS ON NEURAL NETWORKS AND LEARNING SYSTEMS, VOL. 35, NO. 11, NOVEMBER 2024 16129
- Self-Supervised Time Series Representation
- Learning via Cross Reconstruction Transformer
- Wenrui Zhang , Ling Yang , Shijia Geng , and Shenda Hong
- Abstract—Since labeled samples are typically scarce in real- NOMENCLATURE
- world scenarios, self-supervised representation learning in time t Original time series.
- series is critical. Existing approaches mainly employ the con-
- m Magnitude of t.
- trastive learning framework, which automatically learns to
- p Phase of t.
- understand similar and dissimilar data pairs. However, they are
- constrained by the request for cumbersome sampling policies x Concatenation of t, m and p.
- and prior knowledge of constructing pairs. Also, few works have r Dropping ratio.
- focused on effectively modeling temporal-spectral correlations N Number of patches of x.
- to improve the capacity of representations. In this article,
- B Number of x in a batch (batch size).
- we propose the cross reconstruction transformer (CRT) to solve
- x ith x in a batch of x.
- the aforementioned issues. CRT achieves time series represen- i
- tation learning through a cross-domain dropping-reconstruction E i Projection of x i by convolutional neural networks.
- task. Specifically, we obtain the frequency domain of the time E′ Projection of E by transformer.
- i i
- series via the fast Fourier transform (FFT) and randomly drop E [CLS] token for time domain.
- T
- certain patches in both time and frequency domains. Dropping E′ Projection of E by transformer.
- is employed to maximally preserve the global context while T T
- E [CLS] token for magnitude.
- masking leads to the distribution shift. Then a Transformer M
- architecture is utilized to adequately discover the cross-domain E′ M Projection of E M by transformer.
- correlations between temporal and spectral information through E [CLS] token for phase.
- P
- reconstructing data in both domains, which is called Dropped E′ Projection of E by transformer.
- Temporal-Spectral Modeling. To discriminate the representa- P P
- tions in global latent space, we propose instance discrimination
- constraint (IDC) to reduce the mutual information between I. INTRODUCTION
- different time series samples and sharpen the decision bound-
- aries. Additionally, a specified curriculum learning (CL) strategy TIME series analysis [1], [2], [3], [4], [5], [6], [7], [8] is
- is employed to improve the robustness during the pretraining critical in a variety of real-world applications, such as
- phase, which progressively increases the dropping ratio in the transportation, medicine, finance, and industry. With the suc-
- training process. We conduct extensive experiments to evaluate
- cess of deep learning, various tasks in the field of time series
- the effectiveness of the proposed method on multiple real-
- analysis have achieved great performances, which include time
- world datasets. Results show that CRT consistently achieves

### Section, table, and figure headings detected
- L86: 3) To tackle the problem of distribution shift caused
- L93: Fig. 1. Comparisons with previous self-supervised methods. “Encode” is 4) We evaluate the representations learned by our proposed
- L103: A. Self-Supervised Learning
- L128: 1) Segment-level sampling policy used in contrastive learn-
- L136: 2) The distribution shift caused by the masking process in
- L158: 1) To simultaneously model the temporal-spectral informa-
- L172: 2) To avoid the instability occurring in contrast-based meth-
- L176: B. Self-Supervised Learning for Time Series
- L186: Fig. 2. Framework of our CRT. For each time series, we transform it into the frequency domain and calculate the magnitude and phase as explained in
- L235: III. CROSS RECONSTRUCTION TRANSFORMER
- L250: Fig. 3. Masking versus Dropping. (a) Given one time-series data, (b) masking
- L290: Fig. 4. Phase versus Magnitude. (a) Given a time series, (b) reconstruction frequency domain attempt to store the spectral information
- L477: B. Involving Spectral Information
- L497: C. Dropped Temporal-Spectral Modeling
- L533: D. Model Optimization
- L578: TABLE I help reduce pretraining time without influencing negatively
- L585: TABLE II
- L596: A. Experimental Setup
- L624: Table I. d) Temporal Neighborhood Coding [13]: TNC is also
- L680: Fig. 6. Performance on three datasets with and without phase. (a) PTB-XL.
- L681: B. Comparison Results
- L713: C. Analysis of Cross-Domain Reconstruction
- L724: TABLE IV
- L728: Fig. 8. Performance of three cross-domain reconstruction methods. (a)
- L731: TABLE V
- L735: Fig. 7. Performance when using time domain, frequency domain, and both
- L742: Fig. 9. Performance on three datasets with and without CL. (a) PTB-XL.
- L783: Fig. 10. Performance on three datasets with and without IDC. (a) PTB-XL.
- L799: Fig. 11. (a) Three reconstructed cases (the “Reconstructed” row) from

### Evidence snippets: math_formalization

```text
L37: Temporal-Spectral Modeling. To discriminate the representa- P P
L38: tions in global latent space, we propose instance discrimination
L39: constraint (IDC) to reduce the mutual information between I. INTRODUCTION
L40: different time series samples and sharpen the decision bound-
L41: aries. Additionally, a specified curriculum learning (CL) strategy TIME series analysis [1], [2], [3], [4], [5], [6], [7], [8] is
```

```text
L74: 100191, China (e-mail: yangling0818@163.com; hongshenda@pku.edu.cn). the future, relying on Noise-Contrastive Estimation [16] for
L75: Shijia Geng is with HeartVoice Medical Technology, Hefei 230027, China
L76: the loss function in similar ways. Temporal and contextual
L77: (e-mail: gengshijia@heartvoice.com.cn).
L78: Digital Object Identifier 10.1109/TNNLS.2023.3292066 contrasting (TS-TCC) [17] is an improved work of CPC
```

```text
L85: 16130 IEEE TRANSACTIONS ON NEURAL NETWORKS AND LEARNING SYSTEMS, VOL. 35, NO. 11, NOVEMBER 2024
L86: 3) To tackle the problem of distribution shift caused
L87: by masking in existing reconstruction-based methods,
L88: we employ a simple but reasonable “masking” method,
```

```text
L141: Contrastive learning methods typically rely on discriminating
L142: process sets parts of the time series as 0, introducing
L143: manually constructed pairs through an InfoNCE loss [15].
L144: noise to the training process and destroying the shape
L145: InfoNCE maximizes the similarity between positive instances
```

```text
L143: manually constructed pairs through an InfoNCE loss [15].
L144: noise to the training process and destroying the shape
L145: InfoNCE maximizes the similarity between positive instances
L146: of the time series.
L147: and minimizes the similarity between negatives. The largest
```

```text
L197: series representation learning [14]. The researchers design dif- our CRT framework and then transferred to the downstream
L198: ferent time-slicing strategies to construct positive and negative tasks. In this section, we describe our CRT in detail. All
L199: pairs with the assumption that temporally similar fragments important notations are shown in Nomenclature.
L200: could be viewed as positive samples and remote fragments At first, we pay attention to the drawbacks of existing self-
L201: are treated as negative samples [42]. Unsupervised Scalable supervised learning methods for time series data.
```

```text
L201: are treated as negative samples [42]. Unsupervised Scalable supervised learning methods for time series data.
L202: Representation Learning [12] introduces a novel unsupervised 1) The existing reconstruction methods for time series mask
L203: loss with time-based negative sampling to train a scalable original data and reconstruct it. However, masking (set
L204: encoder, shaped as a deep convolutional neural network (CNN) to zeros) can significantly change the original pattern
L205: with dilated convolutions [43]. temporal neighborhood coding of the time series and bring many noises to the pre-
```

```text
L295: between (b) and (a) is 1.62 and Euclidean distance between (c) and (a) is The magnitude of z is ||z|| = (a2 + b2)1/2. However, using
L296: 5.05. only magnitude to restore the complex numbers would cause
L297: information loss. Because we cannot restore z only using ||z||.
L298: between the pretraining stage and fine-tuning stage since it To tackle this problem, we propose a novel way to better
L299: leads to distribution shifts. As shown in Fig. 3(b), masking utilize the spectral information rather than simply using the
```

```text
L498: samples. Hence, we propose a simple instance discrimination
L499: In this section, we introduce our Dropped Temporal-Spectral
L500: constraint (IDC) module to remove redundancy and sharpen
L501: Modeling. For a given time series data t, we first conduct
L502: decision boundary. IDC maximizes the mutual information
```

```text
L531: As explained in Section III-A, dropping the patches can reduce
L532: the gap between the pretraining stage and fine-tuning stage
L533: D. Model Optimization
L534: because it does not change the shape of the original data.
L535: Before the Transformer encoder, we add three CNNs to Combining the reconstruction loss and IDC loss, our final
```

```text
L540: the local features. The patches x from time domain and
L541: i
L542: magnitude and phase are projected to three types of embed- where β is a hyper-parameter. By updating this loss, we hope
L543: dings E respectively. We then add a different learnable [CLS] the representations learned by the model contain as much
L544: i
```

```text
L564: Transformer to E′ i ∈ R(N+3)×D. We use E ¯′ i = (E′ T +E′ M +E′ P /3) (cid:18) (cid:18) i (cid:19)(cid:19)
L565: for down-stream tasks. We concatenate each E′ with learnable r = max r , min r , . (8)
L566: i i min max N
L567: decoding tokens and feed them into the decoder to reconstruct epoch
L568: all patches. The reconstruction loss is When the current epoch i is smaller than r × N , r is
```

### Evidence snippets: architecture

```text
L3: ===== PAGE 1 =====
L5: IEEE TRANSACTIONS ON NEURAL NETWORKS AND LEARNING SYSTEMS, VOL. 35, NO. 11, NOVEMBER 2024 16129
L6: Self-Supervised Time Series Representation
L7: Learning via Cross Reconstruction Transformer
```

```text
L19: to improve the capacity of representations. In this article,
L20: B Number of x in a batch (batch size).
L21: we propose the cross reconstruction transformer (CRT) to solve
L22: x ith x in a batch of x.
L23: the aforementioned issues. CRT achieves time series represen- i
```

```text
L23: the aforementioned issues. CRT achieves time series represen- i
L24: tation learning through a cross-domain dropping-reconstruction E i Projection of x i by convolutional neural networks.
L25: task. Specifically, we obtain the frequency domain of the time E′ Projection of E by transformer.
L26: i i
L27: series via the fast Fourier transform (FFT) and randomly drop E [CLS] token for time domain.
```

```text
L31: E [CLS] token for magnitude.
L32: masking leads to the distribution shift. Then a Transformer M
L33: architecture is utilized to adequately discover the cross-domain E′ M Projection of E M by transformer.
L34: correlations between temporal and spectral information through E [CLS] token for phase.
L35: P
```

```text
L49: the best performance over existing methods by 2%–9%. The series classification [3], [4], forecasting [5], [6] and anomaly
L50: code is publicly available at https://github.com/BobZwr/Cross- detection [7], [8], [9]. However, since labeled time series are
L51: Reconstruction-Transformer. usually difficult to acquire [10], [11], it is essential to study
L52: Index Terms—Cross domain, self-supervised learning, time learning representations from time series data in an unsuper-
L53: series, transformer. vised learning way. Self-supervised learning is an emerging
```

```text
L83: ===== PAGE 2 =====
L85: 16130 IEEE TRANSACTIONS ON NEURAL NETWORKS AND LEARNING SYSTEMS, VOL. 35, NO. 11, NOVEMBER 2024
L86: 3) To tackle the problem of distribution shift caused
L87: by masking in existing reconstruction-based methods,
```

```text
L92: the original distribution of the time series.
L93: Fig. 1. Comparisons with previous self-supervised methods. “Encode” is 4) We evaluate the representations learned by our proposed
L94: the encoder producing the representations of time series. “Temporal” and method on three datasets, and the results demonstrate
L95: “Spectral” are time-domain and frequency-domain data respectively. Note
L96: that our CRT achieves the best performance in terms of
```

```text
L104: on utilizing the long-term context information for the time
L105: As an emerging research field, self-supervised learning has
L106: series with an encoder-decoder architecture. The pretext task
L107: drawn much attention, especially for image data and text
L108: of these methods is reconstructing the original data, which may
```

```text
L111: Transformer architectures [20], [21], [22], a recent work [23]
L112: a way to provide “supervised” information for deep learning
L113: proposes a Transformer-based self-supervised learning frame-
L114: models. The model is expected to capture inherent charac-
L115: work for multivariate time series for the first time.
```

```text
L148: To solve these problems, we propose cross reconstruction
L149: challenge and difficulty is how to construct reasonable and
L150: transformer (CRT) for self-supervised time series repre-
L151: practical positive and negative sets to facilitate the model to
L152: sentation learning. Schematic comparisons for traditional
```

```text
L158: 1) To simultaneously model the temporal-spectral informa-
L159: learning is also applied to other fields, such as graph repre-
L160: tion and discover correlations, we apply a Transformer
L161: sentation learning [38], multimodal learning [39], and so on.
L162: encoder on both time domain and frequency domain
```

```text
L160: tion and discover correlations, we apply a Transformer
L161: sentation learning [38], multimodal learning [39], and so on.
L162: encoder on both time domain and frequency domain
L163: However, contrastive learning heavily depends on constructing
L164: data to automatically fuse cross-domain features. To ade-
```

### Evidence snippets: experiment_defense

```text
L23: the aforementioned issues. CRT achieves time series represen- i
L24: tation learning through a cross-domain dropping-reconstruction E i Projection of x i by convolutional neural networks.
L25: task. Specifically, we obtain the frequency domain of the time E′ Projection of E by transformer.
L26: i i
L27: series via the fast Fourier transform (FFT) and randomly drop E [CLS] token for time domain.
```

```text
L43: phase, which progressively increases the dropping ratio in the transportation, medicine, finance, and industry. With the suc-
L44: training process. We conduct extensive experiments to evaluate
L45: cess of deep learning, various tasks in the field of time series
L46: the effectiveness of the proposed method on multiple real-
L47: analysis have achieved great performances, which include time
```

```text
L52: Index Terms—Cross domain, self-supervised learning, time learning representations from time series data in an unsuper-
L53: series, transformer. vised learning way. Self-supervised learning is an emerging
L54: approach, which designs a pretext task and automatically
L55: generates “labels” for supervision while minimizing effort on
L56: annotation.
```

```text
L91: dropping discards the “masked” segments and preserves
L92: the original distribution of the time series.
L93: Fig. 1. Comparisons with previous self-supervised methods. “Encode” is 4) We evaluate the representations learned by our proposed
L94: the encoder producing the representations of time series. “Temporal” and method on three datasets, and the results demonstrate
L95: “Spectral” are time-domain and frequency-domain data respectively. Note
```

```text
L98: cross-domain dependencies. effectiveness and robustness, with a performance gain of
L99: 2%–9%.
L100: and learns robust representations by a harder prediction task
L101: against perturbations introduced by different timestamps and II. RELATED WORK
L102: augmentations. Reconstruction-based methods [18], [19] focus
```

```text
L104: on utilizing the long-term context information for the time
L105: As an emerging research field, self-supervised learning has
L106: series with an encoder-decoder architecture. The pretext task
L107: drawn much attention, especially for image data and text
L108: of these methods is reconstructing the original data, which may
```

```text
L116: teristics among large-scale unlabeled data, and show a better
L117: However, the existing approaches (including contrast-based
L118: performance on downstream tasks compared to training from
L119: and reconstruction-based learning) neglect to exploit the
L120: spectral information and utilize the temporal-spectral cor- scratch [31].
```

```text
L150: transformer (CRT) for self-supervised time series repre-
L151: practical positive and negative sets to facilitate the model to
L152: sentation learning. Schematic comparisons for traditional
L153: capture similarities and differences among instances. Some
L154: reconstruction-based, contrast-based, and CRT methods are
```

```text
L187: Section III-B. We then slice the data and randomly drop some sliced patches. The remaining patches are projected as three types of embeddings through
L188: three CNNs (shown as arrows in the figure). Decorated with the prefixed [CLS] tokens (ET, EM, and EP) and summed with position embedding and
L189: domain-type embedding, all embeddings are fed into a cross-domain Transformer encoder. For our pretrained reconstruction task, we feed all resultant
L190: cross-domain representations into the decoder to reconstruct the original time, magnitude, and phase data. For downstream tasks, we condense E′ , E′ and
L191: E′
```

```text
L196: mainly leverage the contrastive learning framework for time two domains. Generally, the model is first pretrained following
L197: series representation learning [14]. The researchers design dif- our CRT framework and then transferred to the downstream
L198: ferent time-slicing strategies to construct positive and negative tasks. In this section, we describe our CRT in detail. All
L199: pairs with the assumption that temporally similar fragments important notations are shown in Nomenclature.
L200: could be viewed as positive samples and remote fragments At first, we pay attention to the drawbacks of existing self-
```

```text
L210: the long-term dependencies [14]. Besides, the performance neglect the frequency domain, which is a complemen-
L211: will substantially deteriorate when applied to downstream tary perspective to the time domain of time series. In
L212: tasks containing periodic time series. Section III-B, we propose a novel way to better utilize
L213: A recent work [23] proposes a Transformer-based recon- the spectral information and model temporal-spectral
L214: struction self-supervised task for time series data for the first correlations.
```

```text
L229: Masking parts of data and reconstructing them is a common
L230: learning methods neglect an important characteristic of time
L231: paradigm in self-supervised learning tasks [32], [40]. Inspired
L232: series data - the frequency domain.
L233: by this, some works mask the original time series by setting
```

### Evidence snippets: visualization

```text
L91: dropping discards the “masked” segments and preserves
L92: the original distribution of the time series.
L93: Fig. 1. Comparisons with previous self-supervised methods. “Encode” is 4) We evaluate the representations learned by our proposed
L94: the encoder producing the representations of time series. “Temporal” and method on three datasets, and the results demonstrate
L95: “Spectral” are time-domain and frequency-domain data respectively. Note
```

```text
L154: reconstruction-based, contrast-based, and CRT methods are
L155: works propose to construct pairs via data augmentations meth-
L156: illustrated in Fig. 1. Our contributions include.
L157: ods [29], [35], clustering [36], [37], and so on. Contrastive
L158: 1) To simultaneously model the temporal-spectral informa-
```

```text
L185: ZHANG et al.: SELF-SUPERVISED TIME SERIES REPRESENTATION LEARNING VIA CRT 16131
L186: Fig. 2. Framework of our CRT. For each time series, we transform it into the frequency domain and calculate the magnitude and phase as explained in
L187: Section III-B. We then slice the data and randomly drop some sliced patches. The remaining patches are projected as three types of embeddings through
L188: three CNNs (shown as arrows in the figure). Decorated with the prefixed [CLS] tokens (ET, EM, and EP) and summed with position embedding and
```

```text
L235: III. CROSS RECONSTRUCTION TRANSFORMER
L236: these segments [23]. However, this may significantly change
L237: The framework of CRT is shown in Fig. 2. Our the original pattern of time series and bring noises to the
L238: CRT is a Transformer-based time-frequency domain representation learning process. Besides, it may cause a gap
L239: Authorized licensed use limited to: University of Science & Technology of China. Downloaded on July 05,2026 at 10:01:34 UTC from IEEE Xplore. Restrictions apply.
```

```text
L248: which is a rapid implementation of the discrete Fourier trans-
L249: form (DFT)
L250: Fig. 3. Masking versus Dropping. (a) Given one time-series data, (b) masking
L251: m
L252: so
```

```text
L288: However, these complex numbers cannot be used to train the
L289: neural networks directly. Most of the methods considering the
L290: Fig. 4. Phase versus Magnitude. (a) Given a time series, (b) reconstruction frequency domain attempt to store the spectral information
L291: with phase tends to preserve the shape of the original data, and (c) while using the magnitude of the complex numbers. For any complex
L292: reconstruction with magnitude tends to preserve the value of the original
```

```text
L297: information loss. Because we cannot restore z only using ||z||.
L298: between the pretraining stage and fine-tuning stage since it To tackle this problem, we propose a novel way to better
L299: leads to distribution shifts. As shown in Fig. 3(b), masking utilize the spectral information rather than simply using the
L300: significantly changes the shape and distribution of the original magnitude. We introduce phase φ(z) ∈ (−π, π] as follows:
L301: time series. Different from images or text, the shape is
```

```text
L459: parts of the input time series, and feeds the rest of the data into where
L460: the model. The difference between masking and dropping is  ||b||
L461: shown in Fig. 3. In detail, we slice the input into patches with  , b ̸= 0
L462: Sign(b) = b
L463: the same length, and randomly discard patches in a probability  0, b = 0.
```

```text
L483: spectral perspective can provide several characteristics of the constant vector. In both cases, we restore the complex vector
L484: time series that are not easily acquirable in the time domain. following (4), and conduct inverse FFT to transform complex
L485: Consequently, we attempt to explicitly input both time and vectors to the time domain. As shown in Fig. 4, we can see
L486: frequency domains into the model to enable it to learn both that the original time series is more similar to the restored
L487: Authorized licensed use limited to: University of Science & Technology of China. Downloaded on July 05,2026 at 10:01:34 UTC from IEEE Xplore. Restrictions apply.
```

```text
L669: at various thresholds ranging from zero to one. Accuracy is
L670: calculated for each class, as the ratio of the number of correctly
L671: classified samples over the total number of samples. F1 score Fig. 5. Performance on three datasets when data is dropped or masked during
L672: the pretraining stage. (a) PTB-XL. (b) HAR. (c) Sleep-EDF.
L673: is the harmonic average of precision (the proportion of true
```

```text
L678: all classes, and macro averaged F1 score. Reported numbers
L679: are expressed in percentage values for better reading.
L680: Fig. 6. Performance on three datasets with and without phase. (a) PTB-XL.
L681: B. Comparison Results
L682: (b) HAR. (c) Sleep-EDF.
```

```text
L685: fine-tuning than masking, we compare the results on down-
L686: in terms of ROC-AUC, F1-score, and accuracy. We also
L687: stream tasks under the two setups. From Fig. 5, we see
L688: observe that the results of CRT have a relatively small stan-
L689: dropping always leads to better downstream performances,
```

### Closing evidence
- [35] X. Chen, H. Fan, R. Girshick, and K. He, “Improved baselines with research interests include graph machine learning,
- momentum contrastive learning,” 2020, arXiv:2003.04297. representation learning, and generative modeling.
- [36] M. Caron, P. Bojanowski, A. Joulin, and M. Douze, “Deep clustering for Dr. Yang serves as a Reviewer for IEEE TRANS-
- unsupervised learning of visual features,” in Proc. Eur. Conf. Comput. ACTIONS ON PATTERN ANALYSIS AND MACHINE
- Vis. (ECCV), 2018, pp. 132–149. INTELLIGENCE (TPAMI), NeurIPS, ICML, CVPR,
- [37] M. Caron, I. Misra, J. Mairal, P. Goyal, P. Bojanowski, and A. Joulin, KDD, and AAAI.
- “Unsupervised learning of visual features by contrasting cluster assign-
- ments,” in Proc. Adv. Neural Inf. Process. Syst., vol. 33, 2020,
- Shijia Geng received the bachelor’s degree in neu-
- pp. 9912–9924.
- roscience and the master’s degree in biomedical
- [38] Y. Zheng et al., “Toward graph self-supervised learning with contrastive engineering from the University of Miami, Coral
- adjusted zooming,” IEEE Trans. Neural Netw. Learn. Syst., early access, Gables, FL, USA, in 2011 and 2014, respectively.
- Nov. 10, 2022, doi: 10.1109/TNNLS.2022.3216630. She was at the Data Science and Computa-
- [39] H. Zhang, J. Y. Koh, J. Baldridge, H. Lee, and Y. Yang, “Cross-modal tion Institute, University of Miami, participating in
- contrastive learning for text-to-image generation,” in Proc. IEEE/CVF research and development projects such as signal
- Conf. Comput. Vis. Pattern Recognit. (CVPR), Jun. 2021, pp. 833–842. processing, machine learning, and deep learning.
- [40] K. He, X. Chen, S. Xie, Y. Li, P. Dollár, and R. Girshick, “Masked She is currently working with Heartvoice Medical
- autoencoders are scalable vision learners,” in Proc. IEEE/CVF Conf. Technology, Hefei, China. She is doing research in
- Comput. Vis. Pattern Recognit. (CVPR), Jun. 2022, pp. 15979–15988. algorithms.
- [41] J. Jiang, J. Chen, and Y. Guo, “A dual-masked auto-encoder for robust
- motion capture with spatial–temporal skeletal token completion,” in
- Shenda Hong is currently an Assistant Professor
- Proc. 30th ACM Int. Conf. Multimedia, Oct. 2022, pp. 5123–5131.
- with the National Institute of Health Data Sci-
- [42] Z. Yue et al., “TS2Vec: Towards universal representation of time series,” ence, Peking University, Beijing, China. His research
- 2021, arXiv:2106.10466. interests include data mining and artificial intelli-
- [43] A. Van Den Oord et al., “WaveNet: A generative model for raw audio,” gence for real-world healthcare data, especially deep
- SSW, vol. 125, p. 2, Sep. 2016. learning for temporal medical data-such as temporal
- [44] L. Ye and E. Keogh, “Time series shapelets: A new primitive for data events, time series (e.g., longitudinal data, electronic
- mining,” in Proc. 15th ACM SIGKDD Int. Conf. Knowl. Discovery Data health records, and claims data), and physiological
- Mining, Jun. 2009, pp. 947–956. signals (e.g., ECG, EEG, and PSG).
- [45] A. V. Oppenheim, A. S. Willsky, and S. H. Nawab, Signals & System, Dr. Hong serves as an Associate Editor for Health
- 2nd ed. Upper Saddle River, NJ, USA: Prentice-Hall, 1996. Data Science.
- Authorized licensed use limited to: University of Science & Technology of China. Downloaded on July 05,2026 at 10:01:34 UTC from IEEE Xplore. Restrictions apply.

## Sparsity-Constrained_Invariant_Risk_Minimization_for_Domain_Generalization_With_Application_t
- Extracted chars: 71535

### Opening / abstract evidence
- ===== PAGE 1 =====
- IEEE TRANSACTIONS ON CYBERNETICS, VOL. 54, NO. 3, MARCH 2024 1547
- Sparsity-Constrained Invariant Risk Minimization
- for Domain Generalization With Application to
- Machinery Fault Diagnosis Modeling
- Zhenling Mo , Zijun Zhang , Senior Member, IEEE, Qiang Miao , Senior Member, IEEE,
- and Kwok-Leung Tsui
- Abstract—Machine learning has been widely applied to study models with good adaptiveness to operating condition changes
- AI-informed machinery fault diagnosis. This work proposes is of great importance for enhancing the safety and reliability
- a sparsity-constrained invariant risk minimization (SCIRM)
- of machinery systems.
- framework, which develops machine-learning models with bet-
- In the past, machine-learning models were mainly trained
- ter generalization capacities for environmental disturbances in
- machinery fault diagnosis. The SCIRM is built by innovating via empirical risk minimization (ERM). Its performance
- the optimization formulation of the recently proposed invariant guarantee requires adhering to the assumption that the data are
- risk minimization (IRM) and its variants through the integration independent and identically distributed (IID) [2]. However,
- of sparsity constraints. We prove that if a sparsity measure is
- data collected under changing working conditions do not com-
- differentiable, scale invariant, and semistrictly quasi-convex, the
- ply with the IID assumption. Therefore, machine-learning
- SCIRM can be guaranteed to solve the domain generalization
- problem based on a few predefined problem settings. We mathe- models developed by ERM may generalize poorly in real
- matically derive a family of such sparsity measures. A practical machinery fault diagnosis tasks.
- process of implementing the SCIRM for machinery fault diag- Numerous research attempts have been made in the past
- nosis tasks is offered. We first verify our theoretical exploration
- to deal with modeling under data-label joint distribution dis-
- of the SCIRM by using simulation data. We further compare
- crepancies among various machine working environments to
- SCIRM with a set of state-of-the-art methods by using real
- machinery fault data collected under a variety of working condi- enable better model out-of-distribution (OOD) generalizations.
- tions. The computational results confirm that the machinery fault One prevalent stream of methods is based on transfer learning
- diagnosis model developed by the SCIRM offers a higher general- and domain adaptation [3]. To apply those types of methods,
- ization capacity and performs better than the other benchmarks
- a pretrained model and the target-domain data need to be avail-
- across the different testing datasets.
- able. For example, in [4], a deep joint distribution alignment
- Index Terms—Causal learning, fault diagnosis, model general- method was proposed to align data distributions caused by
- ization, risk minimization, sparsity measure.
- different machine working conditions. In [5], a refined adver-
- sarial adaptation and classifier complementation approach was
- I. INTRODUCTION developed to deal with domain and category discrepancies for
- MACHINE learning for machinery fault diagnosis has industrial fault diagnosis. To effectively transfer knowledge for
- been vigorously discussed due to sensor advancements multidomain fault diagnosis, a dual-channel feature network and
- and the availability of data [1]. Rotational machines often have relation network were constructed to process the source-domain

### Section, table, and figure headings detected
- L45: I. INTRODUCTION developed to deal with domain and category discrepancies for
- L126: A. Problem Setting
- L171: III. METHODOLOGY
- L215: C. Information Bottleneck-Based Invariant Risk Minimization
- L479: Fig. 1. Proposed diagnosis method under different environments. Therefore, the simulation model can be regarded as a relaxed
- L489: IV. CASE STUDIES modulation function to mimic the subtle random fluctuations
- L491: A. Implementation
- L524: B. Experimental Design
- L538: Fig. 2. Train bearing test rig.
- L539: Fig. 4. Training and test results of the classification based on simulation
- L543: Fig. 3. Gearbox test rig.
- L544: Fig. 5. Test results of the classification based on bearing data under the
- L559: Fig. 3, is utilized to acquire the gearbox data. There are three that there are some gaps between the theory and reality. The
- L577: C. Result Analysis
- L590: Fig. 6. Test results of the classification based on bearing data under the two Fig. 8. Test results of the classification based on gearbox data under the two
- L594: Fig. 7. Test results of the classification based on gearbox data under the one
- L619: V. FURTHER DISCUSSION AND VALIDATIONS
- L638: Fig. 8 (two training environments setting). Again, the results domains in Fig. 9. The samples are generated from the simula-
- L647: Fig. 10. Test classification results on the Colored MNIST dataset, where
- L649: Fig. 11. Confusion matrices, where “Normal,” “Inner,” “Outer” means nor-
- L710: C. Confusion Matrix
- L724: TABLE I
- L733: VI. CONCLUSION
- L757: A. Proof of Lemma 1
- L796: C. Proof of Corollary 1
- L829: E. Proof of Lemma 3

### Evidence snippets: math_formalization

```text
L5: IEEE TRANSACTIONS ON CYBERNETICS, VOL. 54, NO. 3, MARCH 2024 1547
L6: Sparsity-Constrained Invariant Risk Minimization
L7: for Domain Generalization With Application to
L8: Machinery Fault Diagnosis Modeling
```

```text
L11: Abstract—Machine learning has been widely applied to study models with good adaptiveness to operating condition changes
L12: AI-informed machinery fault diagnosis. This work proposes is of great importance for enhancing the safety and reliability
L13: a sparsity-constrained invariant risk minimization (SCIRM)
L14: of machinery systems.
L15: framework, which develops machine-learning models with bet-
```

```text
L16: In the past, machine-learning models were mainly trained
L17: ter generalization capacities for environmental disturbances in
L18: machinery fault diagnosis. The SCIRM is built by innovating via empirical risk minimization (ERM). Its performance
L19: the optimization formulation of the recently proposed invariant guarantee requires adhering to the assumption that the data are
L20: risk minimization (IRM) and its variants through the integration independent and identically distributed (IID) [2]. However,
```

```text
L23: differentiable, scale invariant, and semistrictly quasi-convex, the
L24: ply with the IID assumption. Therefore, machine-learning
L25: SCIRM can be guaranteed to solve the domain generalization
L26: problem based on a few predefined problem settings. We mathe- models developed by ERM may generalize poorly in real
L27: matically derive a family of such sparsity measures. A practical machinery fault diagnosis tasks.
```

```text
L31: of the SCIRM by using simulation data. We further compare
L32: crepancies among various machine working environments to
L33: SCIRM with a set of state-of-the-art methods by using real
L34: machinery fault data collected under a variety of working condi- enable better model out-of-distribution (OOD) generalizations.
L35: tions. The computational results confirm that the machinery fault One prevalent stream of methods is based on transfer learning
```

```text
L61: InnoHK initiative, The Government of the HKSAR, and Laboratory for AI-
L62: Powered Financial Technologies. This article was recommended by Associate recent years. One popular attempt was devoted to studying the
L63: Editor J. Q. Gan. (Corresponding author: Zijun Zhang.) interpolation/extrapolation of features/losses, for example, the
L64: Zhenling Mo and Zijun Zhang are with the School of Data Science,
L65: intrinsic and extrinsic losses [8], the interdomain Mixup [9],
```

```text
L63: Editor J. Q. Gan. (Corresponding author: Zijun Zhang.) interpolation/extrapolation of features/losses, for example, the
L64: Zhenling Mo and Zijun Zhang are with the School of Data Science,
L65: intrinsic and extrinsic losses [8], the interdomain Mixup [9],
L66: City University of Hong Kong, Hong Kong, SAR, and also with City
L67: University of Hong Kong Shenzhen Research Institute, Shenzhen, China and the variance risk extrapolation [10]. In addition to inter-
```

```text
L73: Engineering, Virginia Tech, Blacksburg, VA 24061 USA. mask [12], and SAND mask [13]. The dynamic system theory,
L74: Color versions of one or more figures in this article are available at
L75: robust optimization, and causal inference have also been adapted
L76: https://doi.org/10.1109/TCYB.2022.3223783.
L77: Digital Object Identifier 10.1109/TCYB.2022.3223783 to develop domain generalizability models. Pezeshki et al. [14]
```

```text
L84: 1548 IEEE TRANSACTIONS ON CYBERNETICS, VOL. 54, NO. 3, MARCH 2024
L85: utilized the dynamical system theory to study gradient starva- fault diagnosis models with domain generalization
L86: tion, which is a phenomenon hindering model robustness and capabilities.
L87: generalization. Sagawa et al. [15] applied distributional robust 2) Theoretical Exploration: In the proposed SCIRM, we
```

```text
L91: causality-inspired domain generalization. Our work aims to generalization.
L92: establish additional models based on causality-inspired meth- 3) Theoretical Development: We prove that a family of
L93: ods. These studies typically consider the assumption that the sparsity measures, the p-q mean family, with p ≤ 1,
L94: conditional distribution of the variable of interest, given all its q ≥ 1, and p (cid:5)= q, have the desired properties. We
L95: direct causes, is invariant [16]. This assumption is consistent theoretically show that the proposed SCIRM can tackle
```

```text
L95: direct causes, is invariant [16]. This assumption is consistent theoretically show that the proposed SCIRM can tackle
L96: with the real-world observation that the causal mechanism is the OOD issue if the data satisfy the proposed struc-
L97: intact when intervening on the causes. Essentially, a supervised tural equation model and the invariant features are
L98: machine-learning model tries to learn a conditional distribution bounded, strictly separable and satisfy support over-
L99: of targets given observations as a way of prediction [18]. Thus, laps. Meanwhile, the developed theory is also validated
```

```text
L103: target variable is the key to solving the OOD problem, which diagnosis models with improved diagnosis accuracies
L104: then enhances the domain generalization when modeling with under different working conditions. The advantages of
L105: machine-learning techniques. SCIRM are verified by benchmarking against a set of
L106: One direction of causality inspired learning attempts to map state-of-the-art methods under extensive generalization
L107: observations to representations in latent space to approximate tasks designed using bearing and gearbox data col-
```

### Evidence snippets: architecture

```text
L42: ization, risk minimization, sparsity measure.
L43: different machine working conditions. In [5], a refined adver-
L44: sarial adaptation and classifier complementation approach was
L45: I. INTRODUCTION developed to deal with domain and category discrepancies for
L46: MACHINE learning for machinery fault diagnosis has industrial fault diagnosis. To effectively transfer knowledge for
```

```text
L108: the direct causes of the target variable [19]. Invariant risk lected under different working conditions. On average,
L109: minimization (IRM) [20] is one of the causality-inspired learn- the proposed SCIRM outperforms the benchmarking
L110: ing methods and has attracted much attention in recent years. modeling methods.
L111: Arjovsky et al. [20] showed that the IRM has a theoretical Theremainderofthisarticleisorganizedasfollows. SectionII
L112: guarantee of solving OOD problems under linear regression outlines the preliminaries of this article. Section III introduces
```

```text
L208: tion and the empirical loss. In addition, (cid:4) = 1.0 indicates that
L209: the reasons that IBIRM adopts an indirect way of minimizing
L210: the dummy classifier is required for reparametrization. Details
L211: the differential entropy [21].
L212: are offered in [20].
```

```text
L307: Proposition 1: Let Z(X) = −[F(X)/G(X)] be the negative transformation B (cid:11) · N s e pu is often Gaussian as well. Then, B ·
L308: ratio of two positive functions, F(X) and G(X), defined on the Z i e nv and B (cid:11) · N s e pu can have different values of sparsity [26].
L309: convex set (cid:9) ⊆ Rn +. If F(X) is concave and G(X) is convex, In practice, we rely on a neural network to map the data to
L310: Z(X) is semistrictly quasi-convex. the data manifold, approximately satisfying this assumption.
L311: Corollary 1: Let Z(X) = −[(cid:16)X(cid:7) (cid:16)
```

```text
L402: that no algorithm can solve the OOD problem [21]. commonly seen ERM, the proposed SCIRM can be leveraged
L403: 2) Practical Version: To obtain a practical risk function of to train machine-learning models, such as a standard convolu-
L404: SCIRM, we can follow the same IRM and IBIRM tricks. First, tional neural network, for fault diagnosis tasks. In this article,
L405: we can use the reparametrization so that the learning task of we borrow a simple 1-D convolutional neural network from
L406: IRM can be assigned to the feature mapping (cid:3) only. Therefore, previous studies [29] to demonstrate the process of applying
```

```text
L416: (cid:3) = (cid:12)(cid:11) ◦(cid:3)(cid:11) ; and (cid:3)(cid:11) and (cid:12)(cid:11) are two intermediate feature map- corresponds to one environment. Several training environments
L417: pings. For example, we can employ outputs of certain layers in and the test environment containing different observation-label
L418: the neural networks to compute the reverse sparsity measure. pairs are then obtained.
L419: Then, the layers before the intermediate outputs are repre- Step 2: In the forward propagation of the neural network,
L420: sented by
```

```text
L428: SCIRM. Let ζe, ζe and ζe be the first, second and third losses computed based on (17).
L429: 1 2 3
L430: (without weights) in (15), respectively. We name ζe empirical Step 3: In the neural-network backpropagation, the gradients
L431: 1
L432: loss, ζe invariance loss and ζe sparsity loss. The corresponding of the average SCIR with respect to the model parameters are
```

```text
L561: gear and a missing tooth on the planet gear. For each class, fied approximation to the ideal data generation model. The
L562: there are three speed conditions, 900, 1200, and 1500 rpm. second is that the data extraction is limited by the model’s
L563: The vertical direction data of the accelerometer (604B31) are complexity. It is obvious that a shallow neural network and
L564: employed. The sampling frequency is 5 kHz, and approxi- a deep neural network can have different feature extraction
L565: mately 280 000 points are collected in total. The data are then abilities. The third is that the practical version of SCIRM is an
```

```text
L658: in the test domains. To illustrate this, we test our method and Three tasks are designed as follows. Task 1: N15_M01_F10
L659: the baseline methods close to ours on the colored MNIST and N15_M07_F04 for training and N09_M07_F10 for test-
L660: dataset. Details of the dataset, the neural network used and ing. Task 2: N09_M07_F10 and N15_M07_F04 for training
L661: other implementation information are available in [20]. The and for N15_M01_F10 testing. Task 3: N09_M07_F10 and
L662: key design of the dataset is that the labels are strongly cor- N15_M01_F1 for training and N15_M07_F04 for testing. For
```

```text
L689: the data from the training set as the validation set. All the
L690: ate nine generalization tasks. One dataset has been dis-
L691: methods are based on the neural network shown in Fig. 1. We
L692: cussed in Section IV-B2 and is called the “CityU dataset”
L693: tune all the methods so that they perform well on the training
```

```text
L830: or concave. Note that we require p (cid:5)= q. Hence, F(X) and
L831: G(X) cannot be simultaneously affine when defining Z(X). First, it is trivial to know that the labeling hyperplane(cid:4)∗ =
L832: Second, we need to prove that G(X) = (cid:16)X(cid:16) with q > 1is I◦(cid:12)([W inv , 0]T −1(cid:3)∗(Oe)) is the Bayes optimal classifier with-
L833: convex. Since q > 1, (cid:16)X(cid:16) is a norm. By sub q additivity, we out the label noise since: 1) If (cid:4)∗ ≥ 0, P(Le = 1|Oe) ≥
L834: q P(Le = 0|Oe) and the prediction is 1; and 2), if (cid:4)∗ < 0,
```

```text
L835: have
L836: P(Le = 1|Oe) < P(Le = 0|Oe) and the prediction is 0.
L837: (cid:16)αX + (1 − α)Y(cid:16) q ≤ α(cid:16)X(cid:16) q + (1 − α)(cid:16)Y(cid:16) q (35) It is known that given any classifier, its misclassifica-
L838: where α ∈ (0, 1) and X, Y ∈ (cid:9) ⊆ Rn +. tion error is larger than or equal to the Bayes optimal
L839: Finally, we need to prove that F(X) = (cid:16)X(cid:16) , where 0 < classifier [18]. Next, we show that under the noisy environ-
```

### Evidence snippets: experiment_defense

```text
L25: SCIRM can be guaranteed to solve the domain generalization
L26: problem based on a few predefined problem settings. We mathe- models developed by ERM may generalize poorly in real
L27: matically derive a family of such sparsity measures. A practical machinery fault diagnosis tasks.
L28: process of implementing the SCIRM for machinery fault diag- Numerous research attempts have been made in the past
L29: nosis tasks is offered. We first verify our theoretical exploration
```

```text
L35: tions. The computational results confirm that the machinery fault One prevalent stream of methods is based on transfer learning
L36: diagnosis model developed by the SCIRM offers a higher general- and domain adaptation [3]. To apply those types of methods,
L37: ization capacity and performs better than the other benchmarks
L38: a pretrained model and the target-domain data need to be avail-
L39: across the different testing datasets.
```

```text
L103: target variable is the key to solving the OOD problem, which diagnosis models with improved diagnosis accuracies
L104: then enhances the domain generalization when modeling with under different working conditions. The advantages of
L105: machine-learning techniques. SCIRM are verified by benchmarking against a set of
L106: One direction of causality inspired learning attempts to map state-of-the-art methods under extensive generalization
L107: observations to representations in latent space to approximate tasks designed using bearing and gearbox data col-
```

```text
L135: Q.3) can the sparsity-constrained formulation solve the OOD ments, test environments, and all environments, (cid:2)respectively.
L136: problem under certain conditions theoretically and numeri- Note that ε train , ε test ⊆ ε all and generally, ε train ε test = ∅.
L137: cally? Q.4) can we apply the theory more practically to fault Then, the training environment dataset can be defined as
L138: diagnosis tasks? and Q.5) can the proposed method achieve D train : = {(Oe, Le)} e∈ε train . The datasets of the test and all
L139: improvements over the state-of-the-art methods on datasets environments can be defined similarly. We assume that the
```

```text
L298: Thus far, we have merely made assumptions about the
L299: Ideally, the informative feature can be obtained from the
L300: desired sparsity measure. The next task is to find such sparsity
L301: bijective feature mapping (cid:3)∗(·) with (cid:3)∗ ◦ Oe = T[Ze , Ze ].
L302: measures that satisfy our assumptions. inv spu
```

```text
L382: ↑ The coefficient of variation (cid:16)t at time step t can be defined as
L383: Theorem 1: Suppose: 1) the sparsity measure S is dif- i
L384: the normalized relative standard deviation of the loss ratio as
L385: ferentiable, scale-invariant (Definition 1), and semistrictly
L386: follows:
```

```text
L391: rable, and domain level support overlapped [21]). The solution (cid:16) i i=1 i (cid:16) i
L392: t 0 o -1 th l e os p s r a o l p s o o se s d olv o e p s tim th i e za O ti O on D p p r r o o b b l l e e m m d d e e s s c c r r i i b b e e d d i i n n ( ( 1 1 4 ). ) with d w e h v e i r a e tio τ n i t i o s f th th e e re lo la s t s iv r e at s i t o a , n μ da t (cid:16) rd is de t v h i e at m io e n a , n σ (cid:16) o t i f is th t e he lo s s t s an r d at a i r o d ,
L393: Although we only obtain access to the training environments and κt is the sum of all the rel i ative standard deviations. Note
L394: in the proposed optimization problem, the theorem says that that the mean μt (cid:16) and standard deviation σ (cid:16) t can be efficiently
L395: i i
```

```text
L402: that no algorithm can solve the OOD problem [21]. commonly seen ERM, the proposed SCIRM can be leveraged
L403: 2) Practical Version: To obtain a practical risk function of to train machine-learning models, such as a standard convolu-
L404: SCIRM, we can follow the same IRM and IBIRM tricks. First, tional neural network, for fault diagnosis tasks. In this article,
L405: we can use the reparametrization so that the learning task of we borrow a simple 1-D convolutional neural network from
L406: IRM can be assigned to the feature mapping (cid:3) only. Therefore, previous studies [29] to demonstrate the process of applying
```

```text
L483: classify the different fault types in the test environments. feature of the fault condition is a periodic impulse train, which
L484: We will first verify Theorem 1 using simulation data. Next, is non-Gaussian. One unit of the impulse train is generated in
L485: we benchmark the proposed SCIRM-based diagnosis method the time domain by the vibration system with a single degree
L486: against the ERM-, IRM- and IBIRM-based diagnosis methods of freedom. The modulation frequency is 80 Hz. The damping
L487: using real machinery data. ratio is 0.01. The natural frequency is 5 kHz. We also add
```

```text
L498: 20 480 Hz, and the duration is equal to 10 s. To create the
L499: employ full batch data to train the model. The learning rate is
L500: dataset for each environment, we segment the data into pieces
L501: set to 0.001. The maximum epoch number is 500. L2 regular-
L502: without overlaps. Each piece contains 5000 data points. Our
```

```text
L508: experiment, we design two training environments and one
L509: are set as in the previous studies [29]. Regarding validations,
L510: test environment. In addition, each experiment was repeated
L511: we consider both the oracle setting and the leave-one-domain-
L512: 10 times to calculate the mean accuracy and standard devi-
```

```text
L512: 10 times to calculate the mean accuracy and standard devi-
L513: out setting [30]. Metrics evaluating the model performances
L514: ation. Three generalization tasks are designed, which will be
L515: include the mean classification accuracy and the standard devi-
L516: specified later in the corresponding figures showing the experi-
```

### Evidence snippets: visualization

```text
L407: the predictor (cid:4) can be as simple as a fixed scalar [20], [21]. the SCIRM to machinery fault diagnosis. The sparsity measure
L408: Next, we consider the Lagrange multiplier method to convert in this example is chosen as the one defined in Lemma 2. The
L409: the constraint problem into an unconstrained problem. Finally, SCIRM-based diagnosis method is illustrated in Fig. 1. The
L410: the practical version of SCIRM can be simplified as follows: diagnosis procedure follows the four steps described next.
L411: (cid:3) (cid:4) (cid:4) (cid:10) (cid:11) Step 1: The observational signals of the different machine
```

```text
L424: (cid:12)(cid:11)
L425: . on (16). Here, the intermediate outputs from the second dense
L426: To facilitate training, we propose to exploit the coeffi- layer (see Fig. 1) are utilized to compute the reverse sparsity.
L427: cient of variation [27] as the adaptive weighting strategy of Afterward, the average SCIR of all training environments is
L428: SCIRM. Let ζe, ζe and ζe be the first, second and third losses computed based on (17).
```

```text
L477: where the direct causes reside, and that have different values
L478: of sparsity from the spurious noise, is difficult to simulate.
L479: Fig. 1. Proposed diagnosis method under different environments. Therefore, the simulation model can be regarded as a relaxed
L480: and simplified approximation to Assumption 1.
L481: For simplicity, the pseudo invariant feature of the normal
```

```text
L491: A. Implementation
L492: N ˆ e to change the signal-to-noise ratio (SNR) to introduce
L493: We replace the risk function in Fig. 1 with ERM, IRM, spu
L494: the different environments.
L495: and IBIRM to realize the corresponding diagnosis methods.
```

```text
L521: is regarded as better.
L522: 2) Bearing Data Description: Our test rig for collecting
L523: the bearing data is shown in Fig. 2. There are two classes, the
L524: B. Experimental Design
L525: normal condition and roller fault condition. For each class,
```

```text
L537: MO et al.: SCIRM FOR DOMAIN GENERALIZATION 1553
L538: Fig. 2. Train bearing test rig.
L539: Fig. 4. Training and test results of the classification based on simulation
L540: data; (a) result of two training environments (-4 and -10 db) and single test
```

```text
L550: leave 150 km/h out for validation and 200 km/h for testing
L551: but change the different training environments [30]. The goal test dataset. However, once the SNRs are low, ERM general-
L552: is to observe the effects of changing training environments izes poorly on the test dataset, as shown in Fig. 4(b) and (c).
L553: on the model performances of the test environments. Three Different from ERM, it is observable that the performance
L554: generalization tasks are designed and will be specified in the of SCIRM is less influenced by the change in SNRs. Under
```

```text
L556: ten trials for computations of the mean accuracy and standard the training and test datasets. With a decrease in the SNR,
L557: deviation. SCIRM can still obtain relatively high accuracies on the test
L558: 3) Gearbox Data Description: Our test rig, shown in datasets, as shown in Fig. 4(b) and (c). It should be noted
L559: Fig. 3, is utilized to acquire the gearbox data. There are three that there are some gaps between the theory and reality. The
L560: classes, the normal condition, a missing tooth on the sun first is that the simulation model is a relaxed and simpli-
```

```text
L566: segmented without overlaps into instances, and each instance unconstrained optimization problem, which is a compromise
L567: has 2000 points. Oracle validation is employed to show the of the proposed constrained optimization problem. However,
L568: optimal performance [30]. Three experimental designs for the as shown in Fig. 4(d), SCIRM still shows a strong generaliza-
L569: generalization study will be given later in the figures depicting tion ability in the relaxed scenario, which is consistent with
L570: the test results. There are two types of experimental settings, our theorem on the OOD problem.
```

```text
L571: which separately consider the single training environment and 2) Bearing Data Analysis: We observe that all the com-
L572: two training environments. Ten trials are conducted in each pared methods have similar and extremely high accuracies on
L573: experiment to compute the mean accuracy and the standard the training datasets. For a clearer visualization, we only show
L574: deviation. the performances on the test datasets in Fig. 5 (single train-
L575: ing environment setting) and Fig. 6 (two training environments
```

```text
L578: a setting of two training environments than in a one training
L579: 1) Simulation Data Analysis: The classification results of environment setting. It complies with the rule of thumb that
L580: the simulation data are shown in Fig. 4. Generally, both more data encourages more well-behaved invariant features,
L581: SCIRM and ERM perform extremely well on the training and helps to generalize the models [21]. In the single training
L582: dataset. However, they perform differently on the test dataset. environment setting in which the data are collected at speed
```

```text
L589: 1554 IEEE TRANSACTIONS ON CYBERNETICS, VOL. 54, NO. 3, MARCH 2024
L590: Fig. 6. Test results of the classification based on bearing data under the two Fig. 8. Test results of the classification based on gearbox data under the two
L591: training environments setting: (a) result of two training environments (30 and training environments setting; (a) result of two training environments (900 rpm
L592: 50 km/h) and single test environment (200 km/h); (b) and (c) are similarly and 1200 rpm) and one test environment (1500 rpm); (b) and (c) are similarly
```

### Closing evidence
- Sichuan University, Chengdu, Sichuan, China, in neering from the University of Toronto, Toronto,
- 2020. He is currently pursuing the Ph.D. degree with ON, Canada, in 2005.
- the School of Data Science, City University of Hong He is currently a Professor with the College
- Kong, Hong Kong, China. of Electrical Engineering, Sichuan University,
- His current research interests include signal pro- Chengdu, China. In the past years, he received more
- cessing, machine learning, and machinery fault than 40 research grants, and authored or coauthored
- diagnosis. more than 90 research papers and holds 15 patents. His current research
- focuses on reliability and health assessment.
- Dr. Miao has been a Senior Member of the IEEE Reliability Society since
- 2012. He has been with the IEEE RS AdCom since 2019, and has been
- the IEEE RS Vice President since 2020. He acts as an Associate Editor of
- the IEEE TRANSACTIONS ON RELIABILITY and IEEE TRANSACTIONS ON
- INSTRUMENTATION AND MEASUREMENT.
- Kwok-Leung Tsui received the Ph.D. degree
- in statistics from the University of Wisconsin–
- Madison, Madison, WI, USA, in 1986.
- He is a Professor with the Grado Department
- of Industrial and Systems Engineering,
- Virginia Polytechnic and State University,
- Zijun Zhang (Senior Member, IEEE) received the Blacksburg, VA, USA. His current research interests
- B.Eng. degree in systems engineering and engineer- include data science and data analytics, surveillance
- ing management from the Chinese University of in healthcare and public health, personalized
- Hong Kong, Hong Kong, China, in 2008, and the health monitoring, prognostics and systems health
- M.S. and Ph.D. degrees in industrial engineering management, calibration and validation of computer
- from the University of Iowa, Iowa City, IA, USA, models, process control and monitoring, and robust design and Taguchi
- in 2009 and 2012, respectively. methods.
- He is currently an Associate Professor with Dr. Tsui was a recipient of the National Science Foundation Young
- the School of Data Science, City University of Investigator Award. He was the Chair of the INFORMS Section on Quality,
- Hong Kong, Hong Kong. His research focuses on Statistics, and Reliability and the Founding Chair of the INFORMS Section on
- data mining and computational intelligence with Data Mining. He is an Elected Council Member of the International Statistical
- applications in renewable energy, facility energy management, and intelligent Institute, a U.S. Representative to the ISO Technical Committee on Statistical
- transportation domains. Methods, and a Fellow of the American Statistical Association, American
- Dr. Zhang is an Editor of the IEEE TRANSACTIONS ON SUSTAINABLE Society for Quality, International Society of Engineering Asset Management,
- ENERGY and an Associate Editor of the Journal of Intelligent Manufacturing. and Hong Kong Institution of Engineers.
- Authorized licensed use limited to: University of Science & Technology of China. Downloaded on July 05,2026 at 10:04:03 UTC from IEEE Xplore. Restrictions apply.

## Time_Series_Classification_Based_on_Supervised_Contrastive_Learning_and_Homoscedastic_Uncerta
- Extracted chars: 79471

### Opening / abstract evidence
- ===== PAGE 1 =====
- 414 IEEE TRANSACTIONS ON NEURAL NETWORKS AND LEARNING SYSTEMS, VOL. 37, NO. 1, JANUARY 2026
- Time Series Classification Based on
- Supervised Contrastive Learning
- and Homoscedastic Uncertainty
- Tao Zhang , Ke Li , Member, IEEE, and Shaofan Wang
- Abstract—In recent years, contrastive learning (CL) frame- depend on manually crafted features [7], [8], requiring special-
- works have been widely applied to multivariate time series ized knowledge for feature extraction. However, this reliance
- classification (MTSC) tasks. However, existing methods lack task- leads to performance differences due to varying feature extrac-
- specific guidance, leading to limitations in fully capturing the
- tion methods and their limited ability to capture deep-level
- complex dynamics and invariant representations in time series
- information [9]. Modern MTSC methods increasingly utilize
- data. Motivated by the auxiliary tasks in multitask learning
- (MTL) and to fully utilize the rich frequency-domain information deep learning architectures [10], [11], [12], [13], [14], [15].
- of time series data, we propose a novel time series classification These models automatically extract features from raw data
- framework, uncertainty-based time–frequency supervised CL (U- through neural networks, enabling the discovery of complex
- TFSCL). This framework uses SCL in the time and frequency
- patterns. However, the majority of current MTSC methods that
- domains and time–frequency consistency as auxiliary tasks to
- use only instance-level labels and rely on the cross-entropy
- improve the primary task of using only instance-level labels for
- loss function exhibit two critical limitations. First, their deci-
- time series classification. Furthermore, inspired by the homo-
- geneous uncertainty in MTL, we derive a novel uncertainty sion boundaries are prone to overfitting on noisy labels due
- loss function, which automatically adjusts the weights according to the sensitivity of the loss function to mislabeled samples
- to the degree of uncertainty of different tasks to optimize the [16], [17], [18]. Second, the focus on learning discriminative
- learning and prediction process of the model. The proposed
- features neglects the extraction of invariant temporal patterns,
- framework is evaluated on MTSC tasks, including human activity
- resulting in suboptimal generalization performance across
- recognition (HAR), air writing, and gesture recognition. In
- addition, we create a human–drone interaction (HDI) dataset unseen data distributions [19].
- consisting of 20 subjects and conduct real-world experiments The scarcity of high-quality labels in time series domains
- to evaluate the proposed framework. The extensive experiments poses a significant challenge to model training. For instance,
- conducted in various settings verify the effectiveness of the clinical time series data (e.g., ECG, EEG) require expert
- proposed framework.
- physician annotations, but the labeling process remains scarce
- Index Terms—Multitask learning (MTL), multivariate time due to data sensitivity and prohibitive costs. In addition,
- series classification (MTSC), supervised contrastive learning labels may contain noise from doctors’ differing diagnoses
- (SCL). or equipment errors, affecting disease feature learning [20].
- I. INTRODUCTION Contrastive learning (CL) can learn invariant representations
- TIME series data exist in many real-world scenarios, by comparing different views of input samples, thereby reduc-
- ing reliance on high-quality labels and mitigating overfitting
- including wind forecasting [1], stock forecasting [2],

### Section, table, and figure headings detected
- L45: I. INTRODUCTION Contrastive learning (CL) can learn invariant representations
- L172: Fig. 1. Overview of U-TFSCL framework.
- L208: Fig. 2. Schematic of time–frequency domain data augmentation. (a) Original series in time domain. (b) Original series in frequency domain. (c) Augmented
- L247: Fig. 2 illustrates the visualization results of time and
- L433: TABLE I
- L435: Fig. 3. Schematic of gesture movements: (G1) move left, (G2) move right,
- L437: 1) using zero-crossing detection to automatically segment
- L460: Table I shows the details of each gesture; it is clear that
- L478: D. Development and Features of the HDI Gesture Dataset reducing the risk of overfitting, making it more suitable for
- L484: A. Experimental Settings
- L509: TABLE II writing, HAR represents human activity recognition, and G
- L511: C. Experimental Results of the U-TFSCL Framework
- L523: B. Dataset
- L526: Table III shows the model performances under the two test
- L571: D. Ablation Experiment
- L586: Table II shows the details of the datasets used in the were adjusted. Through this process, we can evaluate the
- L595: TABLE III
- L597: TABLE IV
- L633: TABLE V
- L686: Table V presents the results of the ablation studies on the up five different label percentages: 0%, 25%, 50%, 75%, and
- L699: TABLE VI
- L701: Fig. 4. Effect of the number of labels on performance. (a) Generate mask Mc
- L718: Fig. 5. Effect of maximum number of positive pairs per anchor on perfor- designed for frequency-domain features, we applied these aug-
- L739: Fig. 4(b) shows the result. For two test settings, the model
- L756: E. Contrast Experiments
- L773: TABLE VII
- L777: Table VII presents the results of an extensive comparison
- L807: F. Hyperparameter Sensitivity
- L832: G. Computational Cost Analysis
- L857: V. CONCLUSION
- L875: 1) The combination of time- and frequency-domain infor-
- L883: 2) The number of labels used in CL affects the number channels deep convolutional neural networks for multivariate time series

### Evidence snippets: math_formalization

```text
L13: specific guidance, leading to limitations in fully capturing the
L14: tion methods and their limited ability to capture deep-level
L15: complex dynamics and invariant representations in time series
L16: information [9]. Modern MTSC methods increasingly utilize
L17: data. Motivated by the auxiliary tasks in multitask learning
```

```text
L24: use only instance-level labels and rely on the cross-entropy
L25: improve the primary task of using only instance-level labels for
L26: loss function exhibit two critical limitations. First, their deci-
L27: time series classification. Furthermore, inspired by the homo-
L28: geneous uncertainty in MTL, we derive a novel uncertainty sion boundaries are prone to overfitting on noisy labels due
```

```text
L43: series classification (MTSC), supervised contrastive learning labels may contain noise from doctors’ differing diagnoses
L44: (SCL). or equipment errors, affecting disease feature learning [20].
L45: I. INTRODUCTION Contrastive learning (CL) can learn invariant representations
L46: TIME series data exist in many real-world scenarios, by comparing different views of input samples, thereby reduc-
L47: ing reliance on high-quality labels and mitigating overfitting
```

```text
L93: We desire to allow the framework to obtain the ability of on HDI research, consisting of more than 45 000 labeled
L94: robust to noisy time series by using SCL to obtain the sequences.
L95: intrinsic invariant features. Multitask learning (MTL) is a 4) Extensive experiments demonstrate that U-TFSCL
L96: prevalent paradigm for establishing the auxiliary task and achieves SOTA performance on MTSC tasks, outperforming
L97: using the relative information to facilitate the primary task existing methods by an average of 6.7% in classification
```

```text
L97: using the relative information to facilitate the primary task existing methods by an average of 6.7% in classification
L98: [12], [26]. We propose to integrate SCL as an auxiliary accuracy across challenging test settings.
L99: task within the MTL framework to extract invariant temporal The rest of this study is organized as follows. Related works
L100: features. By simultaneously optimizing cross-entropy loss for are briefly reviewed in Section II. In Section III, our U-TFSCL
L101: the primary task and contrastive objectives for the auxiliary and the HDI dataset are introduced in detail. In Section IV, we
```

```text
L114: in the domain of MTSC. However, challenges remain in
L115: increase robustness to noise [28]. Frequency-domain fea-
L116: improving the invariant representations extraction capability
L117: tures, derived via Fourier transformations, serve as effective
L118: and the cross-domain generalization performance. To address
```

```text
L128: a time–frequency dual-domain CL module that optimizes
L129: which transforms time series into 2-D spectrograms, thereby
L130: two complementary objectives: 1) intradomain consistency
L131: incorporating time–frequency information into model inputs
L132: within the time and frequency domains and 2) cross-domain
```

```text
L136: domains. By incorporating instance-level label information
L137: framework that employs time–frequency analysis to extract
L138: into the contrastive objectives, the module balances dis-
L139: features from vibration signals and combine them into input
L140: criminative learning and invariant representation learning;
```

```text
L149: are directly optimized through end-to-end training with
L150: downstream classification tasks, ensuring semantic alignment
L151: between learned features and classification objectives. Fur- B. CL for Time Series
L152: thermore, we adopt the automatic weighting strategy that CL has emerged as a powerful self-supervised framework
L153: balances the loss function by weighting each task according to for learning representations by maximizing similarity between
```

```text
L151: between learned features and classification objectives. Fur- B. CL for Time Series
L152: thermore, we adopt the automatic weighting strategy that CL has emerged as a powerful self-supervised framework
L153: balances the loss function by weighting each task according to for learning representations by maximizing similarity between
L154: the homoscedastic uncertainty [27]. This strategy enables the positive pairs and minimizing dissimilarity between nega-
L155: model to adaptively adjust the weight of each task, allocating tive pairs. CL is extensively used in many fields, including
```

```text
L164: 1) A time–frequency domain contrast module based on SCL time series by assuming negative pairs for distant windows and
L165: fully learns the representation of time series through intratime, positive pairs for neighboring windows. The representation
L166: intrafrequency, and time–frequency domain consistency CL. of the input time series is captured by learning invariant
L167: Authorized licensed use limited to: University of Science & Technology of China. Downloaded on July 05,2026 at 10:02:42 UTC from IEEE Xplore. Restrictions apply.
```

```text
L178: modules. TS2Vec [38] generates different views by random encoder module operating within both the time and frequency
L179: masking operations on time steps and performs a hierarchical domains, a time–frequency domain SCL (TFSCL) module,
L180: CL strategy over augmented views, which enables robust and an MTL module that balances the loss based on task
L181: representations. Khosla et al. [25] extend the self-supervised uncertainty. These components aim to provide a comprehen-
L182: batch contrastive approach to the fully supervised setting, sive and effective approach for analyzing time series data.
```

### Evidence snippets: architecture

```text
L3: ===== PAGE 1 =====
L5: 414 IEEE TRANSACTIONS ON NEURAL NETWORKS AND LEARNING SYSTEMS, VOL. 37, NO. 1, JANUARY 2026
L6: Time Series Classification Based on
L7: Supervised Contrastive Learning
```

```text
L18: (MTL) and to fully utilize the rich frequency-domain information deep learning architectures [10], [11], [12], [13], [14], [15].
L19: of time series data, we propose a novel time series classification These models automatically extract features from raw data
L20: framework, uncertainty-based time–frequency supervised CL (U- through neural networks, enabling the discovery of complex
L21: TFSCL). This framework uses SCL in the time and frequency
L22: patterns. However, the majority of current MTSC methods that
```

```text
L139: features from vibration signals and combine them into input
L140: criminative learning and invariant representation learning;
L141: embeddings for transformers. Furthermore, tight feature align-
L142: it clusters samples from the same class while separating
L143: different classes and enforces invariant feature alignment ment can be achieved by learning the consistency between
```

```text
L154: the homoscedastic uncertainty [27]. This strategy enables the positive pairs and minimizing dissimilarity between nega-
L155: model to adaptively adjust the weight of each task, allocating tive pairs. CL is extensively used in many fields, including
L156: more attention to uncertain and difficult tasks in the training image classification [22], video analysis [33], HAR [34],
L157: process. remote photoplethysmography (rPPG) [35], and time series
L158: To validate the effectiveness of the framework, we con- analysis [18], [23], [24]. Data augmentation is crucial in
```

```text
L169: ===== PAGE 3 =====
L171: 416 IEEE TRANSACTIONS ON NEURAL NETWORKS AND LEARNING SYSTEMS, VOL. 37, NO. 1, JANUARY 2026
L172: Fig. 1. Overview of U-TFSCL framework.
L173: features within the windows as well as differences between III. PRINCIPLE AND METHOD
```

```text
L176: into two views and learn robust representations from the in the time series data, we propose the U-TFSCL framework,
L177: augmented views using temporal and contextual contrasting as shown in Fig. 1. This framework comprises a parallel
L178: modules. TS2Vec [38] generates different views by random encoder module operating within both the time and frequency
L179: masking operations on time steps and performs a hierarchical domains, a time–frequency domain SCL (TFSCL) module,
L180: CL strategy over augmented views, which enables robust and an MTL module that balances the loss based on task
```

```text
L188: achieve better performance than using cross-entropy loss. Within each branch, advanced data augmentation methods are
L189: The closest work to ours is [18], which proposes a novel employed to generate positive and negative sample pairs. Sub-
L190: framework for universal representation learning of multivariate sequently, these pairs are processed using independent encoder
L191: time series using instance-level and cluster-level SCL, aim- modules. These modules consist of several transformer blocks
L192: ing to capture complex patterns and dependencies for better and extract distinct time- and frequency-domain features from
```

```text
L194: on manually weighted loss combinations requiring domain Subsequently, the extracted features are fed into the TFSCL
L195: expertise for tuning, and its two-stage architecture freezes module, which uses SCL to calculate intradomain and interdo-
L196: the pretrained encoder during downstream tasks, restricting main losses and improve the performance of the classification
L197: joint optimization of cross-entropy and contrastive losses task by using the intradomain and interdomain compari-
L198: while neglecting explicit temporal-frequency consistency son tasks as auxiliary tasks. In this module, the time- and
```

```text
L213: model to balance the learning of task-relevant and cross- band. To simplify the discussion, FFT(xT) is denoted as
L214: i
L215: domain features. This balance ensures that the model not xF,G represents the frequency-domain encoder, and hF and
L216: i F i
L217: only captures task-relevant features but also develops a h˜F are the original and augmented view embeddings in the
```

```text
L229: dropout in [24] is used to generate time-domain augmented i.e., (xF, xF) and (xF, x˜F). To facilitate reading and reduce
L230: i j i j
L231: samples x˜T, and the time encoder G is used to map them repetition, in the subsequent content, we use the domain-
L232: i T
L233: to new embeddings, i.e., hT = G (x˜T) and h˜T = G (x˜T). specific superscript D ∈ {T, F}, which includes the time
```

```text
L257: ===== PAGE 5 =====
L259: 418 IEEE TRANSACTIONS ON NEURAL NETWORKS AND LEARNING SYSTEMS, VOL. 37, NO. 1, JANUARY 2026
L260: negative samples; and in this loss, each anchor corresponds to In batch I, which contains 2N samples, i ∈ I¯ ≡ {1, . . . , N}
L261: one positive pair and 2(N − 1) negative pairs. and i ∈ I˜ ≡ {1, . . . , N} denote the indices of the nonaugmented
```

```text
L289: out the negative pairs, which effectively improves the learning
L290: domain embedding zT and frequency-domain embedding zF to
L291: of the embedding hD by the domain-specific encoder G . i i
L292: i D be aligned. The embeddings are then concatenated as inputs
L293: In this study, an approach similar to that in [41] is used,
```

### Evidence snippets: experiment_defense

```text
L10: Abstract—In recent years, contrastive learning (CL) frame- depend on manually crafted features [7], [8], requiring special-
L11: works have been widely applied to multivariate time series ized knowledge for feature extraction. However, this reliance
L12: classification (MTSC) tasks. However, existing methods lack task- leads to performance differences due to varying feature extrac-
L13: specific guidance, leading to limitations in fully capturing the
L14: tion methods and their limited ability to capture deep-level
```

```text
L15: complex dynamics and invariant representations in time series
L16: information [9]. Modern MTSC methods increasingly utilize
L17: data. Motivated by the auxiliary tasks in multitask learning
L18: (MTL) and to fully utilize the rich frequency-domain information deep learning architectures [10], [11], [12], [13], [14], [15].
L19: of time series data, we propose a novel time series classification These models automatically extract features from raw data
```

```text
L23: domains and time–frequency consistency as auxiliary tasks to
L24: use only instance-level labels and rely on the cross-entropy
L25: improve the primary task of using only instance-level labels for
L26: loss function exhibit two critical limitations. First, their deci-
L27: time series classification. Furthermore, inspired by the homo-
```

```text
L31: learning and prediction process of the model. The proposed
L32: features neglects the extraction of invariant temporal patterns,
L33: framework is evaluated on MTSC tasks, including human activity
L34: resulting in suboptimal generalization performance across
L35: recognition (HAR), air writing, and gesture recognition. In
```

```text
L40: proposed framework.
L41: physician annotations, but the labeling process remains scarce
L42: Index Terms—Multitask learning (MTL), multivariate time due to data sensitivity and prohibitive costs. In addition,
L43: series classification (MTSC), supervised contrastive learning labels may contain noise from doctors’ differing diagnoses
L44: (SCL). or equipment errors, affecting disease feature learning [20].
```

```text
L68: and advanced deep learning methods. Most traditional methods
L69: tations of unlabeled time series data [23], [24]. However, in
L70: Received 10 September 2024; revised 26 March 2025; accepted certain instances, they lack task-specific guidance, resulting
L71: 4 September 2025. Date of publication 24 September 2025; date of current in suboptimal performance when applied directly to specific
L72: version 8 January 2026. (Corresponding author: Ke Li.)
```

```text
L71: 4 September 2025. Date of publication 24 September 2025; date of current in suboptimal performance when applied directly to specific
L72: version 8 January 2026. (Corresponding author: Ke Li.)
L73: downstream tasks. To overcome this limitation, incorporating
L74: This work involved human subjects or animals in its research. Approval
L75: of all ethical and experimental procedures and protocols was granted by the labels from existing datasets is an effective strategy. Super-
```

```text
L88: ZHANG et al.: TIME SERIES CLASSIFICATION BASED ON SUPERVISED CL AND HOMOSCEDASTIC UNCERTAINTY 415
L89: [25]. By explicitly maximizing intraclass compactness and 2) A novel MTL module based on contrastive task uncer-
L90: interclass separability, SCL not only enhances discriminative tainty extends the Bayesian probability model based on task
L91: feature learning but also improves robustness to noisy labels uncertainty to SCL.
```

```text
L95: intrinsic invariant features. Multitask learning (MTL) is a 4) Extensive experiments demonstrate that U-TFSCL
L96: prevalent paradigm for establishing the auxiliary task and achieves SOTA performance on MTSC tasks, outperforming
L97: using the relative information to facilitate the primary task existing methods by an average of 6.7% in classification
L98: [12], [26]. We propose to integrate SCL as an auxiliary accuracy across challenging test settings.
L99: task within the MTL framework to extract invariant temporal The rest of this study is organized as follows. Related works
```

```text
L103: discriminative and representation learning paradigms. How- of U-TFSCL and evaluate the impact of each component on the
L104: ever, conventional MTL frameworks are inherently constrained overall performance. Finally, Section V concludes this article
L105: by their reliance on strong task correlations and manual and discusses future work.
L106: hyperparameter tuning for auxiliary task weighting, which
L107: limits generalization in real-world scenarios with diverse noise II. RELATED WORKS
```

```text
L148: intradomain CL [5].
L149: are directly optimized through end-to-end training with
L150: downstream classification tasks, ensuring semantic alignment
L151: between learned features and classification objectives. Fur- B. CL for Time Series
L152: thermore, we adopt the automatic weighting strategy that CL has emerged as a powerful self-supervised framework
```

```text
L151: between learned features and classification objectives. Fur- B. CL for Time Series
L152: thermore, we adopt the automatic weighting strategy that CL has emerged as a powerful self-supervised framework
L153: balances the loss function by weighting each task according to for learning representations by maximizing similarity between
L154: the homoscedastic uncertainty [27]. This strategy enables the positive pairs and minimizing dissimilarity between nega-
L155: model to adaptively adjust the weight of each task, allocating tive pairs. CL is extensively used in many fields, including
```

### Evidence snippets: visualization

```text
L140: criminative learning and invariant representation learning;
L141: embeddings for transformers. Furthermore, tight feature align-
L142: it clusters samples from the same class while separating
L143: different classes and enforces invariant feature alignment ment can be achieved by learning the consistency between
L144: time- and frequency-domain features through cross-domain
```

```text
L171: 416 IEEE TRANSACTIONS ON NEURAL NETWORKS AND LEARNING SYSTEMS, VOL. 37, NO. 1, JANUARY 2026
L172: Fig. 1. Overview of U-TFSCL framework.
L173: features within the windows as well as differences between III. PRINCIPLE AND METHOD
L174: the windows. TS-TCC [37] uses two augmentation methods, A. Overview of the Proposed U-TFSCL Framework
```

```text
L175: strong and weak augmentation, to convert the original series To fully exploit features across the time–frequency domains
L176: into two views and learn robust representations from the in the time series data, we propose the U-TFSCL framework,
L177: augmented views using temporal and contextual contrasting as shown in Fig. 1. This framework comprises a parallel
L178: modules. TS2Vec [38] generates different views by random encoder module operating within both the time and frequency
L179: masking operations on time steps and performs a hierarchical domains, a time–frequency domain SCL (TFSCL) module,
```

```text
L184: clusters of points belonging to the same class are pulled U-TFSCL framework, where they are first converted to their
L185: together in embedding space while simultaneously pushing frequency-domain counterparts using a rapid Fourier trans-
L186: apart clusters of samples from different classes. Tripathi et form. These original and transformed signals are then fed to
L187: al. [39] directly use SCL for air writing recognition and parallel branches for time- and frequency-domain processing.
L188: achieve better performance than using cross-entropy loss. Within each branch, advanced data augmentation methods are
```

```text
L207: ZHANG et al.: TIME SERIES CLASSIFICATION BASED ON SUPERVISED CL AND HOMOSCEDASTIC UNCERTAINTY 417
L208: Fig. 2. Schematic of time–frequency domain data augmentation. (a) Original series in time domain. (b) Original series in frequency domain. (c) Augmented
L209: series in time domain. (d) Augmented series in frequency domain.
L210: After the TFSCL module, the multitask losses are fed into high-frequency components depends on the specificity of the
```

```text
L245: domain is randomly augmented based on the augmentation LD = L i D = − log P exp i (cid:0) hD i · hD/τ (cid:1) (1)
L246: methods in [29]. i∈I i∈I a∈A(i) i a
L247: Fig. 2 illustrates the visualization results of time and
L248: frequency-domain augmentation for a time series sample. where · symbol denotes the dot product and hD and h˜D
L249: i i
```

```text
L433: TABLE I
L434: DETAILS OF THE HDI DATASET
L435: Fig. 3. Schematic of gesture movements: (G1) move left, (G2) move right,
L436: (G3) hover, (G4) move up, (G5) move down, and (G6) move forward.
L437: 1) using zero-crossing detection to automatically segment
```

```text
L483: (G2) Move Right, (G3) Hover, (G4) Move Up, (G5) Move
L484: A. Experimental Settings
L485: Down, and (G6) Move Forward; Fig. 3 illustrates the move-
L486: ment of each gesture. In this task, participants were required The superiority of the framework is validated across exten-
L487: to control drone flight trajectories through six predefined hand sive and widely used MTSC datasets in various domains.
```

```text
L688: egy exhibited the best performance. This may be attributed to degrade to SimCLR [22], and when the percentage is set to
L689: the process of dynamically adjusting the weights for each task 100%, it becomes the standard SCL [25].
L690: and aligning them with the specific attributes of the dataset. Fig. 4(a) illustrates the generation of the matrix M ∈
L691: c
L692: This strategy ensures that the model adapts its focus based on {0, 1}L×L, which is used as the mask to calculate the total
```

```text
L699: TABLE VI
L700: EFFECT OF DIVERSE AUGMENTATION STRATEGIES
L701: Fig. 4. Effect of the number of labels on performance. (a) Generate mask Mc
L702: by limiting the number of labels involved in the loss calculation. (b) Accuracy
L703: as a function of the percentage of labels. Standard and LOSO mean two test
```

```text
L716: original article. Considering that all these strategies performed
L717: augmentation in the time domain and were not specifically
L718: Fig. 5. Effect of maximum number of positive pairs per anchor on perfor- designed for frequency-domain features, we applied these aug-
L719: mance in AW-B dataset. Red markers represent the best accuracy. Standard mentation strategies to the original time signal xT to generate
L720: and LOSO mean two test methods. the augmented view x˜T. We then generated the fr i equency data
```

```text
L737: denoted M = M ⊕ I.
L738: c y performance. Therefore, we adopt for using a dropout ratio
L739: Fig. 4(b) shows the result. For two test settings, the model
L740: of 0.1 in our method. Additionally, the performance of the
L741: performance improves as the percentage of labels increases.
```

### Closing evidence
- China, in 2008.
- ing recognition,” IEEE Sensors Lett., vol. 6, no. 2, pp. 1–4, Feb. 2022,
- doi: 10.1109/LSENS.2021.3139473. From 2008 to 2010, he was a Post-Doctoral
- Researcher at the Institute of Fluid Mechanics, Bei-
- [40] R. Soklaski, M. Yee, and T. Tsiligkaridis, “Fourier-based augmen-
- hang University. From 2012 to 2014, he conducted
- tations for improved robustness and uncertainty calibration,” 2022,
- research as a Visiting Scholar at The Univer-
- arXiv:2202.12412.
- sity of North Carolina at Chapel Hill, Chapel
- [41] A. Radford et al., “Learning transferable visual models from natural
- Hill, NC, USA. He is currently a Professor and
- language supervision,” in Proc. ICML, 2021, pp. 8748–8763.
- the Director of the Experimental Teaching Cen-
- [42] K. He, H. Fan, Y. Wu, S. Xie, and R. Girshick, “Momentum contrast for
- ter, Beihang University. His research interests include theory and engi-
- unsupervised visual representation learning,” in Proc. IEEE/CVF Conf.
- neering of human–machine–environment intelligent systems, data mining,
- Comput. Vis. Pattern Recognit. (CVPR), Jun. 2020, pp. 9729–9738.
- human–machine hybrid intelligent methods, and applications of machine
- [43] M. Obaid, F. Kistler, G. Kasparavicˇiu¯te, A. E. Yantac¸, and M. Fjeld, learning.
- “How would you gesture navigate a drone?: A user-centered approach
- to control a drone,” in Proc. 20th Int. Academic Mindtrek Conf., Oct.
- 2016, pp. 113–121, doi: 10.1145/2994310.2994348. Shaofan Wang received the B.S. degree in mechan-
- [44] M. Seuter, E. R. Macrillante, G. Bauer, and C. Kray, “Running with ical engineering from Shandong University, Jinan,
- drones: Desired services and control gestures,” in Proc. 30th Austral. China, in 2015, the M.S. degree in mechanical
- Conf. Comput.-Human Interact., Dec. 2018, pp. 384–395, doi: 10.1145/ engineering from Karlsruhe Institute of Technology,
- 3292147.3292156. Karlsruhe, Germany, in 2019, and the Ph.D. degree
- [45] J. P. Va´sconez, L. I. Barona Lo´pez, A´ . L. Valdivieso Caraguay, and from the Department of Human-Machine and Envi-
- M. E. Benalca´zar, “Hand gesture recognition using EMG-IMU signals ronmental Engineering, Beihang University, Beijing,
- and deep Q-networks,” Sensors, vol. 22, no. 24, p. 9613, Dec. 2022, China, in 2025.
- doi: 10.3390/s22249613. His research interests include applications of
- [46] A. Bagnall et al., “The UEA multivariate time series classification deep learning, deep reinforcement learning, and
- archive, 2018,” 2018, arXiv:1811.00075. human–robot interaction methods.
- Authorized licensed use limited to: University of Science & Technology of China. Downloaded on July 05,2026 at 10:02:42 UTC from IEEE Xplore. Restrictions apply.
