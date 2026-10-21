# [Class-Independent Modulation Identification]A M-QAM signal modulation identification algorithm under an AWGN channel[with MATLAB code]

Introduction\tIn novel communication systems, effective information transmission can be achieved with clear signals modulated in various ways. Modulation identification is an intermediate process that must be implemented before signal demodulation and information detection, representing the essential characteristic of modern radio systems: providing knowledge about the modulated signal rather than just signal demodulation. It can be used for civilian and military applications such as cognitive radio, signal recognition, threat assessment, spectrum perception, and management, thereby more effectively utilizing available spectrum and enhancing data transmission speeds. Moreover, unknown signal classification is a decisive weapon in electronic warfare scenarios. The Electronic Support Management System plays a crucial role as a source of information needed for electronic countermeasure suppression, threat analysis, warnings, and target acquisition.
Specialized identification of modulation is the recognition of the type of transmitted signals within a non-cooperative channel environment, which is of significant importance for subsequent signal demodulation and data extraction. This is considered the main direction of automatic modulation classification (AMC), attracting researchers as an attractive topic. However, it poses a significant challenge for engineers working with software-defined radio systems (SDRS) and transmission deviations. In the context of electromagnetic spectrum congestion, providing complex information services and systems for military applications is a primary concern for communication engineers. Allies' signals must be safely sent and received, while enemy signals should be detected and interfered [1].
[2] provides the first foundational theory of AMC, the basic idea proposed by Stanford University since 1969, which has been widely used as an integral part of intelligent radio system internal design and is well known among communication engineers [3,4].
Currently, in non-cooperative channel environments, digital modulation recognition algorithms can be categorized into two types: decision theory-based maximum likelihood hypothesis methods [5] and statistical pattern recognition relying on feature extraction ideas. Pattern recognition techniques are commonly used in practical applications due to the lack of prior knowledge from received modulated signals [8]. This recognition method is particularly beneficial for initial mode recognition from data vectors and signal modulation patterns, which is completed when the coverage between feature parameters and extracted features is achieved, and the feature is considered as a known pattern of modulation type [9].
In the past five years, with the development of automatic digital modulation recognition algorithms research, a new modulation classification technique has been proposed, showing a trend towards complex signal sets and high-order modulation signals. The most commonly used features are high-order cumulants (HOC) and high-order moments (HOM) [10]. Based on HOC technology shows superior performance in classifying digital modulated signals under low signal-to-noise ratio (SNR); these algorithms are documented in literature [11-13]. However, they are not suitable for classifying high-order M-QAM modulation formats. The constellation shape varies from one modulated signal type to another to be considered as a robust signature.
Algorithms in literature [14-16] use constellation shapes to recognize various types of high-order modulations, including 8-PSK and 16-QAM. Recognition rates are around 95%, but still require a higher SNR, up to 4 dB. However, constellation shapes can be divided into M-PSK and M-QAM, and they are sensitive to several wireless channels that generate severe overlap during operation, including frequency offset, phase rotation, and application of roll-off filters. In such cases, the symbol rate and frequency offset settings must be more accurate within the presentation cycle, while the most widely used features are cyclic spectrum and cyclic frequency, which can help detect multiple unwanted signals with each time-based and frequency-based overlap [17-20].
In 2012, Dobber and his colleagues [21] proposed two new algorithms to identify 4-QAM, 16-QAM, -QAM, and QAMV.29 modulation schemes; other authors [22, 23] suggested using the higher order cyclic prefix (CCS) obtained from the received signal as a feature for modulation classification. Additionally, [24] presented a method for classifying multiple N-class problems using a hybrid modulation scheme, which achieved significant performance within the low SNR range. Due to the development of algorithms in machine learning, researchers have begun designing classification algorithms based on certain aspects of machine learning, enhancing classification capabilities and further improving classifiers for distinguishing modulation signal types.
Research on the behavior of hidden Naive Bayes (HNB) [25] and studies combining Naive Bayes (NB) with other types of classifiers to create a new classifier called Multi-Classifier [26] demonstrate that this type of classifier is very effective compared to traditional classifiers when trained with fewer iterations.
Based on four well-known optimization algorithms, the combination of supervised learning techniques with improved K-Means algorithm represents a new generation of AMC technology. Similarly, Norouz and his colleagues [27] studied and considered Artificial Neural Networks (ANN) based on genetic algorithms, and Support Vector Machine (SVM) classifiers were also researched and considered in [28, 29].
When there is limited prior information about signal features, methods based on artificial neural networks and Support Vector Machines show better performance. However, it requires multiple training samples and a longer training period to complete sufficient learning, which increases computational complexity and prolongs processing time.
Over the past five years, researchers have extensively explored new technologies to reduce the required signal-to-noise ratio (SNR) and improved recognition capabilities by focusing on robust features and the design of classifiers. One of the drawbacks of previous algorithms is that due to the characteristics proposed by the authors, decision trees inherently require a fixed threshold, which are highly sensitive to any changes in SNR, allowing the threshold to be effective within a small range around 10 dB above the SNR. However, up to now, no work has focused on identifying high-order QAM signals based on the shape of the feature distribution curve.
In fact, this assumption well understands the system behavior and reflects their main trends; therefore, in the case of an AWGN channel, this paper derives the cumulants as a relationship between the extracted features and the threshold level to evaluate the performance of M-QAM modulation recognition technology.
Algorithm and Simulation Performance Analysis: The logarithmic function was used to derive and refine the four HOC parameters mentioned above to achieve optimal recognition quality for M-QAM signals in an AWGN channel. However, the basic process of automatic modulation classification systems is shown in Figure 5 [31], while the actual decision process of the proposed algorithm is shown in Figure 6, and the logarithmic modulation recognition method is effective for 9 sets of M-QAM signals. The feature distribution curves shown in Figure 1-4 display the extracted modulation format features. Feature extraction is an important step in pattern recognition methods. Then, the threshold setting can be determined based on the distribution conditions of the extracted features. The threshold levels are determined by the projections of two lines with effective space, to avoid misclassification. These lines are parallel to the SNR axis (within a certain SNR range). The created clusters are used to separate the required class distribution samples (modulation formats to be distinguished). These points are empirically calculated on the y-axis (feature distribution level), and even under the minimum SNR condition, it can provide an efficient recognition rate.
Table 1 represents the feature thresholds set according to experience. The boolean equations (12)-(16) illustrate the logic decision process, while Figure 7 shows the block diagram of the M-QAM logarithmic identification algorithm, which is an extension of the proposed method that can be easily implemented in real time.
\t  
\t  
\t  
\t  
\t  
\t  
\t  
\t  
\t  
\t  
\t  
\t  
\t  
\t  
\t  
\t  
\t  
\t  
\t  
Conclusion A classifier based on cumulative quantities and fixed threshold natural logarithm features is proposed to handle the modulation identification of high order M-QAM signals under AWGN influence in channel environment.
The combination of higher-order cumulants and logarithmic functions has created a new generation of classifiers based on cumulants, capable of providing superior performance in classifying high-order M-QAM signals even within the low signal-to-noise ratio range.
The simulation results show that, under the additive Gaussian white noise, when the signal-to-noise ratio is 4db, the correct classification rate can reach more than 92% even in different fading channels.
\tAccording to comparison with the algorithms proposed in recent literature, the performance of log classifier is effective and its complexity is lower.
MATLAB simulation results

## Images

![Class-Independent Modulation Identification - A M-QAM Signal Modulation Identification Algorithm under an AWGN Channel [with MATLAB Code]](01.jpg)
![Class-Independent Modulation Identification - A M-QAM Signal Modulation Identification Algorithm under an AWGN Channel [with MATLAB Code]](02.jpg)
![Class-Independent Modulation Identification - A M-QAM Signal Modulation Identification Algorithm under an AWGN Channel [with MATLAB Code]](03.jpg)
![Class-Independent Modulation Identification - A M-QAM Signal Modulation Identification Algorithm under an AWGN Channel [with MATLAB Code]](04.jpg)
![Class-Independent Modulation Identification - A M-QAM Signal Modulation Identification Algorithm under an AWGN Channel [with MATLAB Code]](05.jpg)
![Class-Independent Modulation Identification - A M-QAM Signal Modulation Identification Algorithm under an AWGN Channel [with MATLAB Code]](06.jpg)
![Class-Independent Modulation Identification - A M-QAM Signal Modulation Identification Algorithm under an AWGN Channel [with MATLAB Code]](07.jpg)
![Class-Independent Modulation Identification - A M-QAM Signal Modulation Identification Algorithm under an AWGN Channel [with MATLAB Code]](08.jpg)
![Class-Independent Modulation Identification - A M-QAM Signal Modulation Identification Algorithm under an AWGN Channel [with MATLAB Code]](09.jpg)
![Class-Independent Modulation Identification - A M-QAM Signal Modulation Identification Algorithm under an AWGN Channel [with MATLAB Code]](10.jpg)
![Class-Independent Modulation Identification - A M-QAM Signal Modulation Identification Algorithm under an AWGN Channel [with MATLAB Code]](11.jpg)
![Class-Independent Modulation Identification - A M-QAM Signal Modulation Identification Algorithm under an AWGN Channel [with MATLAB Code]](12.jpg)
![Class-Independent Modulation Identification - A M-QAM Signal Modulation Identification Algorithm under an AWGN Channel [with MATLAB Code]](13.jpg)
![Class-Independent Modulation Identification - A M-QAM Signal Modulation Identification Algorithm under an AWGN Channel [with MATLAB Code]](14.jpg)
![Class-Independent Modulation Identification - A M-QAM Signal Modulation Identification Algorithm under an AWGN Channel [with MATLAB Code]](15.jpg)
![Class-Independent Modulation Identification - A M-QAM Signal Modulation Identification Algorithm under an AWGN Channel [with MATLAB Code]](16.jpg)
![Class-Independent Modulation Identification - A M-QAM Signal Modulation Identification Algorithm under an AWGN Channel [with MATLAB Code]](17.jpg)
![Class-Independent Modulation Identification - A M-QAM Signal Modulation Identification Algorithm under an AWGN Channel [with MATLAB Code]](18.jpg)
![Class-Independent Modulation Identification - A M-QAM Signal Modulation Identification Algorithm under an AWGN Channel [with MATLAB Code]](19.jpg)
![Class-Independent Modulation Identification - A M-QAM Signal Modulation Identification Algorithm under an AWGN Channel [with MATLAB Code]](20.jpg)
![Class-Independent Modulation Identification - A M-QAM Signal Modulation Identification Algorithm under an AWGN Channel [with MATLAB Code]](21.jpg)
![Class-Independent Modulation Identification - A M-QAM Signal Modulation Identification Algorithm under an AWGN Channel [with MATLAB Code]](22.jpg)
![Class-Independent Modulation Identification - A M-QAM Signal Modulation Identification Algorithm under an AWGN Channel [with MATLAB Code]](23.jpg)

<!-- PAYMENT_BLOCK -->

## Get this dataset

- Payment link (Stripe): [Buy now](https://buy.stripe.com/3cs8yP7sY87d0vu9AB)
- Payment QR code: ![Payment QR code](pay.png)

<!-- /PAYMENT_BLOCK -->
