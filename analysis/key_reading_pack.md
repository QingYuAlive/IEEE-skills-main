# Key Reading Pack for IEEE Corpus

Continuous line ranges extracted from every full-text PDF.

## A_Multidataset_Characterization_of_Window-Based_Hyperparameters_for_Deep_CNN-Driven_sEMG_Pattern_Recognition.txt
- Total extracted lines: 718

### Lines 1-45

```text
L3: ===== PAGE 1 =====
L5: IEEE TRANSACTIONS ON HUMAN-MACHINE SYSTEMS, VOL. 54, NO. 1, FEBRUARY 2024 131
L6: A Multidataset Characterization of Window-Based
L7: Hyperparameters for Deep CNN-Driven
L8: sEMG Pattern Recognition
L9: Frank Kulwa , Student Member, IEEE, Haoshi Zhang , Oluwarotimi Williams Samuel , Senior Member, IEEE,
L10: Mojisola Grace Asogbon , Member, IEEE, Erik Scheme , Senior Member, IEEE,
L11: Rami Khushaba , Senior Member, IEEE, Alistair A. McEwan , and Guanglin Li , Senior Member, IEEE
L12: Abstract—The control performance of myoelectric prostheses (window length and overlap) employed for the construction of raw
L13: would not only depend on the feature extraction and classification two-dimensional (2-D) surface electromyogram (sEMG) signals on
L14: algorithms but also on interactions of dynamic window-based hy- the performance of CNNs when used for motion intent decoding.
L15: perparameters (WBHP) used to construct input signals. However, Moreover,weexaminedtherelationshipbetweenthewindowlength
L16: the relationship between these hyperparameters and how they of the 2-D sEMG and three commonly used CNN kernel sizes.
L17: influence the performance of the convolutional neural networks To ensure high confidence in the findings, we implemented three
L18: (CNNs) during motor intent decoding has not been studied. There- CNNs, which are variants of the existing models, and a newly
L19: fore, we investigated the impact of various combinations of WBHP proposed CNN model. Experimental analysis was conducted using
L20: threedistinctbenchmarkdatabases,twofromupperlimbamputees
L21: and one from able-bodied subjects. The results demonstrate that
L22: Manuscript received 3 August 2023; accepted 27 October 2023. Date of
L23: the performance of the CNNs improved as the overlap between
L24: publication 14 December 2023; date of current version 26 January 2024.
L25: This work was supported in part by the Key-Area Research and Development consecutively generated 2-D signals increased, with 75% over-
L26: Program of Guangdong Province under Grant 2020B0909020004, in part by lap yielding the optimal improvement by 12.62% accuracy and
L27: the National Natural Science Foundation of China under Grant #62150410439, 39.60% F1-score compared to no overlap. Moreover, the CNNs
L28: in part by Guangdong Basic and Applied Research Foundation under Grant performance was better for kernel size of seven than three and
L29: #2023A1515011478, in part by the Science and Technology Program of Guang- five across the databases. For the first time, we have established
L30: dong Province under Grant #2022A0505090007, in part by the Ministry of with multiple evidence that WBHP would substantially impact the
L31: Science and Technology, Shenzhen under Grant #QN2022032013L, and in
L32: decoding outcome and computational complexity of deep neural
L33: part by the ANSO Scholarship for Young Talented Students, “The Belt and
L34: networks, and we anticipate that this may spur positive advance-
L35: Road” Innovative Talent Exchange Program for Foreign Experts under Grant
L36: ment in myoelectric control and related fields.
L37: DL2022024002L and Jinan 5150 Program for Talents Introduction. This article
L38: was recommended by Associate Editor X. Hu. (Frank Kulwa and Haoshi
L39: Index Terms—Convolution neural network (CNN), prostheses,
L40: Zhang contributed equally to this work.) (Corresponding authors: Oluwarotimi
L41: surface electromyogram (sEMG) signal, upper limb, window
L42: Williams Samuel; Guanglin Li.)
L43: This work involved human subjects or animals in its research. Approval length, window overlap.
L44: of all ethical and experimental procedures and protocols was granted by the
L45: Institutional Review Board of Shenzhen Institutes of Advanced Technology,
```

### Lines 96-125

```text
L96: The sEMG-based gesture classification task can be modeled of CNNs. Besides, the CNN models employed are simple and
L97: as a 2-D signal recognition problem using convolutional neural low memory enabling practical deployment in upper limb pros-
L98: networks (CNNs), where the input signal to the CNNs has a size theses. Also, we explored the effects of varying kernel sizes on
L99: of J × W (length x width). Many techniques have been used the classification performance of different CNN models. The ex-
L100: to construct 2-D signals from sEMG, which serve as input to perimentation was carried out using sEMG from three different
L101: deep learning models. For instance, 2-D signals have been con- databases comprising amputees and able-bodied individuals that
L102: structedbasedonspectrogramsobtainedfromshort-timeFourier are mostly used for EMG gesture characterization. Moreover,
L103: transforms [14], scalograms obtained from wavelet transforms the databases include both HD-sEMG and sparse multichannel
L104: [15], and construction from engineered features [16]. Other sEMG signals and contain various degrees of freedom move-
L105: methods include high-density sEMG (HD-sEMG) electrode ar- mentsassociatedwiththefinger,hand,wrist,andelbowgestures,
L106: ray topology (where the 2-D resembles an array of electrode which ensures proper coverage. The four primary contributions
L107: placement during data collection) [17], and from raw sEMG of this work are as follows.
L108: signal segments using overlapping time windows [18] (where 1) To provide insight on the deployment of novel and efficient
L109: the signal width is equal to the number of electrodes and the deep learning driven prostheses control scheme, this study
L110: length matches the segmentation window length). However, the explored the impact of the raw 2-D signals’ window length
L111: use of spectrogram, scalogram and 2-D from engineered features and overlap on the performance of CNNs.
L112: impose extra preprocessing time. While the raw EMG as input 2) We explore the effects of receptive window for different
L113: to CNNs represents a seamless and direct approach, several configurations of CNNs and how they influence the feature
L114: studies have leveraged this option towards attaining fairly decent learning on the raw 2-D signal.
L115: classification performance [16], [18]. This partly motivated us to 3) To aid the optimal selection of window parameters, we
L116: further explore the potential impact of 2-D signals constructed derived a rule of thumb on the relationship between kernel
L117: from raw EMG recordings on CNNs for movement intent de- sizes and window parameters.
L118: coding, which may be necessary in developing time-efficient 4) We proposed a novel variant of CNN model characterized
L119: and intuitive deep learning driven prosthetic control schemes. by low computational complexity with simple yet robust,
L120: Recent research has confirmed that 2-D signals’ temporal and accurate decoding performance.
L121: and spatial information can be used by CNN to extract long
L122: and short-term patterns present in sEMG recordings [17], [19],
L123: [20]. With respect to sparse and high-density surface EMG II. MATERIAL AND METHODS
L124: recordings, previous studies have proposed CNN-based models
L125: A. Description of the EMG Databases Utilized
```

### Lines 198-325

```text
L198: C. Convolution Neural Networks
L199: exercise B, which contains 17 classes of movements comprising
L200: 9 basic wrist movements and 8 isotonic isometric hand gestures. This study built four different CNN models to investigate
L201: Each movement gesture lasted 5 s with 6 repetitions, followed by the impact of varied configurations of 2-D sEMG. Among
L202: 3 s of rest. We directly worked with the preprocessed data, which the four CNNs, Model1 has similar architecture to the model
L203: was sampled at 2000 Hz, filtered with a notch filter of 50 Hz and implementedinourpreviouswork[34].Meanwhile,Model2and
L204: a band pass filter of 20–450 Hz [31]. Table I Summarizes the Model3 are built as variants of existing models and the fourth
L205: difference in the parameters of the three databases used in this (Model4) is entirely proposed by the authors. The architectures
L206: study. of the models are as follows.
L207: Authorized licensed use limited to: University of Science & Technology of China. Downloaded on July 05,2026 at 09:59:05 UTC from IEEE Xplore. Restrictions apply.
L209: ===== PAGE 4 =====
L211: 134 IEEE TRANSACTIONS ON HUMAN-MACHINE SYSTEMS, VOL. 54, NO. 1, FEBRUARY 2024
L212: Model1: Model1 is built based on the CNN model imple-
L213: mented in our preliminary work [34]. Our decision for con-
L214: sidering this network is due to its simple structure and stable
L215: performance. In addition, it takes as input a shape that aligns
L216: with the shape of our 2-D sEMG representation (J x W).
L217: Model2: Inspired by the simplicity of the model proposed
L218: by Bakırcıog˘lu and Özkurt [16], we adopted its feature learn-
L219: ing convolution blocks in building our own CNN variant and
L220: replaced the flattening layer in Bakırcıog˘lu and Özkurt’s net-
L221: work with a global-max pooling, which comparably reduces the
L222: network parameters (to enhance its computational cost) and is
L223: not prone to overfitting [35]. Thus, the Model2 consists of three
L224: convolution blocks each having 80, 100, and 120 nodes with
L225: Fig. 3. Proposed multiscale convolution neural network (MS-CNN). D repre-
L226: similar values of kernel sizes, respectively. Succeeding each
L227: sents the dilation rate.
L228: convolution block is a batch normalization and a max-pooling
L229: layers that allows down sampling of the feature maps by half.
L230: The lower part of the network consists of the global max-pooling
L231: layer for feature reduction and a dense layer of 512 nodes for
L232: high-level feature learning.
L233: Model3: It is an improved version of the network proposed
L234: by Maufroy and Bargmann [36] that comprised two convolu-
L235: tion layers and a fully connected layer each having 100 nodes
L236: designed specifically for 1-D EMG signal processing. Thus, we
L237: came up with a variant of the network by replacing the 1-D
L238: convolution layers with 2-D convolution layers and discarded
L239: the dropout layers after each convolution except after the fully
L240: connected layer. Each convolution is followed by a batch nor- Fig. 4. Conceptualization of dilation: The convolution kernel (L) = 3 × 3 and
L241: malization and max-pooling layer of 2 × 2. Similar to Model2, its dilated filters when dilation rate (D) = 1, 2, and 3.
L242: feature reduction is achieved by using the global max-pooling
L243: layer. Because the networks are trained from scratch, we have the concatenation layer without dimension reshaping while
L244: applied weights initialization in both Model2 and Model3 to al- max-pooling is applied to extract the most essential joint
L245: low quick convergence and optimization of the networks [37]. It features. The second multiscale block (Block 2) has a similar
L246: should be noted that the classification in both networks (Model2 operation to Block 1.
L247: and Model3) is performed using a Softmax layer. The subsequent Block 3 contains two point-wise 1 × 1 con-
L248: Model4 (Multiscale CNN) abbreviated as MS-CNN: The con- volutions. These convolutions enable the network to learn more
L249: volution kernels can be treated as view windows of the network, about the joint features from the multiscale blocks while keeping
L250: large size kernels meaning that the network can view 2-D signal the number of network parameters low [41]. The lower part of
L251: at a large dimension (which includes both spatial information the network incorporates a global max-pooling layer, one fully
L252: across channels, and temporal information within channels) at connected layer of 128 nodes, and the classification layer that
L253: once and learn large grained features, likewise, small kernels can employs a Softmax function. Additionally, all the weights were
L254: model fine features of the signal [38]. Therefore, in this study, initializedusingarandomuniforminitializer.Thekeyoperations
L255: we proposed a MS-CNN model, which combines the advantage of the proposed Model4 are described in Sections II-C1) and
L256: of small and large size kernels to improve the classification II-C2).
L257: performance by learning both fine and large-grained patterns 1) Dilated Convolution Layer for Multiscale and Memory
L258: from the signal while keeping the network parameters as low as Efficiency: Dilated convolution layer is a layer that uses larger
L259: possible. Moreover, inspired by the dilated convolution kernel 2-Dfilterstoextendthestandardconvolutionlayer. Fig.4depicts
L260: concept [39], we have utilized them as core layers to achieve the the conceptual representation of a typical dilation process in
L261: multiscale task. The architecture of the proposed network herein the context of the proposed MS-CNN. In order to optimize
L262: referred to as Model4 is presented in Fig. 3. the number of network parameters, traditional CNNs exploit
L263: The essential functional layers in the MS-CNN (see Fig. 3) convolution with small filters (2 × 2 or 3 × 3). However, di-
L264: are the multiscale block 1 and block 2 composed of dilated lated convolution filters are an easy approach to generating
L265: convolution layers at different scales (dilation rates) to enable an a CNN with large filters such as 5 × 5, 7 × 7. while keeping
L266: exponential increase of large receptive fields without loss of out- the parameters similar to 2 × 2 or 3 × 3 kernels. A dilated
L267: put resolution [40]. The input to the network is fed to block1 via convolution with an enlargement rate of d places d − 1 zeros
L268: two means including the upper and lower paths with each having in between successive filter values, which results in enlarging
L269: its own scales. Meanwhile, the upper path contains convolution the size of a L filter to [ L + (L − 1)(d − 1)(d − 1)]. It should
L270: with kernel size = 3 and dilation = 1 to model fine features. be noted that the quantity of nonzero parameters remains equal
L271: The lower path contains convolution with kernel size = 3 and as before. In addition, the dilated filters significantly expand
L272: dilation = 4, which is equivalent to the conventional kernel of CNN’s receptive field, allowing it to capture more contextual and
L273: size = 9 with output resolution equivalent to 3 × 3 convolution. spatialinformation[42].Asaresult,itenablesflexiblemultiscale
L274: Such a large kernel can learn coarse (general) features from contextual information aggregation while maintaining the same
L275: the input. The outputs of the two paths are combined by resolution.
L276: Authorized licensed use limited to: University of Science & Technology of China. Downloaded on July 05,2026 at 09:59:05 UTC from IEEE Xplore. Restrictions apply.
L278: ===== PAGE 5 =====
L280: KULWA et al.: MULTIDATASET CHARACTERIZATION OF WBHP FOR DEEP CNN-DRIVEN SEMG PATTERN RECOGNITION 135
L281: TABLE II TABLE III
L282: NUMBER OF EPOCHS FOR EACH MODEL AND DATABASE EXPERIMENTAL ANALYSES PERFORMED FOR THE THREE PARAMETERS FOR
L283: DIFFERENT MODELS (THE PARAMETERS WERE THE SAME FOR EVERY
L284: SUBJECT)
L285: 2) Handling Internal Covariant Shift Within the MS-CNN:
L286: A major challenge of nonstationary signals such as the sEMG
L287: is the lack of a common distribution, which sometimes result myoelectric pattern recognition. Additionally, to verify the sta-
L288: in internal covariant shift within the network [43]. To resolve tistical significance of the proposed method, a nonparametric
L289: this issue, batch normalization layers were introduced after Friedman’s test was conducted followed by Dunn’s post hoc
L290: each convolution block, and the exponential linear unit (ELU) test. The definitions for the metrics are indicated in
L291: activation function was leveraged afterwards in requisite layers. TP + TN
L292: Thus, the ELU activation function is expressed mathematically, Accuracy = (2)
L293: TP + FP + TN + FN
L294: as shown in
L295: (cid:2) 2TP
L296: f ELU (x k ) = ∝ x k (exp (x ) − 1) ( (x x k > ≤ 0 0 ) ) (1) F1 − score = 2TP + FP + FN . (3)
L297: k k
L298: From (2) and (3), true negative (TN) and true positive (TP)
L299: where x k is the filter output in the kth channel and ∝ represents are the number of accurately classified negative and positive
L300: a parameter to control the value to which an ELU saturates for
L301: samples, respectively. The number of positive cases classified as
L302: negative inputs. In this study, the default value ∝= 1 was con-
L303: negative is a false negative (FN), while the number of negative
L304: sidered. For negative inputs, the ELU activation function returns
L305: samples predicted as positive is false positive (FP).
L306: negative values, as a result its mean (average) outputs approach
L307: zero than that of ReLU. Hence, the ELU activation function
L308: can improve network learning [44]. Thus, in the MS-CNN, III. RESULTS AND ANALYSIS
L309: each pointwise convolution is followed by an ELU activation
L310: A. Analyzing the Impact of Window Length and Overlap on
L311: function.
L312: the Performance of the CNNs.
L313: In this section, we investigated whether or not the 2-D signals
L314: D. Experimental Setups
L315: constructed from varied combinations of window length (W)
L316: Since the Adam Optimizer [45] demonstrated the best net- and overlap (V) would impact the decoding performance of
L317: work performance (in our preliminary/pilot experiments of find- CNNs. For each experiment, the W was kept constant while
L318: ing the optimal hyperparameters for the models) compared to varying the V and vice versa. And the corresponding signals
L319: the stochastic gradient descent optimizer [46], all the described were used to train the built CNNs described in Section II-C. For
L320: models were trained using Adam Optimizer with a learning instance, 2-D signals obtained from W of 175 ms and an overlap
L321: rate of 0.0001. It should also be noted that at least one subject of “75% of W” were employed to train and test a CNN with
L322: from each DB was used to get the optimal hyperparameters a kernel size of 3. Similarly, the impact of other combinations
L323: for the models during preliminary experiments. Besides, due of W and V across kernel sizes on the CNNs was examined.
L324: to its superior performance in multiclass tasks, the categorical Meanwhile, the experiments were carried out for each of the
L325: cross-entropy [47] was utilized as the loss function. The number databases described in Section II-A and the obtained results are
```

### Lines 332-445

```text
L332: To analyze the impact of kernel size on the performance of are presented in Fig. 5 in accuracy and Table IV in F1-score.
L333: the CNNs per time, the same size of the kernel was applied to all Analyzing the results in [see Fig. 5(a)], it can be seen that
L334: convolution layers of the models. Hence, we utilized kernel sizes the accuracy in every CNN improves when the percentage of
L335: of 3 × 3, 5 × 5, and 7 × 7 since they are the basic kernels that overlap (V) increases at constant window length (W) and kernel
L336: have been employed in prior studies and yielded relatively good size (K). For instance, the accuracy of Model1 at W = 25 ms
L337: performances [14], [16], [18], [21], [22]. It should be noted that increases from 97.22%, 97.79%, 98.32%, to 98.74% when V
L338: Model4, utilizes kernels with resolution equivalent to 3. Thus, increases from 0 V, 0.25 V, 0.50 V, to 0.75 V, respectively. This
L339: it was not included in experiments involving the variation of indicates a significant improvement upon statistical analysis re-
L340: kernels 5 × 5 and 7 × 7. sults when comparing overlap 0 V and 0.75 V (p-value: 7x10−6).
L341: Evaluation Measures When investigating the effects of varying W at constant V in a
L342: To analyze the performance of the different networks, we particular model, the results show no considerable difference.
L343: used benchmark evaluation metrics that include accuracy and For instance, in Model1, the performances at the overlap of
L344: F1-score, as they have been widely adopted in the field of 0.75 are 98.74%, 98.88%, 98.84%, 98.86%, 98.84%, 98.74%,
L345: Authorized licensed use limited to: University of Science & Technology of China. Downloaded on July 05,2026 at 09:59:05 UTC from IEEE Xplore. Restrictions apply.
L347: ===== PAGE 6 =====
L349: 136 IEEE TRANSACTIONS ON HUMAN-MACHINE SYSTEMS, VOL. 54, NO. 1, FEBRUARY 2024
L350: (a) (b)
L351: Fig. 5. Classification accuracy of Model1, Model2, Model3, and Model4, when they are applied to DB1. (a) Each subpart in the graphs contains results of all
L352: models at the same window length and varied overlaps 0 V, 0.25 V, 0.50 V, and 0.75 V, which are equivalent to 75% of W, 50% of W, 25% of W, and 0% of W.
L353: Note: Window length (W) unit is in millisecond (ms). (b) Average classification results across window lengths. (a) The classification accuracy for every window
L354: length at varied overlaps. Kernel = 3. (b) Average accuracy accross window lenghts. Kernel = 3.
L355: TABLE IV
L356: CLASSIFICATION F1-SCORE OF MODEL1, MODEL2, MODEL3, AND MODEL4 AT KERNEL SIZE=3 WHEN APPLIED ON DB1
L357: 98.79%, and 98.91% at W of 25 ms, 50 ms, 75 ms, 100 ms, B. Analyzing the Effect of Network Receptive Fields Against
L358: 125 ms, 150 ms, 175 ms, and 200 ms, respectively. To further the Generated 2-D sEMG Signals.
L359: examine this phenomenon, the F1-score results in Table IV also
L360: show that the model’s performance improved by increasing the The effect of each model’s kernel size on different 2-D
L361: percentage of overlap at constant window length. Similarly, the sEMG signals constructed using varied windowing parameters
L362: average results displayed in Fig. 5(b)(accuracy) and Table IV was investigated in this section. The experiments were carried
L363: (F1-score), show that the overlap of 75% (0.75 V) achieved out by varying kernel sizes (3, 5, and 7) while keeping each
L364: much better classification results for upper limb MI decoding window length constant and the networks were configured to
L365: irrespective of the window length. utilize a specific kernel size per training phase. Due to the
L366: To further validate the abovementioned results, we conducted relatively stable and higher performances observed when the
L367: the experiments using amputee databases (D2 and DB3) whose overlap was 75%, only this overlap was reported in this section
L368: results are presented in Figs. 6 and 7 in accuracy, and Table V for brevity. Moreover, due to the architecture of Model4, which
L369: and 6 in F1-score, respectively. The accuracy results in Figs. 6 only incorporates kernels with a resolution equivalent to 3, it was
L370: and 7(for DB2 and DB3, respectively), show that the perfor- excluded from the analysis in the section for a fair comparison.
L371: mance of all the networks increases with an increase in overlap Thus, the F1-score results for three models at different kernel
L372: at a fixed window size per time with statistical significance sizes when 2-D signals were generated from DB1, DB2, and
L373: of p = 4.0x10−6, 3.0x10−6, 3.0x10−6, 7.9x10−5 for model1, DB3 are presented in Fig. 8.
L374: model2, model3, and model4 in DB2, respectively. While Based on analysis of the results for DB1 presented in Fig. 8(a),
L375: p = 3.62x10−4, 2.4x10−5, 2.8 x10−5, 8.26x10−3 were observed in general, the kernel size of 7 yields better classification per-
L376: in DB3 for model1, model2, model3, and model4, respectively, formance across the networks (Model1, Model2, and Model3)
L377: when comparing the results of overlap 0v and 0.75. Also, the as the window length increases from 25 ms to 200 ms.
L378: F1-score values in Tables V and VI depict similar trend, fur- Also, the trend of increment for kernel sizes of 3, 5, and 7 can
L379: ther corroborating the phenomenon observed for the accuracy be observed to be similar in all the models except at window
L380: metrics. 175 in Model1 and Model2, and window 125 in Model3, where
L381: Authorized licensed use limited to: University of Science & Technology of China. Downloaded on July 05,2026 at 09:59:05 UTC from IEEE Xplore. Restrictions apply.
L383: ===== PAGE 7 =====
L385: KULWA et al.: MULTIDATASET CHARACTERIZATION OF WBHP FOR DEEP CNN-DRIVEN SEMG PATTERN RECOGNITION 137
L386: (a) (b)
L387: Fig. 6. Classification accuracy of Model1, Model2, Model3, and Model4, when they are applied to DB2. (a) Each subpart in the graphs contains results of all
L388: models at the same window length and varied overlaps 0 V, 0.25 V, 0.50 V, and 0.75 V, which are equivalent to 75% of W, 50% of W, 25% of W, and 0% of W. Note:
L389: Window length (W) unit is in millisecond (ms). (b) Average classification results across window lengths. (a) Classification accuracy of every window length at
L390: varied overlaps. Kernel = 3. (b) Average accuracy accross window lengths. Kernel = 3.
L391: (a) (b)
L392: Fig. 7. Classification (in accuracy) of Model1, Model2, Model3, and Model4, when they are applied to DB3. (a) Each subpart in the graphs contains results of
L393: all models at the same window length and varied overlaps 0 V, 0.25 V, 0.50 V, and 0.75 V, which are equivalent to 75% of W, 50% of W, 25% of W, and 0% of
L394: W. Note: Window length (W) unit is in millisecond (ms). (b) Average classification results across window lengths. (a) Classification accuracy for every window
L395: length at varied overlaps. Kernel = 3. (b) Average accuracy accross window lengths. Kernel = 3.
L396: TABLE V
L397: CLASSIFICATION F1-SCORE OF MODEL1, MODEL2, MODEL3, AND MODEL4 AT KERNEL SIZE=3 WHEN APPLIED ON DB2
L398: kernel 5 recorded an average F1-score value that is better than is no significant and consistent (increase) effect when varying
L399: that of kernel 7. The average performance shows that kernel size window length (at constant kernel) in the network’s performance
L400: of 3 led to the least classification results in all the CNNs. Besides, in this database (DB1) except from window 25 to 50 ms for
L401: the statistical analysis between kernel 3 and 7 show a significant Model1, and from 25 to 75 ms for Model2 and Model3.
L402: improvement of p = 0.9.92x10−4, 1.30x10−3, and 1.83x10−2. By closely analyzing the variation of kernel sizes and window
L403: Although the impact is realized when varying kernel sizes, there lengths for DB2 in Fig. 8(b), an increase in the performance of
L404: Authorized licensed use limited to: University of Science & Technology of China. Downloaded on July 05,2026 at 09:59:05 UTC from IEEE Xplore. Restrictions apply.
L406: ===== PAGE 8 =====
L408: 138 IEEE TRANSACTIONS ON HUMAN-MACHINE SYSTEMS, VOL. 54, NO. 1, FEBRUARY 2024
L409: TABLE VI
L410: CLASSIFICATION F1-SCORE OF MODEL1, MODEL2, MODEL3, AND MODEL4 AT KERNEL SIZE=3 WHEN APPLIED ON DB3
L411: Fig. 8. Classification performance of Model1, Model2, and Model3 while varying the network kernels (3, 5, and 7) at different 2-D signal lengths (W) of 25, 50,
L412: 75, 100, 125, 150, 175, and 200 of DB1, DB2, and DB3. AV is the average results across all window lengths. Note: Window length (W) unit is in millisecond
L413: (ms). (a) Variation of kernel sizes and window lengths in DB1. (b) Variation of kernel sizes and window lengths in DB2. (c) Variation of kernel sizes and
L414: window lengths in DB3.
L415: every model is realized when the size of kernels increases from impact in the performance of CNNs especially in Model2 and
L416: 3, 5 to 7. The observation in this database shows that the use Model3 where the graphs show a positive gradient with the
L417: of large-size kernels improves the CNN’s performance signif- increase in window lengths for all window sizes (from 25 ms
L418: icantly (with p<0.05 in all models) regardless of the window to 200 ms) in Model2, and from 100 ms to 200 ms in Model2 at
L419: length. Moreover, the variation of window lengths shows an constant kernel size.
L420: Authorized licensed use limited to: University of Science & Technology of China. Downloaded on July 05,2026 at 09:59:05 UTC from IEEE Xplore. Restrictions apply.
L422: ===== PAGE 9 =====
L424: KULWA et al.: MULTIDATASET CHARACTERIZATION OF WBHP FOR DEEP CNN-DRIVEN SEMG PATTERN RECOGNITION 139
L425: From the results illustrated in Fig. 8(c) for DB3, the perfor-
L426: manceofeverymodelincreaseswiththeincreaseinkernelsizeat
L427: constant window length. Although the database contains signals
L428: from amputees, kernel = 7 has achieved good performance.
L429: Comparing the results of kernels 7 and 3 a significant increase
L430: in the performance of the models was observed for DB3 with
L431: p<0.05 in Model 1 and Model3. In that respect the maximum
L432: improvement of 18.46% is observed in Model1 with a window
L433: length of 125 ms, while 8.35% is observed in Model2 with a
L434: window of 75 ms, and 31.75% in Model3 with a window of
L435: 50 ms. Contrary to previous databases (DB1 and DB2), the
L436: effects of increasing window length at constant kernel signif-
L437: icantly increase the performance of the networks when DB3
L438: was utilized. For example, the results in Model1 with a kernel
L439: of 3 improved from 47.48%, 57.81%, 62.42%, 65.42%, 67.09%,
L440: 69.29%, 71.32%, to 72.77% F1-score at window lengths of
L441: 25, 50, 75, 100, 125, 150, 175, and 200 ms, respectively. This
L442: observation correlates with the previous study, which shows that
L443: the impact of window length is more evident in a small number
L444: of channels [26].
L445: C. Analysis of Individual Limb MI Across Window Overlaps
```

### Lines 501-624

```text
L501: TABLE VII IV. DISCUSSION
L502: DELAY TIME (IN SECONDS) OF A SINGLE TRIAL OF MOVEMENT ON DB1
L503: This work investigated the relationship between the length of
L504: the 2-D sEMG signal window and the overlap, which can pro-
L505: duce the network’s best performance. We also studied how CNN
L506: kernel sizes affect the network’s performance on classification
L507: tasks when raw 2-D sEMG signals constructed using different
L508: combinations of window length and overlaps were used as input
L509: to the CNN. The investigation considered four different kinds
L510: of CNN models. It should be noted that, although this study
L511: focused on raw EMG as input to the CNN, we also acknowledge
L512: the potential of using other forms of inputs to the CNN such as
L513: spectrograms [48].
L514: Specifically, the results presented in Section III-A demon-
L515: strated the effects of window overlap and window length of
L516: TABLE VIII the generated 2-D signals on the performance of the CNNs. In
L517: AVERAGE DELAY TIME (SECONDS) OF A SINGLE TRIAL OF MOVEMENT IN DB2 general, the results in Fig. 5 and Table IV, Fig. 6 and Table V,
L518: and Fig. 7 and Table VI for DB1, DB2, and DB3, respectively,
L519: show that the performance of the CNNs is greatly influenced
L520: by the amount of overlap in the generated 2-D signals. Interest-
L521: ingly, the highest overlap achieved the maximum improvement
L522: of 20.91% in DB1, 31.70% in DB2, and 39.60% F1-score in
L523: DB3. Further analysis is presented in Section III-C (see Fig. 9),
L524: which depicts the effects of varying window overlaps and kernel
L525: sizes on the individual motion intention in Fig. 9(a)(for DB1),
L526: Fig. 9(b)(for DB2), and Fig. 9(c)(for DB3). The classification
L527: performances across individual motion intents show that 75%
L528: (0.75 V) of signal overlap has achieved higher performances
L529: in all gestures compared to 0% overlap (0V). This, emphasizes
L530: TABLE IX
L531: that the use of 2-D sEMG signal with large overlaps can achieve
L532: AVERAGE DELAY TIME (SECONDS) OF A SINGLE TRIAL OF MOVEMENT IN DB3
L533: reasonable and practical results for CNN.
L534: On the other hand, the results in Section III-B show that the
L535: effect of window length of 2-D sEMG signals becomes signifi-
L536: cant when the number of channels decreases. In that regard, the
L537: impacts of varying window lengths were not realized when DB1
L538: with 128 channels (signals of size Wx128) was used, as indicated
L539: in Fig. 8(a). The effect started to show up in DB2 (32 channels)
L540: in Fig. 8(b). A consistent and positive impact of window length
L541: is observed in Fig. 8(c) when DB3 (which uses 2-D signals
L542: from 12 channels) was deployed. This finding corroborates the
L543: previous work [26], on engineered features, which also showed
L544: that the effects of window length increase with the decrease in
L545: the number of channels. This relationship is likely described by
L546: latency(programexecutiontime)oftheCNNsbuiltbasedonvar- the feature space in nondense channels (i.e., 12 channels in DB3)
L547: ied combination of window parameters across the kernel sizes, that provide less spatial information, which on the other hand can
L548: as shown in Tables VII, VIII, and IX, for the three databases be compensated by additional temporal information provided by
L549: (DB1, DB2, and DB3), respectively. longer window lengths. But longer window lengths provide less
L550: By closely analyzing the results across one trial of movement benefit to large-channel clusters (i.e., 128 channels in DB1 and
L551: in Tables VII, VIII, and IX, it can be seen that the delay time 32 channels in DB2) that are already more adequately distributed
L552: decreases with a decrease in the overlap. The overlaps of 75% in feature space.
L553: have the highest computation times. Moreover, the increase The CNN’s kernel can be thought of as the network’s eye; the
L554: in kernel size also increases the inference time. DB2 (see Ta- larger the kernel, the larger the network’s receptive field, allow-
L555: ble VIII) has the highest times relative to other databases. While ing it to see more of the signal and identify more widespread
L556: the delay times in DB1 (see Table VII) are all (except for W spatial patterns (features), whereas a smaller kernel size iden-
L557: = 50, 75, and 200 ms at overlap 0.75 V) within an acceptable tifies finer features [22]. The results attained in Fig. 8 indicate
L558: range for the practical application of the prostheses, which is that the increase in kernel size improves the CNN’s performance
L559: stated to be below 200 ms [24]. All delay times in DB3 (see by a significant margin at constant window length, with the
L560: Table IX) are within the acceptable range. Therefore, when con- peak performance attained by kernel = 7. This implied that
L561: sidering the combination of both accuracy and time efficiency the patterns of the sEMG signals can be modeled over a large
L562: of the CNNs for prostheses-based applications, networks with spatial dimension of the signal [49]. Besides, a wide field of view
L563: kernel = 7 and an overlap of 50% would yield reliable operations allows the network to learn hidden temporal connectivity within
L564: in all databases (below 200 ms) and 75% overlap for DB3. the signal [22]. Hence, it can model both spatial and temporal
L565: Authorized licensed use limited to: University of Science & Technology of China. Downloaded on July 05,2026 at 09:59:05 UTC from IEEE Xplore. Restrictions apply.
L567: ===== PAGE 11 =====
L569: KULWA et al.: MULTIDATASET CHARACTERIZATION OF WBHP FOR DEEP CNN-DRIVEN SEMG PATTERN RECOGNITION 141
L570: patterns of the signal. This provides us with an insight that it manufacturing the prostheses, a combination of 75% overlap
L571: may be essential to consider shallow networks but with large with shallow CNN but large kernel sizes (such as 7) would
L572: kernels to have classifiers with high accuracy, which are time provide considerably high accuracy, time, and memory effi-
L573: and memory efficient. ciency. These findings will help assist prostheses manufacturers
L574: Additionally, when we compare the general results across indevelopingmoreefficientsEMG-basedgesturerecognitional-
L575: different databases between the amputees-based database (DB2 gorithms. The newly proposed CNN model yielded significantly
L576: and DB3) and the database containing the able-bodied subjects’ better motor decoding performance than others tested, thus, its
L577: data (DB1). The results obtained in DB1 in all experiments are deployment in prosthetics and other fields such as rehabilitation
L578: relatively higher than in DB2 and DB3. This could be due to the control systems could facilitate multifunctional and intuitive
L579: high quality of the signals collected from able-bodied subjects EMG-PR control schemes. Finally, for the first time, we have
L580: contrary to the amputee subjects, whose signal qualities are been able to establish with substantial evidence through multiple
L581: normally low due to limited residual muscles [50]. However, the experiments that window-based hyper-parameters substantially
L582: applicationofahighpercentageofoverlaps(particularly75%)in impact the decoding outcome and computational complexity of
L583: the generated 2-D signals has improved the classification results deep neural networks. In general, we anticipate that this novel
L584: of DB2 and DB3 to an acceptable level in all Models. Therefore, finding may spur positive development in myoelectric control
L585: a combination of 75% overlap and large kernels such as 7 may and related fields.
L586: have the potential to realize the practical use of CNN-based Transfer learning, where a pretrained model is fine-tuned on a
L587: prostheses. small dataset from the end-application, is an important technique
L588: Furthermore, we estimated the possible delay time of the when using little data (especially human data such as with EMG)
L589: prosthesis microcontroller based on CNNs in relation to the for training deep learning models. In that respect, due to their
L590: window length, overlap, and kernel size on a single trial of simplicity and good performance, we anticipate that the CNN
L591: movement, as indicated in Tables VII, VIII, and IX. The trend models proposed in this study can be useful for transfer learning
L592: shows that the delay time increases with an increase in overlap of parsimonious models in EMG-related fields/tasks such as
L593: and kernel sizes. Besides, we discovered that when considering intersubject and interlimb/hand domain adaptation.
L594: efficiency in time and accuracy, an overlap of 50% and a kernel Despite the merits of the findings observed in this study,
L595: size of 7 can give an ideal response in all tested databases but the analyses were based on offline experiments. Consequently,
L596: with slightly low accuracy compared to 75% overlap, which there is still room for improvement, particularly in the aspect of
L597: gives the highest accuracy (in all databases) with slightly low incorporation of hyperparameters and investigating the variation
L598: efficiency in time, particularly in DB1 and DB2. Hence, such a of window parameters in the performance of the CNN models in
L599: tradeoff between overlaps of 50% and 75% could be taken into an online setting. In our future study, we hope to further validate
L600: account by the prosthesis manufacturers. In general, the analysis the findings of the study and the performance of the proposed
L601: presented in this study leads to the following rule of thumb: The CNN network in an online setting, taking factors that may
L602: overall decoding performance of convolutional neural networks impact the real-time control performance of the multifunctional
L603: is observed to be highly dependent on the window based hyper- prostheses into consideration.
L604: parameters including overlap and kernel size, which validates
L605: our hypothesis.
L606: Finally, we compared the relative performance of the pro-
L607: posed model MS-CNN (Model4) and other models, which have
L608: been used in the study (Model1, Model2, and Model3). Con- REFERENCES
L609: sidering the average classification results depicted in Figs. 5(b),
L610: 6(b), and 7(b), it can be observed that the proposed Model4 [1] E. Nsugbe, C. Phillips, M. Fraser, and J. McIntosh, “Gesture recognition
L611: fortranshumeral prosthesiscontrol usingEMGand NIR,” IETCyber-Syst.
L612: achieved the highest performances in all overlaps in DB1 [see
L613: Robot., vol. 2, no. 3, pp. 122–131, 2020.
L614: Fig. 5(b)], in DB2 [see Fig. 6(b)] for all overlaps except overlap [2] S. Pancholi and A. M. Joshi, “Electromyography-based hand gesture
L615: of 75%, and in DB3 [see Fig. 7(b)] all overlaps except for overlap recognition system for upper limb amputees,” IEEE Sensors Lett., vol. 3,
L616: of 75%. The stable performances exhibited by Model4 across no. 3, Mar. 2019, Art. no. 5500304.
L617: [3] N. N. Unanyan and A. A. Belov, “Design of upper limb prosthesis using
L618: all databases suggest that the proposed Model4 would be more
L619: real-time motion detection method based on EMG signal processing,”
L620: suitable for decoding sEMG based motion intents.
L621: Biomed. Signal Process. Control, vol. 70, 2021, Art. no. 103062.
L622: [4] J.M.Hahne,D.Farina,N.Jiang,andD.Liebetanz,“Anovelpercutaneous
L623: electrode implant for improving robustness in advanced myoelectric con-
L624: V. CONCLUSION trol,” Front. Neurosci., vol. 10, 2016, Art. no. 114.
```

## A_Multimodal_Multilevel_Converged_Attention_Network_for_Hand_Gesture_Recognition_With_Hybrid_.txt
- Total extracted lines: 695

### Lines 1-55

```text
L3: ===== PAGE 1 =====
L5: IEEE TRANSACTIONS ON CYBERNETICS, VOL. 53, NO. 12, DECEMBER 2023 7723
L6: A Multimodal Multilevel Converged Attention
L7: Network for Hand Gesture Recognition With
L8: Hybrid sEMG and A-Mode Ultrasound Sensing
L9: Sheng Wei , Yue Zhang, and Honghai Liu , Fellow, IEEE
L10: Abstract—Gesture recognition based on surface electromyogra- I. INTRODUCTION
L11: phy (sEMG) has been widely used in the field of human–machine THE HAND is the most flexible limb in the human body. It
L12: interaction (HMI). However, sEMG has limitations, such as low
L13: can assist humans in most life behaviors. Hand gestures,
L14: signal-to-noise ratio and insensitivity to fine finger movements,
L15: so we consider adding A-mode ultrasound (AUS) to enhance as an intuitive and convenient human expression, can express a
L16: the recognition impact. To explore the influence of multisource variety of meanings. With the development of human–machine
L17: sensing data on gesture recognition and better integrate the fea- interaction (HMI), HMI methods based on gesture recogni-
L18: tures of different modules. We proposed a multimodal multilevel
L19: tion have gained widespread attention. However, the result of
L20: converged attention network (MMCANet) model for multisource
L21: gesture recognition is strongly affected by the original sig-
L22: signals composed of sEMG and AUS. The proposed model
L23: extracts the hidden features of the AUS signal with a con- nal, so it is especially critical to choose a suitable signal.
L24: volutional neural network (CNN). Meanwhile, a CNN-LSTM The human body carries a large amount of information, and
L25: (long-short memory network) hybrid structure extracts some bio-signals are a great treasure for obtaining the state of the
L26: spatial-temporal features from the sEMG signal. Then, two
L27: human body. With the continuous development of the bio-
L28: types of CNN features from AUS and sEMG are spliced and
L29: signal decoding technology, researchers are extracting and
L30: transmitted to a transformer encoder to fuse the information
L31: and interact with sEMG features to produce hybrid features. analyzing human bio-signals to characterize them as con-
L32: Finally, the classification results are output employing fully con- trol signals to accomplish gesture interaction. The bio-electric
L33: nected layers. Attention mechanisms are used to adjust the signals have received a lot of attention include electromyog-
L34: weights of feature channels. We compared MMCANet’s feature
L35: raphy (EMG) [1], [2], [3], electroencephalography (EEG) [4],
L36: extraction and classification performance with that of manually
L37: electrooculography (EOG) [5], etc. In addition, near-infrared
L38: extracted sEMG-AUS features using four traditional machine-
L39: spectroscopy (NIRS) [6], force myography (FMG) [7], inertial
L40: learning (ML) algorithms. The recognition accuracy increased by
L41: at least 5.15%. In addition, we tried deep learning (DL) methods measurement unit (IMU) [8], and ultrasound (US) sensing [9],
L42: with CNN on single modals. The experimental results showed that etc. They have been used in wearable sensing solutions.
L43: the proposed model improved 14.31% and 3.80% over the CNN The surface EMG (sEMG) signal is the most accessible and
L44: method with single sEMG and AUS, respectively. Compared with
L45: simplest physiological signal, and it is the principal noninva-
L46: some state-of-the-art fusion techniques, our method also achieved
L47: sive method to determine the upper limb bio-electric signals.
L48: better results.
L49: When transmitting the nerve excitation impulse to the mus-
L50: Index Terms—A-mode ultrasound (AUS), attention mecha-
L51: cle, we can obtain the sEMG signals through the surface
L52: nism, gesture recognition, hybrid features, multimodal, surface
L53: electrode guidance and operation of amplification, and it can
L54: electromyography (sEMG), transformer.
L55: reflect the functional change of the neuromuscular system.
```

### Lines 130-160

```text
L130: ful improvements in the decoding of fine finger movements layers. The receptive field was introduced into CNN to mimic
L131: and large arm movements. Xia et al. [15] used feature extrac- the pattern the human brain processes information [27]. So,
L132: tion and traditional machine-learning (ML) algorithms for compared to traditional ML methods, CNN can learn and gen-
L133: classification. The data collected by sEMG and AUS syn- erate more hidden features, which is superior to manual feature
L134: chronously showed a significant improvement over a single extraction methods [14].
L135: modality. Zeng et al. [22] proposed a convolutional neu- 2) LSTM: LSTM is a variant of recurrent neural network
L136: ral network (CNN)-based sEMG and AUS feature fusion (RNN), mainly to figure out the gradient disappearance and
L137: architecture (EU-Net), which surpassed the method of the gradient explosion problems during the long sequences train-
L138: ML algorithm with the manual designed features. In [23], ing. It is a kind of neural network containing LSTM blocks,
L139: researchers proposed a regularized deep fusion of kernel and the LSTM block includes forget gate, input gate, and
L140: machine (RDFKM) approach to merge multimodal physiolog- output gate. The forget gate, which is the key to achieving
L141: ical signals. The above study shows that multimodal gesture the long-term memory task, is the most critical part of each
L142: recognition can complement the strength of different modali- LSTM block [28]. The LSTM network can capture the tem-
L143: ties to improve performance [24], and indicates the possibility poral dependence of time series and has achieved a series of
L144: of combining sEMG and AUS. results in time-series prediction [29], [30].
L145: In the previous studies, methods based on traditional man- 3) AlexNet: AlexNet was designed by Hinton. He is the
L146: ual feature extraction and ML have received much attention winner of the 2012 ImageNet competition and his student
L147: and development. Yet, the classic feature extraction and classi- Alex Krizhevsky. Tricks, such as ReLU, Dropout, and Local
L148: fication algorithms are limited in their ability to extract traits Response Normalization were applied in CNN successfully
L149: from the signal, especially in the correlation of multimodal the first time. It has 6000w parameters and 65w neurons and
L150: data is not well exploited. Deep learning (DL) is an algorithm is composed of five convolution pooling layers, followed by
L151: for learning the representation of data, with the advantages three fully connected layers [31].
L152: of learning ability and good adaptability, which can fully 4) DenseNet: DenseNet is the best paper of CVPR2017,
L153: extract the features of the signal. The most widely used which can be regarded as a network of ResNet and
L154: Authorized licensed use limited to: University of Science & Technology of China. Downloaded on July 05,2026 at 10:00:00 UTC from IEEE Xplore. Restrictions apply.
L156: ===== PAGE 3 =====
L158: WEI et al.: MMCANet FOR HAND GESTURE RECOGNITION 7725
L159: Fig. 1. Structure of transformer encoder.
L160: Fig. 2. Twenty gestures in the dataset [15].
```

### Lines 222-348

```text
L222: Fig. 5. Structure of AUS CNN network.
L223: TABLE I
L224: AUS-CNN ARCHITECTURES
L225: Fig. 3. Picture of the sEMG and AUS fusion device.
L226: a band-pass filter for noise reduction for the sEMG signal. To
L227: ensure the synchronization with the AUS signal, the window
L228: size of the data is 300 ms for the noise reduction signal, and
L229: the step size is 100 ms so that the sampling frequency of the
L230: sEMG signal is consistent with the AUS signal at 10 Hz, and
L231: Fig. 4. Position of the probes. the normalization operation is employed.
L232: D. Experiment Setup
L233: The AUS/sEMG probes were worn on the dominant hand
L234: To test and verify the proposed network structure with
L235: (an appropriate amount of coupling agent should apply to the
L236: sEMG, AUS, and fusion signals. We designed different
L237: AUS probe in advance). We placed the armband on the fore-
L238: network models for the three datasets in this article. For all the
L239: arm of the subject. Before that, we should clean the subjects’
L240: networks, the batch size was 50. The early stopping method
L241: skin with alcohol pads where the probes will place. Two of
L242: would stop training when the training loss no longer decreases.
L243: the probes were attached to the ulnar carpal flexor and ulnar
L244: The specific setup of the experiments will show in later sec-
L245: carpal extensor muscles. While the other two were attached
L246: tions. For the datasets, the first four out of eight trials for
L247: to the radial carpal flexor and radial carpal flexor muscles, as
L248: each subject were the training set, and the data from the last
L249: shown in Fig. 4. The experiment was carried out following
L250: four trials were the test set. The network weight initialization
L251: the Declaration of Helsinki. In the experiment, the duration
L252: method was random initialization. The experiments were per-
L253: of each motion is 5 s, with no rest interval between changes.
L254: formed on i5-11400F CPU, 2.60 GHz, 32-GB RAM, and an
L255: Subjects were free to rest for 25-s after the completion of all
L256: NVIDIA Geforce GTX 3060 GPU-supported PC.
L257: 20 types of actions. The above process was completed once
L258: In all figures of the network structure, the first number
L259: and called one action group. The experiment was repeated
L260: before @ means the channel number of this layer, and a × b
L261: for eight groups. For each gesture action, the middle 3 s of
L262: means the width and height in the layer. The ConvX in the
L263: the steady-state were picked as the experimental data, and the
L264: figure stands for the ConvBlock, the structure of a ConvBlock
L265: number of 20 types of gestures in the database was balanced.
L266: was shown in Fig. 5. In this table, in and out are in_channel
L267: and out_channel, k, s, and p means kernel_size, padding, and
L268: C. Data Preprocessing
L269: stride. In all the tables of network parameters, the activation
L270: The preprocessing process for AUS signals includes time function of the convolutional layer is ReLU.
L271: gain compensation (TGC), Gaussian filtering, envelope extrac- 1) AUS CNN Network: For individual AUS signals, we
L272: tion, and log compression [40]. The TGC was utilized to used one frame of data from four channels as a sample, then
L273: compensate for the energy attenuation caused by dispersion transformed each frame into a shape of 100 × 10 to obtain a
L274: and damping during the propagation of AUS. In band-pass data size of 4 × 100 × 10 for each sample to feed into the
L275: filtering, we used a Gaussian filter with the center frequency network for training. The network structure consists of five
L276: positioned at the center of the passband, and it can filter out the layers, as shown in Fig. 5. The AUS-CNN architectures are in
L277: nonlinear propagation and the noise in the circuit. The Hilbert Table I. Adam was the optimizer, and the initial learning rate
L278: transform was used to perform envelope extraction. The log was 0.001.
L279: compression compressed the large dynamic range caused by 2) sEMG CNN-LSTM Network: For the sEMG signal,
L280: TGC into a smaller space for subsequent processing. We use since the data quantity for each sample was much smaller than
L281: Authorized licensed use limited to: University of Science & Technology of China. Downloaded on July 05,2026 at 10:00:00 UTC from IEEE Xplore. Restrictions apply.
L283: ===== PAGE 5 =====
L285: WEI et al.: MMCANet FOR HAND GESTURE RECOGNITION 7727
L286: TABLE II
L287: SEMG-CNN-LSTM ARCHITECTURES
L288: Fig. 6. Structure of sEMG CNN-LSTM network.
L289: TABLE III
L290: ALEXNET ARCHITECTURES
L291: (a) (b)
L292: TABLE IV
L293: DENSENET ARCHITECTURES
L294: Fig. 7. Time-frequency diagrams of two adjacent. (a) sEMG and (b) AUS
L295: signal samples.
L296: Fig. 8. Multimodal fusion structure of RDFKM.
L297: that of AUS, we stitched the data of four channels together
L298: and converted it into a shape of 300 × 4. Then the data was
L299: sent to the network for training. The entire network consisted
L300: of seven layers, as shown in Fig. 6, and the parameters of signal samples are shown in Fig. 7. The network structure
L301: the sEMG CNN-LSTM Network are shown in Table II. The parameters are shown in Tables III and IV.
L302: optimizer was Adam, and the initial learning rate was 0.01. 4) Some State-of-the-Art Fusion Methods: To prove the
L303: 3) Other Famous Backbones (AlexNet and DenseNet): We superiority and effectiveness of our method, we compared it
L304: chose the well-known AlexNet and DenseNet as a comparison. with the state-of-the-art method EU-Net based on sEMG and
L305: Since these two networks were for image classification and AUS fusion [22], whose network parameters were shown in
L306: sEMG and AUS data are multichannel signal data. We tried Table V. Also, we compared it with an advanced multimodal
L307: two input methods: one is to use the signal data as input and fusion method RDFKM [23]. Since the input signals are dif-
L308: the other is to transform the signal data into a time-frequency ferent, the structure of the multimodal fusion in RDFKM
L309: map of size 227 × 227 by continue wavelet transform (CWT). was reconstructed for comparison, as illustrated in Fig. 8. The
L310: The time-frequency diagrams of two adjacent sEMG and AUS feature dimension was 64, the same as the original paper.
L311: Authorized licensed use limited to: University of Science & Technology of China. Downloaded on July 05,2026 at 10:00:00 UTC from IEEE Xplore. Restrictions apply.
L313: ===== PAGE 6 =====
L315: 7728 IEEE TRANSACTIONS ON CYBERNETICS, VOL. 53, NO. 12, DECEMBER 2023
L316: Fig. 9. Structure of MMCANet. Every ConvBlocks’ configurations are in Table VI.
L317: TABLE V TABLE VII
L318: EU-NET ARCHITECTURES AVERAGE RECOGNITION RATE OF DIFFERENT FUSION TYPES
L319: CNN features of sEMG and AUS signals and reshaped this
L320: fusion data to (batch size, 32, 2200), then sent it into a three-
L321: layer four-head transformer encoder module. These features
L322: were reweighted with a transformer encoder at an appropri-
L323: ate ratio. In this way, more detailed and hidden features can
L324: be extracted. The next step was to obtain the multimodal and
L325: TABLE VI multilevel spatial-temporal fusion feature of sEMG and AUS
L326: DETAILS OF PROPOSED MMCANET signals by splicing the hybrid transformer encoder feature with
L327: the LSTM time features of the sEMG signals. Finally, the
L328: hybrid features were flattened, then sent to the fully connected
L329: layer for classification training, and the classification activa-
L330: tion function was softmax. The specific network structure is
L331: shown in Fig. 9 and Table VI. The optimizer was SGD, and
L332: the learning rate was 0.001.
L333: E. Details of Traditional Methods
L334: Mean absolute deviation (MAV), waveform length (WL),
L335: zero crossing number (ZC), slop sign changes (SSC), and
L336: 5) AUS-sEMG MMCANet: To improve the feature extrac- TD-AR6 were chosen as the sEMG feature. We used
L337: tion capability and classification performance of multisource coefficients of piece-wise linear fitting to characterize the AUS
L338: signals. We need to fuse the sEMG and AUS signals. After feature and applied appropriate PCA on the splicing traits
L339: conducting experimental comparisons of the three fusion of sEMG and AUS normalized features to obtain the hybrid
L340: methods (Table VII), this article adopts the intermediate fusion features. For the selection of classifiers, we used the four
L341: for the feature fusion of sEMG-AUS multimodal fusion oper- most common methods: 1) linear discriminant analysis (LDA);
L342: ation. We proposed an MMCANet structure and sent the 2) k-nearest neighbor algorithm (KNN); 3) support vector
L343: sEMG and AUS signals to their respective networks for feature machine (SVM); and 4) artificial neural network (ANN). The
L344: extraction. For AUS signals, one-layer CNN was performed to n_neighbors in KNN was 10, the standard value in the SVM
L345: extract abstract spatial features, and an SENet module was fol- classifier was the RBF kernel, and hidden_layer_sizes was 128.
L346: lowed to adjust the weight of different channels. For sEMG
L347: signals, CNN, and LSTM networks were employed to extract
L348: III. RESULT AND DISCUSSION
```

### Lines 408-538

```text
L408: Fig. 10. Average recognition rate of SVM classifier and DL methods for sEMG, AUS, and hybrid features.
L409: signals into time-frequency diagrams. Two data organizations: also based on the fusion of sEMG and AUS under the DL
L410: 1) original signals and 2) time-frequency graphs were used as framework. Compared with the 91.55% accuracy of EU-Net,
L411: input data. As shown in Table VIII, for sEMG, the recognition MMCANet was 2.59% higher. Since there were few stud-
L412: rates of original data as input with AlexNet and DenseNet ies on the related fusion gesture recognition based on sEMG
L413: were 63.75% and 61.93%. Meanwhile, the recognition results with AUS, we also compared it with a method for multimodal
L414: of the image as input were 77.39% and 77.91%, separately. In fusion of physiological signals, RDFKM. Experimental results
L415: the first case, AlexNet was slightly higher, and the two input show that the recognition rate based on RDFKM was 92.17%,
L416: modes were almost the same in the second case. For AUS, which was 1.97% lower than that of MMCANet. In summary,
L417: the accuracy of AlexNet with signals and images was 74.98% our proposed method can achieve better performance.
L418: and 77.63%. The performances of DenseNet in time series and
L419: spectrograms were 82.16% and 85.66%. Those showed that the
L420: E. Experiment 5: The Results With Deep Learning Method
L421: performance of the image as input was better than that of the
L422: on Different Gestures
L423: signal. DenseNet was better than AlexNet because its residual
L424: The recognition results of different features are illustrated
L425: blocks alleviate overfitting to some extent, but both of them
L426: in Fig. 11. We can see that AUS is better than sEMG in most
L427: were lower than that of single-layer CNN. The factors that
L428: gestures. For the six wrist actions, sEMG had a higher recog-
L429: may cause this result were the overfitting caused by an over-
L430: nition accuracy for the first four actions than the other two
L431: complicated network. Therefore, three-layers and five-layers
L432: gestures. The accuracy for the first four very different motions
L433: CNN structures on AUS signals were compared. In the results,
L434: was close to the result of AUS and fusion features. However,
L435: the more layers, the worse the effect. Those illustrated that
L436: the other two actions, WS and WP, with fewer differences. The
L437: the AUS signal does not need a very complicated network
L438: recognition accuracy was lower. Therefore, the sEMG decod-
L439: structure, so this study only used a single-layer CNN structure
L440: ing rate was lower for motions with smaller amplitude. The
L441: to extract the features of AUS.
L442: recognition rates of AUS and fusion signals were close to
L443: 100% for these two motions because despite the amplitude
L444: D. Experiment 4: Comparisons With State-of-the-Arts
L445: being tiny between these two actions, the related muscle dif-
L446: Fusion Methods
L447: ferences were immense. It can be seen from the experimental
L448: The recognition rate of the sEMG signal was 79.83% with results that for most finger movements, the recognition rate of
L449: the CNN-LSTM structure network, and the classification accu- AUS was higher than that of sEMG. However, the rest ges-
L450: racy of AUS signals was 90.34% with the CNN method, ture was likely to be confused with other gestures due to the
L451: which achieved a higher decoding rate than other methods. muscle had a corresponding shape. While the sEMG signal
L452: According to the comparison experiments above, it was illus- was basically in a stable state in the resting state, which was
L453: trated that we had the best feature extraction capability and distinctive from other gestures, the recognition rate of sEMG
L454: recognition rate for the CNN-LSTM and CNN architectures was higher.
L455: proposed by sEMG and AUS, respectively. The average classi- In terms of gesture categories, for the hybrid features, the
L456: fication accuracy of MMCANet was 94.14%. To demonstrate gesture with the highest average recognition rate was RS
L457: the superiority of our proposed method, we have compared 100.00%, and the lowest was TIF 78.75%, half of the motions
L458: it with the proposed fusion methods lately. The EU-Net was recognized at 95% or more, and 30% of the gestures were
L459: Authorized licensed use limited to: University of Science & Technology of China. Downloaded on July 05,2026 at 10:00:00 UTC from IEEE Xplore. Restrictions apply.
L461: ===== PAGE 9 =====
L463: WEI et al.: MMCANet FOR HAND GESTURE RECOGNITION 7731
L464: Fig. 11. Results of 20 gestures average recognition accuracy for sEMG-CNN-LSTM, AUS-CNN, and sEMG-AUS-MMCANet.
L465: (a) (b) (c)
L466: Fig. 12. Projections of different features on 2-D space by tSNE. (a) sEMG.
L467: (b) AUS. (c) sEMG-AUS.
L468: Fig. 13. Two methods of four-fold cross-validation.
L469: more than 99%. For the six wrist movements, the recognition
L470: rate of WUD was the lowest at 94.90%, the other five
L471: movements were above 98%, and the highest identification TABLE IX
L472: AVERAGE GESTURE RECOGNITION ACCURACY OF THE FOUR-FOLD
L473: rate was 99.90% for WS, indicating that the method reached
L474: CROSS-VALIDATION RESULTS
L475: a very high accuracy in wrist gesture recognition. For the 13
L476: fine finger movements, the lowest recognition rate was TIF,
L477: with an accuracy rate of 78.13%, which was mainly affected
L478: by the poor discrimination performance of the sEMG signal
L479: on this movement, and most finger gesture recognition rates
L480: were above 90%, with the highest being PH at 97.71%.
L481: The hybrid feature was better than the sEMG signal in all
L482: 20 gestures and better than the AUS feature in most ges-
L483: F. Experiment 6: Four-Fold Cross-Validation
L484: ture decoding. Even if the part of recognition rate of fusion
L485: data was lower than AUS, the difference was within 2%. Four-fold cross-validation was adopted to evaluate the clas-
L486: Because the sEMG signal was the bio-electrical signal of the sification performance of our method in this experiment. We
L487: arm, while the AUS signal was the feature representing the chose two methods to divide all eight trials, as shown in
L488: muscle morphology, the hybrid features can more compre- Fig. 13. The first method was to keep the last four trials as the
L489: hensively illustrate the bio-electric signal state and muscle test set, dividing the first four trials into four folds, of which
L490: morphology in different dimensions. Therefore, the hybrid fea- three folds were used for training and others for validation.
L491: tures can obtain higher accuracy in gesture recognition. As The training would stop early according to the loss of valida-
L492: shown in Fig. 12, the sEMG, AUS, and hybrid characteristics tion set. The second method was to divide all eight trials into
L493: were projected to two dimensions for the visualization. The four folds, three folds for training and one fold for testing,
L494: fusion features can distinguish different gestures better than and training loss was used for early stopping. The results of
L495: the single-modal traits. So they can attain better performances. four-fold cross-validation are shown in Table IX.
L496: Authorized licensed use limited to: University of Science & Technology of China. Downloaded on July 05,2026 at 10:00:00 UTC from IEEE Xplore. Restrictions apply.
L498: ===== PAGE 10 =====
L500: 7732 IEEE TRANSACTIONS ON CYBERNETICS, VOL. 53, NO. 12, DECEMBER 2023
L501: TABLE X
L502: from Method 4, in contrast to using CNN for further feature
L503: AVERAGE GESTURE RECOGNITION ACCURACY OF THE ABLATION
L504: EXPERIMENT RESULTS extraction and fusion, the transformer encoder was more effec-
L505: tive in feature extraction and integration due to its self-attentive
L506: mechanism.
L507: The comparison between the various ablation experimen-
L508: tal methods can indicate the effectiveness of our proposed
L509: MMCANet in multimodal fusion decoding.
L510: H. Future Work
L511: The present study has potential limitations. Due to the lack
L512: From the outcomes of method (a), we can see that the
L513: of relevant public datasets, this study uses our collection of
L514: accuracy trend of early stop using the validation set loss was
L515: sEMG-AUS datasets and therefore lacks comparisons with
L516: almost the same as that of early stop using the training set
L517: other researchers. Thus, the proposed method was compared
L518: loss. The accuracy rate was reduced because method (a) nar-
L519: with four traditional ML algorithms and six DL networks.
L520: rows the training set under the condition that the test set was
L521: In the future, we will try more combinations of multimodal
L522: unchanged. Method (b) was equivalent to expanding the train-
L523: recognition to explore its potential in prosthesis control.
L524: ing set and shrinking the test set. Therefore, all recognition
L525: Meanwhile, in this experiment, there is a lack of data on dis-
L526: rates have increased. Compared with AUS, the accuracy of
L527: abled people. We will try to remedy this deficiency in our
L528: hybrid features decreased from 3.80% to 1.04%, which illus-
L529: future work. In this experiment, only gesture classification
L530: trates that fusion features can achieve better results with less
L531: was recognized but based on the characteristics of sEMG and
L532: training data and have advantages in long-time use.
L533: AUS, the sEMG-AUS fusion signal has potential in joint angle
L534: measure and force estimation, which we will study next.
L535: G. Experiment 7: Ablation Experiment
L536: To investigate the effect of different feature extraction and
L537: combination patterns on networks’ performance, and to bet-
L538: IV. CONCLUSION
```

## Contrast-Assisted_Domain-Specificity-Removal_Network_for_Semi-Supervised_Generalization_Fault.txt
- Total extracted lines: 1263

### Lines 1-50

```text
L3: ===== PAGE 1 =====
L5: IEEE TRANSACTIONS ON NEURAL NETWORKS AND LEARNING SYSTEMS, VOL. 36, NO. 3, MARCH 2025 5403
L6: Contrast-Assisted Domain-Specificity-Removal
L7: Network for Semi-Supervised Generalization
L8: Fault Diagnosis
L9: Qiuyu Song , Xingxing Jiang , Jie Liu , Member, IEEE, Juanjuan Shi , and Zhongkui Zhu
L10: Abstract—Unknown domain shift caused by the unavail- past few years [1], [2], [3], [4]. For example, Yang et al. [5]
L11: ability of target domain during training phase degrades the recently proposed a digital twin-driven fault diagnosis method,
L12: performance of intelligent fault diagnosis models in practical
L13: which can better evaluate the reliability of industrial systems
L14: applications. Domain generalization (DG)-based methods have
L15: and is extremely effective for composite faults. Furthermore,
L16: recently emerged to alleviate the influence of domain shift and
L17: improve the generalization ability of models toward invisible due to the widespread application of rotating machinery in
L18: working conditions. However, most existing studies are con- industrial systems, implementing reliable condition monitor-
L19: ducted on multiple fully labeled source domains. Meanwhile, ing and fault diagnosis of rotating machinery, especially
L20: domain-specific information related to the variations of working
L21: safety-critical assets such as bearings and gears, is essen-
L22: conditions is often neglected during model training. Therefore,
L23: tial [6], [7], [8]. With appealing capabilities of mining implicit
L24: in order to realize reliable generalization fault diagnosis based on
L25: partially labeled source domains, this article proposes a contrast- fault-related features automatically and characterizing internal
L26: assisted domain-specificity-removal network (CDSRN) to extract information in industrial big data through layer-by-layer learn-
L27: transferable features from domain-specificity-removal perspec- ing, intelligent fault diagnosis methods based on deep learning
L28: tive. Concretely, a domain-specific feature removal branch is
L29: (DL) have made significant progress and shown promising
L30: designed to disentangle domain-invariant features and domain-
L31: application prospects [9], [10].
L32: specific features, thus excavating generalized information only in
L33: domain-invariance dimension. Simultaneously, proxy-contrastive Nevertheless, the diagnostic performance of traditional
L34: representation enhancement module is embedded to facilitate DL-based methods usually severely degrades under different
L35: the fault class-discriminative and domain-discriminative feature operating conditions. The basic premise of most DL-based
L36: learning, thereby assisting the model in further improvement
L37: fault diagnosis methods is that the training and testing data are
L38: of generalization capability. Experimental studies confirm the
L39: collected under the same working conditions, thus following
L40: effectiveness and competitiveness of the proposed CDSRN in
L41: semi-supervised generalization fault diagnosis. the same data distribution. However, this basic premise is
L42: difficult to hold in many real engineering scenarios [11].
L43: Index Terms—Adversarial training, contrastive learning, intel-
L44: To overcome this issue, domain adaption (DA) is developed
L45: ligent fault diagnosis, rotating machinery, semi-supervised
L46: domain generalization (DG), unseen target domain. based on the idea of transfer learning to realize reliable fault
L47: diagnosis under varying working conditions [12]. DA aims
L48: I. INTRODUCTION to transfer diagnosis knowledge from the training data, i.e.,
L49: RELIABILITY of industrial systems has always been a source domain, to the testing data, i.e., target domain, thereby
L50: eliminating the discrepancies of data distribution and achieving
```

### Lines 200-273

```text
L200: A. Problem Definition for Semi-Supervised DG-Based Fault Furthermore, confronted with unavailable target domains in
L201: Diagnosis practical scenarios, the key to enhancing the generalization
L202: performance of the fault diagnosis model is to excavate
L203: Fig. 1 illustrates the problem definition for semi-supervised
L204: common knowledge independent of data distributions from the
L205: DG-based fault diagnosis. The distribution of historical moni-
L206: available source domains. Based on the preliminary mentioned
L207: toring data obtained from machinery varies due to different
L208: in Section III, domain knowledge can be viewed as two
L209: working conditions such as speed and load. Assume that
L210: components, i.e., domain-invariant information and domain-
L211: there are M accessible source domains {Ds }M and each
L212: source domain Ds contains ns samples X
L213: m
L214: s
L215: m=
L216: =
L217: 1
L218: {xs
L219: }ns
L220: m .
L221: specific information. It motivates the idea of CDSRN to take
L222: m m m m,i i=1 the domain-specific information related to the variations of
L223: A typical semi-supervised DG-based fault diagnosis task aims
L224: working conditions into account. In addition, the discrim-
L225: to generalize a diagnostic model learned from one fully labeled
L226: source domain D 1 s = {(xs 1,i , y 1 s ,i , d 1,i )} i n = s 1 1 and M − 1 unlabeled i s n u a c b c i e l s it s y fu o l f fa t u h l e t c le la a s r s n i e fi d ca f t e io a n tu . r I e t s in is sp a i l r s e o s t t h h a e t k it ey is t e o ss r e e n a t l i i a z l in to g
L227: source domains D m s = {(xs m,i , d m,i )} i n = s m 1 , m = 2, 3, . . . , M enhance representation learning from the perspective of class
L228: to an unseen unlabeled target domain Dt with nt samples discriminability.
L229: Xt = {x i t} i n = t 1 , where y 1 s ,i and d m,i denote the labels of K Fig. 3 exhibits the overall schematic of the motivation
L230: machine health states and M domains, respectively. It should of CDSRN. Generally, CDSRN attempts to obtain the ulti-
L231: be noted that this work focuses on the problem of domain mate generalized features only in the domain-invariance
L232: shift, i.e., the discrepancy of distribution Ps(Xs) ̸= Ps(Xs) ̸= dimension through domain-specificity-removal, which can
L233: 1 1 2 2
L234: · · · P m s (Xs m ) ̸= Pt(Xt). The category shift is not considered in disentangle domain-specific features and domain-invariant fea-
L235: this work, that is, the source and target domains have the same tures, and contrast-assistance, which can prompt intraclass
L236: category label space. aggregation. It is expected that removing domain-specific
L237: information can provide clearer guidance for the network to
L238: B. Domain-Specific Information in Machinery Fault
L239: learn domain-invariant knowledge in the domain-invariance
L240: Diagnosis
L241: dimension, thereby enhancing the generalization capability of
L242: When a bearing fault occurs in a mechanical system, the fault diagnosis model. Thus, based on the framework of
L243: the bearing fault vibration signal x(t) can be formulated as DANN, a domain-specific feature removal branch is designed
L244: Authorized licensed use limited to: University of Science & Technology of China. Downloaded on July 05,2026 at 10:03:23 UTC from IEEE Xplore. Restrictions apply.
L246: ===== PAGE 4 =====
L248: 5406 IEEE TRANSACTIONS ON NEURAL NETWORKS AND LEARNING SYSTEMS, VOL. 36, NO. 3, MARCH 2025
L249: Fig. 1. Illustration of semi-supervised DG-based fault diagnosis.
L250: generalization capability when source domains are partially
L251: labeled. Fig. 4 shows the network architecture of the pro-
L252: posed CDSRN. CDSRN consists of a domain-invariant feature
L253: extractor G , a domain-specific feature extractor G , a fault
L254: I S
L255: classifier C, a domain classifier D, a domain-invariant fea-
L256: ture projection head P , a domain-specific feature projection
L257: I
L258: head P , a fault-class-proxy projection head P , and a
L259: S f
L260: domain-proxy projection head P . The overall idea of CDSRN
L261: d
L262: is progressive and details are illustrated as follows.
L263: 1) Preliminary Framework Based on DANN: The domain-
L264: invariant feature extractor G , the fault classifier C, and the
L265: I
L266: domain classifier D constitute the preliminary framework of
L267: Fig. 2. Diagram of domain-specific information and domain-invariant
L268: information in machinery fault signal. the proposed CDSRN. The domain-invariant features can be
L269: obtained coarsely by the adversarial training between the
L270: domain-invariant feature extractor G and the domain classifier
L271: I
L272: in the proposed CDSRN to remove domain-specific infor-
L273: D. The basic optimization objective for the fault classifier C
```

### Lines 449-856

```text
L449: B. Method Overview and Network Architecture
L450: optimization in the early training epochs when the accu-
L451: The proposed method intends to tackle cross-domain gen- racy of pseudo labels is low. As the epoch progresses, the
L452: eralized fault diagnosis by excavating the domain-invariant coefficient β(q) increases along with gradually more reliable
L453: and class-discriminative representations that have significant pseudo labels. The adversarial objective function for the
L454: Authorized licensed use limited to: University of Science & Technology of China. Downloaded on July 05,2026 at 10:03:23 UTC from IEEE Xplore. Restrictions apply.
L456: ===== PAGE 5 =====
L458: SONG et al.: CDSRN FOR SEMI-SUPERVISED GENERALIZATION FAULT DIAGNOSIS 5407
L459: Fig. 3. Schematic of the motivation of CDSRN.
L460: domain-invariant feature extractor G and domain classifier where θ is the parameter of domain-specific feature extrac-
L461: I GS
L462: D is given as follows: tor G . By (6), the model extracts domain features for
L463: S
L464: L I,adv (cid:0)θ D , θ GI (cid:1) d d o o m m a a i i n n- c s l p a e s c s i i fi fi c ca f t e io a n tu . r T e h e e x a tr d a v c e to rs r ar G ia
L465: S
L466: l o an b d jec f t a i u v l e t f c u l n a c ss ti i o fi n er of C th i e s
L467: = m
L468: θ G
L469: i
L470: I
L471: n m
L472: θ
L473: a
L474: D
L475: x ( −
L476: m
L477: X M
L478: =1
L479: X
L480: i
L481: n
L482: =
L483: s
L484: 1
L485: d m,i log D (cid:0) G I (cid:0) xs m,i (cid:1)(cid:1) ) (5) wri
L486: L
L487: tte
L488: S
L489: n
L490: ,ad
L491: a
L492: v
L493: s
L494: (cid:0)θ C , θ GS (cid:1)
L495: c
L496: w
L497: a
L498: h
L499: n
L500: W er i
L501: l
L502: e t
L503: e
L504: h
L505: a
L506: θ
L507: r
L508: t D
L509: n
L510: he is
L511: d
L512: p
L513: o
L514: r t e h
L515: m
L516: l e i
L517: a
L518: m
L519: i
L520: p
L521: n
L522: i a n
L523: -
L524: r
L525: i
L526: a a
L527: n
L528: r m
L529: v
L530: y
L531: a
L532: e
L533: r
L534: f t
L535: i
L536: r e
L537: a
L538: a r
L539: n
L540: m
L541: t
L542: o e f w
L543: fe
L544: d o
L545: a
L546: o r
L547: t
L548: m k
L549: ur
L550: a b
L551: e
L552: i a
L553: s
L554: n se c
L555: c
L556: d l
L557: o
L558: a
L559: a
L560: o s
L561: r
L562: n s
L563: s
L564: i
L565: e
L566: D fi
L567: l
L568: e
L569: y
L570: A r
L571: .
L572: N D
L573: N
L574: N .
L575: e
L576: ,
L577: v
L578: t
L579: e
L580: h
L581: r
L582: e
L583: th
L584: m
L585: el
L586: o
L587: e
L588: d
L589: s
L590: e
L591: s
L592: l
L593: ,
L594:   − X ns m y m,i log C (cid:0) G S (cid:0) xs m,i (cid:1)(cid:1)
L595: = minmax i=1 (7)
L596: t t h h e e l v e a a r r i n a e ti d on f s ea o tu f r d es om st a il i l ns c , o w nt h a i i c n h so is m e e xp in e f c o te rm d a t t o io b n e re re la m te o d ve to d θ C θ GS  − M X −1 X ns m β(q)yˆs m,i log C (cid:0) G S (cid:0) xs m,i (cid:1)(cid:1)
L597: delicately. m=1 i=1
L598: 2) Domain-Specific Feature Removal Branch: The pro-
L599: By (7), the model removes fault-related information from
L600: posed CDSRN pursues further fine-grained domain-invariant
L601: the extracted domain features, thus learning only the domain-
L602: features by embedding the domain-specific feature removal
L603: specific features.
L604: branch, which seeks to remove the underlying information
L605: Step 2 (Disentanglement of Domain-Specific Features and
L606: associated with domain-specific attributes. Specifically, the
L607: Domain-Invariant Features): Domain-specific features and
L608: domain-specific feature extractor G is introduced to connect
L609: S domain-invariant features are disentangled by minimizing their
L610: with the domain classifier D to learn the representations for
L611: cosine similarity
L612: domain classification. Meanwhile, adversarial training between
L613: C t n h o e is f d a o u u m s lt e a - d r i e n t l - o a s t p e e e d n c s i i u fi n r c f e o f r e t m h a a t a u t t r i t e o h n e e , x d t t r h o a u m c s t a o i l r n e G - a s r p S n e i a n c n g ifi d c o th n f e l e y a fa t t u u h r l e e t s c d l c a o o s m s n i a t fi a in e in r - L cos (cid:0)θ GI , θ GS (cid:1) = θ G m I , i θ n GS m X M =1 X i n = s m 1 (cid:13) (cid:13) G G I I (cid:0) (cid:0) x x s m s m , , i i (cid:1) (cid:1) T (cid:13) (cid:13) (cid:13) (cid:13) · G G S S (cid:0) (cid:0) x x s m s m , , i i (cid:1) (cid:1) (cid:13) (cid:13) .
L614: specific information. Domain-specific feature extractor G S , (8)
L615: domain classifier D, and fault classifier C are involved in
L616: the domain-specific feature removal branch. Two steps of Afterward, it means that the domain-specific features are
L617: the domain-specific feature removal branch are illustrated as removed from the domain-invariant features.
L618: follows. 3) Proxy-Contrastive Representation Enhancement Module:
L619: Step 1 (Extraction of Domain-Specific Features): The Proxy-contrastive representation enhancement module, includ-
L620: mathematical expression of loss for domain classifier D is ing two parts, is utilized to promote intraclass aggregation and
L621: formulated as follows: interclass separation by extending PCL. The proxies can be
L622: L (cid:0)θ , θ (cid:1) obtained by adding a proxy projection head composed of fully
L623: D GS D connected (FC) layers after the classifier. A feature projection
L624:  
L625: =
L626: θ
L627: mi
L628: ,θ
L629: n  − X M X ns m d m,i log D (cid:0) G s (cid:0) xs m,i (cid:1)(cid:1)  (6) h th e e ad fe , a w tu h r i e c s h t i o s t a h ls e o sa c m om e p s o p s a e c d e o a f s F th C e l p a r y o e x r i s e , s is [3 u 0 ti ] l . iz D e e d ta to ils m a a r p e
L630: Gs D m=1 i=1  given as follows.
L631: Authorized licensed use limited to: University of Science & Technology of China. Downloaded on July 05,2026 at 10:03:23 UTC from IEEE Xplore. Restrictions apply.
L633: ===== PAGE 6 =====
L635: 5408 IEEE TRANSACTIONS ON NEURAL NETWORKS AND LEARNING SYSTEMS, VOL. 36, NO. 3, MARCH 2025
L636: Fig. 4. Overview of the proposed CDSRN.
L637: Part 1 (Fault-Class-Proxy-Contrastive Learning): Fault- feature projection head P and a domain-proxy projection
L638: S
L639: class-proxy-contrastive learning contributes to the discrim- head P are involved in domain-proxy-contrastive learning.
L640: d
L641: inability of domain-invariant features. A domain-invariant The objective function of domain-proxy-contrastive learning
L642: feature projection head P and a fault-class-proxy projection is formulated as
L643: I
L644: head P participate in the fault-class-proxy-contrastive learn-
L645: f L (cid:0)θ , θ , θ , θ (cid:1)
L646: ing. The objective function of fault-class-proxy-contrastive dpcl GS PS D Pd
L647: learning is formulated as X M X ns m
L648: = max log
L649: L fpcl (cid:0)θ GI , θ PI , θ C , θ Pf (cid:1) θ GS ,θ PS ,θ D ,θ Pd m=1 i=1
L650: = θ ,θ ma ,θ x ,θ X M X ns m log × PM exp (cid:0)ωT z ex (cid:1) p (cid:0) + ω P m T z J S d m,i (cid:1) exp (cid:16) zT z (cid:17) (10)
L651: GI PI C Pf m=1 i=1 m=1 m Sm,i j=1,j̸=i Sj Sm,i
L652: exp
L653: (cid:0)ωT
L654: z
L655: (cid:1)
L656: × P k K =1 exp (cid:0)ω k T z Im,i (cid:1) + P c J j I = m f , 1 i ,j̸=i exp (cid:16) zT Ij z Im,i (cid:17) (9) w
L657: p
L658: b
L659: r
L660: y h
L661: o
L662: e
L663: x
L664: d r
L665: y
L666: o e
L667: ,
L668: m
L669: a
L670: z a
L671: n
L672: S i
L673: d
L674: m n ,i -
L675: J
L676: p i r s o
L677: re
L678: x t
L679: p
L680: h y
L681: r
L682: e
L683: e
L684: p
L685: s
L686: d r
L687: e
L688: o o
L689: n
L690: j m e
L691: ts
L692: c a t
L693: t
L694: i i
L695: h
L696: n o
L697: e
L698: - n s
L699: n
L700: p h
L701: u
L702: e e
L703: m
L704: c a i d
L705: b
L706: fi
L707: e
L708: c
L709: r
L710: P
L711: s
L712: f d e
L713: o
L714: , a
L715: f
L716: ω tu
L717: d
L718: m r
L719: o
L720: e
L721: m
L722: is o
L723: ai
L724: f t
L725: n
L726: h
L727: -
L728: x e
L729: c
L730: m
L731: l
L732: m
L733: a
L734: ,i
L735: s
L736: t
L737: s
L738: h p
L739: n
L740: r d o
L741: e
L742: o
L743: g
L744: je m
L745: a
L746: c
L747: t
L748: a t
L749: i
L750: e
L751: v
L752: in d
L753: e
L754: d
L755: where z Im,i is the domain-invariant feature of x m,i projected samples in the same fault class as the anchor sample x m,i .
L756: by domain-invariant feature projection head P , ω is the It is worth noting that fault-class-proxy-contrastive learning
L757: I k
L758: kth fault-class-proxy projected by fault-class-proxy projection and domain-proxy-contrastive learning complement promote
L759: head P , and J represents the numbers of in-domain fault- each other in the proposed proxy-contrastive representa-
L760: f f
L761: class negative samples of the anchor sample x m,i . tion enhancement module. Domain-proxy-contrastive learning
L762: Part 2 (Domain-Proxy-Contrastive Learning): Domain- enhances the discriminability of domain-specific features, thus
L763: proxy-contrastive learning enhances the discriminability of further facilitating the progress of domain-specific feature
L764: domain-specific features, thus further facilitating the progress removal branch. Then, the removal of domain-specific features
L765: of domain-specific feature removal branch. A domain-specific promotes the extraction of domain-invariant features, that
L766: Authorized licensed use limited to: University of Science & Technology of China. Downloaded on July 05,2026 at 10:03:23 UTC from IEEE Xplore. Restrictions apply.
L768: ===== PAGE 7 =====
L770: SONG et al.: CDSRN FOR SEMI-SUPERVISED GENERALIZATION FAULT DIAGNOSIS 5409
L771: TABLE I Algorithm 1 CDSRN
L772: NETWORK ARCHITECTURE OF THE PROPOSED CDSRN # Training stage
L773: Model: Domain-invariant feature extractor G , domain-
L774: I
L775: specific feature extractor G , fault classifier C, domain
L776: S
L777: classifier D, domain-invariant feature projection head P ,
L778: I
L779: domain-specific feature projection head P , fault class-proxy
L780: S
L781: projection head P and domain class-proxy projection head
L782: f
L783: P .
L784: d
L785: Input: Partially labeled source domain data Ds =
L786: train
L787: {Ds , Ds } = {Ds, {Ds }M−1}.
L788: train,labeled train,unlabeled 1 m m=1
L789: For q in epochs do:
L790: Step 1: Randomly sample source data from Ds .
L791: train
L792: Step 2: Forward propagation to calculate total loss
L793: function Eq. (11).
L794: Step 3: Backward propagation to update G , G , C,
L795: I S
L796: D, P , P , P and P by Eqs. (12)-(17).
L797: I S f d
L798: End for
L799: Return: Optimal G , G , C, D, P , P , P and P .
L800: I S I S f d
L801: #Testing stage
L802: Input: Unlabeled target domain data D = Dt.
L803: test
L804: Model: Optimal G and C.
L805: I
L806: Output: Classification results of D .
L807: test
L808: is, fault-class-proxy-contrastive learning. Subsequently, the
L809: enhancement of fault-class-proxy-contrastive learning means updated as follows:
L810: a more thorough disentanglement between domain-invariant ∂L ∂L ∂L ∂L !
L811: features and domain-specific features, thereby promoting θq ← θq−1 − µ C + GI,adv + λ cos + λ fpcl
L812: GI GI θq−1 θq−1 1 θq−1 2 θq−1
L813: the extraction of domain-specific features, i.e., domain- GI GI GI GI
L814: proxy-contrastive learning. As a result, the proxy-contrastive (12)
L815: representation enhancement module is capable of improving
L816: the efficacy of representation learning. ! !
L817: ∂L ∂L ∂L ∂L
L818: Table I lists the details of the proposed architecture. θq ←θq−1−µ λ D + GS,adv + cos +λ dpcl
L819: Domain-invariant feature extractor G and domain-specific
L820: GS GS 1 θq−1 θq−1 θq−1 2 θq−1
L821: I GS GS GS GS
L822: feature extractor G are the same structure, which consists of (13)
L823: S
L824: multiple convolution layers, pooling layers, batch normaliza-
L825: tion (BN), residual connection (RC), and rectified linear unit !
L826: (ReLU) activation functions. Network structures for classifiers θq ← θq−1 − µ
L827: ∂L
L828: C + λ
L829: ∂L
L830: S,adv + λ
L831: ∂L
L832: fpcl (14)
L833: C C θq−1 1 θq−1 2 θq−1
L834: C and D consist of FC layers, BN, ReLU, and Softmax
L835: C C C
L836: c P l S a , ss P ifi f e , r a a n c d tiv P a d ti a o r n e f c u o n m ct p io o n se . d T o h f e o fo n u e r F p C ro l j a e y c e ti r o . n heads d P I , θ D q ← θ D q−1 − µ ∂ θ L q− D 1 + λ 1 ∂ θ L q I − ,a 1 dv + λ 2 ∂ θ L q− dp 1 cl ! (15)
L837: D D D
L838: ∂L ∂L
L839: θq ← θq−1 − µ · λ fpcl , θq ← θq−1 − µ · λ fpcl
L840: PI PI 2 θq−1 Pf Pf 2 θq−1
L841: C. Network Training and Objective Optimization PI Pf
L842: (16)
L843: Based on the abovementioned network architecture, the final
L844: optimization objective is ∂L ∂L
L845: θq ← θq−1 − µ · λ dpcl , θq ← θq−1 − µ · λ dpcl
L846: PS PS 2 θq−1 Pd Pd 2 θq−1
L847: L (cid:0)θ , θ , θ , θ , θ , θ , θ , θ ,(cid:1) PS Pd
L848: total GI GS C D PI PS Pd Pf (17)
L849: = L (cid:0)θ , θ (cid:1) + L (cid:0)θ , θ (cid:1)
L850: + C λ (cid:8) G L I (cid:0) C θ , θ G (cid:1) I + ,adv L D G (cid:0)θ I , θ (cid:1) + L (cid:0)θ , θ (cid:1)(cid:9) where µ is the learning rate. The training and testing pseu-
L851: 1 D GS D GS,adv C GS cos GI GS docodes of the proposed CDSRN are detailed in Algorithm 1.
L852: + λ (cid:8) L (cid:0)θ , θ , θ , θ (cid:1) + L (cid:0)θ , θ , θ , θ (cid:1)(cid:9)
L853: 2 fpcl GI PI C Pf dpcl GS PS D Pd
L854: (11) V. EXPERIMENTAL STUDY
L855: In this section, experiments are conducted on two bear-
L856: where λ and λ are two coefficients to balance the losses. The ing datasets (including laboratory and public datasets) to
```

### Lines 868-1111

```text
L868: A. Datasets Description
L869: 1) SU Wheel Set Bearing Dataset: SU Wheel Set bearing
L870: dataset is used to verify the effectiveness and superiority of
L871: the proposed method for diagnosing wheel set bearing faults
L872: in simulated rail vehicle operation scenarios. The wheel set
L873: bearing test rig established by our own laboratory of Soochow
L874: University (SU) is displayed in Fig. 5(a) [29]. The wheel rail
L875: simulation part consists of a massive wheel set with a 280 mm
L876: TABLE III
L877: diameter acting as a stand-in for the rail and a smaller wheel
L878: GENERALIZATION DIAGNOSIS TASKS BUILT ON THE TWO ROLLING BEAR-
L879: set with a 200 mm diameter representing the train wheels. One ING DATASETS
L880: side of the small wheel set is home to the NJ208E test bearing,
L881: and an accelerometer is mounted on the bearing seat to collect
L882: vibration signals with a 32 768-Hz sampling frequency. Cracks
L883: with a width of 0.4 mm were manually produced on a range of
L884: bearing rolling surfaces. This dataset includes eight different
L885: health states of the tested bearing: one normal state (N); three
L886: single fault states, including inner race fault (I), outer race
L887: fault (O), and ball fault (B); and four compound fault states,
L888: including inner race and ball faults (IB), inner race and outer
L889: race faults (IO), outer race and ball faults (OB) and outer race,
L890: and inner race and ball faults (OIB), which are labeled using
L891: numbers 0–7.
L892: 2) PU Rolling Bearing Dataset: The utilization of PU
L893: rolling bearing dataset aims to prove the universality of the
L894: proposed method for diagnosing rolling bearing faults. This
L895: public dataset is provided by Paderborn University (PU) [31]
L896: and the test rig is shown in Fig. 5(b). Four types of health
L897: states, including normal state (N), inner race fault (I), outer
L898: race fault (O), and compound faults containing I and O (IO),
L899: respectively. Hence, the model is trained through a supervised
L900: are considered in this case. The four health states are labeled
L901: DA-based way and tested using the unseen target domain that
L902: by 0–3. The vibration data were collected at a sampling
L903: was not involved in model training.
L904: frequency of 64 kHz under four different working conditions.
L905: 2) M2: ADGN [28] is a state-of-the-art semi-supervised
L906: According to four working conditions, four domains of SU
L907: DG-based fault diagnosis method.
L908: Wheel Set bearing dataset and PU rolling bearing dataset can
L909: 3) M3: As a state-of-the-art DG method, PCL [22] is used in
L910: be denoted as S1–S4 and C1–C4, respectively, as presented in
L911: a semi-supervised manner with one labeled and two unlabeled
L912: Table II. Each fault class contains 100 samples with a length
L913: source domains in this comparative experiment.
L914: of 4096. Thus, generalization diagnosis tasks are constructed
L915: 4) M4: DIFFN [29] is a state-of-the-art semi-supervised DG
L916: in Table III. Note that only the first source domain emphasized
L917: method for machinery fault diagnosis.
L918: in bold is class-labeled.
L919: 5) M5: Causal disentanglement network (CDN) [18] is a
L920: state-of-the-art DG method for bearing fault diagnosis.
L921: B. Experimental Settings
L922: In this comparative experiment, the model is trained in a
L923: 1) Comparison Methods: To demonstrate the effectiveness semi-supervised manner with one labeled and two unlabeled
L924: and superiority of the proposed CDSRN, some comparison source domains.
L925: methods are used for analyses. 2) Implementation Details: In the proposed CDSRN, Adam
L926: 1) M1: DANN [21] is a classic DA model. In this compar- optimizer with weight decay of 0.01 and betas of (0.9,0.99)
L927: ative experiment, the labeled and unlabeled source domains is adopted for parameter update. The learning rate µ and the
L928: are viewed as the source and target domains for DANN, tradeoff parameters λ and λ are, respectively, set to 0.001,
L929: 1 2
L930: Authorized licensed use limited to: University of Science & Technology of China. Downloaded on July 05,2026 at 10:03:23 UTC from IEEE Xplore. Restrictions apply.
L932: ===== PAGE 9 =====
L934: SONG et al.: CDSRN FOR SEMI-SUPERVISED GENERALIZATION FAULT DIAGNOSIS 5411
L935: 0.5, and 1 by trials, which will be discussed in Section V-D.
L936: The total epochs and the batch size are set to 150 and 16,
L937: respectively.
L938: To reduce randomness and ensure the reliability of results,
L939: each diagnostic task was repeated five times and the aver-
L940: age result is used for analysis. For a fair comparison, all
L941: comparison methods share a similar network structure and
L942: experimental settings with the proposed method.
L943: C. Results and Analysis of Comparative Experiments
L944: 1) Performance Evaluation: Average accuracies and corre-
L945: sponding standard deviations of different methods on the SU
L946: Wheel Set bearing dataset and PU rolling bearing dataset are
L947: presented in Table IV. Some observations and conclusions can
L948: be drawn as follows.
L949: Fig. 6. Confusion matrices in task T2 by (a) M1, (b) M2, (c) M3, (d) M4,
L950: 1) M1 only obtains an average diagnosis accuracy of (e) M5, and (f) CDSRN.
L951: 74.39% and 80.34% in the two experiments, respectively,
L952: which is much worse than other methods. The result may be
L953: arisen from the neglection of unseen domain shift on the target
L954: domain, thereby deteriorating the generalization performance
L955: of DANN.
L956: 2) In the experiment of SU Wheel Set bearing dataset, there
L957: is a significant increase in the average diagnostic accuracy
L958: for M2, M3, M4, and M5 by 19.59%, 15.91%, 17.48%, and
L959: 8.59%, respectively, compared to M1. Comparable improve-
L960: ments can also be observed in the diagnosis accuracies of M2,
L961: M3, M4, and M5 for the PU rolling bearing dataset by 6.98%,
L962: 1.39%, 4.34%, and 0.69%, respectively. These findings may
L963: be attributed to the abilities of M2, M3, M4, and M5 to learn
L964: domain-common knowledge among source domains.
L965: Fig. 7. Confusion matrices in task Q4 by (a) M1, (b) M2, (c) M3, (d) M4,
L966: 3) The final average accuracy of the proposed CDSRN (e) M5, and (f) CDSRN.
L967: method reaches the highest average accuracy of 97.73%
L968: and 89.90% and the minimum standard deviation of 2.4%
L969: and 3.4% in the two experiments, which are superior
L970: to all the comparison methods. The result highlights the
L971: superiority of the proposed CDSRN method based on the
L972: combination of domain-specific feature removal branch and
L973: the proxy-contrastive representation enhancement module in
L974: extracting domain-invariant information and improving the
L975: generalization performance of the model.
L976: Meanwhile, Table V exhibits F1-scores [12] of different Fig. 8. ROC analysis of different methods in (a) task T2 and (b) task Q4.
L977: methods on different diagnosis tasks. It can be clearly seen
L978: that the proposed CDSRN has a higher performance than the In addition, the receiver operating characteristic (ROC)
L979: other comparison methods in both two datasets. curves [26] of different methods on diagnosis tasks T2 and
L980: Considering T2 of SU Wheel Set bearing dataset and Q4 of Q4 are shown in Fig. 8. The diagnostic performance can
L981: PU rolling bearing dataset, confusion matrices obtained by the be reflected by the area under the curves (AUC), which are
L982: different methods are, respectively, presented in Figs. 6 and 7 recorded in the parentheses of the legend. It is evident that
L983: to offer a more intuitive and detailed examination of the class- the curves of the proposed CDSRN in the SU Wheel Set
L984: wise results. It can be observed that fault categories diagnosed bearing dataset and PU rolling bearing dataset have the largest
L985: incorrectly by the comparison methods in Fig. 6(a)–(e) can be AUC values of 1.000 and 0.996, respectively, indicating the
L986: classified more accurately by the proposed CDSRN. For Q4 in superior diagnostic performance of the proposed method in
L987: Fig. 7, almost all methods can accurately diagnose the health semi-supervised DG-based fault diagnosis.
L988: states of N and IO, and their differences of diagnostic per- 2) Visualization Analysis: To further validate the perfor-
L989: formance mainly concentrate on the fault categories I and O. mance of the proposed CDSRN method, the T-distributed
L990: In summary, the effectiveness and superiority of the proposed stochastic neighbor embedding (t-SNE) technique [32] is
L991: CDSRN are further substantiated by the experimental results adopted to provide 2-D visualization of the features in the
L992: in Figs. 6 and 7. last layer of feature extractor on one trial of tasks T2 and Q4.
L993: Authorized licensed use limited to: University of Science & Technology of China. Downloaded on July 05,2026 at 10:03:23 UTC from IEEE Xplore. Restrictions apply.
L995: ===== PAGE 10 =====
L997: 5412 IEEE TRANSACTIONS ON NEURAL NETWORKS AND LEARNING SYSTEMS, VOL. 36, NO. 3, MARCH 2025
L998: TABLE IV
L999: ACCURACY AND STANDARD DEVIATION (%) OF THE DIAGNOSTIC RESULTS
L1000: TABLE V
L1001: F1-SCORE (%) OF THE DIAGNOSTIC RESULTS
L1002: TABLE VI
L1003: ACCURACY AND STANDARD DEVIATION (%) OF THE DIAGNOSTIC RESULTS
L1004: Fig. 9 shows the feature clustering results in task T2 by proposed CDSRN can learn more domain-invariant features on
L1005: different methods. Compared to these comparison methods, available source domains, thereby benefiting the generalization
L1006: the proposed CDSRN not only captures features that have on the unseen target domain.
L1007: the maximum interclass distance and the minimum intraclass 3) Statistical Tests: A comprehensive evaluation for the
L1008: distance in Fig. 9(f) but also realizes well generalization on
L1009: diagnostic performance of different methods was conducted
L1010: unseen domains colored by pink. As for the feature visualiza-
L1011: via statistical tests [12] on all 16 diagnostic tasks. In terms of
L1012: tion of task Q4, features learned through M1, M2, M4, and M5
L1013: diagnostic accuracy, the Friedman test statistic is 59.51 with a
L1014: in Fig. 10(a), (b), (d), and (e) fail to well aligned due to domain corresponding p-value of 3.06 × 10−7, which is less than 0.05,
L1015: discrepancies. From Fig. 10(c), although the ability of M3 to
L1016: implying the null hypothesis of no significant difference in the
L1017: extract domain-invariant features on seen domains is improved
L1018: performance of all these methods is rejected [33]. Meanwhile,
L1019: compared to M1, M2, M4, and M5, the unclear boundary in
L1020: the nonparametric Friedman test based on F-score was also
L1021: Fig. 10(c) is unsatisfactory. Instead, as shown in Fig. 10(f), the
L1022: used to reject the null hypothesis, with a Friedman test statistic
L1023: Authorized licensed use limited to: University of Science & Technology of China. Downloaded on July 05,2026 at 10:03:23 UTC from IEEE Xplore. Restrictions apply.
L1025: ===== PAGE 11 =====
L1027: SONG et al.: CDSRN FOR SEMI-SUPERVISED GENERALIZATION FAULT DIAGNOSIS 5413
L1028: Fig. 10. Feature visualization in task Q4 by (a) M1, (b) M2, (c) M3, (d) M4,
L1029: Fig. 9. Feature visualization in task T2 by (a) M1, (b) M2, (c) M3, (d) M4,
L1030: (e) M5, and (f) CDSRN.
L1031: (e) M5, and (f) CDSRN.
L1032: of 53.10 and a corresponding p-value of 3.71 × 10−6 less than
L1033: 0.05. Subsequently, post hoc analysis was performed using
L1034: the Wilcoxon–Holm method [34]. Finally, Fig. 11 shows the
L1035: computed critical difference diagram. The proposed CDSRN
L1036: is always ranked as first in Fig. 11(a) and (b), indicating
L1037: that CDSRN significantly outperforms all other comparison
L1038: methods.
L1039: D. Ablation Study
L1040: Fig. 11. Critical difference diagrams of post hoc Friedman test based on
L1041: Ablation experiments were conducted to examine the effec- (a) accuracy and (b) F1-score.
L1042: tiveness of our design in the proposed CDSRN. Tables VI
L1043: and VII conclude the diagnostic accuracies and F1-scores
L1044: after removing the domain-specific feature removal branch, CDSRN. Considering their impact on the model performance,
L1045: i.e., L D and L S,adv and L cos , and proxy-contrastive represen- parameter sensitivity analyses are performed in this subsection.
L1046: tation enhancement module, i.e., L and L , respectively. Given that the core innovations of the proposed CDSRN
L1047: fpcl dpcl
L1048: The results show that the performance significantly declines lie on the domain-specific feature removal branch and
L1049: when removing the domain-specific feature removal branch. proxy-contrastive representation enhancement module, the cor-
L1050: Such a phenomenon verifies that the domain-specific infor- responding loss balance coefficients λ 1 and λ 2 determine the
L1051: mation truly exists in the learned features and affects relative importance of the two parts in the overall optimization.
L1052: the performance of DG-based fault diagnosis. Meanwhile, T2 and Q4 are taken as the typical examples for the analysis
L1053: the decrease in diagnostic performance of removing the of the coefficients λ 1 and λ 2 . Fig. 12 shows the diagnosis
L1054: proxy-contrastive representation enhancement module indi- accuracies with variable values of the coefficient λ 1 and
L1055: cates that the proxy-contrastive representation enhancement λ 2 in the range of [1, 0.1]. It can be observed that the
L1056: module can help better learning of domain-invariant features. diagnostic accuracy of the model decreases when λ 1 is too
L1057: large and λ is too small. It indicates that the proportion of the
L1058: 2
L1059: proxy-contrastive representation enhancement module should
L1060: E. Discussion
L1061: be higher. Generally, as depicted by the red dashed ellipses on
L1062: 1) Hyperparameters Analysis: Some adjustable parameters the horizontal projection surfaces of the 3-D curves in Fig. 12,
L1063: are involved in the construction and training of the proposed λ and λ are suggested to be, respectively, selected within the
L1064: 1 2
L1065: Authorized licensed use limited to: University of Science & Technology of China. Downloaded on July 05,2026 at 10:03:23 UTC from IEEE Xplore. Restrictions apply.
L1067: ===== PAGE 12 =====
L1069: 5414 IEEE TRANSACTIONS ON NEURAL NETWORKS AND LEARNING SYSTEMS, VOL. 36, NO. 3, MARCH 2025
L1070: TABLE VII
L1071: F1-SCORE (%) OF THE DIAGNOSTIC RESULTS
L1072: Fig. 13. Diagnosis performance of different learning rates for CDSRN.
L1073: Fig. 14. PAD of (a) source domains and (b) source domains and target
L1074: domain on SU Wheel Set bearing dataset.
L1075: training process. Then, among the three curves of µ < 0.1,
L1076: µ = 0.001, which brings the best accuracy for T1–T4, and
L1077: Q1–Q4 is recommended in this article to guarantee the mode
L1078: performance.
L1079: Fig. 12. Sensitivity analysis of the coefficient λ1 and λ2 in (a) task T2 and
L1080: 2) Domain Divergence Analysis: Proxy A-distance (PAD)
L1081: (b) task Q4.
L1082: [12] is adopted to quantitatively evaluate the generalization
L1083: performance of the proposed CDSRN from the perspective
L1084: of domain divergence. A larger value of PAD means greater
L1085: ranges of [0.3, 0.5] and [1, 0.7] where the proposed CDSRN domain divergence.
L1086: performs well on both T2 and Q4. Therefore, in this article, For easy visualization, domain divergence analysis of SU
L1087: it is feasible for λ and λ to be set as 0.5 and 1, respectively. Wheel Set bearing dataset is presented in Fig. 14 and DANN
L1088: 1 2
L1089: The learning rate µ controls the step size of model parame- is taken as the baseline. Fig. 14(a) shows the values of
L1090: ter update, making it a vital hyperparameter in model training. PAD for different pairs of source domains. All values are
L1091: Fig. 13 illustrates the diagnosis performance with different below the diagonal, indicating that the proposed CDSRN
L1092: values of the learning rate µ for the proposed CDSRN. It can facilities smaller PAD among the source domains, i.e., smaller
L1093: be found that the model performance will drop dramatically source domain divergence. Values of PAD for different source
L1094: when µ ≥ 0.1. It may be because large values of the learning domains and corresponding target domains are shown in
L1095: rate lead to large step sizes of model parameter update, Fig. 14(b). The result implies that the PAD of the proposed
L1096: which may cause the model unable to converge during the CDSRN is smaller than the baseline, indicating smaller domain
L1097: Authorized licensed use limited to: University of Science & Technology of China. Downloaded on July 05,2026 at 10:03:23 UTC from IEEE Xplore. Restrictions apply.
L1099: ===== PAGE 13 =====
L1101: SONG et al.: CDSRN FOR SEMI-SUPERVISED GENERALIZATION FAULT DIAGNOSIS 5415
L1102: divergence between source domains and the target domain. [6] X. Jiang et al., “Central frequency mode decomposition and its appli-
L1103: Based on the quantitative analysis via PAD, the proposed cations to the fault diagnosis of rotating machines,” Mechanism Mach.
L1104: Theory, vol. 174, Aug. 2022, Art. no. 104919.
L1105: CDSRN shows feasible ability of eliminating domain diver-
L1106: [7] Q. Song, X. Jiang, G. Du, J. Liu, and Z. Zhu, “Smart multichannel mode
L1107: gence not only among source domains but also between source extraction for enhanced bearing fault diagnosis,” Mech. Syst. Signal
L1108: domains and the target domain. Process., vol. 189, Apr. 2023, Art. no. 110107.
L1109: [8] B. Cai et al., “Artificial intelligence enhanced two-stage hybrid fault
L1110: prognosis methodology of PMSM,” IEEE Trans. Ind. Informat., vol. 18,
L1111: VI. CONCLUSION no. 10, pp. 7262–7273, Oct. 2022.
```

## Domain_Perturbation_With_Uncertainty_for_Bearing_Fault_Diagnosis_Under_Unseen_Conditions.txt
- Total extracted lines: 758

### Lines 1-50

```text
L3: ===== PAGE 1 =====
L5: 4956 IEEE TRANSACTIONS ON CYBERNETICS, VOL. 55, NO. 10, OCTOBER 2025
L6: Domain Perturbation With Uncertainty for Bearing
L7: Fault Diagnosis Under Unseen Conditions
L8: Yongyi Chen , Dan Zhang , Senior Member, IEEE, Ruqiang Yan , Fellow, IEEE, Min Xie , Fellow, IEEE,
L9: and Qi Xuan , Senior Member, IEEE
L10: Abstract—Domain adaptation (DA) techniques are becoming long been discovered that the success of DL heavily relies on
L11: increasingly proficient in cross-domain fault diagnosis tasks. the assumption that training and testing data follow indepen-
L12: However, DA-based methods are not always applicable due to
L13: dent and identical distributions [5], [6]. Unfortunately, in real
L14: the target domain data is not always accessible. Although there
L15: industrial scenarios, this assumption is difficult to hold. Due
L16: have been some interesting domain generalization methods for
L17: fault diagnosis under unseen conditions, most of them can only to the interference of operating conditions and environmental
L18: be used to mine the fault features on source domain distributions, noise, it is impossible to ensure that the data collected at
L19: and the improvement of model generalization performance is every moment has the same data distribution. In this case,
L20: limited. To solve this problem, the multiplicative noise Gaussian
L21: the diagnosis network obtained by fitting the source domain
L22: perturbation strategy and the additive noise linear fusion strategy
L23: data could fail on data from new domains [7]. To reduce the
L24: are proposed to capture fault information beyond source domain
L25: distributions. The former is used to randomly perturb feature performance loss of diagnosis networks caused by domain
L26: statistics of multisource domains to simulate the uncertainty of shift, domain adaptation (DA) technology is introduced into
L27: domain shift, while the latter is used to perform the additive noise fault diagnosis in some researches [8]. DA technology aims
L28: linear operation on feature statistics of multiple source domains
L29: to make the model adapt and learn based on the target
L30: to ensure the authenticity of the generated feature styles. Further,
L31: domain data received, so as to generalize the fault knowledge
L32: the feature statistics generated by both strategies are mixed with
L33: random convex weights to obtain new feature styles, achieving the learned in the source domain to the target domain. The
L34: best compromise between reliability and diversity. The network most common DA technique is unsupervised DA (UDA).
L35: can learn more fault information from features with diversified Recent UDA methods can be divided into two categories, i.e.,
L36: styles. Extensive experimental results on both public and real
L37: adversarial learning (AL) and reconstruction learning (RL).
L38: datasets verify the effectiveness of our approach.
L39: The former is used to align the marginal distribution (or
L40: Index Terms—Deep learning (DL), domain generalization conditional distribution) of the data from both domains using
L41: (DG), fault diagnosis, feature styles, unseen conditions.
L42: the distance function, and the latter is used to realize the
L43: domain-invariant feature learning by reconstructing the target
L44: I. INTRODUCTION domain data.
L45: DEEP learning (DL) has demonstrated remarkable ability The assumption that the label spaces of the source and
L46: target domains are aligned needs to be satisfied in the UDA
L47: in fault diagnosis, which is proven to be effective in
L48: method. In reality, however, it is difficult to ensure that
L49: many fault diagnosis tasks [1], [2], [3], [4]. However, it has
L50: the label space of the target domain is consistent with that
```

### Lines 120-220

```text
L120: diagnosis, such as causal learning [35], [36], [37], meta learn- data and focus on learning the domain-invariant feature rep-
L121: ing [38], [39], and contrastive learning [30], [40]. However, resentation in the hope that it will remain discriminative
L122: these methods suffer from two major limitations. given the target domain data. Intuitively, the most direct and
L123: 1) In most existing DG methods, new learning mecha- efficient way to improve the generalization ability of the
L124: nisms are usually designed to align multisource domain DG model on the unseen domain data is to let the network
L125: distributions to guide models to learn domain-invariant learn more fault feature styles under limited source domain
L126: features. However, this common practice causes the data. For this purpose, a novel fault diagnosis network, i.e.,
L127: diagnosis model to overfit the feature styles of the exist- DGNSU, is developed to enable the model to learn more styles
L128: ing source domain. Especially, there is no guarantee that of fault features under limited source domain data. Overall,
L129: the diagnosis knowledge learned from the multisource DGNSU comprises the steps listed as follows (see Fig. 1 for
L130: domain data can be effectively generalized to the unseen details).
L131: domain data when the domain gap is large. 1) Two new datasets are first constructed by alternating
L132: 2) Although data-augmentation-based methods (e.g., [28] combinations of labeled multisource domain data as
L133: and [30]) can enable the network to learn more styles the network input, and then network bottom features
L134: of fault features, the augmented data is only a linear of the input data are extracted to capture their style
L135: combination or linear transformation of multisource information.
L136: domain data. The augmented data distribution is difficult 2) Next, the MNGP and ANLF strategies are designed to
L137: to be independent of source domain distributions, which perturbate the feature style vectors of source domains to
L138: makes the model unable to learn potential domain shifts generate new feature styles that are different from the
L139: in unseen conditions. original styles in source domains.
L140: In this article, our architecture, DG network with statistical 3) Finally, new styles are applied to the style-normalized
L141: uncertainty (DGNSU), is designed to be an efficient architec- features to generate features with new styles by adaptive
L142: ture for improving the performance of the diagnosis model instance normalization (AdaIN). The generated features
L143: over unseen conditions. Our main contributions are as follows. are fed into the encoder for fault feature extraction to
L144: 1) The multiplicative noise Gaussian perturbation (MNGP) improve the diversity of fault knowledge learned by the
L145: strategy is designed to model potential domain shift for diagnosis network.
L146: the uncertainty and randomness of unseen conditions. In Remark 1: Instance-normalization (IN) is used to normalize
L147: the MNGP strategy, new styles that do not exist in source feature F according to the mean and standard deviation
L148: x
L149: domains are randomly generated from a range that is of F and perform affine transformations. At this stage, F
L150: x x
L151: relatively consistent with source domain distributions, is transformed into a data distribution with mean 0 and
L152: Authorized licensed use limited to: University of Science & Technology of China. Downloaded on July 05,2026 at 10:05:07 UTC from IEEE Xplore. Restrictions apply.
L154: ===== PAGE 3 =====
L156: 4958 IEEE TRANSACTIONS ON CYBERNETICS, VOL. 55, NO. 10, OCTOBER 2025
L157: perturbation strategies, i.e., MNGP and ANLF, are designed
L158: to make the network more robust to different domain shifts
L159: in this article.
L160: More specifically, two source domains are defined as Dm
L161: and Dn; here, Ds = (xs, ys)R . R is the number of samples,
L162: k k k=1
L163: xs is the kth sample of source domain s, and ys is the label
L164: k k
L165: corresponding to sample xs. The goal of the proposed method
L166: k
L167: is to use limited source domain data to train a model that can
L168: generalize to any unseen conditions. In the testing stage, the
L169: model is evaluated on a new domain that does not overlap with
L170: source domains. To make full use of the style information in
L171: the both source domains, X1 = {Dm, Dn} and X2 = {Dn, Dm}
L172: are constructed by alternating combinations of source domains
L173: Dm and Dn. As shown in Fig. 2, X1 and X2 are obtained by
L174: exchanging the positions of Dm and Dn and are shuffled using
L175: the same shuffling operation. At this stage, samples at the
L176: same position in X1 and X2 come from different domains and
L177: have the same labels. X1 is used to normalize the feature style
L178: (similar to F in (2)) and X2 is used to generate new feature
L179: x
L180: styles (similar to F in (2)).
L181: y
L182: To capture the style information of each sample in X1
L183: and X2, a mini-batch of samples is fed into a convolutional
L184: α β
L185: layer to extract the features F and F at the bottom layers
L186: of the network. Since the operating condition information of
L187: the target domain data is unseen, the period and amplitude
L188: change of the vibration signal are uncertain. If only feature
L189: statistics of samples from different source domains are used
L190: as the determined values for the diagnosis network to learn,
L191: the network can only learn fault information within the given
L192: Fig. 1. Overall flow of the proposed method. distribution range of feature statistics. Once the target domain
L193: has a large domain shift compared with the source domain,
L194: the fault knowledge learned by the network will be difficult
L195: variance 1, thus achieving style normalization to generalize to the target domain data.
L196: (cid:2) (cid:3)
L197: x − μ(F ) 2) Multiplicative Noise Gaussian Perturbation Strategy: In
L198: IN(F x ) = γ σ(F ) x + β. (1) view of uncertainty and randomness of domain shift, the
L199: x
L200: MNGP strategy is designed to generate uncertainty distri-
L201: AdaIN [41] is an improvement on IN to align the mean and butions of feature statistics to simulate the feature styles
L202: variance of each channel of F x with the mean and variance of under different domain shifts. Since the distribution of the
L203: the target feature F y , thereby transforming the style of source newly generated feature statistics is uncertain, the network
L204: domain features into that of target domain features is required to reduce the domain perturbations and encode
L205: (cid:2) (cid:3)
L206: (cid:4) (cid:5) x − μ(F ) (cid:4) (cid:5) better domain-invariant features during training, so as to
L207: AdaIN(F ) = σ F x + μ F . (2) improve the generalization performance of the network for
L208: x y σ(F ) y
L209: x unseen conditions. In the MNGP strategy, the channel-wise
L210: feature mean and standard deviation of each instance feature
L211: B. Uncertainty Estimation of Domain Shift F α and F β ∈ RC×W in a mini-batch are calculated to
L212: b b
L213: 1) Uncertainty Analysis of Feature Statistics: Some obtain the feature statistics at the bottom features of the
L214: research suggests that the style information of the sample network
L215: is preserved at the bottom layer of the network and the
L216: semantic information is at the top layer through instance-level
L217: feature statistics [41], [42]. Replacing the feature statistics (cid:4) (cid:5) 1 (cid:6)W
L218: at the bottom layers of the network can change feature μ F b α = W F b α ,w (3)
L219: styles while ensuring that semantic information remains w=1
L220: u ra n n c d h o a m nge p d e . rtu T r h b e a r t e io fo n re o , f it the can fea b tu e re re s a t s a o ti n s a ti b c l s y a a t ss t u h m e e b d ott t o h m at μ (cid:7) F b β (cid:8) = W 1 (cid:6)W F b β ,w (4)
```

### Lines 220-390

```text
L220: u ra n n c d h o a m nge p d e . rtu T r h b e a r t e io fo n re o , f it the can fea b tu e re re s a t s a o ti n s a ti b c l s y a a t ss t u h m e e b d ott t o h m at μ (cid:7) F b β (cid:8) = W 1 (cid:6)W F b β ,w (4)
L221: layer of the network can enable the network to learn more (cid:9) w=1
L222: (cid:10)
L223: styles of fault features under limited source domain data, thus (cid:4) (cid:5) (cid:10) (cid:6)W (cid:7) (cid:4) (cid:5)(cid:8)
L224: improving the generalization ability of the entire diagnosis σ F α = (cid:11) 1 F α − μ F α 2 (5)
L225: b W b,w b
L226: network. On the basis of this hypothesis, appropriate domain w=1
L227: Authorized licensed use limited to: University of Science & Technology of China. Downloaded on July 05,2026 at 10:05:07 UTC from IEEE Xplore. Restrictions apply.
L229: ===== PAGE 4 =====
L231: CHEN et al.: DOMAIN PERTURBATION WITH UNCERTAINTY FOR BEARING FAULT DIAGNOSIS 4959
L232: Fig. 2. Overview of DGNSU.
L233: (cid:9)
L234: σ (cid:7) F b β (cid:8) = (cid:10) (cid:10) (cid:11) W 1 w (cid:6)W =1 (cid:7) F b β ,w − μ (cid:7) F b β (cid:8)(cid:8) 2 (6) μσ B = B 1 (cid:6) b= B 1 σ (cid:7) F b β (cid:8) (8)
L235: (cid:4) (cid:5) (cid:6)B (cid:7) (cid:7) (cid:8) (cid:8)(cid:7) (cid:7) (cid:8) (cid:8)
L236: σμ 2 = 1 μ F β − μμ μ F β − μμ T (9)
L237: where μ(F) ∈ RC and σ(F) ∈ RC represent the channel-wise B B b B b B
L238: b=1
L239: feature mean and standard deviation computed within each (cid:4) (cid:5) (cid:6)B (cid:7) (cid:7) (cid:8) (cid:8)(cid:7) (cid:7) (cid:8) (cid:8)
L240: channel of F, respectively. Similar to the feature generation σσ 2 = 1 σ F β − μσ σ F β − μσ T . (10)
L241: process of AdaIN in (2), μ(F α) and σ(F α) are applied to B B b B b B
L242: b b b=1
L243: normalize feature styles, while μ(F β) and σ(F β) are used to
L244: b b Once the uncertainty estimates of the feature statistics of
L245: generate new feature styles in this article.
L246: each feature channel are obtained, two Gaussian distributions
L247: Some generative-based studies [43], [44] show that vari- N μ (μμ, (σμ)2) and N σ (μσ, (σσ)2) can be built to simulate
L248: ances between features can be used to measure the range of B B B B
L249: the variety of both feature style vectors. To further enhance the
L250: changes in semantic information. Inspired by this, the variance
L251: uncertainty and randomness of the feature style vectors sim-
L252: of feature statistics is used to guide the generation of new ulated by N μ and N σ, nonlinear perturbations are introduced
L253: feature styles. As shown in Fig. 2, the mean and variance of
L254: feature statistics μ(F β) and σ(F β) for all instance features in into the uncertainty estimation of fe β ature stat ¨ is β tics. Particularly,
L255: b b multiplicative noise is added to F to get F and the feature
L256: a mini-batch are calculated ¨β b b
L257: statistics of F are calculated as
L258: b
L259: (cid:6)B (cid:7) (cid:8) (cid:7) (cid:8) (cid:6)W
L260: μμ = 1 μ F β (7) μ F ¨β = 1 F ¨β (11)
L261: B B b b W b,w
L262: b=1 w=1
L263: Authorized licensed use limited to: University of Science & Technology of China. Downloaded on July 05,2026 at 10:05:07 UTC from IEEE Xplore. Restrictions apply.
L265: ===== PAGE 5 =====
L267: 4960 IEEE TRANSACTIONS ON CYBERNETICS, VOL. 55, NO. 10, OCTOBER 2025
L268: (cid:9)
L269: (cid:10)
L270: σ (cid:7) F ¨ b β (cid:8) = (cid:10) (cid:11) W 1 (cid:6)W (cid:7) F ¨ b β ,w − μ (cid:7) F ¨ b β (cid:8)(cid:8) 2 . (12) o ra n ng th e e o f f e t a h tu e r g e e s n t e a r t a is t t e i d cs fe o a f tu s r o e ur s c ty e le d s o . mains, thus limiting the
L271: w=1 In the ANLF strategy, μ(F α) and σ(F α) used to normalize
L272: b b
L273: β feature styles are applied to generate new feature styles so that
L274: Since F varies nonlinearly under the influence of
L275: b the newly generated features can be as similar as possible to
L276: multiplicative noise, the uncertainty estimates generated by the
L277: ¨β the source domain features. Specifically, Gaussian white noise
L278: feature statistics of F can better characterize the changes in
L279: b with mean 0 and standard deviation 1 is added to the source
L280: data distribution caused by domain shift α ¯ α
L281: domain feature F to obtain F , which aims to ensure the
L282: b b
L283: (cid:6)B (cid:7) (cid:8) authenticity of feature styles while making the model resist
L284: μ¨μ = 1 μ F ¨β (13) some random interference. The feature mean and standard
L285: B B b ¯ α
L286: b=1 deviation of each channel of F are
L287: b
L288: (cid:6)B (cid:7) (cid:8)
L289: μ¨σ B = B 1 b=1 σ F ¨ b β (14) μ (cid:4) F ¯ b α (cid:5) = W 1 (cid:6)W F ¯ b α ,w (23)
L290: (cid:4) σ¨ B μ (cid:5) 2 = B 1 (cid:6) b= B 1 (cid:7) μ (cid:7) F ¨ b β (cid:8) − μ¨μ B (cid:8)(cid:7) μ (cid:7) F ¨ b β (cid:8) − μ¨μ B (cid:8) T (15) σ (cid:4) F ¯ b α (cid:5) = (cid:9) (cid:10) (cid:10) (cid:11) W w 1 = (cid:6) 1 W (cid:7) F ¯ b α ,w − μ (cid:4) F ¯ b α (cid:5)(cid:8) 2 . (24)
L291: (cid:4) (cid:5) (cid:6)B (cid:7) (cid:7) (cid:8) (cid:8)(cid:7) (cid:7) (cid:8) (cid:8) w=1
L292: σ¨ B σ 2 = B 1 b=1 σ F ¨ b β − μ¨σ B σ F ¨ b β − μ¨σ B T . (16) and Fi t n h a e ll n y o , i t s h e e d fe fe a a tu tu re re st F ¯ at α is a ti r c e s m of ix t e h d e s to ou r r e c a e ch do th m e ai f n ul f l e p a o tu te re nt F ia b α l
L293: b
L294: ¨β of linear interpolation, see below
L295: At this stage, the distributions of both style vectors for F
L296: b (cid:4) (cid:5) (cid:4) (cid:5) (cid:4) (cid:5)
L297: in a mini-batch are obtained. To make the generated feature μ F ˜ α = ω˜ μ F ¯ α + ω˜ μ F α (25)
L298: (cid:4) b (cid:5) 1 (cid:4) b(cid:5) 2 (cid:4) b(cid:5)
L299: styles as different as possible from the source domains while σ F ˜ α = ω˜ σ F ¯ α + ω˜ σ F α (26)
L300: ensuring that the new feature styles are valid, the mean and b 1 b 2 b
L301: variance of feature statistics for F β and F ¨β are balanced where ω˜ and ω˜ are hyperparameters controlling the tradeoff
L302: 1 2
L303: μˆ μ = ωˆ μμ + ωˆ μ¨μ (17) between both feature statistics.
L304: B 1 B 2 B
L305: μˆ σ = ωˆ μσ + ωˆ μ¨σ (18)
L306: (cid:4) (cid:5)B 1(cid:4) B (cid:5) 2 B(cid:4) (cid:5) C. New Style Generation and Diagnosis Network Design
L307: (cid:4) σˆ B μ (cid:5) 2 = ωˆ 1 (cid:4) σ B μ (cid:5) 2 + ωˆ 2 (cid:4) σ¨ B μ (cid:5) 2 (19) We combine MNGP and ANLF strategies to generate
L308: σˆ σ 2 = ωˆ σσ 2 + ωˆ σ¨ σ 2 (20) new feature styles. The two strategies have advantages in
L309: B 1 B 2 B
L310: diversity and reliability, respectively, so the feature statistics
L311: where ωˆ 1 and ωˆ 2 are hyperparameters controlling the tradeoff generated by the two strategies are mixed with random convex
L312: between both uncertain estimates. weights [45] to generate new feature statistics. Specifically
L313: Finally, inspired by [42], a pair of style vectors μˆ and σˆ (cid:4) (cid:5)
L314: s s ς = γ μ F ˜ α + (1 − γ )μˆ (27)
L315: can be selected from the corresponding Gaussian distributions DIG (cid:4) (cid:5) s
L316: N μ and N σ by random sampling ρ DIG = γ σ F ˜ α + (1 − γ )σˆ s (28)
L317: (cid:7) (cid:4) (cid:5) (cid:8)
L318: μˆ s ∼ N μ (cid:7) μˆ μ B , (cid:4) σˆ B μ (cid:5) 2 (cid:8) (21) d w i h st e r r i e bu γ tio i n s . a In w s e p i i g re h d t t b h y at a i r s bi r t a ra n r d y om sty ly le s t a r m an p s l f e e d r f i r n om Ad t a h I e N B , t e h t e a
L319: σˆ s ∼ N σ μˆ σ B , σˆ B σ 2 . (22) generated feature statistics ς DIG and ρ DIG are applied to style-
L320: α
L321: normalized F to change its feature style
L322: The MNGP strategy can be used to generate the feature style
L323: F α − μ(F α)
L324: vectors randomly in the specified distribution range, so that F = ς + ρ . (29)
L325: new DIG σ(Fα) DIG
L326: the generation of feature styles can break out of the limitation
L327: of feature statistics in the source domain to obtain new styles The fusion of two generation strategies of feature statistics
L328: that do not exist in the source domain. makes the generated new feature styles achieve the best
L329: 3) Additive Noise Linear Fusion Strategy: The MNGP compromise between reliability and diversity. The proposed
L330: strategy can greatly improve the diversity of feature styles, but method aims to perturb the feature statistics of multiple source
L331: the generated feature styles have randomness and uncertainty domain instances without access to the target domain data,
L332: due to the introduction of two nonlinear operations in the allowing the network to learn more styles of fault features.
L333: sampling process of feature style vectors. Some new styles The entire framework of the proposed DGNSU is presented
L334: may be very different from those of source domain data, which in Fig. 2. Features with new styles generated by MNGP and
L335: brings the risk of authenticity. If there is no restriction in the ANLF strategies are used to update the feature extractor
L336: generated random styles, the learning of the diagnosis network and classifier, avoiding network fitting to specific domain
L337: may be negatively affected. To make the generated styles more styles. Due to the generated features have different distribution
L338: reliable, the ANLF strategy is developed to compensate for the possibilities, the diagnosis network has better robustness to
L339: authenticity risk caused by the MNGP strategy. Particularly, different domain shift. In this article, PCAB [46] (cosine
L340: new feature statistics are generated only by linear operations module removed) is used to build the feature extractor of
L341: Authorized licensed use limited to: University of Science & Technology of China. Downloaded on July 05,2026 at 10:05:07 UTC from IEEE Xplore. Restrictions apply.
L343: ===== PAGE 6 =====
L345: CHEN et al.: DOMAIN PERTURBATION WITH UNCERTAINTY FOR BEARING FAULT DIAGNOSIS 4961
L346: TABLE I Algorithm 1 Training Procedures of DGNSU
L347: DETAILS OF THE PROPOSED DGNSU STRUCTURE
L348: Input: The training sets X1 = {Dm, Dn} and X2 = {Dn, Dm};
L349: The hyper-parameter ωˆ , ωˆ , ω˜ and ω˜ .
L350: 1 2 1 2
L351: 1: for each training epoch do
L352: 2: for each data batch do
L353: α β
L354: 3: Output the bottom features F and F of a mini-batch
L355: of samples in X1 and X2 through a convolutional
L356: layer; (cid:4) (cid:5)
L357: 4: C
L358: (cid:4)
L359: alcu
L360: (cid:5)
L361: late respe(cid:7)ctive(cid:8)ly t(cid:7)he f(cid:8)eature statistics (μ F
L362: b
L363: α ,
L364: σ F α ) and (μ F β , σ F β ) of F α and F β accord-
L365: b b b b b
L366: ing to Eqs. (3)-(6);
L367: ¨β β
L368: 5: Obtain F by adding multiplicativ(cid:7)e no(cid:8)ise t(cid:7)o F (cid:8);
L369: b b
L370: 6: Calculate the feature statistics (μ F ¨β , σ F ¨β ) of
L371: b b
L372: β
L373: F according to Eqs. (11) and (12);
L374: b (cid:4) (cid:5)
L375: 7: Calcu
L376: (cid:4)
L377: late
L378: (cid:5)
L379: the unc(cid:7)ertai(cid:8)nty estim(cid:7) ate(cid:8)s (μμ
L380: B
L381: , σ
L382: B
L383: μ 2) and
L384: DGNSU. The network parameters of DGNSU are shown in (μσ , σσ 2) of μ F β and σ F β according to Eqs.
L385: Table I. 64 samples are sampled from two source domain B B b b
L386: d 64 at × as 2 et d s u i r n in e g ac t h ra m in i i n n i g -b . a T tc h h e , p so ro t p h o e se b d atc D h G s N iz S e U of i t s he su n m et m w a o r r i k ze i d s 8: C (7 a ) l - c ( u 1 (cid:4) l 0 a ) t ; e (cid:5) the unc(cid:7)ertai(cid:8)nty estim(cid:7) ate(cid:8)s (μ¨μ B , (cid:4) σ¨ B μ (cid:5) 2) and
L387: in Algorithm 1. (μ¨σ , σ¨ σ 2) of μ F ¨β and σ F ¨β according to Eqs.
L388: B B b b
L389: (13)-(16); (cid:4) (cid:5) (cid:4) (cid:5)
L390: III. EXPERIMENTS 9: Obtain μˆ μ
```

### Lines 390-562

```text
L390: III. EXPERIMENTS 9: Obtain μˆ μ
L391: B
L392: , μˆ σ
L393: B
L394: , σˆ
L395: B
L396: μ 2 and σˆ
L397: B
L398: σ 2 according to Eqs.
L399: (17)-(20);
L400: A. Dataset Description
L401: 10: Build Gaussian distributions N μ and N σ for two style
L402: We tested the performance of the proposed method on both β
L403: vectors of F ;
L404: real and public datasets. In each dataset, 2450 samples were b
L405: used for training and 1200 samples were used for testing. Each 11: Sample randomly a pair of style vectors μˆ s and σˆ s
L406: according to Eqs. (21) and (22);
L407: vibration signal sample was preprocessed by power spectrum ¯ α β
L408: estimation method, and each sample contains 2048 data points. 12: Obtain F b by adding additive no (cid:4) ise (cid:5) to F (cid:4)b ; (cid:5)
L409: 1) ZJUT Dataset: As shown in Fig. 3, the real dataset 13: Calculate the feature statistics (μ F ¯ b α , σ F ¯ b α ) of F b β
L410: came from Zhejiang University of Technology (ZJUT). The
L411: according(cid:4) to (cid:5)Eqs. (23(cid:4)) a(cid:5)nd (24);
L412: fan end bearing of three-phase asynchronous motor were 14: Obtain μ F ˜ b α and σ F ˜ b α according to Eqs. (25) and
L413: monitored with a sampling rate of 16 kHz. Four health states (26); (cid:4) (cid:5)
L414: are designed, i.e., normal, outer race fault (OF), inner race 15: O σ (cid:4)b F t ¯ a α in(cid:5) ) (ς w D i I t G h , r ρ a D n I d G o ) m by co m n i v x e in x g w (μ e ˆ i s g , h σˆ ts s ) a a c n c d or ( d μ in F g ¯ b α to ,
L415: fault (IF) and ball fault (BF), with three levels of damage for b
L416: Eqs. (27) and (28);
L417: each fault state, i.e., 0.1 (L1), 0.3 (M1), and 0.5 mm (H1). As
L418: shown in Table II, six conditions were simulated to verify the 16: Generate features with new styles (F new ) by applying
L419: ς and ρ to style-normalized F α according to
L420: generalization of the model. DIG DIG
L421: Eq. (29);
L422: 2) CWRU Dataset: In the Case Western Reserve University
L423: (CWRU) public dataset [47], bearing damage occurs at three 17: Extract the fault features of F new by the encoder.
L424: different locations, i.e., OF, IF, and BF. There are three fault 18: Use RMSprop optimization algorithm to train
L425: DGNSU by minimizing the cross-entropy loss func-
L426: diameters for different locations, i.e., 0.1778 (L2), 0.3556
L427: tion.
L428: (M2), and 0.5334 mm (H2). In this article, the bearing fault
L429: data collected at the sampling frequency of 12 kHz was used 19: end for
L430: as the experimental data for experimental verification. The 20: end for
L431: Output: Trained DGNSU
L432: setting of operating conditions is shown in Table III.
L433: B. Comparisons With State-of-the-Art
L434: 1) Comparative Methods: We show the effectiveness of
L435: DGNSU by comparing it with several state-of-the-art methods. 2) ADIG [29] (DG): It learns domain-invariant knowledge
L436: All methods are trained on data from both source domains in multisource domain data through AL between the
L437: and tested on unseen target domain data. The details of these feature extractor and domain classifier.
L438: methods are as follows. 3) ADAG [26] (DG): It generates new domain by convex
L439: 1) MF-DRCN [48] (DL): A traditional DL method. The combination of multisource domain data and its labels,
L440: feature integration module, soft threshold function, and and performs adversarial training on the source domain
L441: multireceptive field attention module are utilized to and the new domain to optimize the domain-invariant
L442: adaptively enhance the network weight of fault features. feature learning.
L443: Authorized licensed use limited to: University of Science & Technology of China. Downloaded on July 05,2026 at 10:05:07 UTC from IEEE Xplore. Restrictions apply.
L445: ===== PAGE 7 =====
L447: 4962 IEEE TRANSACTIONS ON CYBERNETICS, VOL. 55, NO. 10, OCTOBER 2025
L448: the diversity of training data can effectively enhance
L449: the generalization ability of the diagnosis network. This
L450: discovery also guides the design of DGNSU in this
L451: article.
L452: 2) MAGNet and ADAG are very similar methods for
L453: improving data diversity. However, one clear difference
L454: between them is that MAGNet introduces a sam-
L455: ple weighting mechanism to suppress the interference
L456: of unreliable samples on network learning. Although
L457: MAGNet has significant performance improvements
L458: compared with ADAG in some DG tasks, such as
L459: C1+C3, C1+C4, C3+C6, U3+U4, etc. However, the
L460: average accuracy of MAGNet (93.70% ) is lower than
L461: ADAG (94.12% ) but higher than ADIG in all DG tasks
L462: Fig. 3. Experimental setup of ZJUT dataset. on the ZJUT dataset. This may be because the sample
L463: weighting mechanism restricts the learning weights of
L464: TABLE II
L465: OPERATING CONDITION SETTINGS ON THE ZJUT DATASET some augmented samples whose data distribution is
L466: quite different from the source domain distributions,
L467: resulting in the advantages of data augmentation cannot
L468: be fully utilized.
L469: 3) Unlike ADAG and MAGNet, which use Mixup to
L470: perform linear interpolation on multisource domain
L471: TABLE III
L472: data to generate extended domain data, MSG-ACN
L473: OPERATING CONDITION SETTINGS ON THE CWRU DATASET
L474: utilizes AdaIN and RL to generate extended domain
L475: data with more uncertainty in styles. It is theoreti-
L476: cally possible that MSG-ACN can significantly improve
L477: the data distribution in the extended domain, so that
L478: the diagnosis network can learn more fault features
L479: 4) MAGNet [27] (DG): It combines multisource domains that differ significantly from source domain styles.
L480: through Mixup to generate extended domains, and Unfortunately, the introduction of new styles does
L481: reduces the network weights of unreliable samples on not improve performance, in fact it lead to worse
L482: the basis of aligning the data distribution of extended performance. The performance of MSG-ACN is lower
L483: domains and source domains. than that of the traditional multisource domain AL
L484: 5) MSG-ACN [30] (DG): It generates samples with new method (ADIG). This may be due to the lack of certain
L485: styles through multiscale convolution and aligns the data constraints in the generation process of new styles, so
L486: distribution between the generated samples and source that noisy information is introduced into the network
L487: samples. learning process.
L488: 2) Diagnosis Results: Tables IV and V depict detailed 4) DGNSU outperforms ADIG, ADAG, and MAGNet sig-
L489: experimental results of comparing algorithms. Furthermore, nificantly on the ZJUT and CWRU datasets, especially
L490: Bold indicates the best results of all comparative methods and in C1+C2, C2+C3, C4+C6, C5+C6, and U3+U4
L491: underlined indicates the second best result. The following are tasks. These impressive results validate the superiority
L492: some of our findings and highlighted remarks. of the designed MNGP and ANLF strategies against
L493: 1) Compared with DL-based methods (MF-DRCN), DG- existing approaches based on Mixup and style gener-
L494: based methods (ADIG, ADAG, MAGNet, MSG-ACN, ation. DGNSU not only breaks through the limitation
L495: and DGNSU) can provide a significant performance of multisource domain linear combination in diversity,
L496: improvement in cross-domain fault diagnosis tasks under making the distribution of augmented features more
L497: unseen conditions. In these DG methods, ADIG pro- uncertain, but also constrains the generation process
L498: motes domain-invariant features learning by aligning of new styles, ensuring both feature diversity and
L499: multisource domain distributions to enhance the ability authenticity. Compared with MAGNet, DGNSU can
L500: of the diagnosis network to resist domain shift. The diag- effectively mitigate the performance degradation caused
L501: nosis performance of ADIG can be maintained above by domain shift by generating reliable features with new
L502: 90% in multiple DG tasks. Compared with ADIG, styles.
L503: ADAG combines multiple source domain samples and
L504: their labels to generate augmented data through mixup,
L505: C. Further Analyses
L506: which broadens the distribution of fault features learned
L507: by the diagnosis network and achieves higher diagnosis 1) Feature Style Generation Analysis: In this section, abla-
L508: accuracy than ADIG. The performance improvement of tion studies on MNGP and ANLF strategies are conducted,
L509: ADAG compared with ADIG indicates that improving and the ablation experiment settings are shown in Table VI.
L510: Authorized licensed use limited to: University of Science & Technology of China. Downloaded on July 05,2026 at 10:05:07 UTC from IEEE Xplore. Restrictions apply.
L512: ===== PAGE 8 =====
L514: CHEN et al.: DOMAIN PERTURBATION WITH UNCERTAINTY FOR BEARING FAULT DIAGNOSIS 4963
L515: TABLE IV
L516: PERFORMANCE (% ) COMPARISON BETWEEN OUR PROPOSED DGNSU AND OTHER COMPETING METHODS ON THE ZJUT DATASET
L517: TABLE V
L518: PERFORMANCE (% ) COMPARISON BETWEEN OUR PROPOSED DGNSU AND OTHER COMPETING METHODS ON THE CWRU DATASET
L519: TABLE VI
L520: ABLATION EXPERIMENT
L521: Fig. 4. Sensitivity analysis of parameters in DGNSU. (a) ωˆ 1 and ωˆ 2. (b) ω˜ 1
L522: Table VI summarizes the average generalization performance and ω˜ 2.
L523: of each ablation schemes on C1+C2, C1+C3, C1+C4,
L524: C1+C5 and C1+C6. The training and testing settings of
L525: all the ablation experiments are exactly the same as those MNGP and ANLF strategies results in a 0.078% increase in
L526: of DGNSU. The results in Table VI show that the design FLOPs and a 0.003% increase in parameters relative to the
L527: of MNGP and ANLF strategies is effective for improving baseline model. However, these changes have a minimal effect
L528: the generalization of the diagnosis network under unseen on the overall computational demands of the model.
L529: conditions. The comparison results of A1, A2 and A3 validate 2) Hyperparameter: The proposed method contains several
L530: the importance of MNGP strategy and ANLF strategy for hyperparameters, i.e., ωˆ , ωˆ , ω˜ , ω˜ . To find influence of
L531: 1 2 1 2
L532: improving model generalization performance, be short of hyperparameters on network training, multiple group of values
L533: one cannot. The removal of MNGP strategy (A3) makes is used to train DGNSU. First, the influence of different
L534: it difficult for the network to learn fault features beyond weights ωˆ and ωˆ on diagnosis results is studied, as shown
L535: 1 2
L536: source domain distributions, and the performance improve- in Fig. 4(a). It can be observed that DGNSU is very sensitive
L537: ment is limited compared with the baseline (A4). Similarly, to weights ωˆ and ωˆ . The weight ωˆ assigned to nonlinear
L538: 1 2 2
L539: the performance of the diagnosis network removing the ANLF noise features should not be excessively large, otherwise a
L540: strategy decreases, possibly because the generated features lot of noise will be introduced into the generation process
L541: with new styles have a larger domain shift than the source of new styles. The ability of the network to resist domain
L542: domain features. As a result, noise information is introduced, disturbance can be improved by introducing a proper amount
L543: which makes the network unable to effectively learn domain- of nonlinear noise. In Fig. 4(b), we show the fusion parameters
L544: invariant representations. We further analyze the complexity in the ANLF strategy. It can be concluded that the weights of
L545: involved in integrating MNGP and ANLF strategies into the source features and additive noise features should be balanced
L546: diagnosis model. As indicated in Table VI, the adoption of to ensure that the generated styles can resist some interference
L547: Authorized licensed use limited to: University of Science & Technology of China. Downloaded on July 05,2026 at 10:05:07 UTC from IEEE Xplore. Restrictions apply.
L549: ===== PAGE 9 =====
L551: 4964 IEEE TRANSACTIONS ON CYBERNETICS, VOL. 55, NO. 10, OCTOBER 2025
L552: clustered together. There are also some cases of misclassi-
L553: fication of samples. For the unseen target condition C1, the
L554: class boundaries of ORF_H1 and normal samples are close to
L555: each other, resulting in misclassification of samples near their
L556: boundaries. For the target condition C5, a small number of
L557: samples between IRF_M1 and IRF_L1 are confused. These
L558: results demonstrate that the proposed method is able to
L559: effectively generalize the diagnosis knowledge learned in the
L560: source domain to the unseen domain and effectively separate
L561: Fig. 5. Diversity analysis of feature styles. (a) C1 + C3. (b) C5 + C6. the features of various health state bearings.
L562: IV. CONCLUSION
```

## Extended_Invariant_Risk_Minimization_for_Machine_Fault_Diagnosis_With_Label_Noise_and_Data_Sh.txt
- Total extracted lines: 1169

### Lines 1-110

```text
L3: ===== PAGE 1 =====
L5: 15476 IEEE TRANSACTIONS ON NEURAL NETWORKS AND LEARNING SYSTEMS, VOL. 36, NO. 8, AUGUST 2025
L6: Extended Invariant Risk Minimization for Machine
L7: Fault Diagnosis With Label Noise and Data Shift
L8: Zhenling Mo, Zijun Zhang , Senior Member, IEEE, Qiang Miao , Senior Member, IEEE,
L9: and Kwok-Leung Tsui
L10: Abstract—Incorrect labels as well as the discrepancy between conditions [6], [7]. In practice, NLs and data distribution
L11: training and test domain data distributions can significantly shifts are inevitable in machine fault diagnosis. To enhance
L12: affect the effectiveness of supervised data-driven models in
L13: the practical value of data-driven models for machine fault
L14: machine fault diagnosis applications. Such a challenge can be
L15: diagnosis, it is imperative to develop a fault diagnosis model
L16: characterized as the noisy label-domain generalization (NL-DG)
L17: problem. In this article, the extended invariant risk minimization that is both tolerant to label noise (LN) and capable of
L18: (EIRM) is developed, which incorporates flat minima seeking to generalizing across domains.
L19: address the NL-DG challenge. The ability of handling NL-DG is In existing literature of the machine learning community,
L20: realized by shifting the gradient penalty base from the dummy
L21: addressing LNs focused on LN robust learning [8] while
L22: classifier to the entire model. EIRM is shown to be closely related
L23: tackling data distribution shifts was regarded as one major
L24: to locating a flat minimum, which is crucial for label noise (LN)
L25: robustness and model generalization. Explorations on function task in domain generalization (DG) [9]. A significant focus
L26: smoothness and algorithm convergence are offered to understand of recent studies in LN robust learning is designing robust
L27: EIRM from the theoretical aspect. An efficient implementation risk functions [8]. The designed function is considered robust
L28: of EIRM is also developed to construct the fault diagnosis
L29: in the sense that the global minima are unchanged even if
L30: model. The EIRM-based fault diagnosis method is compared with
L31: some portions of labels are corrupted [10]. One technique
L32: strong benchmarks on multiple NL-DG tasks using actuator and
L33: gearbox fault datasets. Results indicate that the EIRM-based enabling such robustness is the symmetric condition [10].
L34: method on average is more effective than the benchmarks. The Inspired by the symmetric condition, different symmetric
L35: code is available at https://github.com/mozhenling/doge-eirm. robust risk functions were studied, such as the mean absolute
L36: Index Terms—Domain generalization (DG), fault diagnosis, error risk function [10], the symmetric cross-entropy (SCE)
L37: flat minimum, invariant learning, label noise (LN) robustness. risk function [11], and the normalized risk function [12].
L38: In general, robust risk functions can facilitate training
L39: I. INTRODUCTION
L40: various risk minimization-based data-driven models in a
L41: INDUSTRIAL machine fault diagnosis can be challeng- straightforward plug-in approach to tackle LNs. However,
L42: ing since the presence of noisy labels (NLs) and data relying solely on designing the robust risk function may not
L43: distribution shifts can greatly diminish the performance of sufficiently address the challenges imposed by DG. To realize
L44: many data-driven methods [1], [2]. Incorrect machine fault DG, one popular direction is to learn invariant features [13].
L45: labels are often introduced due to the similarity among fault The invariant features are informative about the labels and
L46: patterns [3], less experienced labelers [4], or improper data shared across domains, which can enable model generalization
L47: management [5]. In addition, data distribution shifts are often beyond training domains [14]. A notable approach in learning
L48: induced by data collected under different machine operation invariant features is invariant risk minimization (IRM) [15].
L49: The key idea of IRM is penalizing a dummy classifier to
L50: Received 14 May 2024; revised 12 October 2024; accepted 13 January
L51: be simultaneously optimal on multiple training domains.
L52: 2025. Date of publication 5 February 2025; date of current version
L53: 6 August 2025. This work was supported in part by the Shenzhen-Hong However, IRM mainly concentrated on elevating model DG
L54: Kong-Macau Science and Technology Category C Project under Grant performance under LN-free settings. Extending IRM for
L55: SGDX20220530111205037, in part by the Hong Kong RGC General Research
L56: NL-DG problems, especially serving machine fault diagnosis
L57: Fund Project under Grant 11213124, in part by Collaborative Research Fund
L58: Project under Grant C1049-24GF, in part by Hong Kong ITC Innovation and tasks, remains unexplored and several critical questions
L59: Technology Fund Project under Grant ITS/034/22MS, in part by Guangdong demand in-depth investigations.
L60: Provincial Basic and Applied Basic Research - Offshore Wind Power Joint
L61: First, how can IRM be extended to take both LN and
L62: Fund Project under Grant 2022A1515240066, in part by Guangdong Province
L63: Technological Project under Grant 2023A0505030014, and in part by InnoHK DG settings into account? Previous methods, such as IRM
L64: Initiative, The Government of the HKSAR, and Laboratory for AI-Powered developed for addressing distribution shifts of data, are not
L65: Financial Technologies. (Corresponding author: Zijun Zhang.)
L66: designed for tackling corruptions of labels. Similarly, methods
L67: Zhenling Mo and Zijun Zhang are with the Department of Data Science,
L68: College of Computing, City University of Hong Kong, Hong Kong SAR concerning LNs alone may ignore changes in data distribu-
L69: (e-mail: zijzhang@cityu.edu.hk). tions. Thus, a new method for handling both LN and DG
L70: Qiang Miao is with the College of Electrical Engineering, Sichuan Univer-
L71: problems is imperative.
L72: sity, Chengdu, Sichuan 610017, China.
L73: Kwok-Leung Tsui was with the Grado Department of Industrial and Systems Next, what is the design of a practical risk function
L74: Engineering, Virginia Tech, Blacksburg, VA 24061 USA. He is now with possessing the NL-DG capability for machine fault diag-
L75: the Department of Manufacturing, Systems, and Industrial Engineering, The
L76: nosis applications? Frameworks for addressing LN and DG
L77: University of Texas at Arlington, Arlington, TX 76019 USA.
L78: Digital Object Identifier 10.1109/TNNLS.2025.3531214 problems individually have been presented [8], [9]. Among
L79: 2162-237X © 2025 IEEE. All rights reserved, including rights for text and data mining, and training of artificial intelligence
L80: and similar technologies. Personal use is permitted, but republication/redistribution requires IEEE permission.
L81: See https://www.ieee.org/publications/rights/index.html for more information.
L82: Authorized licensed use limited to: University of Science & Technology of China. Downloaded on July 05,2026 at 10:04:47 UTC from IEEE Xplore. Restrictions apply.
L84: ===== PAGE 2 =====
L86: MO et al.: EXTENDED IRM FOR MACHINE FAULT DIAGNOSIS WITH LABEL NOISE AND DATA SHIFT 15477
L87: reported frameworks for LN and DG problems, new develop- proposed EIRM, which, to the best of our knowledge,
L88: ments often happen in the risk function design. Discussions were not studied previously.
L89: in risk functions for NL-DG problems in data-driven machine From the application aspect, they are given as follows.
L90: fault diagnosis are scarce and it is valuable to develop one for 1) To verify the advantage of EIRM, extensive NL-DG
L91: ease of use under such a real application. tasks are designed using gearbox and actuator fault
L92: Moreover, what is theoretical and experimental evidence datasets. EIRM is then compared with 15 strong bench-
L93: supporting the developed methodology for machine fault diag- marks on designed tasks. Based on average classification
L94: nosis considering NL-DG? Theoretical insights can deepen accuracies on test domains, EIRM outperforms all
L95: the understanding of the developed method. Meanwhile, benchmark methods. Quantitatively, EIRM also achieves
L96: experimental results of benchmarking with the state-of-the-art an improvement of more than 4% compared to the
L97: methods can validate the effectiveness of the proposed method. majority of the benchmark methods.
L98: Thus, it is crucial to obtain insights from both theoretical and The remaining part of this work is organized as follows.
L99: experimental aspects for a method developed for machine fault Section II distinguishes our study from previous studies, spec-
L100: diagnosis considering NL-DG. ifies the problem setting concerned, and details the frequent
L101: To address the abovementioned questions, recent theoretical notations in this work. Section III begins with the formulations
L102: and empirical findings regarding LN robustness and DG in of IRM and elaborates on the derivations of EIRM and the
L103: machine learning field that inspire this research are described corresponding fault diagnosis method. Section IV offers theo-
L104: as follows. One recent theoretical finding presented that under retical insights of EIRM via studying the function smoothness
L105: the correct label dominant condition, the correct label-based and convergence properties. Section V presents experimental
L106: loss was smaller than the incorrect label-based loss [16]. Such studies based on actuator and gear datasets. Section VI offers
L107: a finding implied that the incorrect label could lead to a the conclusion.
L108: perturbation of the loss. Thus, finding flat minima during
L109: model optimization to avoid perturbations might improve the
L110: II. PRELIMINARIES
```

### Lines 180-405

```text
L180: remain unfilled by existing studies [15], [31], [32], [33], [54], [55], [56], [57] by concerning on the proposed risk
L181: [34], [35], [36], [37], [38]. First, IRM and its variants still minimization framework.
L182: only assumed distribution shifts on data, while pollutions
L183: on labels were ignored. Second, rare attempts were made B. Problem Description
L184: by IRM-related studies to methodologically and theoretically We first start with a general problem, which, from the practi-
L185: bridge learning invariance with flat minima optimization. Our cal aspect, well matches machine fault diagnosis tasks depicted
L186: study is then significantly different from the existing studies in the later section of case studies. This work considers a
L187: on IRM and its variants by filling these two gaps. general model f as a composition of a feature extractor g
L188: 3) Flat Minima: In training network models, converging to and a classifier/predictor h, i.e., f = h ◦g. The general model
L189: a “flat” minimum often enabled models to possess better gen- f is parametrized by θ ∈ Rd, which contains d independent
L190: eralization performance compared to converging to a “sharp” real-valued parameters.
L191: minimum [39], [40]. This phenomenon has inspired a plethora The data variable and label variable are denoted as X
L192: of methods for model generalization under a standard machine and Y, respectively. They follow a joint distribution P(X, Y).
L193: learning setup, assuming no distribution shifts in data and no A domain denoted as e enjoys a distinct data–label joint
L194: mislabeled samples [41], [42]. Recently, methods optimizing distribution P(Xe, Y). In DG, it means that given the domain
L195: models toward flat minima to tackle DG problems were also e = i and e = j, if i ̸= j, then P(Xi, Y) ̸= P(X j, Y) [9].
L196: proposed. Yet, from the methodological perspective, many The notation e will be ignored if the domain information is
L197: methods were inspired or derived from the weight averaging unnecessary.
L198: technique [41] or the sharpness aware optimization [43] by For clarity, we embody X as the data matrix X ∈ Rm×n
L199: taking into account DG characteristics. For instance, different and Y as the label vector y ∈ Zn. A data point is x ∈ R,
L200: weight averaging or manipulation techniques were proposed to while a data sample is x = [x , x , . . . , x ]T ∈ Rm. Moreover,
L201: 1 2 m
L202: facilitate identifying flat minima for DG, such as dense weight a data sample x is inherently associated with a label y ∈ Z
L203: averaging [18], diverse weight averaging [44], and ensemble named correct label. Then, we have X = [x , x , . . . , x ] and
L204: 1 2 n
L205: weight averaging [45]. Regarding flat minima optimization, y = [y , y , . . . , y ]T ∈ Zn. Let c be the number of classes.
L206: 1 2 n
L207: Zhang et al. [46] first defined the zero- and first-order flat- The elements of y are integers from 0 to c−1. As a result, the
L208: ness and proposed a novel optimizer to find regions of the LN can be introduced by a transition matrix T with entry T
L209: ij
L210: so-defined flatness for DG. Wang et al. [47] proposed to for i, j = 0, 1, . . . , c−1. An entry T describes the conditional
L211: ij
L212: align gradient directions in implementing the sharpness aware probability of flipping label i to label j. The transition matrix
L213: optimization. In the context of flat minima for DG, Shin et al. considered in this study is defined as follows:
L214: [48] proposed to align source domain loss landscapes with T = . p (cid:0) y˜ = j|y = i (cid:1) = p (cid:0) y˜ = j|y = i, x (cid:1). (1)
L215: perturbed domain loss landscapes. Regarding fighting LNs, ij
L216: finding flat minima is also beneficial [43]. Some recent work In (1), y˜ is the observable label, which means that it can be
L217: hence proposed to introduce stochastic noise into optimizers either the correct label or the incorrect label. In addition, the
L218: to help find flat minima to combat LNs [17], [49]. One major transition matrix defined in (1) corresponds to the instance-
L219: difference between this study and prior studies of flat minima independent LN modeling, which has been commonly seen
L220: Authorized licensed use limited to: University of Science & Technology of China. Downloaded on July 05,2026 at 10:04:47 UTC from IEEE Xplore. Restrictions apply.
L222: ===== PAGE 4 =====
L224: MO et al.: EXTENDED IRM FOR MACHINE FAULT DIAGNOSIS WITH LABEL NOISE AND DATA SHIFT 15479
L225: in [8]. This means that the LN is introduced via a mechanism penalizing the gradient of a dummy predictor as follows
L226: independent of the data instance. Another critical assumption according to [15]:
L227: i [ t s o 23 th a ]. a s t It t t h h is e e a c l L o so N rr . t e h c M e t l r o a e b r a e e s o o l v n is e t r d h , o a t t m h t e i h n e a in i n n s t c , ta o i n . r e r c . e e , c - T t in i l i d a > b ep el m en c a a d x n e i n ̸= b t e j T L re i N j fe [ r 1 c r 6 e a ] d n , m g in |D 1 tr | e X ∈D tr Re(g) + λ (cid:13) (cid:13)∇ h|h=1 Re(h ◦ g)(cid:13) (cid:13) 2 (2)
L228: be further categorized into symmetric noise and asymmetric
L229: where λ is the penalty coefficient, and the dummy predictor
L230: noise [8]. Symmetric noise means that T = T , while the
L231: ij ji is denoted as h = 1. The dummy predictor is obtained via the
L232: asymmetric one means that T ̸= T .
L233: ij ji
L234: reparameterization trick, which avoids the complex Hessian
L235: The NL-DG problem targeted in this study considers the
L236: computation of the predictor model [15]. As shown later, there
L237: impact of both NLs and domain information in modeling.
L238: exists an alternative that offers new insights.
L239: Specifically, the data have domain information denoted as Xe,
L240: while the corrupted labels are denoted as y˜. The ultimate goal
L241: is to learn f by adjusting θ such that f can successfully B. Extended IRM
L242: classify the unseen data with correct labels. To achieve this
L243: As shown in (2), it is observable that the gradient penalty
L244: goal, a risk function R can be employed to measure the risk
L245: of IRM is based solely on the dummy predictor. Enlightened
L246: of obtaining a poor θ based on the training domains D . It is
L247: tr by this idea, we propose developing a gradient penalty for
L248: also worth noting that the value of R is determined by the
L249: the entire model rather than only the dummy predictor in
L250: formulation of R, θ, Xe (or e for short), and y˜.
L251: pursuing simultaneous optimality across training domains to
L252: further enhance the invariant feature learning.
L253: C. Notations
L254: Next, we show that if the gradient penalty is developed
L255: Besides notations defined previously, the frequently referred based on the whole model f , such an extension of IRM can
L256: notations are further elaborated. be linked to flat minima optimization. Recall that the model
L257: 1) R is the risk function. To be more specific about a vari- f can be parametrized by θ. Then, the first possible extension
L258: able such as θ, the risk function is then denoted as R(θ). of IRM can be formulated as follows:
L259: O is n a c p e p t l h ie e d d , o su m c a h in as va R ri e a . b T le o i d s i e st m in p g h u a i s s i h ze d d i , ff t e h r e en s t up fo e r r m sc s ri o p f t m θ in |D 1 | X Re(θ) + λ (cid:13) (cid:13)∇Re(θ)(cid:13) (cid:13) 2. (3)
L260: R, different hats are given. For instance, R, R ¯ , and R ˜ tr e∈D tr
L261: depict risk functions of different formulations. It is known that the computation complexity of Hessian
L262: 2) θ′ represents a different value of θ. Similarly, other matrix is O(d2), where d is the dimension of θ. Hence,
L263: values of θ can be identified by different superscripts. computing the gradient of the risk function in (3) is not
L264: The element of θ is indexed by the subscript. For efficient since it requires the computation of the Hessian
L265: instance, the ith element is presented as θ i . matrix. One simple solution is to sacrifice a certain level of
L266: 3) ∇R(θ) is the gradient of R with respect to θ, while computational accuracy for a higher efficiency.
L267: the Hessian is ∇2R(θ). For simplicity, the gradient and For convenience, let us ignore the domain variable e and
L268: the Hessian can be further denoted as ∇R and ∇2R, consider the approximation on one domain. Then, let us
L269: respectively. consider the first-order Taylor expansion around θ as follows:
L270: 4) ∥·∥ describes the L2-norm by default. For referring
L271: to other norms, subscripts are employed. For instance, R(θ + v) ≈ R(θ) + ∇R(θ)T v
L272: ∥·∥ L1 describes the L1-norm. ⇒ R(θ + v) − R(θ) ≈ ∇R(θ)T v (4)
L273: 5) L stands for the Lipschitz constant. To denote different
L274: values, subscripts are employed. For example, L –L where v is a vector of small values with the same dimension as
L275: 1 3
L276: are three different Lipschitz constants. θ. In addition, ∇R(θ)T v is known as the directional derivative
L277: 6) D is a set of training domains. Its dimension is |D |. of R at θ in the direction of v.
L278: tr tr
L279: Hence, it can be perceived as {1, 2, . . . , |D |}. The test The following question is that among all the possible
L280: tr
L281: domain D is similarly comprehended. directions, which one is representative? One natural answer
L282: te
L283: 7) λ, γ , and µ are positive finite scalars. to the question is the steepest direction under a constraint
L284: ∥v∥ ≤ ρ and ρ ∈ R. To proceed further, let us consider the
L285: Cauchy–Schwarz inequality as follows:
L286: III. METHODOLOGY
L287: In this section, the formulation of IRM is first briefed. Next, (cid:13) (cid:13)∇R(θ)T v (cid:13) (cid:13) ≤ ∥∇R(θ)∥∥v∥ (5)
L288: the step-by-step development of EIRM from IRM is elaborated
L289: and the EIRM for machine fault diagnosis tasks is presented. where the equality holds when v∗ = ξ∇R(θ) and ξ ∈ R. Note
L290: that ∥v∗∥ ≤ ρ ⇒ ξ = ρ(1/∥∇R(θ)∥), which implies that
L291: v∗ = ρ(∇R(θ)/∥∇R(θ)∥). Thus, the steepest direction is just
L292: A. Brief of IRM
L293: the gradient direction. Let γ = (ρ/∥∇R(θ)∥) for simplicity.
L294: The essential idea of IRM is to learn invariant features Then, we have the following approximation:
L295: by forcing the single predictor to be simultaneously optimal
L296: cross training domains [15]. The idea was implemented by R(θ + γ ∇R(θ)) − R(θ) ≈ γ ∥∇R(θ)∥2. (6)
L297: Authorized licensed use limited to: University of Science & Technology of China. Downloaded on July 05,2026 at 10:04:47 UTC from IEEE Xplore. Restrictions apply.
L299: ===== PAGE 5 =====
L301: 15480 IEEE TRANSACTIONS ON NEURAL NETWORKS AND LEARNING SYSTEMS, VOL. 36, NO. 8, AUGUST 2025
L302: Note that θ′ = θ + γ ∇R(θ) is the steepest ascent. By plug- Algorithm 1 One Epoch of Gradient Update of EIRM
L303: ging it into (6), we obtain the following: 1. Begin the epoch
L304: 2. Backup model parameter θ◦ ← θ
L305: R (cid:0)θ′(cid:1) − R(θ) ≈ γ ∥∇R(θ)∥2. (7) 3. Enumerate training domains D :
L306: tr
L307: Thus, the second possible extension of IRM can be obtained 3-1. Obtain a copy of parameters after the first enter:
L308: as follows: θ ← θ◦
L309: 3-2. Obtain a batch sample of domain e
L310: min 1 X Re(θ) + λ (cid:2) Re(cid:0)θ′(cid:1) − Re(θ)(cid:3) 3-3. Compute the domain risk Re(θ)
L311: θ |D |
L312: tr e∈D
L313: tr
L314: 3-4. Compute the domain gradient ∇Re(θ)
L315: s.t. θ′ = θ + γ ∇Re(θ). (8) 3-5. Gradient ascent update: θ′ = θ + γ ∇Re(θ)
L316: 3-6. Compute the domain risk at the ascent point:
L317: Re(cid:0)θ′(cid:1)
L318: There are two important observations. First, the gradient
L319: 3-7. Compute the domain gradient at the ascent point:
L320: computation of the risk function can be implemented more ∇Re(cid:0)θ′(cid:1)
L321: efficiently. To check this, we only need to first compute
L322: 3-8. Compute the approximated domain gradient:
L323: ∇Re(θ), update the parameter θ′ = θ + γ ∇Re(θ) after a
L324: backup, compute ∇Re(θ′), and obtain the approximate gra- ∇R ¯ e(θ) = ∇Re(θ)
L325: dient as follows: + λ (cid:2) Re(cid:0)θ′(cid:1) − Re(θ)(cid:3)(cid:2)∇Re(cid:0)θ′(cid:1) − ∇Re(θ)(cid:3)
L326: 1 X ∇Re(θ) + λ (cid:2)∇Re(cid:0)θ′(cid:1) − ∇Re(θ)(cid:3). (9) 3-9. Collect ∇R ¯ e(θ)
L327: |D |
L328: tr e∈D
L329: tr
L330: 4. Average the collected domain gradients
L331: It is observable that the computation only incurs a linear 5. Obtain a copy of parameters θ ← θ◦
L332: complexity O(d). The second observation is that the risk 6. Gradient update by an optimizer. e.g., Adam.
L333: difference, Re(θ′) − Re(θ), can be regarded as a measure of 7. End the epoch
L334: “flatness” round θ. It then bridges learning invariance with
L335: finding flat minima.
L336: In practice, the optimization problem is usually nonconvex
L337: and the learning rate γ can be imperfect. It means that
L338: the risk difference Re(θ′) − Re(θ) can be negative due to
L339: overshooting, leading to an undesired property of measuring
L340: flatness. To solve the problem, the third possible extension of
L341: IRM can be proposed as follows:
L342: min 1 X Re(θ) + λ (cid:2) Re(cid:0)θ′(cid:1) − Re(θ)(cid:3)2
L343: θ |D | 2
L344: tr e∈D
L345: tr
L346: s.t. θ′ = θ + γ ∇Re(θ). (10)
L347: The gradient of the risk function can be approximated as
L348: follows:
L349: 1 X ∇Re(θ) + λ (cid:2) Re(cid:0)θ′(cid:1) − Re(θ)(cid:3)(cid:2)∇Re(cid:0)θ′(cid:1) − ∇Re(θ)(cid:3).
L350: |D |
L351: tr e∈D
L352: tr
L353: Fig. 1. Fault diagnosis model training based on EIRM and 1-D LeNet.
L354: (11)
L355: from [59] and employed in this study. The 1-D LetNet is a
L356: Finally, the proposed EIRM is based on (10). To compute 1-D variant of the celebrated LetNet-5 network. Training the
L357: its gradient in (11), we only need to obtain Re(θ), compute fault diagnosis model is illustrated in Fig. 1.
L358: ∇Re(θ), update parameter θ′ = θ + γ ∇Re(θ) after a backup,
L359: compute Re(θ′) and ∇Re(θ′), and finally obtain the gradient IV. THEORETICAL ANALYSES
L360: based on (11). The computation complexity is still O(d). For In this section, two theoretical explorations, the smoothness
L361: better illustration, one epoch of gradient update of EIRM is analysis and convergence analysis, are conducted to better
L362: detailed in Algorithm 1. understand the proposed EIRM. All proofs are offered in
L363: Appendix.
L364: C. EIRM-Based Fault Diagnosis Model
L365: A. Smoothness of the Vanilla Risk Function
L366: In developing a data-driven model for the fault diagno-
L367: sis task, we leverage EIRM as the objective function and First, let us leave the domain variable e aside and consider
L368: apply the optimization process in Algorithm 1 to train a 1-D the setting of one domain. Then, we attempt to characterize
L369: convolutional neural network (1-D CNN) to classify faults. different levels of “smoothness” of the vanilla risk function
L370: The selection of 1-D CNN as the data-driven model is due R based on the Lipschitz continuity. The definitions based
L371: to its popularity in fault diagnosis applications [58], [59]. on Lipschitz continuity to capture function smoothness are
L372: In particular, the 1-D CNN named 1-D LetNet is brought commonly used in the literature [52], [53], [54], [55]. Note
L373: Authorized licensed use limited to: University of Science & Technology of China. Downloaded on July 05,2026 at 10:04:47 UTC from IEEE Xplore. Restrictions apply.
L375: ===== PAGE 6 =====
L377: MO et al.: EXTENDED IRM FOR MACHINE FAULT DIAGNOSIS WITH LABEL NOISE AND DATA SHIFT 15481
L378: that although the basic assumptions considered in convergence from L -LCH to L -LCG and L -LCG to L -LCR. In short,
L379: 3 2 2 1
L380: analyses may be similar, the theoretical deviations of conver- L -LCR can be related to flatness, and the direction from
L381: 1
L382: gences can vary significantly since different algorithms and L -LCR to L -LCH means “smoother” conditions. In addition,
L383: 1 3
L384: loss functions have different gradient characteristics. In this we also refer to L -LCR, L -LCG, and L -LCH as the first,
L385: 1 2 3
L386: study, the vanilla risk function R is assumed to be twice second, and third levels of “smoothness,” respectively. For
L387: differentiable and definitions of different smoothness levels convenience, we will drop the quotation marks. However,
L388: are also presented to facilitate theoretical developments. it should be minded that smoothness has a specific meaning
L389: Definition 1 (L -Lipschitz Continuous Risk, L -LCR): The as given by the respective definitions.
L390: 1 1
L391: risk function R is L -Lipschitz continuous if
L392: 1
L393: (cid:13) (cid:13)R (cid:0)θ′(cid:1) − R(θ)(cid:13) (cid:13) ≤ L 1 (cid:13) (cid:13) θ′ − θ(cid:13) (cid:13) . (12) B. Smoothness of the Extended Risk Function
L394: The practical risk function in (10) is the approximation to
L395: Definition 2 (L 2 -Lipschitz Continuous Gradient, L 2 -LCG): the extended risk function R ˜ by considering (7) and ignoring
L396: The risk function R has L -Lipschitz continuous gradient if
L397: 2 the domain variable e, which is given as follows:
L398: (cid:13) (cid:13)∇R (cid:0)θ′(cid:1) − ∇R(θ)(cid:13) (cid:13) ≤ L 2 (cid:13) (cid:13) θ′ − θ(cid:13) (cid:13) . (13) R ˜ (θ) = R(θ) + λ∥∇R(θ)∥4. (16)
L399: Definition 3 (L -Lipschitz Continuous Hessian, L -LCH):
L400: 3 3 Here, we theoretically study the form of risk function in (16)
L401: The risk function R has L -Lipschitz continuous Hessian if
L402: 3 rather than in (10) just for simplicity and convenience. Then,
L403: (cid:13) (cid:13)∇2R (cid:0)θ′(cid:1) − ∇2R(θ)(cid:13) (cid:13) ≤ L 3 (cid:13) (cid:13) θ′ − θ(cid:13) (cid:13) (14) it is notable that to have the same level of smoothness,
L404: R ˜ demands more conditions than R since ∇R is involved.
L405: where a matrix norm such as ∥∇2R∥ can be induced by a
```

### Lines 405-572

```text
L405: where a matrix norm such as ∥∇2R∥ can be induced by a
L406: To check this, we provide the lemma regarding the L -LCR
L407: vector v ∈ Rd as follows: 1
L408: as follows.
L409: (cid:13) (cid:13)∇2R (cid:13) (cid:13) = sup (cid:13) (cid:13)∇2Rv (cid:13) (cid:13) . (15) Lemma 2: If the vanilla risk function R satisfies L 1 -LCR,
L410: ˜
L411: ∥v∥=1 the extended risk function R will satisfy
L412: tio T ns h . e S re pe a c r i e fic s a o l m ly e , L im - m L e C d R iat i e mp c l o i n es se t q h u e en b c o e u s nd f e ro d m gr t a h d e ie d n e t fi a n n i d - (cid:13) (cid:13)R ˜ (cid:0)θ′(cid:1) − R ˜ (θ)(cid:13) (cid:13) ≤ L 1 (cid:13) (cid:13) θ′ − θ(cid:13) (cid:13) + 2λ L4 1 . (17)
L413: 1
L414: ˜
L415: L 2 -LCG implies the bounded Hessian. In addition, L 2 -LCG In addition, if R continues to satisfy L 2 -LCG, R will satisfy
L416: T m h e e a s n e s r l e o s c u a l l ts L c 1 a - n LC be R s , h w ow hi n le by L 3 t - h L e C c H oro m ll e a a r n ie s s l o o f ca a l le L m 2 - m L a CG as . (cid:13) (cid:13)R ˜ (cid:0)θ′(cid:1) − R ˜ (θ)(cid:13) (cid:13) ≤ L 4 (cid:13) (cid:13) θ′ − θ(cid:13) (cid:13) (18)
L417: follows. where L = L + 4λ L3L .
L418: Lemma 1 [52, Lemma 2.6]: Let M : Rm → Rn be a As sho 4 wn i 1 n Lemm 1 a 2 2 , if R only satisfies L -LCR, the
L419: 1
L420: differentiable function. Then, M is L-Lipschitz if and only risk difference of R ˜ can be bounded by the sum of the model
L421: if ∥DM(z)∥ ≤ L for ∀z ∈ Rm, where DM is the Jacobian of parameter difference and a model parameter independent term.
L422: M and L is the Lipschitz constant. In addition, the proof of the first statement in Appendix shows
L423: Corollary 1: The risk function R satisfies L 1 -LCR if and that if 2λ L4 is dropped, the inequality of (17) will not be
L424: only if ∥∇R(θ)∥ ≤ L 1 . Similarly, R satisfies L 2 -LCG if and always true 1 unless gradient penalties are the same for all
L425: only if ∥∇2R(θ)∥ ≤ L 2 . possible values of θ. Hence, by Definition 1, R ˜ does not
L426: Corollary 2: If the risk function R satisfies L 2 -LCG and satisfy L 1 -LCR. However, once R satisfies both L 1 -LCR and
L427: there exists a point θ· such that ∥∇R(θ·)∥ ≤ (L 1 /2), then R L 2 -LCG, it can guarantee that R ˜ satisfies L 1 -LCR. Hence, R ˜
L428: satisfies L 1 -LCR locally around the point within the radius requires a smoother R to reach the first level of smoothness.
L429: (L 1 /2L 2 ). Similarly, if R satisfies L 3 -LCH and there exists Similarly, to reach the second level of smoothness, R ˜
L430: a point θ· such that ∥∇2R(θ·)∥ ≤ (L 2 /2), then R satisfies requires that R satisfies the first, second, and third levels of
L431: L 2 -LCG around the point within the radius (L 2 /2L 3 ). smoothness, which can be stated as follows.
L432: The proof of Lemma 1 was provided in [52]. Although Lemma 3: Suppose that the vanilla risk function R satisfies
L433: Corollaries 1 and 2 result from Lemma 1, these two claims L -LCR and L -LCG, and then, the extended risk function R ˜
L434: 1 2
L435: were not examined in [52]. To facilitate our development, the satisfies
L436: proofs of Corollaries 1 and 2 are offered in Appendixes A
L437: and B, respectively. From the first statement of Corollary 1, (cid:13) (cid:13)∇R ˜ (cid:0)θ′(cid:1) − ∇R ˜ (θ)(cid:13) (cid:13) ≤ L 2 (cid:13) (cid:13) θ′ − θ(cid:13) (cid:13) + 8λ L3 1 L 2 . (19)
L438: we can see that L -LCR is equivalent to requiring a uniformly
L439: 1 In addition, suppose that R continues to satisfy L -LCH, and
L440: 3
L441: bounded gradient. Locally, the gradient bounded uniformly by ˜
L442: then, R satisfies
L443: a small Lipschitz constant implies that such a local area is flat.
L444: Therefore, L 1 -LCR is closely related to flatness. The second (cid:13) (cid:13)∇R ˜ (cid:0)θ′(cid:1) − ∇R ˜ (θ)(cid:13) (cid:13) ≤ L 5 (cid:13) (cid:13) θ′ − θ(cid:13) (cid:13) (20)
L445: statement of Corollary 1 means that having L -LCG requires
L446: 2 where L = L + 4λ L3L + 4λ L2L2.
L447: the uniformly bounded Hessian. With a bounded Hessian, 5 2 1 3 1 2
L448: the gradient cannot change “too fast,” which means that we Regarding the third level of smoothness, we would expect
L449: ˜
L450: are more likely to bound the gradient locally. Consequently, that R may also rely on more conditions than R. However,
L451: L -LCR is more likely to hold in a local area. In fact, Corol- since we only assume that R is twice differentiable, it is not
L452: 1
L453: lary 2 offers specific conditions, which allow the directions sufficient to discuss such a case.
L454: Authorized licensed use limited to: University of Science & Technology of China. Downloaded on July 05,2026 at 10:04:47 UTC from IEEE Xplore. Restrictions apply.
L456: ===== PAGE 7 =====
L458: 15482 IEEE TRANSACTIONS ON NEURAL NETWORKS AND LEARNING SYSTEMS, VOL. 36, NO. 8, AUGUST 2025
L459: C. Convergence Based on the Extended Risk Function flat minima. To this end, the global convergence analysis is
L460: significant and valuable to understand the characteristics of
L461: Before stating the main result, it is necessary to offer the
L462: the proposed risk function.
L463: last lemma derived from Lemma 3 as follows.
L464: Lemma 4: Suppose that the extended risk function R ˜ sat- In general, global convergence is challenging in practice
L465: since some assumed conditions may not be attainable or
L466: isfies the inequality in (19), and then,
L467: satisfied globally. For instance, if R does not satisfy L -LCH
L468: R ˜ (cid:0)θ′(cid:1) ≤ R ˜ (θ) + ∇R ˜ (θ)T (cid:0)θ′ − θ(cid:1) + L 2 (cid:13) (cid:13) θ′ − θ(cid:13) (cid:13) 2 or the learning rate is larger than 1/L 5 , it is not po 3 ssible
L469: 2 to reach the global convergence under our setup as shown
L470: + 8λ L3 1 L 2 (cid:13) (cid:13) θ′ − θ(cid:13) (cid:13) . (21) in (25). In this case, a practical approach is to upper bound
L471: ˜ the loss difference between the current point and the global
L472: In addition, if R satisfies the inequality in (20), then
L473: optimal point as shown in (24). As discussed in the previous
L474: R ˜ (cid:0)θ′(cid:1) ≤ R ˜ (θ) + ∇R ˜ (θ)T (cid:0)θ′ − θ(cid:1) + L 5 (cid:13) (cid:13) θ′ − θ(cid:13) (cid:13) 2. (22) paragraph, implications of (24) and (25) could offer theoretical
L475: 2 insights on the preference of flat minima of the proposed risk
L476: Now, it is ready to provide the main results on the global function. Apart from conditions assumed in this study, there
L477: convergence and local convergence of the GD algorithm based exist some other conditions for enabling global convergence in
L478: on the gradient of the extended risk function. recent literature, such as special initializations [50] and special
L479: Theorem 1 (Global Convergence): If the extended risk neural network models [56]. However, these studies offered
L480: function R ˜ has the global optimal value R ˜ (θ∗) and satisfies the little knowledge on linking global convergence with seeking
L481: Polyak–Lojasiewicz condition with the finite positive constant flat minima. In addition to the global convergence analysis, the
L482: µ, i.e., local convergence analysis is also important and usually more
L483: R ˜ (θ) − R ˜ (cid:0)θ∗(cid:1) ≤ 2 1 µ (cid:13) (cid:13)∇R ˜ (θ)(cid:13) (cid:13) 2 (23) p im ra p c l t y ic t a h l a . t W th il e l G th D e l b o a c s a e l d co o n n v t e h r e ge p n r c o e po a s n e a d ly r s i i s s k a f l u s n o c c ti o o n n si p st r e e n fe tl r y s
L484: flat minima? This question is answered by the second theorem
L485: and the vanilla risk function R satisfies L -LCR and L -LCG,
L486: 1 2 in the following, which also implies such a preference for flat
L487: then the GD algorithm using ∇R ˜ and the learning rate 0 <
L488: minima.
L489: γ ≤ min((1/L ), (1/µ)) at iteration t + 1 gives
L490: 2 Theorem 2 (Local Convergence): If the vanilla risk func-
L491: R ˜ (cid:0)θt+1(cid:1) − R ˜ (cid:0)θ∗(cid:1) ≤ (1 − γ µ)t+1(cid:2) R ˜ (cid:0)θ0(cid:1) − R ˜ (cid:0)θ∗(cid:1)(cid:3) tion R satisfies L 2 -LCG in the considered local area
L492: ∥θ − θ×∥ ≤ (L /2L ) with ∥∇R(θ×)∥ ≤ (L /2) and
L493: + 8λ γ L µ 3 1 L 4 (cid:2) 1 − (1 − γ µ)t+1(cid:3). (24) ma 1 x (cid:0) L 2 + 4λ L3L , 16λ L3L (cid:1) ≤ 1 1 (26)
L494: 1 1 2 1 2
L495: In addition, if R continues to satisfies L -LCH, then with the ˜
L496: 3 as well as the extended risk R function has the local opti-
L497: learning rate 0 < γ ≤ min((1/L 5 ), (1/µ)), the bound in (24) mal value R ˜ (θ×) and satisfies the local Polyak–Lojasiewicz
L498: can be reduced to condition with finite positive constant µ, i.e.,
L499: R ˜ (cid:0)θt+1(cid:1) − R ˜ (cid:0)θ∗(cid:1) ≤ (1 − γ µ)t+1(cid:2) R ˜ (cid:0)θ0(cid:1) − R ˜ (cid:0)θ∗(cid:1)(cid:3). (25) R ˜ (θ) − R ˜ (cid:0)θ×(cid:1) ≤ 1 (cid:13) (cid:13)∇R ˜ (θ)(cid:13) (cid:13) 2 (27)
L500: 2µ
L501: Thus, the GD algorithm converges globally as t approaches
L502: infinity. then the GD algorithm using ∇R ˜ and the learning rate
L503: In Theorem 1, the given conditions, i.e., the L 1 -LCR, the 16λ L3 1 < γ ≤ min((1/L 2 ), (1/µ) + 16λ L3 1 ) at iteration
L504: L 2 -LCG, and the Polyak–Lojasiewicz conditions, are typical t + 1 gives
L505: in the convergence analysis of GD algorithm [52], [53], [54],
L506: [55]. In particular, the Polyak–Lojasiewicz condition can be R ˜ (cid:0)θt+1(cid:1) − R ˜ (cid:0)θ×(cid:1)
L507: true even if the function is nonconvex [52]. However, under ≤ (cid:0) 1 + 16λµL3 − γ µ(cid:1)t+1(cid:2) R ˜ (cid:0)θ0(cid:1) − R ˜ (cid:0)θ∗(cid:1)(cid:3). (28)
L508: the conditions of the first statement, the algorithm may not 1
L509: easily converge due to the existence of the gradient penalty. Thus, the GD algorithm converges locally as t approaches
L510: This can be seen from the second term of the upper bound. infinity.
L511: Interestingly, the second term is also highly associated with In Theorem 2, if we further assume that R locally satisfies
L512: L . As discussed previously, the flatness is related to L . L -LCR with bounded gradients, then the explicit constraints
L513: 1 1 1
L514: When L is small, the region is more likely to be flat. With an on the local area will become implicit, which may widen the
L515: 1
L516: appropriate λ and a small L , the algorithm can attain a tighter suitable areas. In addition, the only constraint on the local area
L517: 1
L518: bound in (24). This is different from the case when returning to is now given by (26). Then, it is also observable that with the
L519: R by setting λ = 0, which leads to an easy convergence under increase of the penalty coefficient λ, it demands smaller L ,
L520: 1
L521: the given conditions with little regard to the flatness. From which corresponds to a flatter zone. However, λ should not
L522: the second statement of Theorem 1, the GD algorithm based increase arbitrarily since larger λ leads to a shorter range of
L523: ˜
L524: on R will have a global convergence, given that R becomes the desired learning rate. As such, there should be a tradeoff
L525: more smoother by satisfying L -LCH and the learning rate between flatness and convergence. Note that this tradeoff also
L526: 3
L527: is constrained by L . Note that L consists of L and λ as exists in Theorem 1.
L528: 5 5 1
L529: derived in (20). From these discussions, Theorem 1 can imply To summarize the theoretical analyses, we offer several
L530: that pursuing global convergence is closely related to seeking important take-away notes as follows.
L531: Authorized licensed use limited to: University of Science & Technology of China. Downloaded on July 05,2026 at 10:04:47 UTC from IEEE Xplore. Restrictions apply.
L533: ===== PAGE 8 =====
L535: MO et al.: EXTENDED IRM FOR MACHINE FAULT DIAGNOSIS WITH LABEL NOISE AND DATA SHIFT 15483
L536: 1) The extended risk function enables the vanilla risk func-
L537: tion to exhibit certain smooth characteristics. Namely,
L538: if the GD settles at a smooth region of the extended
L539: risk function, this region is likely to be perceived as
L540: smoother in the context of the vanilla risk function. This
L541: characteristic stems directly from the gradient penalty,
L542: which requires regulating the first-order derivatives.
L543: 2) The coefficients of upper bounds in (25) and (28) range
L544: between zero and one. This indicates that under the
L545: conditions outlined in Theorems 1 and 2, the current Fig. 2. Test rig of the linear electromechanical actuator.
L546: risk difference goes to zero as t approaches infinity. The
L547: we only introduce the essential information for task design.
L548: global and local convergences of the GD algorithm are
L549: The data were collected under three loading conditions, 20 kgf
L550: then obtained based on the gradient of the extended risk
L551: (DG task 0), 40 kgf (DG task 1), and −40 kgf (DG task
L552: function.
L553: 2). Herein, DG task 0 means that data under 20 kgf are the
L554: 3) Compared to the vanilla function, the extended risk
L555: DG test domain, while data under other loads are two DG
L556: function necessitates smoother and flatter zones for the
L557: training domains. The configurations for DG tasks 1 and 2 are
L558: GD algorithm convergence. However, it is crucial to
L559: structured in a similar manner.
L560: maintain a balance between pursuing convergence and
L561: The final task is to classify samples of three types of faults
L562: locating the desired minimum, which is controlled by
L563: in the DG tasks under two LN noise types. DG test domains
L564: the penalty coefficient λ.
L565: were LN free, but DG training domains were corrupted by
L566: 4) Finally, it should be mentioned that the main purpose of
L567: LNs. Recall the definition of transition matrix introduced in
L568: the theoretical analysis is to provide a better understand-
L569: the preliminary. The LN corruption can be defined by the
L570: ing of the proposed methodology. We leave the more
L571: transition matrix [8]. There are three classes, i.e., c = 3.
L572: in-depth theoretical and experimental analyses regarding
```

### Lines 576-698

```text
L576: V. EXPERIMENTS η/(c − 1). Regarding asymmetric noise case, it is generated
L577: In this section, the proposed risk functions are bench- by setting η = 0.2 for: 1) ∀ i=j T ij = 1 − η; 2) T ij =
L578: marked against other methods in training data-driven models η × 0.2 for T 0,1 , T 1,2 , and T 2,0 ; and 3)T ij = η × 0.8 for
L579: for machine fault classifications. The classification tasks are T 0,2 , T 1,0 , and T 2,1 .
L580: designed so that they belong to NL-DG settings. A higher In summary, there are two noise types, symmetric and
L581: classification accuracy means that the method is more effective asymmetric noises, with noise rate η = 0.2. For each DG
L582: in identifying different fault types. Thus, the evaluation metric task, there are three fault classes. For each class, there are
L583: is the average accuracy over the test domains. 160 samples. For each sample, there are 1000 signal points.
L584: 2) Task Design Based on Gearbox Dataset: The second
L585: A. Benchmark Method dataset contains data reflecting three health conditions of a
L586: The compared methods encompass a variety of risk func- gearbox: normal condition (labeled as 0), missing tooth of sun
L587: tions, including the ERM based on the standard CE [21], gear (labeled as 1), and missing tooth of planet gear (labeled
L588: the SCE [11], the normalized CE (NCE) [12], the JSD as 2). The test rig is shown in Fig. 3. For complete information
L589: [20], the ANL [22], the generalized label smoothing (GLS) of the data collection, please refer to [32]. Next, we provide
L590: [24], the asymmetric unhinged loss (AUL) [23], and the pre- only the key information necessary to illustrate the task design.
L591: diction clipping (Clipping) [26]. The considered methods also In this case, we employ data collected at shaft speeds of 1200,
L592: include the ANDMask (AMask) [29], the representation self- 1500, and 1800 r/min, to design three DG tasks, DG tasks 0,
L593: challenging (RSC) [13], the interdomain mix-up (Mixup) [28], 1, and 2, respectively. We follow a similar procedure to that
L594: the IRM [15], the IB-IRM [31], the risk distribution matching of the actuator dataset to design the final tasks. There are only
L595: two differences. For each class, there are 140 samples, and,
L596: (RDM) [60], and the causal representation of sufficiency and
L597: in each sample, there are 2000 points.
L598: necessity (CaSN) [61]. Regarding the vanilla risk function
L599: of EIRM, it is chosen as the standard CE risk function.
L600: A total of 15 methods, most proposed in recent years, serve as C. Experiment Implementation
L601: benchmarks. Each method is applied to train the 1-D LeNet In each fault classification task, we separately apply EIRM
L602: (Fig. 1) to classify faults in the experiments. and the benchmark methods to train the 1-D LeNet (shown in
L603: Fig. 1) based on two training domains and then test the trained
L604: B. Machine Fault Diagnosis Task model on one test domain.
L605: 1) Task Design Based on Actuator Dataset: The first dataset Regarding the experimental procedure, we follow a similar
L606: contains three fault types of an electromechanical actuator, the principled protocol to that employed in the “DomainBed”
L607: backlash (labeled as 0), lack of lubrication (labeled as 1), and experiments [27]. The key principles of the DomainBed are
L608: spalling defect (labeled as 2). The test rig is shown in Fig. 2. as follows: 1) the hyperparameters are selected using random
L609: The full information of the dataset is provided in [62]. Next, search within the specified grids and 2) the process is repeated
L610: Authorized licensed use limited to: University of Science & Technology of China. Downloaded on July 05,2026 at 10:04:47 UTC from IEEE Xplore. Restrictions apply.
L612: ===== PAGE 9 =====
L614: 15484 IEEE TRANSACTIONS ON NEURAL NETWORKS AND LEARNING SYSTEMS, VOL. 36, NO. 8, AUGUST 2025
L615: TABLE I
L616: FAULT CLASSIFICATION RESULTS BASED ON THE ACTUATOR AND GEARBOX DATASETS WITH SYMMETRIC LNS
L617: TABLE II
L618: FAULT CLASSIFICATION RESULTS BASED ON THE ACTUATOR AND GEARBOX DATASETS WITH ASYMMETRIC LNS
L619: their respective original papers, as they are not included in the
L620: DomainBed.
L621: D. Result Analysis
L622: The fault classification results of DG tasks with symmet-
L623: ric LNs are presented in Table I, while the results of the
L624: asymmetric counterpart are displayed in Table II. The essential
L625: observations from Tables I and II are as follows.
L626: 1) All models generally perform better on the gearbox
L627: dataset than the actuator dataset. This likely results from
L628: Fig. 3. Test rig of the gearbox. the complexity of the actuator’s two motion profiles,
L629: the trapezoidal and the sinusoidal, as detailed in [62],
L630: 20×, with each search averaged over three random seeds of which are more complex than the simple constant speed
L631: trials. We also highlight the major adaptations as follows. First, rotation of the gear [32]. Hence, it can be more difficult
L632: the total number of epochs for each method is selected from to diagnose the actuator faults.
L633: [500, 1000, . . . , 5000] instead of being fixed to 5000. Second, 2) It is challenging for a single method to consistently
L634: the penalty coefficient λ is 10ξ, where ξ ∼ U(−1, 5), i.e., outperform the others in the NL-DG tasks. However, the
L635: ξ is drawn uniformly from (−1, 5). Other hyperparameter average results show that the proposed method is more
L636: grids of the benchmark methods are also set to match those effective than all the benchmarks.
L637: in DomainBed, except for JSD [20], GLS [24], RDM [60], 3) Compared to most state-of-the-art methods, such as the
L638: and CaSN [61]. For these methods, the grids are taken from AUE [23] or ANL [22], EIRM demonstrates more stable
L639: Authorized licensed use limited to: University of Science & Technology of China. Downloaded on July 05,2026 at 10:04:47 UTC from IEEE Xplore. Restrictions apply.
L641: ===== PAGE 10 =====
L643: MO et al.: EXTENDED IRM FOR MACHINE FAULT DIAGNOSIS WITH LABEL NOISE AND DATA SHIFT 15485
L644: performances on both the symmetric case (Table I) and Section V-C. Regarding the theoretical developments, future
L645: the asymmetric case (Table II). For instance, although studies can further explore the convergence properties with
L646: ANL and our method are comparable in Table I, our less or more smoothness conditions, which may lead to more
L647: method consistently outperforms ANL across all tasks knowledge discoveries that can enrich the understanding of
L648: in Table II. Thus, these experimental results suggest EIRM or innovate its current formulation.
L649: that EIRM can bring benefits for solving the NL-DG
L650: problems. APPENDIX
L651: A. Proof of Corollary 1
L652: E. Ablation Analysis By Lemma 1, M : Rm → Rn is differentiable. The i j-entry
L653: The CE [21] in our experiments is the ERM based on of the Jacobian DM is defined as follows:
L654: the standard CE loss. The IRM [15] has two terms, the CE ∂M(z )
L655: [DM] = i
L656: loss and IRM regularization, as shown in (2). Our method, ij ∂z
L657: j
L658: EIRM, also includes two terms, the CE loss and the EIRM
L659: for i = 1, 2, . . . , n, and j = 1, 2, . . . , m. (29)
L660: regularization, as shown in (10). The EIRM regularization
L661: is developed on top of the IRM regularization by linking it Replacing M in Lemma 1 by R gives ∥∇R(θ)∥ ≤ L ,
L662: 1
L663: with flat minima optimization as explained in Section III-B. which proves the first statement. Similarly, replacing M in
L664: In addition, all compared methods consider the same model Lemma 1 by ∇R gives ∥∇2R(θ)∥ ≤ L , which proves the
L665: 2
L666: structures and searching processes of hyperparameters. Hence, second statement.
L667: by comparing the results of CE [21] with those of IRM [15]
L668: and EIRM, we can observe the effect of adding IRM-related
L669: B. Proof of Corollary 2
L670: regularization. By comparing the results of IRM with those
L671: Considering the reverse triangle inequality and the Lipschitz
L672: of EIRM, we can observe the effect of innovating the IRM
L673: gradient, we have
L674: regularization from the perspective of flat minima optimiza-
L675: tion. Quantitatively, based on the average results of Table I, (cid:13) (cid:13)∇R (cid:0)θ′(cid:1)(cid:13) (cid:13) − ∥∇R(θ)∥ ≤ (cid:13) (cid:13)∇R (cid:0)θ′(cid:1) − ∇R(θ)(cid:13) (cid:13) ≤ L 2 (cid:13) (cid:13) θ′ − θ(cid:13) (cid:13) .
L676: EIRM outperforms IRM [15] and CE [21] by 5.7% and
L677: (30)
L678: 9.2%, respectively. Based on the average results of Table II,
L679: EIRM surpasses IRM [15] and CE [21] by 5.8% and 8.3%, If there exists a point θ· such that ∥∇R(θ·)∥ ≤ (L /2) (i.e.,
L680: 1
L681: respectively. Hence, we can confirm that our developments a bounded gradient at a point), then we can show that the
L682: from CE [21] to EIRM result in improvements. Essentially, gradients within ∥θ − θ·∥ ≤ (L /2L ) are uniformly bounded
L683: 1 2
L684: we attribute this effectiveness to the integration of learning by L . Namely, we have
L685: 1
L686: invariance with the pursuit of flat minima, which is the core ∥∇R(θ)∥ = (cid:13) (cid:13)∇R(θ) − ∇R (cid:0)θ·(cid:1) + ∇R (cid:0)θ·(cid:1)(cid:13) (cid:13)
L687: concept behind the development of EIRM.
L688: ≤ (cid:13) (cid:13)∇R(θ) − ∇R (cid:0)θ·(cid:1)(cid:13) (cid:13) + (cid:13) (cid:13)∇R (cid:0)θ·(cid:1)(cid:13) (cid:13)
L689: VI. CONCLUSION ≤ L 2 (cid:13) (cid:13) θ − θ·(cid:13) (cid:13) + (cid:13) (cid:13)∇R (cid:0)θ·(cid:1)(cid:13) (cid:13) ≤ L 1 . (31)
L690: In this article, a new risk minimization method, EIRM, was By Lemma 1 and Corollary 1, we know that R is
L691: proposed to develop data-driven models capable of addressing L -Lipschitz in ∥θ − θ·∥ ≤ (L /2L ). The second statement
L692: 1 1 2
L693: NL-DG problems in machine fault diagnosis. Theoretical stud- can be similarly proved by considering the reverse triangle
L694: ies on the smoothness analysis and the convergence analysis inequality and the Lipschitz and Hessian.
L695: were conducted to deepen the understanding of the proposed
L696: EIRM. In the case studies, extensive NL-DG tasks based on
L697: C. Proof of Lemma 2
L698: actuator and gearbox datasets were employed to benchmark
```

## Learning_Motor_Cues_in_Brain-Muscle_Modulation.txt
- Total extracted lines: 894

### Lines 1-100

```text
L3: ===== PAGE 1 =====
L5: 86 IEEE TRANSACTIONS ON CYBERNETICS, VOL. 55, NO. 1, JANUARY 2025
L6: Learning Motor Cues in Brain-Muscle Modulation
L7: Tian-Yu Xiang , Student Member, IEEE, Xiao-Hu Zhou , Member, IEEE, Xiao-Liang Xie , Member, IEEE,
L8: Shi-Qi Liu , Mei-Jiang Gui , Graduate Student Member, IEEE, Hao Li , Graduate Student Member, IEEE,
L9: De-Xing Huang , Graduate Student Member, IEEE, Xiu-Ling Liu , Member, IEEE,
L10: and Zeng-Guang Hou , Fellow, IEEE
L11: Abstract—Current studies for brain-muscle modulation often data-driven approach for the neuroscience community, offering
L12: analyze selected properties in electrophysiological signals, leading a comprehensive perspective of brain-muscular modulation.
L13: to a partial understanding. This article proposes a cross-
L14: Index Terms—Brain-muscle modulation, generative model,
L15: modal generative model that converts brain activities measured
L16: motor analysis.
L17: by electroencephalography (EEG) to corresponding muscular
L18: responses recorded by electromyography (EMG). Examining the
L19: generation process in the model highlights how the motor cue,
L20: representing implicit motor information hidden within brain I. INTRODUCTION
L21: activities, modulates the interaction between brain and muscle
L22: MUSCLE contractions are driven by motor cues that
L23: systems. The proposed model employs a two-stage generation
L24: process to bridge the semantic gap in cross-modal signals. represent implicit motor information of brain activities.
L25: Initially, the shared movement-related information between EEG These cues, originating from brain neurons, are transmitted via
L26: and EMG signals is extracted using a contrastive learning frame- motor nerves to activate muscle movements. Investigating the
L27: work. These shared representations act as conditional vectors
L28: neural pathways and motor cues is critical for understanding
L29: in the subsequent EMG generation stage based on generative
L30: brain-muscle modulation. These insights have wide-ranging
L31: adversarial networks (GANs). Experiments on a self-collected
L32: multimodal electrophysiological signal data set show the algo- implications, including the development of treatments for
L33: rithm’s superiority over existing time series generative methods neuromuscular disorders [1], [2], the enhancement of motor
L34: in cross-modal EMG generation. Further insights derived from learning protocols [3], and advancements in prosthetics and
L35: the model’s inference process underscore the brain’s strategy
L36: exoskeleton equipment [4]. To investigate the motor cues
L37: for muscle control during movements. This research provides a
L38: in brain-muscular modulation, it’s important to record the
L39: corresponding activities.
L40: Received 1 February 2024; revised 28 March 2024 and 16 May 2024; Electroencephalography (EEG) and electromyography
L41: accepted 31 May 2024. Date of publication 18 October 2024; date of
L42: (EMG), as noninvasive electrophysiological signals, are
L43: current version 20 December 2024. This work was supported in part by
L44: the National Key Research and Development Program of China under Grant well-suited for recording brain and muscle activities. EEG
L45: 2023YFC2415100; in part by the National Natural Science Foundation of records the electrical activities of neurons [5], offering
L46: China under Grant 62373351, Grant 62222316, Grant U20A20224, Grant
L47: insights into how the brain governs muscle systems [6], [7].
L48: 62303463, Grant 82327801, and Grant 62073325; in part by the Youth
L49: Innovation Promotion Association of the Chinese Academy of Sciences (CAS) Simultaneously, EMG characterizes muscle activities [8],
L50: under Grant 2020140; and in part by the CIE-Tencent Robotics X Rhino- reflecting motor patterns [3]. Analyzing the interaction
L51: Bird Focused Research Program. This article was recommended by Associate
L52: between EEG and EMG is crucial for understanding brain-
L53: Editor N. A. M. Isa. (Corresponding authors: Xiao-Hu Zhou; Zeng-Guang
L54: Hou.) muscle modulation during human movement.
L55: This work involved human subjects or animals in its research. Approval Current research primarily examines relationships in
L56: of all ethical and experimental procedures and protocols was granted by
L57: EEG and EMG signals, focusing on attributes, such as
L58: the Ethics Committee of the Institute of Automation, Chinese Academy of
L59: Sciences. frequency [9], [10], temporal [11], [12], [13], and spatial–
L60: Tian-Yu Xiang, Xiao-Hu Zhou, Xiao-Liang Xie, Shi-Qi Liu, Mei-Jiang Gui, temporal domains [14], [15]. Recent work explores shared
L61: Hao Li, and De-Xing Huang are with the State Key Laboratory of Multimodal
L62: motor information within EEG and EMG using a Siamese
L63: Artificial Intelligence Systems, Institute of Automation, Chinese Academy
L64: of Sciences, Beijing 100190, China, and also with the School of Artificial structure [16], [17]. While these studies provide valuable
L65: Intelligence, University of Chinese Academy of Sciences, Beijing 100049, insights, they often view brain-muscle modulation from lim-
L66: China (e-mail: xiangtianyu2021@ia.ac.cn; xiaohu.zhou@ia.ac.cn).
L67: ited perspectives. This study proposes a novel approach by
L68: Xiu-Ling Liu is with the College of Electronic Information Engineering and
L69: the Hebei Key Laboratory of Digital Medical Engineering, Hebei University, using the generation of EMG from EEG as a proxy task,
L70: Baoding 071000, China. for considering multiple signal properties simultaneously. This
L71: Zeng-Guang Hou is with the State Key Laboratory of Multimodal Artificial
L72: method offers a more comprehensive understanding of the
L73: Intelligence Systems and the CAS Center for Excellence in Brain Science
L74: and Intelligence Technology, Institute of Automation, Chinese Academy brain’s control over muscle movements by analyzing the
L75: of Sciences, Beijing 100190, China, also with the School of Artificial generation process.
L76: Intelligence, University of Chinese Academy of Sciences, Beijing 100049,
L77: Two primary methodologies have emerged for the time-
L78: China, and also with the Joint Laboratory of Intelligence Science and
L79: Technology, Institute of Systems Engineering, Macau University of Science series generation: 1) autoregressive models [18], [19], [20]
L80: and Technology, Taipa, Macau, China (e-mail: zengguang.hou@ia.ac.cn). and 2) generative adversarial networks (GANs) [21], [22].
L81: Color versions of one or more figures in this article are available at
L82: Autoregressive models treat the generation process as a series
L83: https://doi.org/10.1109/TCYB.2024.3415369.
L84: Digital Object Identifier 10.1109/TCYB.2024.3415369 of conditional probabilities, focusing on learning transitions
L85: 2168-2267 (cid:2)c 2024 IEEE. Personal use is permitted, but republication/redistribution requires IEEE permission.
L86: See https://www.ieee.org/publications/rights/index.html for more information.
L87: Authorized licensed use limited to: University of Science & Technology of China. Downloaded on July 05,2026 at 10:00:54 UTC from IEEE Xplore. Restrictions apply.
L89: ===== PAGE 2 =====
L91: XIANG et al.: LEARNING MOTOR CUES IN BRAIN-MUSCLE MODULATION 87
L92: from prior to current states. On the other hand, GAN aims method for analyzing brain-muscle modulation are delineated
L93: to directly learn the distributions that govern entire sequences in Section V. Section VI carries out a discussion on the role
L94: by two adversarially trained neural networks. Despite the of shared EEG-EMG representations and future works. This
L95: inherent challenges in capturing entire distributions, GAN has article culminates with conclusions in Section VII.
L96: become increasingly popular in time-series generation. This is
L97: attributed to its ability to mitigate the accumulated error often II. RELATED WORK
L98: observed in autoregressive models [23].
L99: A. Contrastive Learning for Electrophysiological Signals
L100: GAN has been successfully applied to synthesize various
```

### Lines 210-280

```text
L210: The primary objective of this stage is to derive shared B B (cid:2) B (cid:3)
L211: representations, which are parts of motor cues, from the zi = p ri (4)
L212: M M M
L213: brain and muscular activities based on the contrastive learning
L214: where zi denotes the latent for the ith brain/muscular signal.
L215: paradigm. To achieve this, an encoder is employed to extract B/M
L216: spatial–temporal representations from the electrophysiological The function p B/M implemented as a two-layer multilayer
L217: perceptron, serves as a projector for the signals to map the
L218: signals which measure the muscular and brain activities
L219: (cid:2) (cid:3) representations into the latent domain nonlinearly.
L220: ri B = f B (cid:2) Xi B (cid:3) (1) Muscular activities exhibit variation in each trial, even
L221: ri = f Xi (2) when the same subject performs identical movements. This
L222: M M M
L223: variation requires extracting unique characteristics inherent in
L224: where f B/M denotes the encoder for brain/muscular signals, brain and muscle activities within each trial. Consequently,
L225: Xi B/M represents the ith brain/muscular signal in a batch, and instance discrimination, commonly utilized in the contrastive
L226: ri B/M is the corresponding representation. In this study, the learning framework [32], is employed as the proxy task. This
L227: brain activities are measured by EEG, while the muscular choice is particularly pertinent in cross-modal representation
L228: movements are recorded via EMG. The backbone encoder learning, where EEG and corresponding EMG are treated
L229: in this research is a modified version of EEGNet [45], as a positive pair. The primary objective is to enhance the
L230: which retains only the feature extraction stage and omits similarity between the latent of these positive pairs, utilizing
L231: the classification head (shown in Table I). The adaptation the InfoNCE loss (l ) function
L232: c
L233: ⎡ ⎤
L234: of EEGNet extracts spatial–temporal representations from
L235: (cid:2) (cid:3)
L236: e fi d l i l e s te c c r t r - r i b o m a p i n h n k y a s n c i t o o c l m o o g m m ic o p a n o l n s s e p i n g a t t n i a a a n l l s a p , l a y m t s t i e i s r r r n o (B r ( i F D n B g C C A th S ) e P [ ) 4 p 7 [ r 4 o ]. 6 ce ] s a s n e d s b u i s l e in d e i a n r l c i = − log ⎢ ⎣ (cid:7) N j= es 1 z e i B s , (cid:8) z z i M i B , / zj M τ (cid:9) /τ ⎥ ⎦ (5)
L237: Authorized licensed use limited to: University of Science & Technology of China. Downloaded on July 05,2026 at 10:00:54 UTC from IEEE Xplore. Restrictions apply.
L239: ===== PAGE 4 =====
L241: XIANG et al.: LEARNING MOTOR CUES IN BRAIN-MUSCLE MODULATION 89
L242: Algorithm 1 Training Scheme for Representation Learning TABLE II
L243: DESIGN OF GENERATOR STRUCTURE
L244: Require: X , X , N, E (raw EEG/EMG signals, batch size,
L245: B M
L246: and epoch numbers.)
L247: 1: Initialize parameters for EEG/EMG encoder and projector.
L248: 2: for i = 1 to E do
L249: 3: repeat
L250: 4: Sample N EEG/EMG signals.
L251: 5: z B = p B (f B (X B )).
L252: 6: z M = p M (f M (X M )).
L253: 7: Calculate loss L c by (5)-(7).
L254: 8: Update parameters of f B/M and p B/M with adamW
L255: algorithm based on L .
L256: c
L257: 9: until all EEG/EMG are enumerated.
L258: 10: end for
L259: where P denotes the conditional probability distribution
L260: where τ is a temperature hyperparameter and s(·) denotes relating r1 and r2, the term r2(j) refers to the jth ele-
L261: ment of r2, while l represents the length of the conditional
L262: cosine similarity which measures similarity in the latent space
L263: (cid:2) (cid:3) z · z samples. The model captures multiscale conditional proba-
L264: s z , z = i j (6) bilities with k different lengths of samples, with L being
L265: i j ||z ||||z ||
L266: i j the maximum length. Consequently, the range of l, defined
L267: where z and z represent two latent vectors and ||·|| indicates as [L, L/2, L/4, . . . , L/2 (k−1) ], establishes a multiscale con-
L268: i j
L269: the l norm of the vector. The contrastive representation ditional dependencies. This strategy enables simultaneous
L270: 2
L271: learning’s overall loss function is computed as the average of consideration of various temporal scales, essential for captur-
L272: the cross InfoNCE loss over the samples in a batch ing both long-term and short-term dependencies in EMG.
L273: ⎛ ⎞
L274: The third substep, denoted as g , is designed as a 1-D
L275: (cid:15)N 3
L276: L = 1 ⎝ lj ⎠ (7) CNN to refine the generated distribution. This refinement is
L277: c N c essential for reducing high-frequency noise and enhancing the
L278: j=1
L279: smoothness of the generated EMG signals.
L280: where N is the batch size. This loss function aims to enhance The final substep, labeled g , integrates multiscale distri-
```

### Lines 345-388

```text
L345: loss function is formulated as 10: Update parameters of D based on L D and k+=1.
L346: (cid:18) (cid:8) (cid:9)(cid:19)
L347: L = E[D(X )] − E D X ˆ + λgp (11) 11: end while
L348: D M M 12: ## Update the classifier with Adam.
L349: where D represents the discriminator, L is the loss func- 13: Update parameters of clf with L clf based on (13).
L350: D
L351: tion for D, λ is the penalty factor, and “gp” denotes the 14: ## Update the generator with Adam.
L352: gradient penalty. The gradient penalty can be mathematically 15: Update parameters of G with L G based on (14).
L353: 16: until all EEG/EMG sampled are enumerated.
L354: formulated as
L355: (cid:20)(cid:8)(cid:21) (cid:8) (cid:9)(cid:21) (cid:9) (cid:22) 17: end for
L356: gp = E (cid:21) (cid:21)∇ ˆ D X ˆ (cid:21) (cid:21) − 1 2 (12)
L357: X
L358: 2
L359: ˆ threshold t. The training of the discriminator is halted either
L360: where X are samples drawn from the distribution of the real
L361: EMG signals (X ) and the generated EMG signals (X ˆ ), and when its loss function falls below this threshold or when
L362: ∇ represents the M gradients of D of the input data. M it reaches the specified maximum update limit (K). Such a
L363: strategy ensures a balanced interplay between the discriminator
L364: Within the algorithm, the classifier discerns the specific
L365: and generator, crucial for maintaining the stability of the
L366: type of movement of the EMG signals. This ensures that the
L367: training process.
L368: synthesized EMG accurately reflects the movement patterns.
L369: The classification loss (L ) is computed using the cross-
L370: clf
L371: entropy loss function C. Inference Process
L372: (cid:15)(cid:23) (cid:2) (cid:3)(cid:24)
L373: While the training procedure is intricate, the inference
L374: L = − y log yˆ (13)
L375: clf c c process is more straightforward. As depicted in Fig. 2, only
L376: m
L377: the encoder for brain activities and the generator are utilized
L378: where y c denotes the classification label, yˆ c stands for the during inference. This process can be represented as
L379: classifier’s prediction, and m represents the movement types.
L380: The generator’s primary responsibility is to synthesize EMG X ˆ M = G ◦ f B (X B ). (15)
L381: signals from EEG representations. The loss function for the
L382: The procedure begins by extracting movement-related rep-
L383: generator, L , is formulated as
L384: G
L385: (cid:8) (cid:9) (cid:18) (cid:8) (cid:9)(cid:19) resentations of brain activities. These representations are then
L386: L = L X , X ˆ + E D X ˆ + L (14) used to synthesize the corresponding EMG signals.
L387: G r M M M clf
L388: where the first term (L ) signifies the reconstruction loss based
```

### Lines 436-620

```text
L436: types of EMG signals (hand extension, elbow flexion, motivated because if the generated data closely mirrors the
L437: wrist rotation, and rest). real data distribution, the same classifier will effectively on
L438: 2) Preprocessing: EEG signals are first processed by a both data.
L439: notch filter at 50 Hz to reduce powerline interference. The 2) Train on Synthetic and Test on Real Paradigm: The
L440: signals then undergo a band-pass filter within 8 to 30 Hz, train on synthetic, test on real (TSTR) paradigm serves as
L441: spanning the frequency bands of the alpha (8–12 Hz) and beta the inverse form of TRTS, where a classifier is trained on
L442: (13–30 Hz). These bands are known for their correlation with synthetic data and evaluated on real data. This paradigm also
L443: motor functions [49], and are prevalently employed in motor- measures the similarity between real and generated data by
L444: related brain-computer interface paradigms [50]. Independent the classifier’s performance metrics.
L445: component analysis is applied to EEG signals for removing 3) Statistic Metrics: The statistic metrics directly evaluate
L446: artifacts. The EMG signals undergo downsampling to 100 Hz the similarity between synthetic and real EMG signals, includ-
L447: to emphasize the signal components within the low- and ing maximum mean discrepancy (MMD) and dynamic time
L448: middle-frequency ranges. This procedure aims to retain critical warping (DTW). MMD measures the distributional distance
L449: motor information while facilitating model training stabiliza- between datasets using a kernel function. DTW aligns two
L450: tion by removing high-frequency noise. Before the training sequences through time stretching or compression, and then
L451: phase, both EEG and EMG signals undergo normalization to quantifies their similarity using Euclidean distance to measure
L452: achieve a mean of 0 and a standard deviation of 1. temporal dynamics and patterns.
L453: Authorized licensed use limited to: University of Science & Technology of China. Downloaded on July 05,2026 at 10:00:54 UTC from IEEE Xplore. Restrictions apply.
L455: ===== PAGE 7 =====
L457: 92 IEEE TRANSACTIONS ON CYBERNETICS, VOL. 55, NO. 1, JANUARY 2025
L458: TABLE V
L459: COMPARISON BETWEEN THE PROPOSED METHOD AND OTHER METHODS IN EMG GENERATION. ↑: HIGHER IS BETTER AND ↓: LOWER IS BETTER
L460: (a) (b) (c) (d) (e)
L461: Fig. 4. Visualization of the synthetic EMG generated by different methods and real EMG after PCA. (a) T-force [19]. (b) P-force [20]. (c) RCGAN [22].
L462: (d) TimeGAN [21]. (e) Ours.
L463: D. Experimental Results generator in synthesizing EMG signals with more pronounced
L464: movement-related characteristics. Additionally, the multiscale
L465: An analysis is conducted between the proposed algorithm
L466: CNN adeptly models both the long-term and short-term
L467: and other time series generation methods. These algorithms are
L468: dependencies inherent in EMG signals, setting it apart from
L469: categorized into autoregressive methods, such as T-force [19]
L470: other GAN-based designs [21], [22]. Among the evaluated
L471: and P-force [20], and GAN methods, including RCGAN [22]
L472: methods, the proposed algorithm distinguishes itself by excep-
L473: and TimeGAN [21]. For a consistent evaluation, the EEG
L474: tional performance across multiple metrics, highlighting its
L475: latent vectors derived during the contrastive learning phase are
L476: capability to generate high-quality EMG signals.
L477: provided to these methods as conditional vectors for EMG
L478: generation.
L479: E. Ablation Study
L480: As shown in Table V, the proposed algorithm surpasses
L481: others across various evaluation metrics in two experimental An ablation study is conducted to further assess the efficacy
L482: setups. Notably, GAN-based methods tend to outperform of the proposed algorithm. Ablation studies are crucial in
L483: autoregressive algorithms. This result might stem from the understanding the contribution of different components to the
L484: limitations of autoregressive algorithms relying on transi- overall performance of the algorithm. This study examines
L485: tion probabilities from previous states to current ones. The three critical components: 1) the classifier in categorizing
L486: intrinsic noise in electrophysiological signals poses challenges generated EMG; 2) the incorporation of EMG signals in
L487: in accurately learning these transition probabilities. GAN- contrastive learning for shared representation extraction; and
L488: based methods, focusing on learning the entire probability 3) the multiscale CNN within the generator.
L489: distribution, offer a more reliable solution. This is corroborated Quantitative results are shown in Table VI. The findings
L490: by Fig. 4, showing that plots (c)–(e), representing GAN-based indicate that integrating all components yields optimal EMG
L491: methods, produce a closer synthetic EMG signal distribution signal generation performance across various metrics and
L492: to the actual signals. experimental setups. Each component contributes uniquely
L493: Delving deeper into the comparison with other GAN- to the algorithm’s effectiveness. The classifier proves vital
L494: based methods, the proposed algorithm consistently exhibits for embedding movement-related information into synthesized
L495: superior performance. The enhanced performance can be signals, as its absence leads to a notable performance decline
L496: attributed to specific design elements in the proposed method in both TRTS and TSTR paradigms. Similarly, EMG signals
L497: that optimize for generating electrophysiological signals. For used in the contrastive learning phase enhance movement-
L498: instance, including a classifier in the pipeline, guides the related representation. While omitting this component slightly
L499: Authorized licensed use limited to: University of Science & Technology of China. Downloaded on July 05,2026 at 10:00:54 UTC from IEEE Xplore. Restrictions apply.
L501: ===== PAGE 8 =====
L503: XIANG et al.: LEARNING MOTOR CUES IN BRAIN-MUSCLE MODULATION 93
L504: TABLE VI
L505: ABLATION STUDY ON EMG GENERATION TASK. W/O IS THE ABBREVIATION OF WITHOUT. ↑: HIGHER IS BETTER AND ↓: LOWER IS BETTER
L506: (a) (b) (c) (d) (e)
L507: Fig. 5. Comparison between real EMG and synthetic EMG generated by different methods (x-axis: time (s) and y-axis: normalized amplitude). Root mean
L508: square error (RMSR) between the synthesis EMG and the ground truth is displayed at the left top corner. (a) Real EMG. (b) W/o classifier. (c) W/o EMG.
L509: (d) W/o multi CNN. (e) Ours.
L510: impacts TSTR metrics, a substantial decrease in TRTS metrics in the high-frequency region. The coefficients’ root mean
L511: indicates a bias in the generated EMG relative to the authentic square (RMS) values are reported to enable a more direct
L512: signal. and quantitative comparison. The RMS values of the proposed
L513: The multiscale CNN contributes to the overall performance algorithm closely align with the ground truth. This align-
L514: of the proposed model. This enhancement is particularly ment demonstrates that the EMG signals synthesized by the
L515: evident in Fig. 5, where the detailed features of the EMG proposed algorithm closely replicate the intensity profile of
L516: signal are refined by integrating the multiscale CNN into real EMG signals across the frequency spectrum.
L517: the generator. In essence, the collective integration of these
L518: components substantially elevates the quality of the synthe-
L519: sized EMG. The root mean square error (RMSE) for each
L520: signal against the ground truth is included for a robust visual
L521: V. BRAIN-MUSCULAR MODULATION ANALYSIS
L522: comparison. The integration of all the proposed modules A. Analysis Pipeline
L523: achieves the best performance as indicated by the lowest Understanding the brain-muscle modulation is pivotal in
L524: RMSE. neuroscience research. To quantitatively elucidate the motor
L525: Another essential aspect of evaluating the quality of the cues in the brain-muscle modulation process, an analysis
L526: synthesized EMG signals is in the spectral domain. For pipeline inspired by our prior work is developed [17].
L527: each movement type, the relationship between the average The primary focus of this investigation is the spatial rela-
L528: coefficients obtained using the fast Fourier transform (FFT), tionship between the brain and muscles, as manifested by
L529: and the frequency of an EMG channel are visualized in the placement of sensor channels. This relationship is fur-
L530: Fig. 6. It can be found that the proposed algorithm achieves ther explored by examining the generation process from
L531: a relatively stable coefficient distribution, particularly notable EEG to EMG.
L532: Authorized licensed use limited to: University of Science & Technology of China. Downloaded on July 05,2026 at 10:00:54 UTC from IEEE Xplore. Restrictions apply.
L534: ===== PAGE 9 =====
L536: 94 IEEE TRANSACTIONS ON CYBERNETICS, VOL. 55, NO. 1, JANUARY 2025
L537: (a) (b) (c) (d) (e)
L538: Fig. 6. Comparison between real EMG and synthetic EMG generated by different methods in the spectral domain (x-axis: frequency (Hz) and y-axis:
L539: coefficient). The RMS of the signals’ FFT coefficients is shown in the left top corner. (a) Real EMG. (b) W/o classifier. (c) W/o EMG. (d) W/o multi CNN.
L540: (e) Ours.
L541: The analysis pipeline introduces a function N to alter the on the EMG signal, thus providing insights into the spatial
L542: raw signal of a specific EEG channel interplay between brain activity and muscular responses.
L543: X ˆ (cid:8) (c) = N(X (c)) (16)
L544: B B B. Analysis Results
L545: where c represents the designated EEG channel and X ˆ (cid:8) is the The visualization of I(c) for correlation between EMG and
L546: B
L547: modified EEG data. Importantly, N substitutes a channel (c) EEG channels using topographic maps is shown in Fig. 7. The
L548: of raw EEG signal with Gaussian noise that adheres to the importance score, I(c), is derived from the EMG generation
L549: original distribution. model designed to generate binary movements in EMG sig-
L550: After modifying the EEG data, the inference procedure of nals (wrist rotation/hand extension/elbow flexion versus rest).
L551: the proposed model is applied to derive the EMG signal. It is These topographic maps yield several insightful observations.
L552: pertinent to note that the proposed EMG generation pipeline First, a clear contralateral activation pattern can be observed.
L553: employs distinct generators for each EMG channel. While Contralateral activation refers to the phenomenon where one
L554: the description here focuses on a single EMG channel, the hemisphere of the brain controls and responds to the opposite
L555: methodology is uniformly applied across all channels side of the body. The left brain hemisphere demonstrates
L556: (cid:8) (cid:9)
L557: a significantly higher-importance score than the right hemi-
L558: X ˆ (cid:8) (c) = G ◦ f X ˆ (cid:8) (c) (17)
L559: M B B sphere. This pronounced activation in the left hemisphere
L560: ˆ (cid:8) can be attributed to the experimental design, wherein par-
L561: where X represents the generated EMG signal from modified
L562: M ticipants utilized their right hands for the movements. Such
L563: EEG signal. Finally, to evaluate the influence of EEG channels
L564: on the generated EMG signal, X ˆ (cid:8) (c) is compared to X ˆ contralateral activation is a recognized occurrence in recent
L565: M M human–brain interference systems [53]. Examining specific
L566: (EMG signal generated by raw EEG signal) under a certain
L567: brain regions further reveals that most EMG channels display
L568: metric. The variation in this metric serves as the importance
L569: high-importance scores in the central region and the parietal
L570: score
L571: (cid:18) (cid:8) (cid:9) (cid:8) (cid:9)(cid:19) lobe. Previous studies have identified these regions as crucial
L572: I(c) = E e X ˆ , X − e X ˆ (cid:8) (c), X (18) for motor organization and execution [54], [55].
L573: M M M M
L574: Another notable observation in Fig. 7 is the consistency of
L575: where E denotes expectation, and e represents a metric for topographic patterns across different movements within the
L576: measuring similarity between signals. Accuracy under the same EMG channel, as compared to the variability observed
L577: TRTS paradigm is chosen as the metric, given its broad when comparing the same movement across various EMG
L578: acceptance in evaluating the congruence between generated channels. This finding is quantitatively supported by Fig. 8,
L579: and raw signals’ distributions in time series generation tasks. which presents the Pearson correlation values between each
L580: The term I represents the importance score of specific EEG set of importance scores. Fisher’s Z value is employed as
L581: channels c in generating the EMG signal. This score is an intermediary measure to accommodate multiple sets of
L582: quantified by the difference in expectations between X ˆ (cid:8) (c) importance scores for a single EMG channel. This Fisher’s
L583: M
L584: ˆ
L585: and X , as calculated under the metric e. A larger difference Z value is then converted to a mean group-level Pearson
L586: M
L587: indicates a more significant influence of the EEG channel score. All correlation tests yielded p-values less than 0.01,
L588: Authorized licensed use limited to: University of Science & Technology of China. Downloaded on July 05,2026 at 10:00:54 UTC from IEEE Xplore. Restrictions apply.
L590: ===== PAGE 10 =====
L592: XIANG et al.: LEARNING MOTOR CUES IN BRAIN-MUSCLE MODULATION 95
L593: Fig. 7. Visualization of I of different EMG channels for different movements by topographic maps: (a) Wrist rotation, (b) hand extension, and (c) elbow
L594: flexion.
L595: TABLE VII
L596: COMPARISON OF THE REPRESENTATIONS EXTRACTED WITH (OURS) OR
L597: WITHOUT EMG (W/O EMG) UNDER MOTOR CLASSIFICATION AND
L598: SUBJECT CLASSIFICATION TASK. CLASSIFICATION IS
L599: ABBREVIATED AS CLF
L600: Fig. 8. Visualization of Pearson correlation coefficients of I between different
L601: EMG channels. The p-value for all correlation tests is less than 0.01. Channel
L602: is abbreviated as C.
L603: VI. DISCUSSION
L604: A. Role of the Shared EEG-EMG Representations
L605: underscoring the statistical significance of this analysis. The
L606: importance scores within the same EMG channel show a high The shared EEG-EMG latent serves as conditional vec-
L607: correlation, nearly 0.90, indicating a significant correlation in tors in EMG generation. This section aims to validate that
L608: brain activities related to the same muscle channel. Conversely, these representations encapsulate motor-related information,
L609: the group-level Pearson score decreases notably, averaging including movement class and manipulation characteristics.
L610: around 0.4, when comparing different channels. Despite Two two-layer multilayer perceptrons, each with hidden unit
L611: being statistically significant, these lower-Pearson correlation configurations of (64, 16), are applied to classify the motor
L612: coefficients suggest a milder correlation. It implies that while type and the subjects from the latent vectors.
L613: movement-related brain regions may share some similarities, Table VII presents a comparative analysis. The performance
L614: the marked decrease in correlation points to distinct brain of the proposed model’s representations significantly surpasses
L615: control mechanisms for different muscles, even during varied random chance in both motor (binary/multiclass: 50%/25%)
L616: movements. This finding aligns with neuroscience theories and subject classification (10%) tasks, underscoring the pres-
L617: proposing that the brain maps control mechanisms for different ence of motor-related information within these representations.
L618: muscles to specific but interconnected brain regions [56]. Notably, when compared to representations derived without
L619: Authorized licensed use limited to: University of Science & Technology of China. Downloaded on July 05,2026 at 10:00:54 UTC from IEEE Xplore. Restrictions apply.
```

### Lines 635-688

```text
L635: While the proposed algorithm effectively generates EMG [3] X.-H. Zhou et al., “A multilayer and multimodal-fusion architecture for
L636: simultaneous recognition of endovascular manipulations and assessment
L637: from EEG, some limitations may impact broader applications.
L638: of technical skills,” IEEE Trans. Cybern., vol. 52, no. 4, pp. 2565–2577,
L639: First, the generative model is confined to single-channel EMG Apr. 2022.
L640: signal generation, a decision driven by ensuring stability [4] H. Lorach et al., “Walking naturally after spinal cord injury using a
L641: brain–spine interface,” Nature, vol. 618, pp. 126–133, May 2023.
L642: during the training phase. This design, while effective for
L643: [5] T. Kirschstein and R. Köhling, “What is the source of the EEG?” Clin.
L644: training robustness, inherently restricts the model’s capacity EEG Neurosci., vol. 40, no. 3, pp. 146–149, 2009.
L645: to capture spatial interactions across multiple EMG chan- [6] F. Qi et al., “Spatiotemporal-filtering-based channel selection for
L646: single-trial EEG classification,” IEEE Trans. Cybern., vol. 51, no. 2,
L647: nels. Furthermore, the generated EMG signals exhibit a
L648: pp. 558–567, Feb. 2021.
L649: relatively low frequency. This reflects a tradeoff between
L650: [7] F. Tang, P. Tinˇo, and H. Yu, “generalized learning vector quantization
L651: training stability and the preservation of motor information. with log-Euclidean metric learning on symmetric positive-definite man-
L652: It is noteworthy that the higher-frequency ranges, despite ifold,” IEEE Trans. Cybern., vol. 53, no. 8, pp. 5178–5190, Aug. 2023.
L653: [8] C. De Luca, “Electromyography,” in Encyclopedia of Medical Devices
L654: being less emphasized, also harbor motor-related information.
L655: and Instrumentation. Hoboken, NJ, USA: Wiley, 2006.
L656: Additionally, the current experimental settings may not fully [9] B. Kim, L. Kim, Y.-H. Kim, and S. K. Yoo, “Cross-association analysis
L657: replicate real-world scenarios. Although sufficient for validat- of EEG and EMG signals according to movement intention state,” Cogn.
L658: Syst. Res., vol. 44, pp. 1–9, Aug. 2017.
L659: ing the conceptual framework, bridging this gap is essential for
L660: [10] X. Xi et al., “Analysis of functional corticomuscular coupling based on
L661: practical engineering applications and advanced neuroscience
L662: multiscale transfer spectral entropy,” IEEE J. Biomed. Health Inform.,
L663: research. vol. 26, no. 10, pp. 5085–5096, Oct. 2022.
L664: Future efforts will focus on refining the algorithm [11] N. N. Tun, F. Sanuki, and K. Iramina, “EEG-EMG correlation anal-
L665: ysis with linear and nonlinear coupling methods across four motor
L666: for broader applications in engineering and neuroscience.
L667: tasks,” in Proc. 43rd Annu. Int. Conf. IEEE Eng. Med. Biology Soc.
L668: Incorporating spatial–temporal dynamics of EMG signals is (EMBC), 2021, pp. 783–786.
L669: essential for enhancing the pipeline. By accounting for the [12] X. Xi, X. Wu, Y.-B. Zhao, J. Wang, W. Kong, and Z. Luo, “Cortico-
L670: muscular functional network: An exploration of cortico-muscular
L671: spatial relationships among EMG channels and capturing high-
L672: coupling in hand movements,” J. Neural Eng., vol. 18, no. 4, 2021,
L673: frequency temporal dynamics, future efforts aim to generate Art. no. 46084.
L674: more comprehensive EMG signals. The strategy of extracting [13] X. Xi et al., “Construction and analysis of cortical–muscular
L675: shared representations in a unified space is promising for functional network based on EEG-EMG coherence using wavelet coher-
L676: ence,” Neurocomputing, vol. 438, pp. 248–258, May 2021.
L677: evolving sophisticated human-machine interfaces and compu-
L678: [14] I. Korolczuk et al., “Temporal unpredictability increases error monitoring
L679: tational methods [57], [58], [59], [60]. Furthermore, future as revealed by EEG-EMG investigation,” Psychophysiology, vol. 61,
L680: studies will apply this analysis pipeline within the neuro- no. 2, 2024, Art. no. e14442.
L681: [15] J. Sun, T. Jia, Z. Li, C. Li, and L. Ji, “Enhancement of EEG-EMG cou-
L682: science community to analyze brain-muscle modulation using
L683: pling detection using corticomuscular coherence with spatial–temporal
L684: varied data and experimental setups. optimization,” J. Neural Eng., vol. 20, no. 3, 2023, Art. no. 36001.
L685: [16] J.-H. Cho, J.-H. Jeong, and S.-W. Lee, “NeuroGrasp: Real-time EEG
L686: classification of high-level motor imagery tasks using a dual-stage
L687: deep learning framework,” IEEE Trans. Cybern., vol. 52, no. 12,
L688: VII. CONCLUSION
```

## Multisource_Domain_Separation_Network_for_Industrial_Intelligent_Monitoring_in_Unseen_Conditi.txt
- Total extracted lines: 760

### Lines 1-60

```text
L3: ===== PAGE 1 =====
L5: This article has been accepted for inclusion in a future issue of this journal. Content is final as presented, with the exception of pagination.
L6: IEEE TRANSACTIONS ON CYBERNETICS 1
L7: Multisource Domain Separation Network for
L8: Industrial Intelligent Monitoring in
L9: Unseen Conditions
L10: Zidi Jia , Member, IEEE, Lei Ren , Senior Member, IEEE, Zuo-Jun Max Shen, Member, IEEE,
L11: and Laurence T. Yang , Fellow, IEEE
L12: Abstract—Industrial time-series prediction is one of the crucial time-series prediction, multisource domain separation network
L13: tasks of industrial artificial intelligence, which has been exten- (MS-DSN), supervised contrastive similarity.
L14: sively adopted in intelligent monitoring. However, continuous
L15: variations in the working conditions of industrial processes
L16: I. INTRODUCTION
L17: lead to continuous changing in monitoring data, resulting in
L18: distribution shift. Industrial time-series prediction models may RECENTLY, the advancements in artificial intelligence
L19: not be able to maintain satisfactory accuracy. Domain general- technology have made data-driven methods popular in
L20: ization (DG) methods can effectively improve the robustness and
L21: Industrial Internet of Things (IIoT) [1]. These methods only
L22: generalization of the models for unseen or dynamic distribution
L23: need to obtain information from monitoring data and can
L24: data. However, existing methods have drawbacks limit their
L25: applicability in practice. First, most DG methods are designed realize better performance, thus they have been extensively
L26: for classification tasks and lack a general framework for regres- studied [2]. The widespread application of advanced artificial
L27: sion tasks. Second, extracting domain-invariance may obscure intelligence technology has led to significant breakthroughs
L28: task-relevant information, thereby degrading the prediction pre-
L29: in many area of industrial manufacturing, such as predictive
L30: cision. Third, DG methods are generally sensitive to extremely
L31: maintenance [3], product life-cycle management [4], and smart
L32: distributed data, potentially compromising the robustness. To
L33: address these issues, a multisource domain separation network grids [5]. Industrial time-series prediction is a critical com-
L34: (MS-DSN) is proposed. First, by constructing a DSN to separate ponent of these issues [6], and holds great importance for
L35: the features into domain-private and -shared spaces, domain- ensuring safe, stable, and efficient industrial production [7].
L36: specific information can be filtered while domain-invariant
L37: Deep learning models are commonly employed to analysis
L38: features are preserved. Second, a supervised contrastive loss is
L39: industrial time-series [8]. While these methods generally per-
L40: defined to preserve the domain invariant information related to
L41: the label changing tendency in the domain-shared space. Finally, form well in controlled experimental settings, the presence
L42: a directional risk extrapolation (DREx) method is proposed to of numerous uncertainties in complex industrial environments
L43: represents the extreme distributed data. Experiments on two hinders their widespread practical application.
L44: datasets, CMAPSS and N-CMAPSS, verify the effectiveness of
L45: Industrial process conditions in IIoT are increasingly com-
L46: our method.
L47: plex and varying. It may lead to variations in the distribution
L48: Index Terms—Directional risk extrapolation (DREx), domain of collected monitoring data, referred to as a distribution
L49: generalization (DG), industrial intelligent monitoring, industrial
L50: shift [9]. For instance, in a flexible manufacturing process,
L51: the operational state of production equipment continually
L52: fluctuates in response to varying manufacturing tasks. It poses
L53: Received 27 May 2025; revised 24 September 2025; accepted 29 September
L54: 2025. This work was supported in part by the National Key Research a challenge to the independent and identically distributed data
L55: and Development Program of China under Grant 2023YFB3308000 and in assumption required by most models. Conventional time-series
L56: part by the National Science Foundation of China (NSFC) under Project
L57: prediction methods may not be able to adapt to sudden changes
L58: 62225302 and Project 62173023. This article was recommended by Associate
L59: Editor C. Zhao. (Corresponding author: Lei Ren.) in working conditions or gradual evolution processes, resulting
L60: Zidi Jia is with the School of Automation Science and Electrical Engineer- in reduced reliability. While it is theoretically possible to
```

### Lines 120-360

```text
L120: under different conditions. Despite recent progress, there are monitoring systems are sensor signals and control signals,
L121: still many issues that need to be addressed. time-series prediction is a core task in intelligent monitoring.
L122: First, to the best of our knowledge, most of the solutions to Time-series prediction methods based on deep learning are a
L123: distribution shift so far are aimed at classification problems. promising technology for extracting and analyzing spatiotem-
L124: Cross-domain methods for prediction and regression issues poral correlations between features in industrial time-series.
L125: have not yet received much attention, especially in industrial These methods can identify and analyze these correlations,
L126: scenarios. Many current studies on cross-domain learning providing a powerful means of understanding the complex
L127: methods rely on techniques such as pseudo-label [21] or dis- relationships between different features of temporal data [7].
L128: tribution assumptions [22]. However, assessing the reliability As demand for flexibility in industrial tasks continues to
L129: of relevant metrics for these techniques in regression tasks can grow, manufacturing on mixed production lines involving mul-
L130: be challenging. Second, basic distribution alignment is likely tiple, constantly changing processes is becoming increasingly
L131: to obscure specific information related to downstream tasks. common. Consequently, the distribution of monitoring data
L132: Because downstream task information may be irrelevant to is subject to constant change, which makes related moni-
L133: inter-domain correlation. There is currently no feasible method toring tasks more challenging. Furthermore, industrial time
L134: for analyzing industrial time-series under distribution shifts, data originate from a variety of sources, is high-throughput
L135: particularly when the target data is not accessible. Therefore, and low-value intensive, and is highly dynamic. Traditional
L136: studying general DG methods that can be applied to various methods struggle to effectively deal with the complexity and
L137: issues is also a thorny problem that needs to be solved urgently. dynamic characteristics of industrial time data. Therefore,
L138: Third, DG models may be sensitive to extreme distribution highly generalized, robust, and evolvable models are needed.
L139: changes, resulting in satisfactory robustness not always being
L140: maintained. Therefore, this article is to study a DG method to B. Domain Generalization
L141: solve the problem of industrial time-series prediction under DG enables the model to maintain high robustness when
L142: varying and unseen working conditions. As the targets of processing more widely distributed data by learning invariant
L143: industrial monitoring tasks are typically fixed, these tasks knowledge across various domains. Let X represent the data
L144: can be considered invariant. This means that the distribution and Y denote its corresponding labels. A domain, denoted
L145: of features related to the predicted targets in the monitoring as D = {(x , y )}n , consists of data sampled from a joint
L146: i i i=1
L147: signals remains unchanged in the feature space, and features distribution P . Conventional methods involve acquiring a
L148: XY
L149: that vary with working conditions can be considered noise. prediction function f:X → Y within the hypothesis space
L150: Therefore, the method described in this article is based on the through empirical risk minimization (ERM) applied to the
L151: strategy of invariant risk minimization (IRM). training set D. However, when the training and test sets do not
L153: ===== PAGE 3 =====
L155: This article has been accepted for inclusion in a future issue of this journal. Content is final as presented, with the exception of pagination.
L156: JIA et al.: MULTISOURCE DSN FOR INDUSTRIAL INTELLIGENT MONITORING IN UNSEEN CONDITIONS 3
L157: Fig. 1. Overall framework of MS-DSN. Autoencoders are used for representation learning in private space and shared space, respectively.
L158: obey the assumption of independent and identical distributed, to standardize the alignment of features in different domains,
L159: ERM is less robust and difficult to generalize, despite its such as IRM [24]. Krueger et al. [25] advocate for feature
L160: high computational efficiency. Therefore, DG is proposed and invariance by minimizing the extrapolation risk among source
L161: applied. domains, effectively diminishing the variance of the source
L162: Given a training set S = {Sk}K containing K source domain risk. In industrial intelligent monitoring tasks, working
L163: k=1
L164: domains, Sk ∼ Pk , obeying different distributions Pk , the conditions may change very frequently, which can lead to
L165: XY XY
L166: objective of DG is to acquire a robust and generalizable predic- changes in the distribution of monitoring signals. Therefore,
L167: tion function f from S through minimizing the expected error DG methods are required to improve the robustness of the
L168: on any unseen target domain T , where the joint distribution monitoring model, with the IRM method being the most
L169: PT is distinct from Pi for i = 1, . . . , K suitable for this purpose.
L170: XY XY
L171: Although there have been many related studies, most of
L172: f = arg min E L (f (x) , y) . (1)
L173: (x,y)∈T them are used for classification tasks (such as fault diagnosis),
L174: and only consider aligning the features of the overall source
L175: Numerous DG methods have been proposed, broadly
L176: domain data features to reduce the differences between the
L177: categorized into approaches based on data manipulation, rep-
L178: domains. How to design a more universal DG method is an
L179: resentation learning, and learning strategies [17]. Our primary
L180: urgent issue that needs to be solved.
L181: focus is on methods grounded in representation learning.
L182: Domain adversarial training stands as a widely employed
L183: III. METHODOLOGY
L184: technique for acquiring domain-invariant representations, with
L185: A. Multisource DSN
L186: the domain adversarial neural network [23] serving as the most
L187: frequently utilized method in this context. Explicit alignment Inspired by domain-separated networks [26] for DA, this
L188: is a more direct approach, directly utilizing specific constraints article applies domain-private components and domain-shared
L190: ===== PAGE 4 =====
L192: This article has been accepted for inclusion in a future issue of this journal. Content is final as presented, with the exception of pagination.
L193: 4 IEEE TRANSACTIONS ON CYBERNETICS
L194: information as possible is extracted by the encoders. During
L195: model training, the data X (k = 1, . . . , K) of the kth source
L196: k
L197: domain are input into the domain private encoder EP and the
L198: k
L199: domain shared encoder ES , respectively, to obtain the domain
L200: private hidden features HP and the domain shared hidden
L201: k
L202: features HS . After this, HS is input into the shared predictor to
L203: k k
L204: obtain the monitoring indicator Y . After HP is concatenated
L205: k k
L206: with HS , it is input into the domain private decoder DP to
L207: k k
L208: generate reconstructed data Xˆ . In our method, by maximizing
L209: k
L210: the diversity between domain-private and -shared hidden fea-
L211: Fig. 2. Topology of the neural network structure of MS-DSN. tures HP and HS , domain-private features could be removed
L212: k k
L213: from HS and consistency could be maintained. Besides, the
L214: k
L215: effectiveness of feature extraction is ensured by minimizing the
L216: components to gain domain invariant insights from multiple difference between the reconstructed data Xˆ k and the original
L217: source domain data. Traditional DG methods typically involve data X k . Furthermore, by minimizing the difference among
L218: aligning features between different data domains. While these HS across domains (in MS-DSN, it is realized by maximiz-
L219: methods are effective and feasible in theory, they can retain ing the mutual information lower bound), the extraction of
L220: significant amounts of noise shared between domains, which domain-invariant information is further ensured. Finally, the
L221: can mask useful information. To address this issue, this article risk differences in different training domains are reduced by
L222: introduces the concepts of domain-private and domain-shared minimizing risk extrapolation to reduce the sensitivity of the
L223: spaces. For each domain, these two spaces are conjugate to model to a wide range of extreme distribution changes. The
L224: each other and together they contain all the information in that trained domain shared encoder and shared predictor are models
L225: domain. The domain-private space is unique to each domain, with high generalization ability to data distribution shifts.
L226: while the domain-shared space is shared by all domains. Algorithm 1 shows the flow of the proposed MS-DSN.
L227: Since this method is based on the assumption of IRM, it
L228: Algorithm 1 Algorithm of Training MS-DSN
L229: is hypothesized that information relevant to the downstream
L230: monitoring task is contained within the domain-shared space. Input: Source data Dk = {X k,i , y k,i }n i= k 1 , k = 1, . . ., K,
L231: By identifying a shared subspace that is orthogonal to the pri- Initialized shared encoder ES ,
L232: vate subspace, the method can separate unique domain-specific Initialized private encoders EP, k = 1, . . ., K,
L233: k
L234: information and generate more meaningful representations for Initialized private decoders DP, k = 1, . . ., K,
L235: k
L236: downstream tasks. In this case, modeling of the downstream Initialized predictor P.
L237: tasks can be performed in the domain-shared space to achieve Output: Trained shared encoder ES ,
L238: high generalization. Trained predictor P.
L239: MS-DSN utilizes parallel domain-private encoders and a 1: for number of iterations do
L240: domain-shared encoder to explicitly represent domain private 2: Sample minibatch data X k ∼ Dk, k = 1, . . ., K
L241: information and domain shared information. By maximiz- 3: Extract the shared latent representation: H k S = ES (X k ),
L242: ing the difference between domain shared representation and k = 1, . . ., K
L243: domain private representation, domain-specific information 4: Extract the private latent representation: H k P = E k P(X k ),
L244: is filtered to obtain domain-invariant information related to k = 1, . . ., K
L245: downstream tasks. It is to note that, given the based assumption 5: Predict Y k of X k : Y k = P(hS k ), k = 1, . . ., K, and compute
L246: of domain-IRM, it is not applicable to heterogeneous DG L task by Eq.(12)
L247: tasks. 6: Reconstruct X k : Xˆ k = D k P(concat(hS k , h k P)), k = 1, . . ., K,
L248: Fig. 1 shows the framework of the proposed MS-DSN and compute the reconstruct loss L reconstruct by Eq.(5)
L249: method. We believe that MS-DSN is applicable to a variety of 7: Compute the loss of diversities L diversity of h k P and hS k ,
L250: DG tasks. Without losing generalization, we choose regres- k = 1, . . ., K, by Eq.(4)
L251: sion task as downstream task. Assume there are K source 8: Compute the loss of similarity L similarity of {hS k }, k =
L252: domains, S 1, . . . , S K. The topology of the neural network 1, . . ., K, by Eq.(7)
L253: structure of MS-DSN is shown in Fig. 2. The model consists 9: Update ES with L ES = L diversity + L similarity + L task +
L254: of a encoder layer and a decoder layer, with 1 domain L recontrust
L255: shared encoder, 1 domain shared predictor, K domain private 10: Update E k P, k = 1, . . ., K with L EP = L diversity +
L256: k
L257: encoders, and K domain private decoders (corresponding to L recontrust
L258: K source domains, respectively). The domain-private encoder 11: Update D k P, k = 1, . . ., K with L DP = L recontrust
L259: and domain-shared encoders are utilized for the extraction of 12: Update P with L P = L task k
L260: domain-private features and domain-shared features, respec- 13: end for
L261: tively. The domain-shared predictor is employed for the
L262: purpose of making predictions for downstream tasks. The Let HS and HP represent the shared and the private repre-
L263: k k
L264: domain-private decoders are used to reconstruct the original sentation of each domain, X and Xˆ represent the raw data
L265: k k
L266: data, with the objective being to ensure that as much effective and its reconstruction in the kth domain, and Y represent the
L268: ===== PAGE 5 =====
L270: This article has been accepted for inclusion in a future issue of this journal. Content is final as presented, with the exception of pagination.
L271: JIA et al.: MULTISOURCE DSN FOR INDUSTRIAL INTELLIGENT MONITORING IN UNSEEN CONDITIONS 5
L272: B. Supervised Contrastive Similarity
L273: A supervised contrastive similarity loss, L is defined
L274: similarity
L275: to reduce the difference of the shared representations, that is,
L276: to obtain domain invariant representation. As shown in many
L277: studies, the domain-invariant information extracted by many
L278: methods is likely to contain a large amount of noise related
L279: to shared representations [26], [27]. Simple extraction of this
L280: information (just like domain adversarial neural network) may
L281: lead to losing valuable information. Besides, these methods
L282: Fig. 3. Structure of the module for each domain.
L283: are effective in classification tasks, especially the alignment of
L284: data distribution boundaries has significant benefits for the DG
L285: predicted indicator. ES , EP, DP, and P are domain shared of classification methods. The regression prediction problem
L286: encoder, domain private encoder, domain private decoder, pays more attention to the trend of label changes with features,
L287: and shared predictor, respectively. The inference of MS-DSN so these methods may not always work.
L288: consists of the following parts: Thus, L similarity based on supervised contrastive learning
L289: is defined to enable the data in each domain converge to
L290: 8 HS = ES (X ) similar distribution in the feature space. We adopt the density
L291: ˆˆˆ<H k
L292: P = EP (X
L293: k
L294: ) ratio assumption from van den Oord et al. [28] and define
L295: ˆˆˆ:y Xˆ k k
L296: =
L297: =
L298: P
L299: D
L300: (cid:0)
L301: k P k
L302: H
L303: (cid:0)
L304: S
L305: co
L306: (cid:1)
L307: k n
L308: .
L309: cat (cid:0) H k S , H k P(cid:1)(cid:1) (2) a Th c e on lo tr s a s st f i u v n e c s ti i o m n ila is rit b y as l e o d ss o m n e th tr e ic fo w ll i o th wi l n ab g e a ls ss a u s m a pt m io e n t : ri t c h s e .
L310: k k variation tendency of labels in various domains is positively
L311: related to the variation of data distribution in the feature space.
L312: The training goal is to minimize the following loss:
L313: L acts on the domain sharing features, and its goal is to
L314: similarity
L315: obtain similar representations for samples with similar labels
L316: L = L + αL + βL + γL (3)
L317: task reconstruct diversity similarity in all domains
L318: where α, β, γ are hyperparameters that control the interaction L
L319: similarity
L320: o ar f e th lo e ss lo f s u s nc te ti r o m n s s . f L o t r ask c , ol L la r b ec o o r n a st t r i u v c e t , t L ra d i i n ve i r n s g ity . , T a h n e d p L re si d m i il c a t r o ity r = − log X "P k(cid:44)i ex P p (−τ |y i − (cid:0) y k |) ˇ cosin (cid:0) ˇ H (cid:1) i S , H k S (cid:1) + ε #
L321: trained on the shared representation generalizes better across i j(cid:44)i exp −τ ˇy i − y jˇ
L322: domains since its input is not contaminated by aspects of the (6)
L323: representation which are unique to each domain.
L324: where cosin means cosine similarity and H is the encoding of
L325: The data in each domain is projected in shared space and
L326: all source domain data in minibatch. ε is the hyperparameter,
L327: private space, respectively, and is analyzed in the shared and we let ε = 1e−5 in our experiments. In order to avoid
L328: predictor. The module corresponding to the kth domain is
L329: unnecessary computation, batch normalization is performed
L330: shown in Fig. 3. To induce the model to produce such a split
L331: on hS before L ’s computing. The loss function can be
L332: representation, we define diversity loss, L , to encourage similarity
L333: diversity further simplified to
L334: the independence of these parts. L operates across
L335: diversity
L336: domains, fostering the extraction of distinct facets of the input L
L337: similarity
L338: by both shared and private encoders. The definition of L diversity 2P exp (−τ |y − y |) (cid:13) (cid:13)HS (cid:62) HS (cid:13) (cid:13) 3
L339: involves a soft subspace orthogonality constraint between the = − log X 4 k(cid:44)i P (cid:0) i ˇ k (cid:13) i ˇ(cid:1) j (cid:13) + ε5 . (7)
L340: private and shared representations i j(cid:44)i exp −τ ˇy i − y jˇ
L341: L diversity = X K (cid:13) (cid:13) (cid:13) h k p(cid:62) h k s (cid:13) (cid:13) (cid:13) 2 . (4) B in y v m ar i i n o i u m s i fi zi e n l g ds th c i a s n lo o s b s ta f i u n nc si t m io i n l , ar sa r m ep p r l e e s s en w ta it t h io s n i s m . ilar labels
L342: F
L343: k=1
L344: To ensure that the private representation retains as much C. Risk Extrapolation
L345: information as possible and add generalization, a reconstruc- We hypothesize that the differences among source domains
L346: tion loss L reconstruct is applied. The concatenation of h k s and h k p represent the changes we are likely to encounter, but that the
L347: is reconstructed into Xˆ through the private decoder ensuring changes at test time may be more extreme in magnitude. Solely
L348: the effectiveness of the encoder. A scale-invariant mean square using prediction bias (such as mean square error) to train the
L349: error term is utilized to represent the reconstruction loss model may cause the model to focus too much on a certain
L350: L reconstruct , which is applicable to each domain area, leading to model bias. This may render the model less
L351: robust to distribution shift.
L352: K
L353: L reconstruct = X m 1 (cid:13) (cid:13)X k − Xˆ k (cid:13) (cid:13) 2 2 + m 1 2 (cid:0)(cid:0) X k − Xˆ k (cid:1) · 1 m (cid:1)2 (5) do T m h a e in re s fo p re re , ve r n e t d s uc m in o g dels risk from diff b e e re in n g ces ove b r e ly twe se e n n siti s v o e urc to e
L354: k=1
L355: extreme distributions. To this end, we use the idea of IRM
L356: where m is the number of the sampling points of each sample. to improve the overall robustness by reducing the worst-case
L358: ===== PAGE 6 =====
L360: This article has been accepted for inclusion in a future issue of this journal. Content is final as presented, with the exception of pagination.
```

### Lines 456-645

```text
L456: TABLE IV This part provides a brief introduction to the baseline mod-
L457: SELECTED MEASUREMENTS AND SCENARIO DESCRIPTORS els employed for DG. Each baseline method can be concise
L458: OF N-CMAPSS described as.
L459: 1) Empirical Risk Minimization: DG through ERM is
L460: accomplished by minimizing the empirical risk within each
L461: source domain, mitigating the impact on model performance.
L462: 2) Domain Adversarial Neural Network: Domain adversar-
L463: ial neural network (DANN) [23] employs adversarial training
L464: for domain-invariant representations. The DANN framework
L465: is utilized here specifically to obtain domain-invariant repre-
L466: sentations of the source data.
L467: 3) Correlation Alignment: Correlation alignment (CORAL)
L468: [31] minimizes the covariance shift among each source
L469: domains for distribution alignment.
L470: 4) Mixup: Mixup [32] realizes DG by mixing data from
L471: various source domains to generate new data to expand the
L472: distribution of training data.
L473: 5) Variance Risk Extrapolation: Variance risk extrapolation
L474: (VREx) [25] realizes DG by mitigating training risks and
L475: enhancing the homogeneity of training risks.
L476: B. Experimental Setting
L477: 6) Representation Self-Challenging: Representation self-
L478: 1) Model Details: The training process of each model challenging (RSC) [33] realize DG through an iterative process
L479: consists of up to 50 epochs, with a batch size set at 256 of challenging and discarding dominant features activated
L480: and a learning rate of 3e−4. Our network contains one sparse during training. This compels the network to focus on activat-
L481: preencoder, one shared encoder, K private encoders, K private ing the remaining labels-relevant features, thereby improving
L482: decoders, and one shared predictor (K is the count of source overall performance.
L483: domains). The preencoder expands the dimensionality of the
L484: data to 100 dimensions; the shared encoder, each private
L485: D. Experimental Results
L486: encoder and each private decoder are three-layer multihead
L487: To assess our proposed method in a cross-domain scenario,
L488: self-attention (four-head) with residual links; the shared pre-
L489: we utilize labeled training data from the source domain
L490: dictor is a two-layer perceptron (hidden layer dimension is
L491: for model training, and evaluate its performance with test
L492: 128). The baseline comparison method, and the shared parts
L493: data from the target domain, measured in terms of RMSE
L494: of our proposed method all adopt the same network archi-
L495: and score. To establish the effectiveness of our approach,
L496: tecture details. To delve deeper into the model’s capabilities,
L497: it is recommended to set different loss weights for balanced we compare it with classic transfer learning methods such
L498: as DANN, CORAL, and mixup. Additionally, we include
L499: multitask learning. However, for the sake of simplicity, we set
L500: advanced methods like VERX and RSC for comparative anal-
L501: the hyperparameters in all loss functions to 1.
L502: 2) Evaluation Metrics: The effectiveness of the proposed ysis. The experimental results presented are averages derived
L503: from ten randomly repeated experiments, providing a robust
L504: method is assessed by two metrics: root-mean-square error
L505: evaluation of the proposed method’s performance.
L506: (RMSE) and score metric. RMSE is defined as
L507: The results of the comparative experiments on CMAPSS are
L508: v shown in Table V and Fig. 5. It can be found that the perfor-
L509: u n
L510: RMSE = u t 1 n X (cid:0) yˆ j − y j (cid:1)2 . (13) mance of the proposed MS-DSN is better than all competing
L511: j=1 methods in various unknown scenarios. The error of MS-DSN
L512: is around 25, the maximum error of the other methods is
L513: RMSE treats larger and smaller RUL predictions equally. around 30, and the maximum error of Mixup is even close
L514: For practical applications, smaller RUL predictions may be to 40. DANN and CORAL are representative cross-domain
L515: more detrimental to the system. A fractional metric is thus transfer methods based on distribution alignment. These meth-
L516: introduced to impose more penalties on late predictions, in ods primarily emphasize the consistency of data distributions
L518: ===== PAGE 8 =====
L520: This article has been accepted for inclusion in a future issue of this journal. Content is final as presented, with the exception of pagination.
L521: 8 IEEE TRANSACTIONS ON CYBERNETICS
L522: Fig. 5. Visualization of the RUL prediction results of FD004 test engine #248 by each method in case 1. The shaded region indicates the error margin
L523: between the prediction and the actual RUL values. (a) DANN. (b) CORAL. (c) Mixup. (d) VREx. (e) RSC. (f) MS-DSN.
L524: TABLE V
L525: PERFORMANCE COMPARISONS AMONG MS-DSN AND SEVERAL STATE-OF-THE-ART METHODS ON CMAPSS
L526: while overlooking the role of labels in multisource domain significant advantages over the second best method in these
L527: alignment. It may obscure valuable information relevant to two cases. Taking FD004 as an example, the errors of our
L528: downstream tasks. Therefore, their capabilities are limited in method are 50.66% and 14.29% lower than ERM and the
L529: scenarios such as case 2 where is apparent distribution shift. second-best method, respectively.
L530: Our method explicitly extracts domain-invariant information The results of the comparative experiment on the dataset
L531: through an external parallel domain private encoder, and uses N-CMAPSS are shown in Table VI. Since the difference
L532: labels to correct the features of the shared space. Therefore, in data distribution in different sub-datasets is not obvious,
L533: our method enables the model to obtain better generalization the DG effects of various baseline models are not much
L534: capabilities and can simultaneously preserve more informa- better than ERM. However, the performance of our method
L535: tion relevant to downstream tasks. Furthermore, we also has obvious advantages. We believe this is because, on the
L536: observe that DG methods do not always perform well on one hand, our method can filter out the influence of unique
L537: relatively complex data due to large shifts in the domain. But information in each domain; on the other hand, our method can
L538: MS-DSN can successfully generalize domain knowledge to enlarge the boundaries of data distribution and enhance DG
L539: distant domains. For example, FD002 and FD004 are relatively capabilities.
L540: complex sub-datasets, and various baseline models have rel- Generally speaking, MS-DSN can effectively extract invari-
L541: atively poor generalization effects. However, our method has ant information from multiple source domains, making the
L543: ===== PAGE 9 =====
L545: This article has been accepted for inclusion in a future issue of this journal. Content is final as presented, with the exception of pagination.
L546: JIA et al.: MULTISOURCE DSN FOR INDUSTRIAL INTELLIGENT MONITORING IN UNSEEN CONDITIONS 9
L547: TABLE VI
L548: PERFORMANCE COMPARISONS AMONG MS-DSN AND SEVERAL STATE-OF-THE-ART METHODS ON N-CMAPSS
L549: Fig. 7. Visualization of the domain shared representation of MS-DSN and
L550: the latent representation of DANN encoder. (a) MS-DSN. (b) DANN.
L551: SCS,” “w/o DREx,” and “DANN1,” respectively. In particular,
L552: “w/o SCS” refers to the model version for which without
L553: supervised comparative similarity (replaced by the Euclidean
L554: distance of the discrepancy), “w/o DREx” refers to the model
L555: version for which without DREx, and “DANN1” refers to
L556: Fig. 6. Case 1 visualization of domain-shared features and domain-private
L557: features in each sub-dataset of CMAPSS. (a) FD001. (b) FD002. (c) FD003. DANN with supervised contrastive similarity and DREx. The
L558: (d) FD004. results of the ablation study are presented in Table VII. While
L559: the accuracy of our method is not consistently the highest in all
L560: cases, it outperforms the version without a specific component
L561: model have strong generalization ability, and the generalization
L562: in most scenarios. Especially the comparison with DANN1
L563: and accuracy are better than those of existing models.
L564: shows that our MS-DSN architecture is of effectiveness in
L565: filtering domain-specific information and gaining insight into
L566: E. Visualization Analysis domain-invariant information. Thus, the effectiveness of these
L567: Fig. 6 shows the t-SNE visualization of domain-private three components are verified.
L568: features and domain-shared features in each sub-dataset of Besides, we verify the contribution of each loss function
L569: the CMAPSS dataset in Case 1. As can be seen from the in MS-DSN framework. We named the three variants of MS-
L570: figure, MS-DSN can effectively separate and decouple domain- DSN “w/o L ,” “w/o L ,” and “w/o L ,”
L571: reconstruct similarity diversity
L572: specific information and domain-shared information in the which represent the MS-DSN frameworks without loss func-
L573: original data, thereby filtering out information in the data that tion L , L , and L , respectively. It can
L574: reconstruct similarity reconstruct
L575: is irrelevant to downstream tasks, thereby realizing DG. It can be seen that in the MS-DSN framework, each calculation goal
L576: be seen from Fig. 6 that the distribution pattern of domain is very important. Removing any loss function will cause a
L577: shared features in the feature space is related to the changing significant drop in performance. However, it should be noted
L578: trend of the labels. that the results of these ablation experiments are better than
L579: Besides, for the FD004 test engine #248 of the test set of those of ERM or even DANN because our framework has
L580: Case 1, the domain shared representation of MS-DSN and more than one DG-capable component.
L581: the latent representation of DANN encoder are extracted by
L582: t-SNE and presented in Fig. 7(a) and (b), respectively. It can be
L583: G. Sensitivity Analysis
L584: seen from the figure that in the shared space of MS-DSN, the
L585: In this part, we evaluate the sensitivity of the proposed MS-
L586: distribution of features is related to the trend of labels; while
L587: DSN to the weights of individual loss functions. We focus
L588: there is no such correlation in the latent space of DANN.
L589: on the loss functions of each auxiliary task in the MS-DSN
L590: framework, namely L , L , and L . These
L591: reconstruct similarity diversity
L592: F. Ablation Studies
L593: loss functions are relevant to the updating of the model. We
L594: In this subsection, we verify the contribution of each com- conduct experiments on case1 of CMAPSS. For the weight of
L595: ponent in MS-DSN to DG through ablation experiments on each loss function, candidate values of 0, 0.001, 0.01, 0.1, 1,
L596: CMAPSS. We named the three variants of MS-DSN “w/o and 10 are assigned, respectively. Fig. 8 shows the results of
L598: ===== PAGE 10 =====
L600: This article has been accepted for inclusion in a future issue of this journal. Content is final as presented, with the exception of pagination.
L601: 10 IEEE TRANSACTIONS ON CYBERNETICS
L602: TABLE VII
L603: ABLATION STUDIES OF MS-DSN ON CMAPSS
L604: REFERENCES
L605: [1] Z. Chen, Z. Song, and Z. Ge, “Variational inference over graph: Knowl-
L606: edge representation for deep process data analytics,” IEEE Trans. Knowl.
L607: Data Eng., vol. 36, no. 6, pp. 2730–2744, Jun. 2024, doi: 10.1109/
L608: TKDE.2023.3327415.
L609: [2] X. Zhou et al., “Spatial–temporal federated transfer learning with multi-
L610: sensor data fusion for cooperative positioning,” Inf. Fusion, vol. 105,
L611: May 2024, Art. no. 102182.
L612: [3] L. Ren, Z. Jia, T. Wang, Y. Ma, and L. Wang, “LM-CNN: A cloud-
L613: edge collaborative method for adaptive fault diagnosis with label
L614: sampling space enlarging,” IEEE Trans. Ind. Informat., vol. 18, no. 12,
L615: pp. 9057–9067, Dec. 2022.
L616: [4] Y.-N. Sun, W. Qin, H.-W. Xu, R.-Z. Tan, Z.-L. Zhang, and W.-T. Shi, “A
L617: multiphase information fusion strategy for data-driven quality prediction
L618: of industrial batch processes,” Inf. Sci., vol. 608, pp. 81–95, Aug. 2022.
L619: [5] W. Zheng and G. Chen, “An accurate GRU-based power time-
L620: series prediction approach with selective state updating and stochastic
L621: optimization,” IEEE Trans. Cybern., vol. 52, no. 12, pp. 13902–13914,
L622: Dec. 2022.
L623: Fig. 8. Experimental results with different weights of individual loss for case [6] H. Jiang, S. Zhang, W. Yang, X. Peng, and W. Zhong, “Integration of
L624: 1 of CMAPSS. (a) Lrecontrust. (b) Lsimilarity. (c) Ldiversity. encoding and temporal forecasting: Toward end-to-end NOx prediction
L625: for industrial chemical process,” IEEE Trans. Neural Netw. Learn. Syst.,
L626: vol. 35, no. 3, pp. 2984–2996, Mar. 2024.
L627: [7] L. Ren, Z. Jia, Y. Laili, and D. Huang, “Deep learning for time-series
L628: the ablation experiment, which shows that the weights of each prediction in IIoT: Progress, challenges, and prospects,” IEEE Trans.
L629: loss function have little impact on the performance of MS- Neural Netw. Learn. Syst., vol. 35, no. 11, pp. 15072–15091, Nov. 2024,
L630: DSN. This may be due to the large enough number of epochs doi: 10.1109/TNNLS.2023.3291371.
L631: [8] J. Li, Y. Wang, Y. Zi, H. Zhang, and Z. Wan, “Causal disentanglement:
L632: in our experimental setting. MS-DSN is more robust in this
L633: A generalized bearing fault diagnostic framework in continuous degra-
L634: regard. Besides, when the weight is equal to 10 (the loss dation mode,” IEEE Trans. Neural Netw. Learn. Syst., vol. 34, no. 9,
L635: function is given a larger weight), the performance of the pp. 6250–6262, Sep. 2023.
L636: [9] L. Chen, Q. Li, C. Shen, J. Zhu, D. Wang, and M. Xia, “Adversarial
L637: model does not drop significantly, which shows that each
L638: domain-invariant generalization: A generic domain-regressive frame-
L639: optimization objective does not have a negative impact on DG. work for bearing fault diagnosis under unseen conditions,” IEEE Trans.
L640: In comparison, MS-DSN is sensitive to L . Ind. Informat., vol. 18, no. 3, pp. 1790–1800, Mar. 2022.
L641: reconstruct
L642: [10] Q. Qian, J. Zhou, and Y. Qin, “Relationship transfer domain general-
L643: ization network for rotating machinery fault diagnosis under different
L644: working conditions,” IEEE Trans. Ind. Informat., vol. 19, no. 9,
L645: V. CONCLUSION pp. 9898–9908, Sep. 2023.
```

## Self-Supervised_Time_Series_Representation_Learning_via_Cross_Reconstruction_Transformer.txt
- Total extracted lines: 954

### Lines 1-90

```text
L3: ===== PAGE 1 =====
L5: IEEE TRANSACTIONS ON NEURAL NETWORKS AND LEARNING SYSTEMS, VOL. 35, NO. 11, NOVEMBER 2024 16129
L6: Self-Supervised Time Series Representation
L7: Learning via Cross Reconstruction Transformer
L8: Wenrui Zhang , Ling Yang , Shijia Geng , and Shenda Hong
L9: Abstract—Since labeled samples are typically scarce in real- NOMENCLATURE
L10: world scenarios, self-supervised representation learning in time t Original time series.
L11: series is critical. Existing approaches mainly employ the con-
L12: m Magnitude of t.
L13: trastive learning framework, which automatically learns to
L14: p Phase of t.
L15: understand similar and dissimilar data pairs. However, they are
L16: constrained by the request for cumbersome sampling policies x Concatenation of t, m and p.
L17: and prior knowledge of constructing pairs. Also, few works have r Dropping ratio.
L18: focused on effectively modeling temporal-spectral correlations N Number of patches of x.
L19: to improve the capacity of representations. In this article,
L20: B Number of x in a batch (batch size).
L21: we propose the cross reconstruction transformer (CRT) to solve
L22: x ith x in a batch of x.
L23: the aforementioned issues. CRT achieves time series represen- i
L24: tation learning through a cross-domain dropping-reconstruction E i Projection of x i by convolutional neural networks.
L25: task. Specifically, we obtain the frequency domain of the time E′ Projection of E by transformer.
L26: i i
L27: series via the fast Fourier transform (FFT) and randomly drop E [CLS] token for time domain.
L28: T
L29: certain patches in both time and frequency domains. Dropping E′ Projection of E by transformer.
L30: is employed to maximally preserve the global context while T T
L31: E [CLS] token for magnitude.
L32: masking leads to the distribution shift. Then a Transformer M
L33: architecture is utilized to adequately discover the cross-domain E′ M Projection of E M by transformer.
L34: correlations between temporal and spectral information through E [CLS] token for phase.
L35: P
L36: reconstructing data in both domains, which is called Dropped E′ Projection of E by transformer.
L37: Temporal-Spectral Modeling. To discriminate the representa- P P
L38: tions in global latent space, we propose instance discrimination
L39: constraint (IDC) to reduce the mutual information between I. INTRODUCTION
L40: different time series samples and sharpen the decision bound-
L41: aries. Additionally, a specified curriculum learning (CL) strategy TIME series analysis [1], [2], [3], [4], [5], [6], [7], [8] is
L42: is employed to improve the robustness during the pretraining critical in a variety of real-world applications, such as
L43: phase, which progressively increases the dropping ratio in the transportation, medicine, finance, and industry. With the suc-
L44: training process. We conduct extensive experiments to evaluate
L45: cess of deep learning, various tasks in the field of time series
L46: the effectiveness of the proposed method on multiple real-
L47: analysis have achieved great performances, which include time
L48: world datasets. Results show that CRT consistently achieves
L49: the best performance over existing methods by 2%–9%. The series classification [3], [4], forecasting [5], [6] and anomaly
L50: code is publicly available at https://github.com/BobZwr/Cross- detection [7], [8], [9]. However, since labeled time series are
L51: Reconstruction-Transformer. usually difficult to acquire [10], [11], it is essential to study
L52: Index Terms—Cross domain, self-supervised learning, time learning representations from time series data in an unsuper-
L53: series, transformer. vised learning way. Self-supervised learning is an emerging
L54: approach, which designs a pretext task and automatically
L55: generates “labels” for supervision while minimizing effort on
L56: annotation.
L57: Existing works of self-supervised learning can be
L58: Manuscript received 28 November 2022; revised 1 January 2023 and 7 April grouped into two categories: contrast-based methods and
L59: 2023; accepted 24 June 2023. Date of publication 21 July 2023; date of current reconstruction-based. Contrast-based methods [12], [13], [14]
L60: version 30 October 2024. This work was supported by the National Natural
L61: are the main-stream approach of self-supervised representation
L62: Science Foundation of China under Grant 62102008. (Wenrui Zhang and Ling
L63: Yang contributed equally to this work.) (Corresponding author: Shenda Hong.) learning for time series. They are mainly to apply a segment-
L64: Wenrui Zhang is with the National Institute of Health Data Science, level sampling policy and construct positive pairs and negative
L65: Peking University, Beijing 100871, China, also with the Institute of Medical
L66: pairs. The model is then forced to maximize the similarity of
L67: Technology, Health Science Center of Peking University, Beijing 100191,
L68: China, and also with the Department of Mathematics, National University of positive pairs while minimizing the similarity of negative pairs
L69: Singapore, Singapore 119077 (e-mail: zhangwenrui@u.nus.edu). in the feature space. For example, contrastive predictive coding
L70: Ling Yang and Shenda Hong are with the National Institute of Health Data
L71: (CPC) [15] conducts representation learning by using powerful
L72: Science, Peking University, Beijing 100871, China, and also with the Institute
L73: of Medical Technology, Health Science Center of Peking University, Beijing auto-regressive models in latent space to make predictions in
L74: 100191, China (e-mail: yangling0818@163.com; hongshenda@pku.edu.cn). the future, relying on Noise-Contrastive Estimation [16] for
L75: Shijia Geng is with HeartVoice Medical Technology, Hefei 230027, China
L76: the loss function in similar ways. Temporal and contextual
L77: (e-mail: gengshijia@heartvoice.com.cn).
L78: Digital Object Identifier 10.1109/TNNLS.2023.3292066 contrasting (TS-TCC) [17] is an improved work of CPC
L79: 2162-237X © 2023 IEEE. Personal use is permitted, but republication/redistribution requires IEEE permission.
L80: See https://www.ieee.org/publications/rights/index.html for more information.
L81: Authorized licensed use limited to: University of Science & Technology of China. Downloaded on July 05,2026 at 10:01:34 UTC from IEEE Xplore. Restrictions apply.
L83: ===== PAGE 2 =====
L85: 16130 IEEE TRANSACTIONS ON NEURAL NETWORKS AND LEARNING SYSTEMS, VOL. 35, NO. 11, NOVEMBER 2024
L86: 3) To tackle the problem of distribution shift caused
L87: by masking in existing reconstruction-based methods,
L88: we employ a simple but reasonable “masking” method,
L89: which is randomly dropping certain parts of data in time
L90: and frequency domains. Instead of setting values as 0,
```

### Lines 180-340

```text
L180: training process. ing for time series still needs to be promoted. Inspired by
L181: Authorized licensed use limited to: University of Science & Technology of China. Downloaded on July 05,2026 at 10:01:34 UTC from IEEE Xplore. Restrictions apply.
L183: ===== PAGE 3 =====
L185: ZHANG et al.: SELF-SUPERVISED TIME SERIES REPRESENTATION LEARNING VIA CRT 16131
L186: Fig. 2. Framework of our CRT. For each time series, we transform it into the frequency domain and calculate the magnitude and phase as explained in
L187: Section III-B. We then slice the data and randomly drop some sliced patches. The remaining patches are projected as three types of embeddings through
L188: three CNNs (shown as arrows in the figure). Decorated with the prefixed [CLS] tokens (ET, EM, and EP) and summed with position embedding and
L189: domain-type embedding, all embeddings are fed into a cross-domain Transformer encoder. For our pretrained reconstruction task, we feed all resultant
L190: cross-domain representations into the decoder to reconstruct the original time, magnitude, and phase data. For downstream tasks, we condense E′ , E′ and
L191: E′
L192: P
L193: (corresponding to ET, EM and EP) as the representation. T M
L194: the well-studied self-supervised learning methods in computer cross-reconstruction method. The goal of our method is
L195: vision and natural language processing areas, recent works to learn representations combining useful information from
L196: mainly leverage the contrastive learning framework for time two domains. Generally, the model is first pretrained following
L197: series representation learning [14]. The researchers design dif- our CRT framework and then transferred to the downstream
L198: ferent time-slicing strategies to construct positive and negative tasks. In this section, we describe our CRT in detail. All
L199: pairs with the assumption that temporally similar fragments important notations are shown in Nomenclature.
L200: could be viewed as positive samples and remote fragments At first, we pay attention to the drawbacks of existing self-
L201: are treated as negative samples [42]. Unsupervised Scalable supervised learning methods for time series data.
L202: Representation Learning [12] introduces a novel unsupervised 1) The existing reconstruction methods for time series mask
L203: loss with time-based negative sampling to train a scalable original data and reconstruct it. However, masking (set
L204: encoder, shaped as a deep convolutional neural network (CNN) to zeros) can significantly change the original pattern
L205: with dilated convolutions [43]. temporal neighborhood coding of the time series and bring many noises to the pre-
L206: (TNC) [13] introduces the concept of a temporal neighbor- training process that would deteriorate the performance.
L207: hood with stationary properties as the distribution of similar To tackle these problems, we propose the dropping
L208: windows in time. Nevertheless, these time-based methods are approach, which is discussed in Section III-A.
L209: sometimes unreasonable for long time series and fail to capture 2) Most representation learning methods for time series
L210: the long-term dependencies [14]. Besides, the performance neglect the frequency domain, which is a complemen-
L211: will substantially deteriorate when applied to downstream tary perspective to the time domain of time series. In
L212: tasks containing periodic time series. Section III-B, we propose a novel way to better utilize
L213: A recent work [23] proposes a Transformer-based recon- the spectral information and model temporal-spectral
L214: struction self-supervised task for time series data for the first correlations.
L215: time. This method masks part of the original time series data
L216: Combining the above two modules, we propose our Dropped
L217: by setting the values as zeros and uses a linear layer to recon-
L218: Temporal-Spectral Modeling for time series and discuss it
L219: struct the masked data. The results show that reconstructing
L220: in Section III-C. In Section III-D, we introduce an effective
L221: the masked data can help extract dense vector representations
L222: progressive training strategy to improve the stability and
L223: of multivariate time series and facilitate models to understand
L224: capacity of our CRT.
L225: contextual information. However, masking original data intro-
L226: duces a gap between the pretraining stage and fine-tuning
L227: stage, because it changes the original distribution of time series A. Dropping Rather Than Masking
L228: significantly. In addition, all methods including contrastive
L229: Masking parts of data and reconstructing them is a common
L230: learning methods neglect an important characteristic of time
L231: paradigm in self-supervised learning tasks [32], [40]. Inspired
L232: series data - the frequency domain.
L233: by this, some works mask the original time series by setting
L234: the value of certain temporal segments to 0 and reconstructing
L235: III. CROSS RECONSTRUCTION TRANSFORMER
L236: these segments [23]. However, this may significantly change
L237: The framework of CRT is shown in Fig. 2. Our the original pattern of time series and bring noises to the
L238: CRT is a Transformer-based time-frequency domain representation learning process. Besides, it may cause a gap
L239: Authorized licensed use limited to: University of Science & Technology of China. Downloaded on July 05,2026 at 10:01:34 UTC from IEEE Xplore. Restrictions apply.
L241: ===== PAGE 4 =====
L243: 16132 IEEE TRANSACTIONS ON NEURAL NETWORKS AND LEARNING SYSTEMS, VOL. 35, NO. 11, NOVEMBER 2024
L244: temporal and spectral information and model cross-domain
L245: correlations.
L246: The most common method to transform time series into the
L247: frequency domain is the fast Fourier transform (FFT) [45],
L248: which is a rapid implementation of the discrete Fourier trans-
L249: form (DFT)
L250: Fig. 3. Masking versus Dropping. (a) Given one time-series data, (b) masking
L251: m
L252: so
L253: e
L254: m
L255: an
L256: e
L257: s
L258: se
L259: to
L260: gm
L261: se
L262: e
L263: t
L264: n
L265: s
L266: ts
L267: e
L268: .
L269: gments of values to zeros, and (c) dropping means to discard
L270: F[k] = X
L271: N−1
L272: t[n]
L273: (cid:18)
L274: cos
L275: (cid:18) 2knπ (cid:19)
L276: − sin
L277: (cid:18) 2knπ (cid:19)
L278: i
L279: (cid:19)
L280: N N
L281: n=0
L282: k = 0, 1, . . . , N − 1 (2)
L283: where t is original time series data, N is the length of t,
L284: k is the index of frequency data, i is called imaginary unit
L285: satisfying i2 = −1, and F is the frequency domain data. After
L286: FFT, the original time series is transformed into the frequency
L287: domain and is converted to a sequence of complex numbers.
L288: However, these complex numbers cannot be used to train the
L289: neural networks directly. Most of the methods considering the
L290: Fig. 4. Phase versus Magnitude. (a) Given a time series, (b) reconstruction frequency domain attempt to store the spectral information
L291: with phase tends to preserve the shape of the original data, and (c) while using the magnitude of the complex numbers. For any complex
L292: reconstruction with magnitude tends to preserve the value of the original
L293: number z = a +bi, where a and b are arbitrary real numbers.
L294: data. All data are conducted min-max normalization. The Euclidean distance
L295: between (b) and (a) is 1.62 and Euclidean distance between (c) and (a) is The magnitude of z is ||z|| = (a2 + b2)1/2. However, using
L296: 5.05. only magnitude to restore the complex numbers would cause
L297: information loss. Because we cannot restore z only using ||z||.
L298: between the pretraining stage and fine-tuning stage since it To tackle this problem, we propose a novel way to better
L299: leads to distribution shifts. As shown in Fig. 3(b), masking utilize the spectral information rather than simply using the
L300: significantly changes the shape and distribution of the original magnitude. We introduce phase φ(z) ∈ (−π, π] as follows:
L301: time series. Different from images or text, the shape is
L302:  b
L303: a
L304: m
L305: d
L306: n
L307: e
L308: a
L309: t
L310: s
L311: e
L312: i
L313: k
L314: r
L315: m
L316: i
L317: i
L318: o
L319: n
L320: p
L321: r
L322: g
L323: o
L324: a
L325: r
L326: t
L327: t
L328: e
L329: w
L330: an
L331: o
L332: th
L333: t
L334: u
L335: e
L336: l
L337: a
L338: d
L339: d
L340: n
```

### Lines 500-575

```text
L500: constraint (IDC) module to remove redundancy and sharpen
L501: Modeling. For a given time series data t, we first conduct
L502: decision boundary. IDC maximizes the mutual information
L503: FFT and convert t from the time domain to the frequency
L504: between the representations and original input, and simultane-
L505: domain. The obtained vector is a complex vector, of which
L506: ously constrains the redundant information that other samples
L507: we store both the magnitude and the phase as mentioned in
L508: have in common. Also, we maximize the distance between E
L509: ¯′
L510: Section III-B. Thus, the complex vector is transformed into i
L511: and E where i ̸= j in latent space, that is minimizing
L512: j
L513: two real vectors m (magnitude) and p (phase) with the same
L514: length. We then concatenate t, m, and p to get the input x = 1
L515: L =
L516: [t, m, p] of length L. IDC B(B − 1)
L517: For the input x, we choose to drop parts of it as mentioned  
L518: B
L519: in Section III-A. Each of the sliced patches contains only × log X X esim ( Proj 1 ( E¯ i ′),Proj 2 ( Ej ))  (6)
L520: one type of data (time, magnitude, or phase). After that,
L521: i=1 j=1..B,j̸=i
L522: we drop r × N (r ∈ (0, 1) is the given dropping ratio and
L523: N is the number of patches) patches and use the remaining where B is the batch size, sim(·, ·) is cosine similarity
L524: (1 − r) × N patches to reconstruct the dropped patches. For sim(x, y) = (x · y/||x||||y||), and Proj , Proj are two pro-
L525: 1 2
L526: patches containing time information, we randomly drop them. jection heads to project E′ and E into the same latent
L527: i j
L528: Also, for patches containing frequency information (phase or space. The projection heads can be either a linear layer or
L529: magnitude), we drop the corresponding pair of patches (phase a multilayer perceptron, and we use a two-layer perceptron in
L530: and magnitude of the same segments of complex vectors). our experiments.
L531: As explained in Section III-A, dropping the patches can reduce
L532: the gap between the pretraining stage and fine-tuning stage
L533: D. Model Optimization
L534: because it does not change the shape of the original data.
L535: Before the Transformer encoder, we add three CNNs to Combining the reconstruction loss and IDC loss, our final
L536: extract local features for three types of patches respectively. loss is
L537: We hypothesize CNN can help extract local features, and
L538: Transformer can help model cross-domain information using L = L + βL (7)
L539: Recon IDC
L540: the local features. The patches x from time domain and
L541: i
L542: magnitude and phase are projected to three types of embed- where β is a hyper-parameter. By updating this loss, we hope
L543: dings E respectively. We then add a different learnable [CLS] the representations learned by the model contain as much
L544: i
L545: token before each type of embeddings (the [CLS] before the sample-specific information as possible. Thus, the represen-
L546: time, magnitude, and phase embeddings are referred to as tations are both informative and discriminable. As for the
L547: E , E and E respectively). The three types of embeddings complexity, the FFT process is conducted before pretrain-
L548: T M P
L549: are summed with their corresponding learnable domain-type ing the model and frequency data is directly used during
L550: embeddings and concatenated into a vector E ∈ R(N+3)×D, self-supervised training. Consequently, the increase in com-
L551: where D is the dimension of the embeddings. Before fed putational complexity of optimizing L is negligible.
L552: into the Transformer, E is summed with the corresponding However, it is difficult to reconstruct the dropped patches
L553: learnable position embeddings. when r is initially set as a large value. As a result, we introduce
L554: We input the whole E into the Transformer encoder and CL [46], which is a strategy that trains the model from “easy”
L555: use the produced features to reconstruct the original data to “hard.” In detail, we set a relatively small dropping ratio
L556: (time, magnitude, and phase). The learned representations r at the beginning of the pretraining stage, and increase r as
L557: are used to reconstruct the original data of both domains the self-supervised learning goes. Formally, we refer to the
L558: so that the Transformer encoder can automatically capture initial r as r min , final r as r max , and the number of epochs for
L559: complementary information from both domains. increasing r as N epoch . r min and r max are hyperparameters, and
L560: Formally, in a batch, there are B inputs x , i = 1, . . . , B. x should be tuned on the validation set. Then, the r for each
L561: i i
L562: is projected to E ∈ R(N+3)×D by CNNs, and E is projected by epoch i is
L563: i i
L564: Transformer to E′ i ∈ R(N+3)×D. We use E ¯′ i = (E′ T +E′ M +E′ P /3) (cid:18) (cid:18) i (cid:19)(cid:19)
L565: for down-stream tasks. We concatenate each E′ with learnable r = max r , min r , . (8)
L566: i i min max N
L567: decoding tokens and feed them into the decoder to reconstruct epoch
L568: all patches. The reconstruction loss is When the current epoch i is smaller than r × N , r is
L569: min epoch i
L570: L = 1 X L X d (cid:0) x′[i] (cid:2) j (cid:3) − x[i] (cid:2) j (cid:3)(cid:1)2 (5) e e q q u u a a l l t t o o r ( m i/ in N . Whe ) n . T r m he in n × , r N e r p e o m ch ai ≤ ns i e ≤ qua r m l a t x o × r N epo u c n h t , il r i th i e s
L571: Recon L × d epoch i max
L572: i=1 j=1 pretraining stage ends.
L573: Authorized licensed use limited to: University of Science & Technology of China. Downloaded on July 05,2026 at 10:01:34 UTC from IEEE Xplore. Restrictions apply.
L575: ===== PAGE 6 =====
```

### Lines 585-843

```text
L585: TABLE II
L586: and phase of this half sequence. After concatenating three
L587: KEY HYPER-PARAMETERS OF DATASETS
L588: sequences, the new sequence is with the double length of the
L589: original time series. When we slice the sequence into patches,
L590: we make sure that each patch contains only one type of data
L591: (time, magnitude, or phase). We then randomly drop patches
L592: in a probability of r (as mentioned in Section III-D) in the
L593: ith epoch during pretraining. The patch length and dropping
L594: IV. EXPERIMENTS hyper-parameters for each dataset are given in Table II.
L595: 4) Baselines: We compare our performances with the fol-
L596: A. Experimental Setup
L597: lowing self-supervised learning approaches, including the ones
L598: 1) Datasets: We conduct experiments on three publicly designed for time series specifically as well as the ones for
L599: available time series datasets. general data.
L600: a) PTB-XL [47], [48]: PTB-XL is an electrocardiogram a) Contrastive Predictive Coding [15]: CPC is to learn
L601: (ECG) dataset with 21 837 12-lead ECGs of 10 s, where 52% representations by predicting the future data in the latent space
L602: are male and 48% are female, ranging in age from 0 to 95. through autoregressive models. It constructs a contrastive loss
L603: The sample rate is 500 Hz, and the length of each recording to maximally preserve the mutual information in the latent
L604: is 5000. Our task is to classify time series into one of space between data in the present time step and data in the
L605: the five classes including normal ECG (NORM), conduction future.
L606: disturbance (CD), hypertrophy (HYP), myocardial infarction b) SimCLR [29]: SimCLR is a contrastive learning
L607: (MI), and ST/T change (STTC). method first designed for image data. It constructs positive
L608: b) HAR [49]: HAR is a human activity recognition pairs and negative pairs by conducting different data augmen-
L609: dataset with 10 299 9-variable time series with a length of tation methods. We replace the original encoder architecture
L610: 128 from 30 individuals. The data are sampled from the with our encoder for a fair comparison. Also, we use the same
L611: accelerometer and gyroscope with a sampling rate of 50 Hz. augmentations as previous work [52] for time series. The same
L612: Our task is to classify time series into one of the six classes of data with two data augmentation methods form positive pairs,
L613: daily activity, including walking, walking upstairs, downstairs, and the other pairs are negative pairs. The self-supervised
L614: standing, sitting, and lying down. learning task is to maximize the similarity of positive pairs and
L615: c) Sleep-EDF [48], [50]: Sleep-EDF is built for sleep minimize the similarity of negative pairs in the latent space.
L616: stage classification. We use data from four subjects in their c) Temporal and Contextual Contrasting [17]: TS-TCC
L617: normal daily life recorded by a modified cassette tape recorder. is a self-supervised learning method for time series data.
L618: With a sampling rate of 100 Hz, we choose three channels: Similar to SimCLR, it transforms the raw time series data
L619: horizontal EOG, FpzCz, and PzOz EEG. Each recording is a into two views by using weak and strong augmentations. The
L620: 24-h time series, and we cut them into 30-s segments. Our task task is a combination of a cross-view prediction task and a
L621: is to classify time series into one of the eight classes including contrastive task. The contrastive learning task maximizes the
L622: wake, sleep stage 1–4, rapid eye movement, movement, and similarity among different views of the same sample while
L623: unscored. The overview of our adopted datasets is shown in minimizing similarity among views of different samples.
L624: Table I. d) Temporal Neighborhood Coding [13]: TNC is also
L625: All three datasets are randomly split into three parts, training a contrastive learning method for time series data. It utilizes
L626: set (80%), validation set (10%), and test set (10%). In real- the stationary properties of time series data. Similar to SRL,
L627: world scenarios, unlabeled data is much more common than TNC also constructs positive pairs using near segments, and
L628: labeled data. To better simulate this situation, we use the constructs negative pairs using far segments.
L629: whole training set to pretrain, and randomly select 20% of e) Time Series Transformer (TST) [23]: TST is a
L630: the training set to fine-tune the pretrained model. self-supervised learning method for time series data by
L631: 2) Model Architecture: Our framework is an auto-encoder reconstructing the masked parts of original time series data.
L632: architecture, which is composed of an encoder and a decoder. Different from our method, it neglects the frequency domain
L633: Our encoder is based on a deeper Transformer (which is a six- and masks the original data by setting the value as 0, which
L634: layer Transformer), and we add CNNs before the Transformer causes a large gap between the pretraining and fine-tuning.
L635: as the local feature extractors. The CNN employed in our For fair comparisons, we implement these methods using
L636: experiment is a 1-D ResNet-18 architecture [51]. Like the public code with the same encoder architectures as the original
L637: recent work [40], our decoder is a shallower Transformer work (except SimCLR). The models are optimized using
L638: (which has only two layers), because a lighter decoder can Adam [53]. The representation dimensions are all set to 256,
L639: Authorized licensed use limited to: University of Science & Technology of China. Downloaded on July 05,2026 at 10:01:34 UTC from IEEE Xplore. Restrictions apply.
L641: ===== PAGE 7 =====
L643: ZHANG et al.: SELF-SUPERVISED TIME SERIES REPRESENTATION LEARNING VIA CRT 16135
L644: the same as ours. All experiments are conducted on a server TABLE III
L645: with five NVIDIA GeForce RTX 3090ti GPUs. COMPARISON BETWEEN BASELINE METHODS AND OUR METHOD. THE
L646: 5) Evaluations: Linear probing is a popular method to eval- VALUE BEFORE ± IS THE MEAN VALUE OF MULTIPLE-TIME RUNS,
L647: AND THE VALUE AFTER ± IS THE STANDARD DEVIATION
L648: uate the self-supervised learning method. However, it restricts
L649: the ability of deep learning since it cannot pursue stronger
L650: and dataset-specific representations. Hence, we add a two-
L651: layer fully connected neural network as the classifier after
L652: the Transformer encoder and fine-tune the whole model. The
L653: validation set is used to tune the hyper-parameters (such as
L654: beta in L, batch size and learning rate) in fine-tuning stage,
L655: and the model reaching the highest accuracy on the validation
L656: set is saved and evaluated on the test set.
L657: In the self-supervised learning stage, we randomly choose
L658: five seeds and get five pretrained models. In the fine-tuning
L659: stage, we also randomly use five seeds to fine-tune each of
L660: the five pretrained models. Thus, we get 25 results per self-
L661: supervised learning method per dataset.
L662: We use ROC-AUC, F1-Score, and Accuracy to evaluate the
L663: methods. ROC-AUC is defined as the area surrounded by the
L664: receiver operator characteristic curve (ROC curve), the x-axis,
L665: and the y-axis. Regarding the ROC curve, it is first computed
L666: based on the predicted probability and ground truth of each
L667: label directly without a predefined threshold, then defined as
L668: the curve of the true positive rate versus the false positive rate
L669: at various thresholds ranging from zero to one. Accuracy is
L670: calculated for each class, as the ratio of the number of correctly
L671: classified samples over the total number of samples. F1 score Fig. 5. Performance on three datasets when data is dropped or masked during
L672: the pretraining stage. (a) PTB-XL. (b) HAR. (c) Sleep-EDF.
L673: is the harmonic average of precision (the proportion of true
L674: positive cases among the predicted positive cases) and recall
L675: (the proportion of positive cases that are correctly identified).
L676: As a multiclass classification task, we report average ROC-
L677: AUC values across all classes, average Accuracy values across
L678: all classes, and macro averaged F1 score. Reported numbers
L679: are expressed in percentage values for better reading.
L680: Fig. 6. Performance on three datasets with and without phase. (a) PTB-XL.
L681: B. Comparison Results
L682: (b) HAR. (c) Sleep-EDF.
L683: We compare our CRT with baseline methods and show
L684: the results in Table III. Our CRT outperforms all baselines
L685: fine-tuning than masking, we compare the results on down-
L686: in terms of ROC-AUC, F1-score, and accuracy. We also
L687: stream tasks under the two setups. From Fig. 5, we see
L688: observe that the results of CRT have a relatively small stan-
L689: dropping always leads to better downstream performances,
L690: dard deviation, which implies a more stable performance on
L691: except for the Sleep-EDF dataset, where dropping yields a
L692: downstream tasks. In addition, we notice that TST (another
L693: slightly lower ROC-AUC but outperforms masking for other
L694: reconstruction-based self-supervised learning method) also
L695: metrics. This is because zeros brought by masking may create
L696: obtains a relatively small standard deviation. The reason
L697: wrong patterns for time series data, and dropping can tackle
L698: might be that reconstruction tasks do not require constructing
L699: this problem. Our dropping approach can keep the shape of the
L700: negative and positive pairs, which is difficult and may cause
L701: original time series, and reduce the gap between the pretraining
L702: instability. It indicates that reconstruction-based methods may
L703: and fine-tuning phases caused by the masking process.
L704: provide a more stable way for self-supervised learning. One
L705: 2) Adding Phase Helps Frequency Learning: We also con-
L706: baseline named Scalable Representation Learning [12] is not
L707: duct a simple ablation study to support that phase can provide
L708: included in our results, as it requires a much longer running
L709: supplementary spectral information. We evaluate the model
L710: time and we failed to produce its results in several days.
L711: pretrained and fine-tuned with and without phase data under
L712: the same experimental setups as our CRT. The results on three
L713: C. Analysis of Cross-Domain Reconstruction
L714: datasets with and without phase data are shown in Fig. 6.
L715: More ablation studies and comparison experiments are We can see that adding the phase can help improve the final
L716: conducted to further verify the effectiveness of our method. performance in terms of three metrics. This supports our view
L717: 1) Dropping Is Better Than Masking: To verify that drop- that magnitude is not informative enough to represent the
L718: ping can better alleviate the gap between pretraining and frequency domain, and phase can complement magnitude.
L719: Authorized licensed use limited to: University of Science & Technology of China. Downloaded on July 05,2026 at 10:01:34 UTC from IEEE Xplore. Restrictions apply.
L721: ===== PAGE 8 =====
L723: 16136 IEEE TRANSACTIONS ON NEURAL NETWORKS AND LEARNING SYSTEMS, VOL. 35, NO. 11, NOVEMBER 2024
L724: TABLE IV
L725: COMPARISON OF CROSS-DOMAIN AND SINGLE-DOMAIN. TIME REP-
L726: RESENTS TIME-TO-TIME RECONSTRUCTION AND FREQ REPRESENTS
L727: FREQUENCY-TO-FREQUENCY RECONSTRUCTION
L728: Fig. 8. Performance of three cross-domain reconstruction methods. (a)
L729: ROC-AUC of all five classes on PTB-XL. (b) Accuracy on Sleep-EDF when
L730: the ratio of the training set used for fine-tuning is 0.2, 0.4, 0.6, and 0.8.
L731: TABLE V
L732: COMPARISONS OF THREE KINDS OF CROSS-DOMAIN RECONSTRUC-
L733: TION. T2F REPRESENTS TIME-TO-FREQUENCY AND F2T REPRESENTS
L734: FREQUENCY-TO-TIME
L735: Fig. 7. Performance when using time domain, frequency domain, and both
L736: domains. (a) ROC-AUC of all five classes on PTB-XL. (b) Accuracy on
L737: Sleep-EDF when the ratio of the training set used for fine-tuning is 0.2, 0.4,
L738: 0.6, and 0.8.
L739: 3) Cross-Domain Is Better Than Single-Domain: We com-
L740: pare our method with the trivial single-domain reconstruction
L741: tasks. After conducting time-domain and frequency-domain
L742: Fig. 9. Performance on three datasets with and without CL. (a) PTB-XL.
L743: (phase and magnitude) reconstruction tasks respectively,
L744: (b) HAR. (c) Sleep-EDF.
L745: we fine-tune the models using the corresponding domain’s
L746: data. As shown in Table IV, CRT performs best in terms a) Time-to-Frequency Reconstruction (T2F): with only
L747: of all 3 metrics. The ROC-AUCs of all five classes on the time-domain part of E fed into the Transformer encoder,
L748: PTB-XL datasets are shown in Fig. 7(a). We can see that we use the encoded features to reconstruct the dropped original
L749: cross-domain representations help improve performance in all frequency-domain data (including phase and magnitude).
L750: classes. This is because some abnormalities of ECGs can be b) Frequency-to-Time Reconstruction (F2T): contrary to
L751: more easily observed from the perspective of the frequency T2F, we input the frequency-domain part of E and reconstruct
L752: domain. Fig. 7(b) shows the performance on the Sleep-EDF the dropped time-domain data. We used the same inputs for
L753: dataset under different training sizes. We give the results when fine-tuning to only evaluate the cross-reconstruction tasks.
L754: 20%, 40%, 60%, and 80% of the training set is used for fine- As shown in Table V, our complete cross-domain solution
L755: tuning. The results show that by combining two domains, our outperforms the other two methods on three datasets. We also
L756: cross-domain representations can yield higher accuracy under give the results of all five classes on the PTB-XL dataset
L757: different ratios. [Fig. 8(a)], and the accuracy on the Sleep-EDF dataset under
L758: All results support our hypothesis that learning from two four training set ratios [Fig. 8(b)]. From Fig. 8(a), we can
L759: domains can yield more informative representations than from see CRT outperforms others on all classes, especially on
L760: a single domain. This is because some patterns of the fre- “MI” (11.6% higher than F2T and 4.7% higher than T2F).
L761: quency domain can complement the temporal patterns. Also, In Fig. 8(b), CRT also performs better, and T2F performs
L762: the cross-domain Transformer encoder can fuse different types similar to F2T.
L763: of features, and extract useful and complementary patterns Our CRT adopts Transformer as part of our encoder to fuse
L764: from both domains. the embeddings from different domains. The representations
L765: In addition, we notice that in all three datasets, using the obtained from the Transformer encoder contain information of
L766: time domain yields better performance compared with using both time domain and frequency domain, which benefits the
L767: the frequency domain. This may be because the patterns reconstruction as well as the downstream tasks. T2F and F2T,
L768: of the time domain are more direct for neural networks to on the other hand, only capture a single-direction relationship
L769: discover, and the three classification tasks are strongly related rather than a mutual relationship. It is intuitive that CRT can
L770: to these patterns. However, adding the frequency domain can produce more semantic representations, and the experiment
L771: supplement some patterns, leading to better performance. results will prove it.
L772: 4) Exploring Cross-Domain Learning: We explore cross- 5) CL and IDC Help Learning Cross-Domain Represen-
L773: domain learning with two experiments: tations: We conduct another ablation study to verify the
L774: Authorized licensed use limited to: University of Science & Technology of China. Downloaded on July 05,2026 at 10:01:34 UTC from IEEE Xplore. Restrictions apply.
L776: ===== PAGE 9 =====
L778: ZHANG et al.: SELF-SUPERVISED TIME SERIES REPRESENTATION LEARNING VIA CRT 16137
L779: of our framework. For future work, we would adapt our
L780: framework to the out-of-distribution scenarios and address
L781: more challenging problems [54].
L782: REFERENCES
L783: Fig. 10. Performance on three datasets with and without IDC. (a) PTB-XL.
L784: (b) HAR. (c) Sleep-EDF. [1] Q. Tan et al., “Explainable uncertainty-aware convolutional recurrent
L785: neural network for irregular medical time series,” IEEE Trans. Neural
L786: Netw. Learn. Syst., vol. 32, no. 10, pp. 4665–4679, Oct. 2021.
L787: [2] F. M. Bianchi, S. Scardapane, S. Løkse, and R. Jenssen, “Reservoir
L788: computing approaches for representation and classification of multivari-
L789: ate time series,” IEEE Trans. Neural Netw. Learn. Syst., vol. 32, no. 5,
L790: pp. 2169–2179, May 2021.
L791: [3] Y. Huang, G. G. Yen, and V. S. Tseng, “Snippet policy network V2:
L792: Knee-guided neuroevolution for multi-lead ECG early classification,”
L793: IEEE Trans. Neural Netw. Learn. Syst., early access, Jul. 11, 2022, doi:
L794: 10.1109/TNNLS.2022.3187741.
L795: [4] T. Bradde, G. Fracastoro, and G. C. Calafiore, “Multiclass sparse
L796: centroids with application to fast time series classification,” IEEE
L797: Trans. Neural Netw. Learn. Syst., early access, Nov. 12, 2021, doi:
L798: 10.1109/TNNLS.2021.3124300.
L799: Fig. 11. (a) Three reconstructed cases (the “Reconstructed” row) from
L800: [5] W. Zheng and J. Hu, “Multivariate time series prediction based
L801: PTB-XL, (b) HAR, and (c) Sleep-EDF. “Original” represents the original time
L802: on temporal change information learning method,” IEEE Trans.
L803: series, and “Dropped input” represents the time series after being dropped.
L804: Neural Netw. Learn. Syst., early access, Jan. 4, 2022, doi:
L805: 10.1109/TNNLS.2021.3137178.
L806: effectiveness of CL and IDC, and show the results in [6] K. Bandara, C. Bergmeir, and H. Hewamalage, “LSTM-MSNet: Lever-
L807: aging forecasts on sets of related time series with multiple seasonal
L808: Figs. 9 and 10.
L809: patterns,” IEEE Trans. Neural Netw. Learn. Syst., vol. 32, no. 4,
L810: As we expect, these two modules facilitate learning cross- pp. 1586–1599, Apr. 2021.
L811: domain representations. CL helps the reconstruction tasks and [7] A. Garg, W. Zhang, J. Samaran, R. Savitha, and C. Foo, “An evalu-
L812: ation of anomaly detection and diagnosis in multivariate time series,”
L813: improves the performance on downstream tasks. CL gives a
L814: IEEE Trans. Neural Netw. Learn. Syst., vol. 33, no. 6, pp. 2508–2517,
L815: progressively increasing dropping ratio rather than a constant Jun. 2022.
L816: large dropping ratio, which helps better reconstruct the original [8] S. Benkabou, K. Benabdeslem, V. Kraus, K. Bourhis, and B. Canitia,
L817: “Local anomaly detection for multivariate time series by temporal
L818: data. As a regularization, IDC minimizes the mutual infor-
L819: dependency based on Poisson model,” IEEE Trans. Neural Netw. Learn.
L820: mation between different samples which helps Transformer Syst., vol. 33, no. 11, pp. 6701–6711, Nov. 2022.
L821: extract more discriminable patterns. It is worth noting that [9] Q. Chen, A. Zhang, T. Huang, Q. He, and Y. Song, “Imbalanced dataset-
L822: IDC is not a contrastive loss, since it does not minimize the based echo state networks for anomaly detection,” Neural Comput. Appl.,
L823: vol. 32, no. 8, pp. 3685–3694, Apr. 2020.
L824: distance of any pair of samples. It only minimizes common
L825: [10] A. Hyvarinen and H. Morioka, “Unsupervised feature extraction by
L826: information of all time series. time-contrastive learning and nonlinear ICA,” in Proc. Adv. Neural Inf.
L827: In Fig. 11, we illustrate three reconstructed cases with a Process. Syst., vol. 29, 2016, pp. 1–9.
L828: 0.7 dropping ratio. We see that the model almost reconstructs [11] X. Lan, D. Ng, S. Hong, and M. Feng, “Intra-inter subject
L829: self-supervised learning for multivariate cardiac signals,” 2021,
L830: the trend of dropped inputs with such a high dropping ratio,
L831: arXiv:2109.08908.
L832: especially for the ECG case from the PTB-XL dataset. The [12] J.-Y. Franceschi, A. Dieuleveut, and M. Jaggi, “Unsupervised scalable
L833: reason for the well-performed ECG reconstruction might be representation learning for multivariate time series,” in Proc. Adv. Neural
L834: Inf. Process. Syst., vol. 32, 2019, pp. 1–12.
L835: because ECG is periodic and there are abundant similar
L836: [13] S. Tonekaboni, D. Eytan, and A. Goldenberg, “Unsupervised representa-
L837: patterns in the time series. Such amazing reconstruction per- tion learning for time series with temporal neighborhood coding,” 2021,
L838: formance also proves that our cross-domain representations arXiv:2106.00750.
L839: [14] L. Yang and S. Hong, “Unsupervised time-series representation learning
L840: are highly informative and sample-specific.
L841: with iterative bilinear temporal-spectral fusion,” in Proc. Int. Conf.
L842: Mach. Learn., 2022, pp. 25038–25054.
L843: V. CONCLUSION [15] A. van den Oord, Y. Li, and O. Vinyals, “Representation learning with
```

## Sparsity-Constrained_Invariant_Risk_Minimization_for_Domain_Generalization_With_Application_t.txt
- Total extracted lines: 1101

### Lines 1-120

```text
L3: ===== PAGE 1 =====
L5: IEEE TRANSACTIONS ON CYBERNETICS, VOL. 54, NO. 3, MARCH 2024 1547
L6: Sparsity-Constrained Invariant Risk Minimization
L7: for Domain Generalization With Application to
L8: Machinery Fault Diagnosis Modeling
L9: Zhenling Mo , Zijun Zhang , Senior Member, IEEE, Qiang Miao , Senior Member, IEEE,
L10: and Kwok-Leung Tsui
L11: Abstract—Machine learning has been widely applied to study models with good adaptiveness to operating condition changes
L12: AI-informed machinery fault diagnosis. This work proposes is of great importance for enhancing the safety and reliability
L13: a sparsity-constrained invariant risk minimization (SCIRM)
L14: of machinery systems.
L15: framework, which develops machine-learning models with bet-
L16: In the past, machine-learning models were mainly trained
L17: ter generalization capacities for environmental disturbances in
L18: machinery fault diagnosis. The SCIRM is built by innovating via empirical risk minimization (ERM). Its performance
L19: the optimization formulation of the recently proposed invariant guarantee requires adhering to the assumption that the data are
L20: risk minimization (IRM) and its variants through the integration independent and identically distributed (IID) [2]. However,
L21: of sparsity constraints. We prove that if a sparsity measure is
L22: data collected under changing working conditions do not com-
L23: differentiable, scale invariant, and semistrictly quasi-convex, the
L24: ply with the IID assumption. Therefore, machine-learning
L25: SCIRM can be guaranteed to solve the domain generalization
L26: problem based on a few predefined problem settings. We mathe- models developed by ERM may generalize poorly in real
L27: matically derive a family of such sparsity measures. A practical machinery fault diagnosis tasks.
L28: process of implementing the SCIRM for machinery fault diag- Numerous research attempts have been made in the past
L29: nosis tasks is offered. We first verify our theoretical exploration
L30: to deal with modeling under data-label joint distribution dis-
L31: of the SCIRM by using simulation data. We further compare
L32: crepancies among various machine working environments to
L33: SCIRM with a set of state-of-the-art methods by using real
L34: machinery fault data collected under a variety of working condi- enable better model out-of-distribution (OOD) generalizations.
L35: tions. The computational results confirm that the machinery fault One prevalent stream of methods is based on transfer learning
L36: diagnosis model developed by the SCIRM offers a higher general- and domain adaptation [3]. To apply those types of methods,
L37: ization capacity and performs better than the other benchmarks
L38: a pretrained model and the target-domain data need to be avail-
L39: across the different testing datasets.
L40: able. For example, in [4], a deep joint distribution alignment
L41: Index Terms—Causal learning, fault diagnosis, model general- method was proposed to align data distributions caused by
L42: ization, risk minimization, sparsity measure.
L43: different machine working conditions. In [5], a refined adver-
L44: sarial adaptation and classifier complementation approach was
L45: I. INTRODUCTION developed to deal with domain and category discrepancies for
L46: MACHINE learning for machinery fault diagnosis has industrial fault diagnosis. To effectively transfer knowledge for
L47: been vigorously discussed due to sensor advancements multidomain fault diagnosis, a dual-channel feature network and
L48: and the availability of data [1]. Rotational machines often have relation network were constructed to process the source-domain
L49: a variety of working conditions, for example, various loads and target-domain signals [6]. Compared with the existing stud-
L50: or speeds. Thus, studying machine-learning fault diagnosis ies [4], [5], [6], this work attempts to innovate machine learning
L51: for developing novel fault diagnosis models from a domain gen-
L52: Manuscript received 18 September 2022; revised 1 November 2022; eralization aspect. The importance and benefits of developing
L53: accepted 17 November 2022. Date of publication 8 December 2022; date models that work with data with different distributions due to the
L54: of current version 16 February 2024. This work was supported in part by the
L55: working environments have been discussed in [7]. Compared
L56: National Natural Science Foundation of China through Youth Scientist Fund
L57: Project under Grant 52007160; in part by the Hong Kong Research Grants with the works in [4], [5], and [6], domain generalization is free
L58: Council General Research Fund Project under Grant 11204419; in part by the of pretrained models and target-domain data. Different types
L59: CityU HK Strategic Research Grant under Grant 7005692; and in part by the
L60: of domain generalization techniques have been presented in
L61: InnoHK initiative, The Government of the HKSAR, and Laboratory for AI-
L62: Powered Financial Technologies. This article was recommended by Associate recent years. One popular attempt was devoted to studying the
L63: Editor J. Q. Gan. (Corresponding author: Zijun Zhang.) interpolation/extrapolation of features/losses, for example, the
L64: Zhenling Mo and Zijun Zhang are with the School of Data Science,
L65: intrinsic and extrinsic losses [8], the interdomain Mixup [9],
L66: City University of Hong Kong, Hong Kong, SAR, and also with City
L67: University of Hong Kong Shenzhen Research Institute, Shenzhen, China and the variance risk extrapolation [10]. In addition to inter-
L68: (e-mail: zijzhang@cityu.edu.hk). polation or extrapolation methods, a few studies have explored
L69: Qiang Miao is with the College of Electrical Engineering, Sichuan
L70: different mask mechanisms to encourage the learning of more
L71: University, Chengdu 610017, Sichuan, China.
L72: Kwok-Leung Tsui is with the Grado Department of Industrial and Systems generalized models, for example, the sparse mask [11], AND
L73: Engineering, Virginia Tech, Blacksburg, VA 24061 USA. mask [12], and SAND mask [13]. The dynamic system theory,
L74: Color versions of one or more figures in this article are available at
L75: robust optimization, and causal inference have also been adapted
L76: https://doi.org/10.1109/TCYB.2022.3223783.
L77: Digital Object Identifier 10.1109/TCYB.2022.3223783 to develop domain generalizability models. Pezeshki et al. [14]
L78: 2168-2267 (cid:2)c 2022 IEEE. Personal use is permitted, but republication/redistribution requires IEEE permission.
L79: See https://www.ieee.org/publications/rights/index.html for more information.
L80: Authorized licensed use limited to: University of Science & Technology of China. Downloaded on July 05,2026 at 10:04:03 UTC from IEEE Xplore. Restrictions apply.
L82: ===== PAGE 2 =====
L84: 1548 IEEE TRANSACTIONS ON CYBERNETICS, VOL. 54, NO. 3, MARCH 2024
L85: utilized the dynamical system theory to study gradient starva- fault diagnosis models with domain generalization
L86: tion, which is a phenomenon hindering model robustness and capabilities.
L87: generalization. Sagawa et al. [15] applied distributional robust 2) Theoretical Exploration: In the proposed SCIRM, we
L88: optimization to promote model generalizability. Peters et al. [16] discover that the differentiability, scale invariance,
L89: leveraged ideas from causal inference to develop the causal and semistrictly quasi-convexity are the key proper-
L90: invariance prediction method, which was a milestone for ties needed by the sparsity measures to enable OOD
L91: causality-inspired domain generalization. Our work aims to generalization.
L92: establish additional models based on causality-inspired meth- 3) Theoretical Development: We prove that a family of
L93: ods. These studies typically consider the assumption that the sparsity measures, the p-q mean family, with p ≤ 1,
L94: conditional distribution of the variable of interest, given all its q ≥ 1, and p (cid:5)= q, have the desired properties. We
L95: direct causes, is invariant [16]. This assumption is consistent theoretically show that the proposed SCIRM can tackle
L96: with the real-world observation that the causal mechanism is the OOD issue if the data satisfy the proposed struc-
L97: intact when intervening on the causes. Essentially, a supervised tural equation model and the invariant features are
L98: machine-learning model tries to learn a conditional distribution bounded, strictly separable and satisfy support over-
L99: of targets given observations as a way of prediction [18]. Thus, laps. Meanwhile, the developed theory is also validated
L100: the direct causes can elicit an invariant predictor (the condi- via simulation data.
L101: tional distribution), which is not influenced by distributional 4) Application Development: The proposed SCIRM facil-
L102: shifts of data. In other words, finding the direct causes of the itates machine learning to develop machinery fault
L103: target variable is the key to solving the OOD problem, which diagnosis models with improved diagnosis accuracies
L104: then enhances the domain generalization when modeling with under different working conditions. The advantages of
L105: machine-learning techniques. SCIRM are verified by benchmarking against a set of
L106: One direction of causality inspired learning attempts to map state-of-the-art methods under extensive generalization
L107: observations to representations in latent space to approximate tasks designed using bearing and gearbox data col-
L108: the direct causes of the target variable [19]. Invariant risk lected under different working conditions. On average,
L109: minimization (IRM) [20] is one of the causality-inspired learn- the proposed SCIRM outperforms the benchmarking
L110: ing methods and has attracted much attention in recent years. modeling methods.
L111: Arjovsky et al. [20] showed that the IRM has a theoretical Theremainderofthisarticleisorganizedasfollows. SectionII
L112: guarantee of solving OOD problems under linear regression outlines the preliminaries of this article. Section III introduces
L113: settings and can offer a strong empirical performance under the proposed framework. Section IV presents the experimental
L114: some linear classification settings. Inspired by information studies. Section V provides further discussions and validations.
L115: bottleneck theory, Ahuja et al. [21] exploited entropy as an Finally, Section VI summarizes the key conclusions.
L116: additional measure, and built the information bottleneck-based
L117: IRM (IBIRM) to fill the theoretical vacancy in the linear classi- II. PRELIMINARIES
L118: fication settings. However, the indirect calculation of entropy,
L119: In this section, we first define the OOD problem targeted in
L120: and the weight determination problems of IBIRM may not
```

### Lines 236-432

```text
L236: 1 We start with the definition of some notations. Let S be
L237: Re((cid:4) ◦ (cid:3)) ≤ r ∗ (4)
L238: the (standard) sparsity measure, which means that the larger
L239: N
L240: e∈ε
L241: train values indicate sparser states. Let S
L242: ↓
L243: be the reverse sparsity
L244: where N is the number of training environments, He(·) is the measure, which is the negative of the standard sparsity mea-
L245: entropy measure, r ∗ is the risk given by the optimal predic- sure, namely, S ↓ = −S ↑ . Thus, smaller values of S ↓ indicate
L246: tor, and the other notations are the same as (2). The entropy sparser states. Let X, Y ∈ (cid:9) ⊆ Rn + , n > 1 and S ↑(X) (cid:5)= S ↑(Y).
L247: measure mainly considered is the differential entropy. For In other words, we have the positive inputs X and Y defined
L248: Authorized licensed use limited to: University of Science & Technology of China. Downloaded on July 05,2026 at 10:04:03 UTC from IEEE Xplore. Restrictions apply.
L250: ===== PAGE 4 =====
L252: 1550 IEEE TRANSACTIONS ON CYBERNETICS, VOL. 54, NO. 3, MARCH 2024
L253: on the convex set (cid:9), a subset of Rn + with n > 1. We only B. Structural Equation Model
L254: consider the positive inputs. For the negative inputs, we can
L255: In the causal inference literature, the structural equation
L256: simply employ the absolute values. The inputs should not be
L257: model is usually utilized to describe the causal relations among
L258: all zeros but our theory can possibly be extended to inputs
L259: the different variables [17]. In particular, we assume that
L260: having at least one nonzero element. In addition, the sparsity
L261: our data of all environments satisfy the following structural
L262: of X and Y should be different.
L263: equation model.
L264: With the notations above, we formally define the scale
L265: Assumption 1 (Structural Equation Model): For each envi-
L266: invariance and semistrict quasi-convexity for the sparsity ronment e ∈ ε
L267: all
L268: measures as follows. (cid:8) (cid:9)
L269: 1
L270: Definition 1 (Scale-Invariance): For the standard sparsity Ne ← Bernoulli(q), q < , Ne⊥ Ze , Ze (10)
L271: measure S ↑ and variable X ∈ (cid:9) ⊆ Rn + , n > 1, S ↑ is called (cid:10) (cid:10) (cid:11)(cid:11) 2 inv spu
L272: scale-invariant if Le ← I (cid:12) W inv · Z i e nv ⊕ Ne (11)
L273: Ze ← AZe + Ne (12)
L274: spu inv (cid:8)spu (cid:9)
L275: S ↑(X) = S ↑(ρX), ρ ∈ R1 + . (6) Oe ← (cid:3)∗−1 ◦ T Z i e nv , Z s e pu (13)
L276: Definition 2 (Semistrictly Quasi-Convex): For the standard where ← denotes a single direction assignment from the
L277: sparsity measure S ↑ and variables X, Y ∈ (cid:9) ⊆ Rn + , n > 1, cause variables to the effect variable; Ne is the label noise;
L278: and, S ↑ is called semistrictly quasi-convex if Bernoulli(q) is the Bernoulli distribution returning a value 1
L279: (cid:5) (cid:6) with probability q; Le is the observational label; I(·) is the
L280: S ↑(αX + (1 − α)Y) < max S ↑(X), S ↑(Y) , α ∈ (0, 1). (7) indicator function, which returns value 1 if the input is non-
L281: negative and 0 otherwise; (cid:12)(·) is an intermediate prediction
L282: Now, we can deliver our first lemma as shown next. mapping (cid:12): Rk → R; (cid:3)∗−1(·) is the inverse feature map-
L283: Lemma 1: If the sparsity measure is scale-invariant and ping; W ∈ Rk×n is the invariant coefficient; Ze ∈ Rn×1
L284: inv inv
L285: semistrictly quasi-convex, we have the following two is the non-Gaussian invariant feature, and usually, B · Ze is
L286: inv
L287: inequalities: also non-Gaussian, where B ∈ Rk×n; ⊕ represents the XOR
L288: (cid:5) (cid:6) operation; and Ze ∈ Rm×1 stands for the spurious features
L289: S ↑(X + Y) < max S ↑(X), S ↑(Y) . (8) and Ne ∈ Rm× s 1 pu is the corresponding noise (bounded and
L290: spu
L291: with zero mean). Particularly, we require that Ze ⊥ Ne and
L292: Or equivalently S ↑(B · Ze ) (cid:5)= S ↑(B (cid:11) · Ne ), where B (cid:11) ∈ Rk×m. i T nv ∈ Rn+ sp m u and
L293: (cid:5) (cid:6) inv spu
L294: S ↓(X + Y) > max S ↓(X), S ↓(Y) . (9) A ∈ Rm×n are transformation matrices; T is invertible, A is
L295: nonzero, and [Ze , Ze ] is the concatenation of the invariant
L296: inv spu
L297: feature and the spurious feature.
L298: Thus far, we have merely made assumptions about the
L299: Ideally, the informative feature can be obtained from the
L300: desired sparsity measure. The next task is to find such sparsity
L301: bijective feature mapping (cid:3)∗(·) with (cid:3)∗ ◦ Oe = T[Ze , Ze ].
L302: measures that satisfy our assumptions. inv spu
L303: In addition, Ze is supposed to be non-Gaussian such that
L304: To search for the desired sparsity measure, we exploit the inv
L305: (12) is causally identifiable [25]. If Ne is Gaussian, the affine
L306: following proposition and corollary. spu
L307: Proposition 1: Let Z(X) = −[F(X)/G(X)] be the negative transformation B (cid:11) · N s e pu is often Gaussian as well. Then, B ·
L308: ratio of two positive functions, F(X) and G(X), defined on the Z i e nv and B (cid:11) · N s e pu can have different values of sparsity [26].
L309: convex set (cid:9) ⊆ Rn +. If F(X) is concave and G(X) is convex, In practice, we rely on a neural network to map the data to
L310: Z(X) is semistrictly quasi-convex. the data manifold, approximately satisfying this assumption.
L311: Corollary 1: Let Z(X) = −[(cid:16)X(cid:7) (cid:16)
L312: p
L313: /(cid:16)X(cid:16)
L314: q
L315: ] be the negative Finally, the binary case is merely employed to facilitate the
L316: ra(cid:7)tio of two functions (cid:16)X(cid:16)
L317: p
L318: = ( n
L319: i=1
L320: x
L321: i
L322: p)1/p and (cid:16)X(cid:16)
L323: q
L324: = proofs. It can possibly be generalized to multiclass problems.
L325: ( n
L326: i=1
L327: x
L328: i
L329: q)1/q defined on convex set (cid:9) ⊆ Rn +. If 0 < p ≤ 1,
L330: q ≥ 1, and p (cid:5)= q, then Z(X) is semistrictly quasi-convex. C. Sparsity-Constrained Invariant Risk Minimization
L331: Based on Proposition 1 or Corollary 1, we present our sec-
L332: 1) Optimization Problem: We propose the following
L333: ond lemma, which gives one example of the desired sparsity
L334: optimization problem as shown in (14) based on extending
L335: measure.
L336: the IRM and IBIRM formulations:
L337: Lemma 2: Let S ↑(X) = −[(cid:16)X(cid:16) /(cid:16)X(cid:16) ] be the negative
L338: L1 L2 (cid:3)
L339: 1
L340: ratio of the L1 norm and L2 norm defined on convex set min S ↓e((cid:3))
L341: (cid:9) ⊆ Rn +. Then, S ↑(X) satisfies (8), or equivalently, S ↓(X) (cid:4) ∈ (cid:5) N e∈ε
L342: train
L343: satisfies (9). (cid:3) ∈ (cid:6)
L344: Finally, it should be mentioned that the differentiability, subject to (cid:4) ∈ arg min Re((cid:4) ◦ (cid:3))
L345: scale invariance, and semistrict quasi-convexity are the mini- (cid:4)(cid:11) ∈ (cid:5)
L346: mal requirements for the sparsity measures to be considered. ∀e ∈ ε
L347: train
L348: To tackle complicated real-world data, more properties, such (cid:3)
L349: 1
L350: as the robustness to outliers, are also favored and thus worthy Re((cid:4) ◦ (cid:3)) ≤ r ∗ (14)
L351: of investigation in future work. N e∈ε
L352: train
L353: Authorized licensed use limited to: University of Science & Technology of China. Downloaded on July 05,2026 at 10:04:03 UTC from IEEE Xplore. Restrictions apply.
L355: ===== PAGE 5 =====
L357: MO et al.: SCIRM FOR DOMAIN GENERALIZATION 1551
L358: where S ↓ is the reverse sparsity measure, (cid:3) is the feature map- follows:
L359: ping defined in function space (cid:6), (cid:4) is the prediction mapping (cid:3)3
L360: defined in function space (cid:5), ◦ denotes function composition, ζe = θe(cid:16)e (16)
L361: the function we want to learn in OOD is f = (cid:4) ◦ (cid:3), N is the SCIR i i
L362: i=1
L363: number of training environments ε train and r ∗ is the risk given 1 (cid:3)
L364: by the optimal predictor. ζ SCIR = N ζ S e IR (17)
L365: Based on the structural equation model, the optimal predic-
L366: e∈ε
L367: train
L368: tor is the labeling hyperplane, and it achieves a risk of q in where (cid:16)e is the loss ratio and N is the number of training
L369: i
L370: each environment. Formally, we have the following lemma. environments. For convenience, we ignore the environmental
L371: Lemma 3: If data collected from all environments satisfy variable e in the subsequent formulations. For loss ζ at time
L372: i
L373: the structural equation model (Assumption 1), the labeling step t, the loss ratio (cid:16)t is defined by the current loss over the
L374: hyperplane (cid:4)∗ = I ◦ (cid:12)([W inv , 0]T −1(cid:3)∗(Oe)) solves the OOD mean loss up to t − 1 i as follows:
L375: problem described in (1) and attains a risk of q in each
L376: ζt
L377: environment. (cid:16)t = i . (18)
L378: i μt−1
L379: The following theorem states our main results on the OOD ζ
L380: i
L381: problem.
L382: ↑ The coefficient of variation (cid:16)t at time step t can be defined as
L383: Theorem 1: Suppose: 1) the sparsity measure S is dif- i
L384: the normalized relative standard deviation of the loss ratio as
L385: ferentiable, scale-invariant (Definition 1), and semistrictly
L386: follows:
L387: quasi-convex (Definition 2); 2) the data from all environments
L388: σt σt
L389: follow the structural equation model (Assumption 1); and 3) the θt = 1 τt = 1 (cid:16) i = (cid:7) 1 (cid:16) i (19)
L390: invariant features are well behaved (i.e., bounded, strictly sepa- i κt i κt μt 3 τt μt
L391: rable, and domain level support overlapped [21]). The solution (cid:16) i i=1 i (cid:16) i
L392: t 0 o -1 th l e os p s r a o l p s o o se s d olv o e p s tim th i e za O ti O on D p p r r o o b b l l e e m m d d e e s s c c r r i i b b e e d d i i n n ( ( 1 1 4 ). ) with d w e h v e i r a e tio τ n i t i o s f th th e e re lo la s t s iv r e at s i t o a , n μ da t (cid:16) rd is de t v h i e at m io e n a , n σ (cid:16) o t i f is th t e he lo s s t s an r d at a i r o d ,
L393: Although we only obtain access to the training environments and κt is the sum of all the rel i ative standard deviations. Note
L394: in the proposed optimization problem, the theorem says that that the mean μt (cid:16) and standard deviation σ (cid:16) t can be efficiently
L395: i i
L396: once our requirements about the sparsity measure, data, and estimated by Welford’s algorithm [28].
L397: invariant features are met, we can solve the OOD problem The final practical version of the risk function of SCIRM
L398: defined for all environments. The proofs are given in the is defined in (17). By using this version, it is not required to
L399: Appendix. We will also verify Theorem 1 by simulation data. manually set the weights for the empirical loss, the invariance
L400: Finally, the third requirement is equally important to any meth- loss, and the sparsity loss.
L401: ods. The reason is that if it is not satisfied, it can be proven 3) SCIRM-Based Fault Diagnosis Method: Similar to the
L402: that no algorithm can solve the OOD problem [21]. commonly seen ERM, the proposed SCIRM can be leveraged
L403: 2) Practical Version: To obtain a practical risk function of to train machine-learning models, such as a standard convolu-
L404: SCIRM, we can follow the same IRM and IBIRM tricks. First, tional neural network, for fault diagnosis tasks. In this article,
L405: we can use the reparametrization so that the learning task of we borrow a simple 1-D convolutional neural network from
L406: IRM can be assigned to the feature mapping (cid:3) only. Therefore, previous studies [29] to demonstrate the process of applying
L407: the predictor (cid:4) can be as simple as a fixed scalar [20], [21]. the SCIRM to machinery fault diagnosis. The sparsity measure
L408: Next, we consider the Lagrange multiplier method to convert in this example is chosen as the one defined in Lemma 2. The
L409: the constraint problem into an unconstrained problem. Finally, SCIRM-based diagnosis method is illustrated in Fig. 1. The
L410: the practical version of SCIRM can be simplified as follows: diagnosis procedure follows the four steps described next.
L411: (cid:3) (cid:4) (cid:4) (cid:10) (cid:11) Step 1: The observational signals of the different machine
L412: (cid:3) m ∈ i (cid:6) n Re((cid:3)) + λ · (cid:4)∇ (cid:4)|(cid:4)=1.0 Re((cid:4) · (cid:3))(cid:4)2 + β · S ↓e (cid:3)(cid:11) (15) fault types under different working conditions are collected
L413: e∈ε
L414: train and preprocessed, such as normalization. Different fault types
L415: where β is the weight for the reverse sparsity measure S ↓ ; are assigned different labels. However, each working condition
L416: (cid:3) = (cid:12)(cid:11) ◦(cid:3)(cid:11) ; and (cid:3)(cid:11) and (cid:12)(cid:11) are two intermediate feature map- corresponds to one environment. Several training environments
L417: pings. For example, we can employ outputs of certain layers in and the test environment containing different observation-label
L418: the neural networks to compute the reverse sparsity measure. pairs are then obtained.
L419: Then, the layers before the intermediate outputs are repre- Step 2: In the forward propagation of the neural network,
L420: sented by
L421: (cid:3)(cid:11)
L422: , and the layers after the intermediate outputs are the SCIR of each training environment is first calculated based
L423: represented by
L424: (cid:12)(cid:11)
L425: . on (16). Here, the intermediate outputs from the second dense
L426: To facilitate training, we propose to exploit the coeffi- layer (see Fig. 1) are utilized to compute the reverse sparsity.
L427: cient of variation [27] as the adaptive weighting strategy of Afterward, the average SCIR of all training environments is
L428: SCIRM. Let ζe, ζe and ζe be the first, second and third losses computed based on (17).
L429: 1 2 3
L430: (without weights) in (15), respectively. We name ζe empirical Step 3: In the neural-network backpropagation, the gradients
L431: 1
L432: loss, ζe invariance loss and ζe sparsity loss. The corresponding of the average SCIR with respect to the model parameters are
```

### Lines 477-725

```text
L477: where the direct causes reside, and that have different values
L478: of sparsity from the spurious noise, is difficult to simulate.
L479: Fig. 1. Proposed diagnosis method under different environments. Therefore, the simulation model can be regarded as a relaxed
L480: and simplified approximation to Assumption 1.
L481: For simplicity, the pseudo invariant feature of the normal
L482: Step 4: After the model is well trained, it is employed to condition is set to Gaussian. However, the pseudo invariant
L483: classify the different fault types in the test environments. feature of the fault condition is a periodic impulse train, which
L484: We will first verify Theorem 1 using simulation data. Next, is non-Gaussian. One unit of the impulse train is generated in
L485: we benchmark the proposed SCIRM-based diagnosis method the time domain by the vibration system with a single degree
L486: against the ERM-, IRM- and IBIRM-based diagnosis methods of freedom. The modulation frequency is 80 Hz. The damping
L487: using real machinery data. ratio is 0.01. The natural frequency is 5 kHz. We also add
L488: both the 1% random noises to the amplitude and period of the
L489: IV. CASE STUDIES modulation function to mimic the subtle random fluctuations
L490: that exist in real-world machinery operations [31]. We alter
L491: A. Implementation
L492: N ˆ e to change the signal-to-noise ratio (SNR) to introduce
L493: We replace the risk function in Fig. 1 with ERM, IRM, spu
L494: the different environments.
L495: and IBIRM to realize the corresponding diagnosis methods.
L496: Finally, in each environment, the sampling frequency is
L497: Important hyperparameters are determined as follows. We
L498: 20 480 Hz, and the duration is equal to 10 s. To create the
L499: employ full batch data to train the model. The learning rate is
L500: dataset for each environment, we segment the data into pieces
L501: set to 0.001. The maximum epoch number is 500. L2 regular-
L502: without overlaps. Each piece contains 5000 data points. Our
L503: ization with weight 0.001 is applied to reduce overfitting. The
L504: goal is to correctly classify the normal condition and fault
L505: burn-in steps of the IRM, IBIRM, and SCIRM are selected by
L506: condition in both the training and test environments. In each
L507: first using a grid search and then fine tuning. Other parameters
L508: experiment, we design two training environments and one
L509: are set as in the previous studies [29]. Regarding validations,
L510: test environment. In addition, each experiment was repeated
L511: we consider both the oracle setting and the leave-one-domain-
L512: 10 times to calculate the mean accuracy and standard devi-
L513: out setting [30]. Metrics evaluating the model performances
L514: ation. Three generalization tasks are designed, which will be
L515: include the mean classification accuracy and the standard devi-
L516: specified later in the corresponding figures showing the experi-
L517: ation, which are shown in the bar charts. The method that
L518: mental results. Oracle validation is applied to show the optimal
L519: achieves a higher mean accuracy and lower standard deviation
L520: performance [30].
L521: is regarded as better.
L522: 2) Bearing Data Description: Our test rig for collecting
L523: the bearing data is shown in Fig. 2. There are two classes, the
L524: B. Experimental Design
L525: normal condition and roller fault condition. For each class,
L526: We first simulate the data to verify Theorem 1. As our pri- the data are collected under five speed conditions, which
L527: mary purpose is verifying the theorem, we only benchmark are 30, 50, 100, 150 and 200 km/h. There are two sensors,
L528: SCIRM against the commonly seen risk functions, that is, the single-direction piezoelectric vibration sensor (SNy563)
L529: ERM, using the simulation data. Next, we compare SCIRM and the three-direction strain vibration sensor (ZW9609A-
L530: with ERM, IRM and IBIRM in bearing and gearbox fault 18 SN7068). Therefore, four channels of data are obtained
L531: diagnoses involving different speed conditions. One work- for each speed condition. The sampling frequency is 10 kHz,
L532: ing condition defines one environment. For the real data, we and the duration is equal to 10 s. Each channel of data is
L533: Authorized licensed use limited to: University of Science & Technology of China. Downloaded on July 05,2026 at 10:04:03 UTC from IEEE Xplore. Restrictions apply.
L535: ===== PAGE 7 =====
L537: MO et al.: SCIRM FOR DOMAIN GENERALIZATION 1553
L538: Fig. 2. Train bearing test rig.
L539: Fig. 4. Training and test results of the classification based on simulation
L540: data; (a) result of two training environments (-4 and -10 db) and single test
L541: environment (-16 db); (b) and (c) are similarly interpreted; (d) average result
L542: based on (a)–(c).
L543: Fig. 3. Gearbox test rig.
L544: Fig. 5. Test results of the classification based on bearing data under the
L545: segmented into instances without overlaps, and each instance
L546: single training environment setting; (a) result of single training environment
L547: has 5000 data points. Two kinds of experimental settings (30 km/h) and single test environment (200 km/h); (b) and (c) are similarly
L548: are designed, that is, the setting of one training environment interpreted; (d) average result based on (a)–(c).
L549: and the setting of two training environments. In addition, we
L550: leave 150 km/h out for validation and 200 km/h for testing
L551: but change the different training environments [30]. The goal test dataset. However, once the SNRs are low, ERM general-
L552: is to observe the effects of changing training environments izes poorly on the test dataset, as shown in Fig. 4(b) and (c).
L553: on the model performances of the test environments. Three Different from ERM, it is observable that the performance
L554: generalization tasks are designed and will be specified in the of SCIRM is less influenced by the change in SNRs. Under
L555: corresponding figures of the test results. Each experiment has a high SNR, SCIRM can achieve 100% accuracy in both
L556: ten trials for computations of the mean accuracy and standard the training and test datasets. With a decrease in the SNR,
L557: deviation. SCIRM can still obtain relatively high accuracies on the test
L558: 3) Gearbox Data Description: Our test rig, shown in datasets, as shown in Fig. 4(b) and (c). It should be noted
L559: Fig. 3, is utilized to acquire the gearbox data. There are three that there are some gaps between the theory and reality. The
L560: classes, the normal condition, a missing tooth on the sun first is that the simulation model is a relaxed and simpli-
L561: gear and a missing tooth on the planet gear. For each class, fied approximation to the ideal data generation model. The
L562: there are three speed conditions, 900, 1200, and 1500 rpm. second is that the data extraction is limited by the model’s
L563: The vertical direction data of the accelerometer (604B31) are complexity. It is obvious that a shallow neural network and
L564: employed. The sampling frequency is 5 kHz, and approxi- a deep neural network can have different feature extraction
L565: mately 280 000 points are collected in total. The data are then abilities. The third is that the practical version of SCIRM is an
L566: segmented without overlaps into instances, and each instance unconstrained optimization problem, which is a compromise
L567: has 2000 points. Oracle validation is employed to show the of the proposed constrained optimization problem. However,
L568: optimal performance [30]. Three experimental designs for the as shown in Fig. 4(d), SCIRM still shows a strong generaliza-
L569: generalization study will be given later in the figures depicting tion ability in the relaxed scenario, which is consistent with
L570: the test results. There are two types of experimental settings, our theorem on the OOD problem.
L571: which separately consider the single training environment and 2) Bearing Data Analysis: We observe that all the com-
L572: two training environments. Ten trials are conducted in each pared methods have similar and extremely high accuracies on
L573: experiment to compute the mean accuracy and the standard the training datasets. For a clearer visualization, we only show
L574: deviation. the performances on the test datasets in Fig. 5 (single train-
L575: ing environment setting) and Fig. 6 (two training environments
L576: setting). It is observable that all the methods perform better in
L577: C. Result Analysis
L578: a setting of two training environments than in a one training
L579: 1) Simulation Data Analysis: The classification results of environment setting. It complies with the rule of thumb that
L580: the simulation data are shown in Fig. 4. Generally, both more data encourages more well-behaved invariant features,
L581: SCIRM and ERM perform extremely well on the training and helps to generalize the models [21]. In the single training
L582: dataset. However, they perform differently on the test dataset. environment setting in which the data are collected at speed
L583: As shown in Fig. 4(a), under a high SNR, ERM is less influ- = 30 km/h, we observe that all the trained models perform
L584: enced by spurious features, and can perform quite well on the poorly in testing. One possible reason is that the training
L585: Authorized licensed use limited to: University of Science & Technology of China. Downloaded on July 05,2026 at 10:04:03 UTC from IEEE Xplore. Restrictions apply.
L587: ===== PAGE 8 =====
L589: 1554 IEEE TRANSACTIONS ON CYBERNETICS, VOL. 54, NO. 3, MARCH 2024
L590: Fig. 6. Test results of the classification based on bearing data under the two Fig. 8. Test results of the classification based on gearbox data under the two
L591: training environments setting: (a) result of two training environments (30 and training environments setting; (a) result of two training environments (900 rpm
L592: 50 km/h) and single test environment (200 km/h); (b) and (c) are similarly and 1200 rpm) and one test environment (1500 rpm); (b) and (c) are similarly
L593: interpreted; and (d) average result based on (a)–(c). interpreted; (d) average result based on (a)–(c).
L594: Fig. 7. Test results of the classification based on gearbox data under the one
L595: training environment setting: (a) result of one training environment (900 rpm)
L596: and one test environment (1200 rpm); (b) and (c) are similarly interpreted; Fig. 9. Comparison of standardized training and test samples from the sim-
L597: and (d) average result based on (a)–(c). ulation experiment: (a) time waveform of the 8-db training sample; (b) time
L598: waveform of the 20-db test sample; and (c) probability density estimation
L599: curves.
L600: data at a speed of 30 km/h are significantly different from the
L601: test data at a speed of 200 km/h. Thus, the data distribution
L602: shown in Fig. 7(c) in which all the methods fail to gener-
L603: shift may be too drastic. In addition, there is only one training
L604: alize well. As discussed in the bearing fault diagnosis, it may
L605: environment available, which may limit the feature extraction.
L606: be difficult to learn overlapped invariant features when there
L607: Due to the drastic change in distribution and the scarcity of
L608: are drastic changes in distributions and scarce training envi-
L609: training environments, the assumption about the support over-
L610: ronments. As we increase the training environments, SCIRM
L611: lap of invariant features [21] may be severely violated. Hence,
L612: can perform relatively better than the other methods in Fig. 8.
L613: it is difficult to generalize the model. The general observation
L614: Other observations are similar to those discussed in the bearing
L615: from comparing Fig. 5(b) and (c) with (a) is that once the
L616: data analysis.
L617: training environments are closer to the test environment, the
L618: performance of SCIRM can improve significantly. In addition,
L619: V. FURTHER DISCUSSION AND VALIDATIONS
L620: we also note that the results in Fig. 5(b) are relatively bet-
L621: ter than those in Fig. 5(c). There may be some unexpected A. Domain Generalization
L622: interventions during the data collection period, which pol- In Section II-A, we have depicted the problem setting
L623: luted the data from 100 km/h. In Fig. 5(b), when the IRM studied in this work. In short, the joint distribution of data
L624: already achieves an extremely high accuracy, adding an addi- and labels can change, while the invariant features (possibly
L625: tional loss function may overregulate the model. Therefore, and hopefully the causal features) are general to the various
L626: it may require a great effort in tuning the model to continue domains and can be employed to execute classifications. This
L627: making improvements. However, we should not consider only general assumption is consistent with many other papers [7].
L628: one particular case. In general, SCIRM provides a better aver- Invariant features may act as connections among the domains
L629: age performance, as shown in Figs. 5(d) and 6(d). In other and benefit model generalization. The data components, other
L630: words, the model trained by SCIRM generalizes better than than the invariant features, can change, leading to a change
L631: the models trained by the other methods. in the joint distribution of the data and labels. The change in
L632: 3) Gearbox Data Analysis: In the gearbox fault diagnosis, the joint distribution means a new domain of data. If this new
L633: we observe similar general patterns as those observed in the domain is not in the training domains, then it can be regarded
L634: bearing fault diagnosis. First, all the methods achieve simi- as “unseen” by the model. Our model has been tested for
L635: larly high accuracies on the training dataset but the results on generalization to unseen domains. To better illustrate this, we
L636: the test dataset vary greatly. Therefore, we visualize only the show the time waveforms and estimated probability density
L637: test results in Fig. 7 (single training environment setting) and function curves of the data samples from the training and test
L638: Fig. 8 (two training environments setting). Again, the results domains in Fig. 9. The samples are generated from the simula-
L639: based on a setting of two training environments are better tion experiment in Section IV-B1), which verifies Theorem 1.
L640: than those based on a setting of one training environment. The samples have been standardized. It is observable that the
L641: In the one training environment setting, there is one case training samples are still different from the test samples in
L642: Authorized licensed use limited to: University of Science & Technology of China. Downloaded on July 05,2026 at 10:04:03 UTC from IEEE Xplore. Restrictions apply.
L644: ===== PAGE 9 =====
L646: MO et al.: SCIRM FOR DOMAIN GENERALIZATION 1555
L647: Fig. 10. Test classification results on the Colored MNIST dataset, where
L648: “Guess” means the random guess and “Best” means the best method in theory.
L649: Fig. 11. Confusion matrices, where “Normal,” “Inner,” “Outer” means nor-
L650: mal, inner race fault, and outer race fault, respectively. (a) ERM. (b) SCIRM.
L651: terms of both the waveforms and density curves. However, as
L652: seen from Fig. 4(c) and (d), our method can generalize well
L653: to the unseen domains. called K006 (normal condition), KA22 (outer race fault) and
L654: It should also be noted that some prominent features may KI21 (inner race fault). In the naming of the working con-
L655: correlate with the labels in the training domains. However, the ditions, “N” represents the rotation speed, “M” standards
L656: correlations are fragile and may not exist in the test domains. for the load torque and “F” denotes the radial force. The
L657: If a model learns correlated features, it may perform poorly digits following “N,” “F” and “M” encode their values.
L658: in the test domains. To illustrate this, we test our method and Three tasks are designed as follows. Task 1: N15_M01_F10
L659: the baseline methods close to ours on the colored MNIST and N15_M07_F04 for training and N09_M07_F10 for test-
L660: dataset. Details of the dataset, the neural network used and ing. Task 2: N09_M07_F10 and N15_M07_F04 for training
L661: other implementation information are available in [20]. The and for N15_M01_F10 testing. Task 3: N09_M07_F10 and
L662: key design of the dataset is that the labels are strongly cor- N15_M01_F1 for training and N15_M07_F04 for testing. For
L663: related with the background colors in the training domains, ease of computation, each health condition at each working
L664: while such a correlation is insignificant in the test domain. As condition has 120 samples, and each sample has 2000 points.
L665: all methods perform well on the training environments, we 3) MFPT Dataset: The full information about this dataset
L666: only show their results on the test environment in Fig. 10. It is also offered in [32]. There are only three data files of normal
L667: is observable that our method is less affected by the correlation conditions under a load of 270 lbs. Seven data files indexed
L668: change, and its result is nearly the best possible. In contrast, from 1 to 7 are under seven different load conditions from
L669: ERM is trapped by the correlation, and its result is even worse 25 to 3000 lbs for the outer and inner race fault conditions,
L670: than a random guess. respectively. An environment is named by Nx_Ox_Ix, where
L671: “x” specifies the data files, and “N,” “O,” and “I” indicate the
L672: B. Additional Benchmarks normal, outer race and inner race fault conditions, respectively.
L673: For each health condition under each load condition, there are
L674: In addition to the previously discussed baseline meth-
L675: 146 samples, and each sample has 1000 points. Three gen-
L676: ods, seven extra recently proposed methods are considered.
L677: eralization tasks are developed as follows. Task 1: N2_O2_I6
L678: The additional methods cover the information bottleneck-
L679: and N3_O3_I7 for training and N1_O5_I1 for testing. Task 2:
L680: based ERM (IBERM) [21], spectral decoupling (SD) [14],
L681: N1_O1_I5 and N3_O3_I7 for training and N2_O6_I2 for
L682: variance risk extrapolation (VREx) [10], distribution robust
L683: testing. Task 3: N1_O1_I5 and N2_O2_I6 for training and
L684: optimization (DRO) [15], interdomain mixup (Mixup) [9],
L685: N3_O7_I3 for testing.
L686: AND mask (AMask) [12] and SAND mask (SMask) [13].
L687: 4) Benchmarking Result: In each task, we reserve 20% of
L688: We use three bearing fault datasets as examples to cre-
L689: the data from the training set as the validation set. All the
L690: ate nine generalization tasks. One dataset has been dis-
L691: methods are based on the neural network shown in Fig. 1. We
L692: cussed in Section IV-B2 and is called the “CityU dataset”
L693: tune all the methods so that they perform well on the training
L694: for easy reference. Two other datasets, the Paderborn
L695: and validation sets and their performances have no significant
L696: University (PU) dataset and the Machinery Failure Prevention
L697: differences on these two sets. Therefore, we only present the
L698: Technology (MFPT) dataset, are opensource datasets discussed
L699: results on the test sets in Table I, and each task is repeated ten
L700: in [32]. Thus, we only provide the essential information next.
L701: times to obtain the mean accuracy and standard deviation. The
L702: 1) CityU Dataset: The dataset has been applied to design
L703: summary column presents the averaged results over the nine
L704: several generalization tasks shown in Figs. 4 and 6. However,
L705: tasks. As we can see, our method is among the top three in each
L706: the test environments are fixed to 200 km/h. We continue
L707: task and, on average, performs better than the other methods.
L708: to use data at speeds of 100, 150, and 200 km/h to cre-
L709: ate three generalization tasks. In each task, the signal size
L710: C. Confusion Matrix
L711: is set to 2000 points to increase the total number of sam-
L712: ples. The generalization tasks are designed as follows. Task 1: We take the first task of the MFPT dataset as an example
L713: 150-200Train_100Test, which means the data of 150 and to show the confusion matrices of SCIRM and ERM. Here,
L714: 200 km/h are for training and the data of 100 km/h is for ERM is employed as a baseline. Our main purpose is to show
L715: testing. Similarly, we have Task 2: 100-200Train_150Test and the health conditions that our method has been successfully
L716: Task 3: 100-150Train_200Test. used to diagnose. From confusion matrices in Fig. 11, we
L717: 2) PU Dataset: Details of this dataset are offered in [32]. observe that SCIRM and ERM are good at identifying the
L718: Data files from accelerated life tests are considered and normal condition and outer race fault condition. In addition,
L719: Authorized licensed use limited to: University of Science & Technology of China. Downloaded on July 05,2026 at 10:04:03 UTC from IEEE Xplore. Restrictions apply.
L721: ===== PAGE 10 =====
L723: 1556 IEEE TRANSACTIONS ON CYBERNETICS, VOL. 54, NO. 3, MARCH 2024
L724: TABLE I
L725: TEST RESULTS OVER NINE GENERALIZATION TASKS BASED ON THREE DATASETS
```

### Lines 733-780

```text
L733: VI. CONCLUSION
L734: −[αF(X) + (1 − α)F(Y)]
L735: In this article, we proposed the SCIRM framework for model (cid:14) (cid:15)
L736: F(Y)
L737: generalizations and demonstrated its application in machinery < − α G(X) + (1 − α)F(Y)
L738: fault diagnosis. We provided the essential requirements for
L739: G(Y)
L740: the sparsity measure to enable OOD generalizations. We dis- = −
L741: F(Y)
L742: [αG(X) + (1 − α)G(Y)]. (27)
L743: cussed the setting where SCIRM could have a theoretical G(Y)
L744: guarantee. Our theory was validated by the simulation data.
L745: Considering the left-hand side (L.H.S) of (25)
L746: In addition, we showed that, on average, the proposed diag-
L747: nosis method outperformed the state-of-the-art methods across F(Y)
L748: different generalization tasks. In future work, efforts will be
L749: − F(αX + (1 − α)Y) < −
L750: G(Y)
L751: [αG(X) + (1 − α)G(Y)].(28)
L752: devoted to studying generalization error bounds, theories on
L753: the number of training environments, extending or relaxing Note that G(X) is convex
L754: some assumptions, more adaptive loss balancing methods, etc.
L755: G(αX + (1 − α)Y) ≤ αG(X) + (1 − α)G(Y). (29)
L756: APPENDIX Since G(·) > 0, F(·) > 0, and α ∈ (0, 1)
L757: A. Proof of Lemma 1
L758: F(Y)
L759: Since the sparsity measure is scale invariant − [αG(X) + (1 − α)G(Y)]
L760: G(Y)
L761: (Definition 1) and semistrictly quasi-convex (Definition 2),
L762: F(Y)
L763: we have ≤ − G(αX + (1 − α)Y). (30)
L764: (cid:12) (cid:12) (cid:13) (cid:13) (cid:5) (cid:6) G(Y)
L765: 1 1
L766: S ↑(X + Y) = S ↑ X + 1 − Y < max S ↑(X), S ↑(Y) .
L767: 2 2 Hence, the L.H.S of (28) must be smaller than the R.H.S
L768: (23) of (30)
L769: Since S ↓ = −S ↑ , it follows that: − F(αX + (1 − α)Y) < − F(Y) G(αX + (1 − α)Y)
L770: (cid:5) (cid:6) G(Y)
L771: S ↓(X + Y) > max S ↓(X), S ↓(Y) (24) F(αX + (1 − α)Y) F(Y)
L772: ⇒ − < − . (31)
L773: G(αX + (1 − α)Y) G(Y)
L774: As Z(X) < Z(Y), and Z(·) = −[F(·)/G(·)], we complete the
L775: B. Proof of Proposition 1 proof as follows:
L776: We define X, Y ∈ (cid:9) ⊆ Rn + and Z(X) (cid:5)= Z(Y). Without loss F(αX + (1 − α)Y)
L777: of generality, we continue to let Z(X) < Z(Y) and α ∈ (0, 1). Z(αX + (1 − α)Y) = −
L778: G(αX + (1 − α)Y)
L779: By concavity of F(X)
L780: F(Y)
```

## Time_Series_Classification_Based_on_Supervised_Contrastive_Learning_and_Homoscedastic_Uncerta.txt
- Total extracted lines: 1025

### Lines 1-60

```text
L3: ===== PAGE 1 =====
L5: 414 IEEE TRANSACTIONS ON NEURAL NETWORKS AND LEARNING SYSTEMS, VOL. 37, NO. 1, JANUARY 2026
L6: Time Series Classification Based on
L7: Supervised Contrastive Learning
L8: and Homoscedastic Uncertainty
L9: Tao Zhang , Ke Li , Member, IEEE, and Shaofan Wang
L10: Abstract—In recent years, contrastive learning (CL) frame- depend on manually crafted features [7], [8], requiring special-
L11: works have been widely applied to multivariate time series ized knowledge for feature extraction. However, this reliance
L12: classification (MTSC) tasks. However, existing methods lack task- leads to performance differences due to varying feature extrac-
L13: specific guidance, leading to limitations in fully capturing the
L14: tion methods and their limited ability to capture deep-level
L15: complex dynamics and invariant representations in time series
L16: information [9]. Modern MTSC methods increasingly utilize
L17: data. Motivated by the auxiliary tasks in multitask learning
L18: (MTL) and to fully utilize the rich frequency-domain information deep learning architectures [10], [11], [12], [13], [14], [15].
L19: of time series data, we propose a novel time series classification These models automatically extract features from raw data
L20: framework, uncertainty-based time–frequency supervised CL (U- through neural networks, enabling the discovery of complex
L21: TFSCL). This framework uses SCL in the time and frequency
L22: patterns. However, the majority of current MTSC methods that
L23: domains and time–frequency consistency as auxiliary tasks to
L24: use only instance-level labels and rely on the cross-entropy
L25: improve the primary task of using only instance-level labels for
L26: loss function exhibit two critical limitations. First, their deci-
L27: time series classification. Furthermore, inspired by the homo-
L28: geneous uncertainty in MTL, we derive a novel uncertainty sion boundaries are prone to overfitting on noisy labels due
L29: loss function, which automatically adjusts the weights according to the sensitivity of the loss function to mislabeled samples
L30: to the degree of uncertainty of different tasks to optimize the [16], [17], [18]. Second, the focus on learning discriminative
L31: learning and prediction process of the model. The proposed
L32: features neglects the extraction of invariant temporal patterns,
L33: framework is evaluated on MTSC tasks, including human activity
L34: resulting in suboptimal generalization performance across
L35: recognition (HAR), air writing, and gesture recognition. In
L36: addition, we create a human–drone interaction (HDI) dataset unseen data distributions [19].
L37: consisting of 20 subjects and conduct real-world experiments The scarcity of high-quality labels in time series domains
L38: to evaluate the proposed framework. The extensive experiments poses a significant challenge to model training. For instance,
L39: conducted in various settings verify the effectiveness of the clinical time series data (e.g., ECG, EEG) require expert
L40: proposed framework.
L41: physician annotations, but the labeling process remains scarce
L42: Index Terms—Multitask learning (MTL), multivariate time due to data sensitivity and prohibitive costs. In addition,
L43: series classification (MTSC), supervised contrastive learning labels may contain noise from doctors’ differing diagnoses
L44: (SCL). or equipment errors, affecting disease feature learning [20].
L45: I. INTRODUCTION Contrastive learning (CL) can learn invariant representations
L46: TIME series data exist in many real-world scenarios, by comparing different views of input samples, thereby reduc-
L47: ing reliance on high-quality labels and mitigating overfitting
L48: including wind forecasting [1], stock forecasting [2],
L49: induced by noisy labels [21]. It divides the input samples
L50: human activity recognition (HAR) [3], industrial fault diagno-
L51: into positive and negative ones and learns representations
L52: sis [4], [5], and healthcare [6]. Such continuous data represent
L53: from the time series data by maximizing the similarity within
L54: states or events at points in time, making them ideal for ana-
L55: positive pairs and minimizing the similarity within negative
L56: lyzing trends, patterns, and anomalies. The key to analyzing
L57: pairs. A typical framework is SimCLR [22], which uses
L58: time series data is to extract the information-rich features for
L59: data augmentation methods to generate different views and
L60: in-depth analysis and decision support.
```

### Lines 120-260

```text
L120: these challenges, this study proposes a novel framework
L121: ments time-domain data [24], [26], [29], [30]. The key is
L122: named uncertainty-based time–frequency SCL (U-TFSCL),
L123: to effectively integrate these two domains to leverage their
L124: which systematically integrates SCL with homoscedastic
L125: complementary strengths. One intuitive approach is signal-
L126: uncertainty-based MTL. The proposed framework constructs
L127: level fusion via the short-time Fourier transform (STFT),
L128: a time–frequency dual-domain CL module that optimizes
L129: which transforms time series into 2-D spectrograms, thereby
L130: two complementary objectives: 1) intradomain consistency
L131: incorporating time–frequency information into model inputs
L132: within the time and frequency domains and 2) cross-domain
L133: [31]. Fusion can also occur at the feature level, for example,
L134: discrepancy minimization between the time and frequency
L135: Jin and Chen [32] proposed an end-to-end deep learning
L136: domains. By incorporating instance-level label information
L137: framework that employs time–frequency analysis to extract
L138: into the contrastive objectives, the module balances dis-
L139: features from vibration signals and combine them into input
L140: criminative learning and invariant representation learning;
L141: embeddings for transformers. Furthermore, tight feature align-
L142: it clusters samples from the same class while separating
L143: different classes and enforces invariant feature alignment ment can be achieved by learning the consistency between
L144: time- and frequency-domain features through cross-domain
L145: across time–frequency domains for the same instances. The
L146: CL [29] and by learning the domain independence through
L147: module generates joint time–frequency representations that
L148: intradomain CL [5].
L149: are directly optimized through end-to-end training with
L150: downstream classification tasks, ensuring semantic alignment
L151: between learned features and classification objectives. Fur- B. CL for Time Series
L152: thermore, we adopt the automatic weighting strategy that CL has emerged as a powerful self-supervised framework
L153: balances the loss function by weighting each task according to for learning representations by maximizing similarity between
L154: the homoscedastic uncertainty [27]. This strategy enables the positive pairs and minimizing dissimilarity between nega-
L155: model to adaptively adjust the weight of each task, allocating tive pairs. CL is extensively used in many fields, including
L156: more attention to uncertain and difficult tasks in the training image classification [22], video analysis [33], HAR [34],
L157: process. remote photoplethysmography (rPPG) [35], and time series
L158: To validate the effectiveness of the framework, we con- analysis [18], [23], [24]. Data augmentation is crucial in
L159: duct comprehensive experiments on six benchmark datasets, a CL-based framework; unlike traditional data augmentation
L160: including a newly constructed human–drone interaction (HDI) in computer vision, time series augmentation must consider
L161: dataset containing real-world gesture sequences from 20 par- temporal dependencies. For instance, TCL [36] splits the time
L162: ticipants. The key contributions of this work include the series into nonoverlapping windows and treats each window as
L163: following. an independent view, exploiting the properties of nonstationary
L164: 1) A time–frequency domain contrast module based on SCL time series by assuming negative pairs for distant windows and
L165: fully learns the representation of time series through intratime, positive pairs for neighboring windows. The representation
L166: intrafrequency, and time–frequency domain consistency CL. of the input time series is captured by learning invariant
L167: Authorized licensed use limited to: University of Science & Technology of China. Downloaded on July 05,2026 at 10:02:42 UTC from IEEE Xplore. Restrictions apply.
L169: ===== PAGE 3 =====
L171: 416 IEEE TRANSACTIONS ON NEURAL NETWORKS AND LEARNING SYSTEMS, VOL. 37, NO. 1, JANUARY 2026
L172: Fig. 1. Overview of U-TFSCL framework.
L173: features within the windows as well as differences between III. PRINCIPLE AND METHOD
L174: the windows. TS-TCC [37] uses two augmentation methods, A. Overview of the Proposed U-TFSCL Framework
L175: strong and weak augmentation, to convert the original series To fully exploit features across the time–frequency domains
L176: into two views and learn robust representations from the in the time series data, we propose the U-TFSCL framework,
L177: augmented views using temporal and contextual contrasting as shown in Fig. 1. This framework comprises a parallel
L178: modules. TS2Vec [38] generates different views by random encoder module operating within both the time and frequency
L179: masking operations on time steps and performs a hierarchical domains, a time–frequency domain SCL (TFSCL) module,
L180: CL strategy over augmented views, which enables robust and an MTL module that balances the loss based on task
L181: representations. Khosla et al. [25] extend the self-supervised uncertainty. These components aim to provide a comprehen-
L182: batch contrastive approach to the fully supervised setting, sive and effective approach for analyzing time series data.
L183: thereby enabling effective utilization of label information. The Specifically, the original time-domain signals are input into the
L184: clusters of points belonging to the same class are pulled U-TFSCL framework, where they are first converted to their
L185: together in embedding space while simultaneously pushing frequency-domain counterparts using a rapid Fourier trans-
L186: apart clusters of samples from different classes. Tripathi et form. These original and transformed signals are then fed to
L187: al. [39] directly use SCL for air writing recognition and parallel branches for time- and frequency-domain processing.
L188: achieve better performance than using cross-entropy loss. Within each branch, advanced data augmentation methods are
L189: The closest work to ours is [18], which proposes a novel employed to generate positive and negative sample pairs. Sub-
L190: framework for universal representation learning of multivariate sequently, these pairs are processed using independent encoder
L191: time series using instance-level and cluster-level SCL, aim- modules. These modules consist of several transformer blocks
L192: ing to capture complex patterns and dependencies for better and extract distinct time- and frequency-domain features from
L193: downstream task performance. However, this approach relies the pairs.
L194: on manually weighted loss combinations requiring domain Subsequently, the extracted features are fed into the TFSCL
L195: expertise for tuning, and its two-stage architecture freezes module, which uses SCL to calculate intradomain and interdo-
L196: the pretrained encoder during downstream tasks, restricting main losses and improve the performance of the classification
L197: joint optimization of cross-entropy and contrastive losses task by using the intradomain and interdomain compari-
L198: while neglecting explicit temporal-frequency consistency son tasks as auxiliary tasks. In this module, the time- and
L199: modeling. Our method addresses these constraints by inte- frequency-domain losses are calculated first. Then, the features
L200: grating adaptive multiloss weighting and instance-level labels that calculate the intradomain loss are projected into a shared
L201: driven explicit temporal-frequency alignment in an end-to-end latent space by separate projection layers. In this space, the
L202: framework. time–frequency domain consistency loss is calculated.
L203: Authorized licensed use limited to: University of Science & Technology of China. Downloaded on July 05,2026 at 10:02:42 UTC from IEEE Xplore. Restrictions apply.
L205: ===== PAGE 4 =====
L207: ZHANG et al.: TIME SERIES CLASSIFICATION BASED ON SUPERVISED CL AND HOMOSCEDASTIC UNCERTAINTY 417
L208: Fig. 2. Schematic of time–frequency domain data augmentation. (a) Original series in time domain. (b) Original series in frequency domain. (c) Augmented
L209: series in time domain. (d) Augmented series in frequency domain.
L210: After the TFSCL module, the multitask losses are fed into high-frequency components depends on the specificity of the
L211: the MTL module, which introduces a novel task uncertainty- signal. Therefore, this study did not augment a specific fre-
L212: driven weight adjustment strategy. This strategy enables the quency component but randomly perturbed the full frequency
L213: model to balance the learning of task-relevant and cross- band. To simplify the discussion, FFT(xT) is denoted as
L214: i
L215: domain features. This balance ensures that the model not xF,G represents the frequency-domain encoder, and hF and
L216: i F i
L217: only captures task-relevant features but also develops a h˜F are the original and augmented view embeddings in the
L218: i
L219: robust understanding of domain-independent features, thereby frequency domain, respectively. As the difference between the
L220: enhancing the adaptability and performance across a wide original data and its augmented view is generally minimal,
L221: range of time series analysis tasks. it is assumed that the original data and its augmented view
L222: are positive pairs in the time-domain branch, namely, (xT, x˜T),
L223: i i
L224: and in the frequency-domain branch, namely, (xF, x˜F). The
L225: i i
L226: B. Cross Time–Frequency Information Interaction Strategy different samples are negative pairs in the time-domain branch,
L227: For a given input time series sample xT, the random i.e., (xT, xT) and (xT, x˜T), and the frequency-domain branch,
L228: i i j i j
L229: dropout in [24] is used to generate time-domain augmented i.e., (xF, xF) and (xF, x˜F). To facilitate reading and reduce
L230: i j i j
L231: samples x˜T, and the time encoder G is used to map them repetition, in the subsequent content, we use the domain-
L232: i T
L233: to new embeddings, i.e., hT = G (x˜T) and h˜T = G (x˜T). specific superscript D ∈ {T, F}, which includes the time
L234: i T i i T i
L235: Similarly, in the frequency-domain branch, the time series is domain T and the frequency domain F, to introduce the
L236: augmented and projected after the fast Fourier transform (FFT) intradomain concepts.
L237: (cid:93)
L238: operations. i.e., hF = G (FFT(xT)) and h˜F = G (FFT(xT)). In a multiview batch, i ∈ I ≡ {1, . . . , 2N} is denoted as
L239: i F i i F i
L240: Each frequency component in the frequency domain represents the indices of the samples, and the self-supervised contrastive
L241: a corresponding basis function that plays a key role in signal loss is used to maximize the similarity within positive pairs
L242: processing [40], and perturbation augmentations (additions or and minimize the similarity within negative pairs
L243: deletions) to the frequency component may result in signifi-
L244: cant alterations to the time pattern. Therefore, the frequency X X exp (cid:0) hD · h˜D/τ (cid:1)
L245: domain is randomly augmented based on the augmentation LD = L i D = − log P exp i (cid:0) hD i · hD/τ (cid:1) (1)
L246: methods in [29]. i∈I i∈I a∈A(i) i a
L247: Fig. 2 illustrates the visualization results of time and
L248: frequency-domain augmentation for a time series sample. where · symbol denotes the dot product and hD and h˜D
L249: i i
L250: Zhang et al. [29] showed that in physiological signal data, are the original and augmented views of domain-specific
L251: the performance of perturbing low-frequency components was embeddings, respectively. τ is the temperature parameter to
L252: slightly better than that of perturbing the full frequency band. scale the sensitivity of the loss function; A(i) ≡ I{i} denotes
L253: Conversely, the opposite result was observed for mechanical the set of negative samples to be computed for the ith sample
L254: vibration signals. This implies that the selection of low- and (ith sample is called the anchor in CL), which contains 2(N−1)
L255: Authorized licensed use limited to: University of Science & Technology of China. Downloaded on July 05,2026 at 10:02:42 UTC from IEEE Xplore. Restrictions apply.
L257: ===== PAGE 5 =====
L259: 418 IEEE TRANSACTIONS ON NEURAL NETWORKS AND LEARNING SYSTEMS, VOL. 37, NO. 1, JANUARY 2026
L260: negative samples; and in this loss, each anchor corresponds to In batch I, which contains 2N samples, i ∈ I¯ ≡ {1, . . . , N}
```

### Lines 430-520

```text
L430: ===== PAGE 7 =====
L432: 420 IEEE TRANSACTIONS ON NEURAL NETWORKS AND LEARNING SYSTEMS, VOL. 37, NO. 1, JANUARY 2026
L433: TABLE I
L434: DETAILS OF THE HDI DATASET
L435: Fig. 3. Schematic of gesture movements: (G1) move left, (G2) move right,
L436: (G3) hover, (G4) move up, (G5) move down, and (G6) move forward.
L437: 1) using zero-crossing detection to automatically segment
L438: can be rewritten as
L439: gestures and nongestural signals in recorded signals and
L440: (cid:18) (cid:19)
L441: L = X 1 L +log (σ ) + 1 L 2) manually examining the results of the automatic label-
L442: total σ2 D D σ2 TF ing and eliminating the misclassified signal segments that
L443: D TF
L444: 1 (cid:0) (cid:1) oscillated up and down around smaller mean values, which
L445: + log (σ ) + L + log σ (9)
L446: TF σ2 pre pre were inferred to be either preparatory movements or hand
L447: pre
L448: rebound oscillations after the rapid execution of a gesture.
L449: where σ , σ , and σ denote the homoscedastic uncertain-
L450: D TF pre After eliminating invalid signal segments, we obtained 3318
L451: ties of L , L , and L , respectively. The larger value of
L452: D TF pre gesture instances. For each instance, a lookback window with
L453: σ indicates that the task is more uncertain and it is harder to
L454: a length of 20 sample points and a stride of ten sample points
L455: optimize the total loss function L , and the importance of the
L456: total was used to generate samples; after the lookback window
L457: task in the total loss function decreases and has a lower weight.
L458: operation, the valid gesture dataset contains 45 376 samples.
L459: Conversely, a smaller σ indicates that the task is simpler and
L460: Table I shows the details of each gesture; it is clear that
L461: will have a higher weight value in L . To avoid division
L462: total the duration time (average in 0.94 ± 0.34 s) and the length of
L463: by zero and to make the values more stable during learning,
L464: each sample are all shorter than the previous gesture dataset
L465: s: = log(σ2) is substituted into (9), thus giving the final loss
L466: [45], which results in reduced intersample variability, thereby
L467: function L , where s , s , and s are in the optimization
L468: total D TF pre decreasing the model’s ability to sufficiently capture dynamic
L469: set of learnable parameters
L470: patterns or periodic features, ultimately significantly affecting
L471: (cid:18) (cid:19)
L472: L = X 1 L + s D + 1 L + s TF the performance of MTSC tasks. In addition, compared to
L473: total esD T 2 esTF TF 2 traditional MTSC datasets such as UEA [46] (mostly less than
L474: 1 s 10 000 samples), our HDI dataset provides more than 45 000
L475: + L + pre (D ∈ T, F) . (10)
L476: espre pre 2 samples, addressing the critical data scarcity in MTSC. This
L477: scale enables robust training of deep neural networks while
L478: D. Development and Features of the HDI Gesture Dataset reducing the risk of overfitting, making it more suitable for
L479: the training and evaluation of deep learning networks.
L480: To complement the existing MTSC dataset, based on previ-
L481: ous gesture HDI studies [43], [44], we designed six gestures
L482: for a challenging gesture-based HDI task: (G1) Move Left, IV. EXPERIMENT
L483: (G2) Move Right, (G3) Hover, (G4) Move Up, (G5) Move
L484: A. Experimental Settings
L485: Down, and (G6) Move Forward; Fig. 3 illustrates the move-
L486: ment of each gesture. In this task, participants were required The superiority of the framework is validated across exten-
L487: to control drone flight trajectories through six predefined hand sive and widely used MTSC datasets in various domains.
L488: gestures while wearing an inertial measurement unit (IMU) The programs are written in Python 3.8 using PyTorch and
L489: sensor on their dominant hand. All participants started the executed on NVIDIA GeForce RTX 3090Ti GPUs. Two
L490: experiment without prior training on the target gestures to layers of transformer blocks are used as encoders in both
L491: preserve interindividual variability. time and frequency domains. For time-domain augmentation,
L492: We obtained data from 20 participants (14 males and six the dropout ratio is set to 0.1, and for frequency-domain
L493: females) to construct the gesture dataset; the participants have augmentation, the perturbation ratio is set to 0.1. Additionally,
L494: an average age of 22.6 (±2.9) and mostly had backgrounds the temperature parameter τ in the TFSCL module is set to
L495: in computer science. All participants are right-handed. Partic- 0.07.
L496: ipants repeated each gesture approximately 30 times after a The Adam optimizer was employed with a learning rate of
L497: 3-s preparation period for each gesture. Recorded six-channel 1e−4, weight decay of 3e−4, β1 = 0.9, and β2 = 0.99. Given
L498: signals (accelerometer and gyroscope) during executions are the difference in the dataset sizes, a batch size of 64 is applied
L499: transmitted at 200 Hz via Bluetooth low energy (BLE) to a after the pre-experiment. The data are split into 60%, 20%, and
L500: ground station. 20% portions for training, validation, and testing, respectively.
L501: In order to improve the efficiency of labeling and to To ensure robustness, the experiments are repeated five times
L502: obtain more high-quality labeled data, we adopted a semi- with five different random seeds, and the results are reported
L503: automatic data labeling method that consisted of two phases: based on the averages and standard deviations over these runs.
L504: Authorized licensed use limited to: University of Science & Technology of China. Downloaded on July 05,2026 at 10:02:42 UTC from IEEE Xplore. Restrictions apply.
L506: ===== PAGE 8 =====
L508: ZHANG et al.: TIME SERIES CLASSIFICATION BASED ON SUPERVISED CL AND HOMOSCEDASTIC UNCERTAINTY 421
L509: TABLE II writing, HAR represents human activity recognition, and G
L510: DETAILS OF THE SIX DATASETS represents gesture.
L511: C. Experimental Results of the U-TFSCL Framework
L512: In the experiments, a testing method with two test datasets
L513: is used: the standard setting and the leave-one-subject-out
L514: (LOSO) setting. In the standard setting, the test dataset con-
L515: tains subjects who are already included in the training dataset.
L516: Conversely, in the LOSO setup, the test dataset consists of
L517: subjects excluded during the training process. This setting
L518: enables the comprehensive evaluation of the generalization
L519: The model is optimized over 100 training epochs. Reported capability of the model. The LOSO experiment is valuable for
L520: numbers are expressed in percentage values for better reading. evaluating the ability of the model to predict the results of data
```

### Lines 571-777

```text
L571: D. Ablation Experiment
L572: categories, five of which are static (e.g., wave-in and wave-
L573: out) and six are dynamic (e.g., up and down, and left and In this section, the importance of various components of
L574: right movements). Additionally, one gesture in a relaxed state U-TFSCL is evaluated through a series of ablation studies.
L575: is included. Data are collected from 85 users using armband Different model variants were constructed by adjusting and
L576: electromyogram (EMG) sensors and IMUs [45]. removing key modules, and then, a detailed comparative
L577: 6) Gesture-B (Ours): Based on typical HDI tasks, six analysis was performed.
L578: interactive gestures are designed and data are collected from Initially, the model was simplified by removing the MTL
L579: 20 participants (14 males and six females) to construct a module while retaining the TFSCL module. This step allows
L580: dataset of these gestures. The participants were asked to repeat the independent evaluation of the performance of the TFSCL
L581: each gesture set 30 times based on the gesture collection. Dur- module. By gradually adding contrastive task losses, their
L582: ing each experiment, the output signals from the accelerometer impact on the overall framework performance is discussed
L583: and gyroscope of the IMUs were recorded at a sampling rate in depth. Subsequently, the potential of the MTL modules is
L584: of 200 Hz. This resulted in a final dataset containing 45 376 discussed. The complete TFSCL module was added and the
L585: gesture samples. weights of different contrastive tasks within the MTL module
L586: Table II shows the details of the datasets used in the were adjusted. Through this process, we can evaluate the
L587: experiment, including the sampling rates, dataset size, data impact of the weights for different tasks on the performance,
L588: sample length, number of data channels, class numbers, and thereby optimizing them to adapt better to MTL environments.
L589: number of participants in the dataset. AW represents air The final part of the ablation studies mainly explored the
L590: Authorized licensed use limited to: University of Science & Technology of China. Downloaded on July 05,2026 at 10:02:42 UTC from IEEE Xplore. Restrictions apply.
L592: ===== PAGE 9 =====
L594: 422 IEEE TRANSACTIONS ON NEURAL NETWORKS AND LEARNING SYSTEMS, VOL. 37, NO. 1, JANUARY 2026
L595: TABLE III
L596: EXPERIMENTAL RESULTS OF THE U-TFSCL FRAMEWORK
L597: TABLE IV
L598: ABLATION STUDY RESULTS FOR FEATURE FUSION IN THE TFSCL MODULE
L599: impact of instance-level labels on model performance. To frequency-domain contrastive loss, and their combination,
L600: this end, we separately increased the number of labels and respectively. In this loss fusion strategy, the projection layer is
L601: increased the maximum number of positive pairs of the anchor removed from the TFSCL, allowing the features derived from
L602: in the TFSCL module. Furthermore, the impact of different the domain-specific supervision contrastive loss to be concate-
L603: data augmentation ratios and strategies on performance was nated into new features. The features are further processed
L604: discussed. through a fully connected layer to obtain the final prediction
L605: 1) Ablation Experiments of the TFSCL Module: In this probabilities. By contrast, LT + LF + LTF indicates the
L606: sup sup sup
L607: section of the ablation study, a strategy was adopted in which use of a full TFSCL module. The final loss of the model is
L608: the loss weights for different tasks are manually set to be composed of contrastive losses computed within the module
L609: equalized based on the assumption that all tasks are equally and the cross-entropy loss based on the output features of
L610: important to the model during the learning process. The the module. The experiments are conducted using the AW-B
L611: purpose of this strategy is to eliminate any potential effects dataset.
L612: of the MTL module, thereby allowing a clearer evaluation of Table IV shows the impact of different feature fusion
L613: the contribution of each component to the performance of the strategies and combinations of loss functions on the model per-
L614: model. formance. Specifically, within the SCL loss fusion strategies,
L615: We compare the performance of the model with and without the combination of the time-domain loss LT and frequency-
L616: sup
L617: the TFSCL module. Without the TFSCL module, the original domain loss LT outperforms the use of either loss function in
L618: sup
L619: model is simplified into two independent submodels, each isolation. This finding suggests that the time- and frequency-
L620: of which processes the time- and frequency-domain features. domain features are complementary and collectively enhance
L621: The outputs of these submodels are then integrated using the predictive capabilities of the model. The strategy using
L622: specific fusion strategies. Three common fusion strategies are LT + LF was then compared with the fusion strategy
L623: sup sup
L624: investigated: sum, maximum, and concatenation. within the cross-entropy loss function. The results indicate
L625: When using the TFSCL module, LT , LF , and LT +LF a better performance for the former approach, which under-
L626: sup sup sup sup
L627: represent the use of only the time-domain contrastive loss, scores the importance of CL in a time series, highlighting
L628: Authorized licensed use limited to: University of Science & Technology of China. Downloaded on July 05,2026 at 10:02:42 UTC from IEEE Xplore. Restrictions apply.
L630: ===== PAGE 10 =====
L632: ZHANG et al.: TIME SERIES CLASSIFICATION BASED ON SUPERVISED CL AND HOMOSCEDASTIC UNCERTAINTY 423
L633: TABLE V
L634: ABLATION STUDY RESULTS FOR THE MULTITASK LOSS FUSION IN THE MTL MODULE
L635: its ability to capture and learn generalizable representations overall performance and demonstrating its effectiveness across
L636: of time series more effectively. Furthermore, the performance multiple datasets.
L637: of the full TFSCL module is evaluated, which includes the Specifically, in two experiments with different test settings
L638: time–frequency domain consistency loss. Among the seven on the AW-B dataset, the uncertainty-based weight assignment
L639: fusion strategies, the full TFSCL module achieves the highest strategy resulted in an average performance improvement of
L640: scores. approximately 0.5%, a result similar to that in [50], which
L641: Notably, these results are obtained when all the contrastive used a regression task as an auxiliary task to the classification
L642: task weights are equal. Although the potential competitive task with weight assignment based on the respective uncertain-
L643: relationships between these tasks remain to be determined, ties, compared with a single-task setup, which improved the
L644: achieving the highest performance with such a straightforward classification performance by 0.6% compared with a single-
L645: setup indicates that CL within the shared time–frequency task setup. Although the improvement is limited, this strategy
L646: domain can effectively extract more universal representations remains an effective solution for automatically determining
L647: from the series, thereby positively influencing downstream the optimal parameters for multiple tasks. In addition, the
L648: classification tasks. experimental results reveal the specific effects of different
L649: 2) Ablation Experiments of the MTL Module: The full weight assignments on the model performance, which provides
L650: MTL module contains four tasks: the time-domain CL L , valuable insights for further optimization of the model. When
L651: T
L652: the frequency-domain CL L , the time–frequency consistency the weight assignment is biased to the time–frequency consis-
L653: F
L654: CL L , and supervised classification L . To simplify the tency comparison learning, the model demonstrates enhanced
L655: TF pre
L656: capability in capturing cross-domain features, which con-
L657: experimental design in this section, the following strategy
L658: tributes to an improved understanding and generalization of the
L659: is adopted; when manually setting the weights, the time-
L660: relationship across domains. Furthermore, if the weights are
L661: and frequency-domain contrastive losses are merged into the
L662: biased toward the primary classification task, the classification
L663: intradomain contrastive loss and assigned equal weights. When
L664: performance of the model improves slightly. For example,
L665: using the uncertainty-based weighting strategy (i.e., the full
L666: the model performance under the (0.1, 0.1, 0.8) strategy in
L667: MTL module), the weights of each of the four tasks are
L668: the AW-B dataset is superior to that under the (0.8, 0.1,
L669: calculated separately. This design allows clear observations
L670: of how different task weights affected the performance. 0.1) strategy because more weights are assigned to directly
L671: Four sets of different weight settings are manually derived to related tasks. Although manually set weights may result in
L672: discuss the potential impact of different tasks on performance. superior performance in certain scenarios, they are typically
L673: not as effective as dynamic weight assignment strategies
L674: In addition to a setting in which all tasks are equally weighted,
L675: based on task uncertainty, which provide greater flexibility
L676: the other three settings emphasize specific tasks: a weight
L677: and adaptability in automatic adjustments to optimize model
L678: distribution of (0.8, 0.1, 0.1), for the importance of CL in both
L679: performance.
L680: the time- and frequency-domains; a weight distribution of (0.1,
L681: 0.8, 0.1), for the role of cross-domain consistency CL; and a 3) Effect of Labels in TFSCL Module: To investigate the
L682: weight distribution of (0.1, 0.1, 0.8), for directly improving impact of labels on model performance, we generated the
L683: the classification performance of the model. Experiments are contrastive mask by limiting the percentage of labels involved
L684: also conducted on the AW-B dataset. in the calculation of LT , LF , and LTF for each batch and set
L685: sup sup sup
L686: Table V presents the results of the ablation studies on the up five different label percentages: 0%, 25%, 50%, 75%, and
L687: MTL module. The uncertainty-based weight assignment strat- 100%. When the percentage is set to 0%, the contrast methods
L688: egy exhibited the best performance. This may be attributed to degrade to SimCLR [22], and when the percentage is set to
L689: the process of dynamically adjusting the weights for each task 100%, it becomes the standard SCL [25].
L690: and aligning them with the specific attributes of the dataset. Fig. 4(a) illustrates the generation of the matrix M ∈
L691: c
L692: This strategy ensures that the model adapts its focus based on {0, 1}L×L, which is used as the mask to calculate the total
L693: the inherent uncertainties within each task, thereby improving distance within the positive pairs in the batch. Specifically,
L694: Authorized licensed use limited to: University of Science & Technology of China. Downloaded on July 05,2026 at 10:02:42 UTC from IEEE Xplore. Restrictions apply.
L696: ===== PAGE 11 =====
L698: 424 IEEE TRANSACTIONS ON NEURAL NETWORKS AND LEARNING SYSTEMS, VOL. 37, NO. 1, JANUARY 2026
L699: TABLE VI
L700: EFFECT OF DIVERSE AUGMENTATION STRATEGIES
L701: Fig. 4. Effect of the number of labels on performance. (a) Generate mask Mc
L702: by limiting the number of labels involved in the loss calculation. (b) Accuracy
L703: as a function of the percentage of labels. Standard and LOSO mean two test
L704: methods. Red markers represent the best accuracy. Standard and LOSO mean
L705: two test methods.
L706: 4) Effect of the Data Augmentation: In this section, we
L707: compared the effects of different augmentation strategies on
L708: model performance, including different data augmentation
L709: methods and augmentation ratios. Specifically, we increased
L710: the augmentation ratios in our augmentation method (i.e.,
L711: random dropout in the time domain and random perturbation
L712: in the full frequency band) of the original manuscript from
L713: 0.05 to 0.2. Additionally, we compared three commonly used
L714: time series augmentation strategies [51], and the settings
L715: of these strategies were kept consistent with those in the
L716: original article. Considering that all these strategies performed
L717: augmentation in the time domain and were not specifically
L718: Fig. 5. Effect of maximum number of positive pairs per anchor on perfor- designed for frequency-domain features, we applied these aug-
L719: mance in AW-B dataset. Red markers represent the best accuracy. Standard mentation strategies to the original time signal xT to generate
L720: and LOSO mean two test methods. the augmented view x˜T. We then generated the fr i equency data
L721: i
L722: and its augmented view xF = FFT(xT), x˜F = FFT(x˜T) through
L723: i i i i
L724: FFT. Subsequently, these data were fed into the domain-
L725: we segment vectors y of original length L and use only the
L726: specific encoder G to generate embeddings and perform the
L727: first α percentage of data y to generate the subsequence y . D
L728: α following calculations.
L729: Then, we compute the matrix M ∈ {0, 1}αL×αL, where each
L730: y Table VI shows the results, and “-” is used to indicate
L731: element indicates whether the corresponding pair of labels in
L732: the setting consistent with the original article. The dropout
L733: y is identical. The block-diagonal matrix M is formed as the
L734: α c strategy with an augmentation ratio of 0.1 achieves the best
L735: direct sum of M and the identity matrix I ∈ {0, 1}(1−α)L×(1−α)L,
L736: y results, while both higher and lower ratios lead to decreased
L737: denoted M = M ⊕ I.
L738: c y performance. Therefore, we adopt for using a dropout ratio
L739: Fig. 4(b) shows the result. For two test settings, the model
L740: of 0.1 in our method. Additionally, the performance of the
L741: performance improves as the percentage of labels increases.
L742: other three data augmentation strategies was lower than that
L743: Among them, the performance improvement is particularly
L744: of dropout, with the Rotation strategy showing a significant
L745: significant when the label percentage is from 0% to 25%, with
L746: performance gap, of over 8%. This is because randomly flip-
L747: increases of 5.4% and 8.9%. The best performance is achieved
L748: ping the channels of the time series data in this augmentation
L749: when all labels are used.
L750: strategy distorts the semantic information and reduces the
L751: To further investigate how the increase of labels in the
L752: quality of the representation.
L753: TFSCL module improves the performance, the maximum
L754: number of positive pairs per anchor is increased from 1 to
L755: unlimited. Here, 1 signifies the inherent augmented view in
L756: E. Contrast Experiments
L757: CL, while unlimited aligns with standard SCL. Fig. 5 shows
L758: the result. When the maximum number is increased from 1 The U-TFSCL framework was thoroughly evaluated and
L759: to 3, the performance is significantly improved in both tests, compared with classical machine learning algorithms and
L760: which is 6.49% and 13.38%. However, when the maximum SOTA deep learning models to demonstrate its exceptional
L761: number is increased further, the performance enhancement is performance. Baselines were implemented following corre-
L762: not readily apparent. This is attributable to the utilization of sponding studies, including KNN, XG Boost, FCN [52],
L763: a batch size of 64, whereas the AW-B dataset encompasses 1D-Resnet [53], Bi-LSTM [54], TSTformer [55], and Con-
L764: as many as 26 classes. Furthermore, the data distribution vTran [56]. To implement these deep learning models, the
L765: is uniform across all classes, without any long-tailed cases. construction designs presented in the original articles are
L766: Consequently, the number of positive pairs in the batch for strictly followed. For hyperparameters presented in their mod-
L767: each anchor is seldom greater than three. els, but not discussed in this study, consistency was maintained
L768: Authorized licensed use limited to: University of Science & Technology of China. Downloaded on July 05,2026 at 10:02:42 UTC from IEEE Xplore. Restrictions apply.
L770: ===== PAGE 12 =====
L772: ZHANG et al.: TIME SERIES CLASSIFICATION BASED ON SUPERVISED CL AND HOMOSCEDASTIC UNCERTAINTY 425
L773: TABLE VII
L774: AVERAGE ACCURACY OF DIFFERENT MTSC MODELS OVER SIX MULTIVARIATE TIME SERIES DATASETS
L775: with the original papers, while other parameters are adapted
L776: to the settings in this study.
L777: Table VII presents the results of an extensive comparison
```

### Lines 807-857

```text
L807: F. Hyperparameter Sensitivity
L808: CL tasks, which are designed to deeply learn intrinsically
L809: invariant representations of time series. In previous experiments in this article, all of our results used
L810: While further analyzing the performance of the U-TFSCL a temperature of τ = 0.07. Smaller temperatures benefit train-
L811: framework on different datasets, it is observed that although ing more than higher ones, but extremely low temperatures
L812: the framework showed significant performance advantages are harder to train due to numerical instability [29]. Fig. 6
L813: across the other five datasets, such advantages are less sig- shows the performances of two test methods on the AW-B
L814: nificant on the G-B dataset, both on the standard and on datasets. The model achieves the best performance when the
L815: LOSO settings. This result may be attributed to the unique temperature is 0.07 or 0.1. Compared to the contrastive-based
L816: characteristics of the G-B dataset. Specifically, the G-B dataset methods, whose performance tends to present a reverse-U
L817: is created with a sampling rate of 200 Hz, with each time series shape [57]. The performance of U-TFSCL remains stable
L818: sample consisting of only 20 points. This setting implies that after a rise in temperature in two different test methods.
L819: each sample contains only 0.1 s of action segments. Compared This is because models with a large temperature tend to be
L820: to the complete action with an average time length of 1.3 s, more tolerant of semantically consistent samples, leading to
L821: such a short sample length is clearly insufficient to capture the inability to generate uniformly distributed embeddings,
L822: Authorized licensed use limited to: University of Science & Technology of China. Downloaded on July 05,2026 at 10:02:42 UTC from IEEE Xplore. Restrictions apply.
L824: ===== PAGE 13 =====
L826: 426 IEEE TRANSACTIONS ON NEURAL NETWORKS AND LEARNING SYSTEMS, VOL. 37, NO. 1, JANUARY 2026
L827: whereas, in our framework, this uniformity is guaranteed by [3] F. Moya Rueda, R. Grzeszick, G. A. Fink, S. Feldhorst, and M. Ten
L828: the labels. Hompel, “Convolutional neural networks for human activity recognition
L829: using body-worn sensors,” Informatics, vol. 5, no. 2, p. 26, May 2018,
L830: doi: 10.3390/informatics5020026.
L831: [4] W. Gao, H. Jin, and G. Yang, “Series arc fault diagnosis method
L832: G. Computational Cost Analysis
L833: of photovoltaic arrays based on GASF and improved DCGAN,” Adv.
L834: The computational cost of U-TFSCL was evaluated. The Eng. Informat., vol. 54, Oct. 2022, Art. no. 101809, doi: 10.1016/
L835: j.aei.2022.101809.
L836: U-TFSCL, which includes two transformer blocks in each
L837: [5] Y. He, C. Zhao, and W. Shen, “Cross-domain compound fault diagnosis
L838: domain-specific encoder, has a total of 0.86 million of trainable
L839: of machine-level motors via time–frequency self-contrastive learning,”
L840: parameters. During inference, the GPU memory usage was IEEE Trans. Ind. Informat., vol. 20, no. 7, pp. 1–10, Jul. 2024, doi:
L841: 11.46 MB, and the throughput reached 1.67 kf/s. After training 10.1109/TII.2024.3384603.
L842: [6] Y. Xu, S. Biswal, S. R. Deshpande, K. O. Maher, and J. Sun, “RAIM:
L843: with the G-B dataset and conducting real-world tests, the
L844: Recurrent attentive and intensive model of multimodal patient monitor-
L845: system’s delay was approximately 0.4 s. This delay includes ing data,” in Proc. 24th ACM SIGKDD Int. Conf. Knowl. Discovery Data
L846: data preprocessing, BLE data transmission time, and inference Mining, Jul. 2018, pp. 2565–2573, doi: 10.1145/3219819.3220051.
L847: [7] H. P. Gupta, H. S. Chudgar, S. Mukherjee, T. Dutta, and K. Sharma,
L848: time. These results demonstrate the potential of the framework
L849: “A continuous hand gestures recognition technique for human-
L850: for practical applications in real-world scenarios. The compu- machine interaction using accelerometer and gyroscope sensors,” IEEE
L851: tations were performed on a machine equipped with an Intel Sensors J., vol. 16, no. 16, pp. 6425–6432, Aug. 2016, doi: 10.1109/
L852: JSEN.2016.2581023.
L853: i7 2.5-GHz CPU and 64 GB of RAM.
L854: [8] Y.-T. Liu, Y.-A. Zhang, and M. Zeng, “Novel algorithm for hand
L855: gesture recognition utilizing a wrist-worn inertial sensor,” IEEE
L856: Sensors J., vol. 18, no. 24, pp. 10085–10095, Dec. 2018, doi: 10.1109/
L857: V. CONCLUSION
```
