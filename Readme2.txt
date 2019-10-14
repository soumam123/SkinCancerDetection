
Melanoma, most threatening type of skin cancer,
is on the rise. In this paper an implementation of a deep-
learning system on a computer server, equipped with graphic
processing unit (GPU), is proposed for detection of melanoma
lesions. Clinical (non-dermoscopic) images are used in the
proposed system, which could assist a dermatologist in early
diagnosis of this type of skin cancer. In the proposed system,
input clinical images, which could contain illumination and
noise effects, are preprocessed in order to reduce such artifacts.
Afterward, the enhanced images are fed to a pre-trained
convolutional neural network (CNN) which is a member of
deep learning models. The CNN classifier, which is trained by
large number of training samples, distinguishes between
melanoma and benign cases. Experimental results show that
the proposed method is superior in terms of diagnostic
accuracy in comparison with the state-of-the-art methods.



Melanoma, also referred to as malignant melanoma, is a
type of skin cancer caused by abnormal multiplication of
pigment producing cells that give color to the skin [1].
Despite significant death rate, early stage detected melanoma
is curable in most cases [2]. Meanwhile differentiation
between melanoma and other benign moles in their initial
growth phases is a challenging task even for experienced
dermatologists [3]. Computerized algorithms are being
developed for this purpose. Some low complexity methods
are designed, which are intended for running on tablets and
smartphones, and can help non-specialists. But professional
decision making, in this regard, requires sophisticated
algorithms and equipment. There are various methods in
dermatology such as ABCD (asymmetry, border irregularity,
color patterns, and diameter) rule [4] and the seven-point
checklist [5] that guide physicians in this task. Figure 1
shows the general structure Automated analysis of pigmented lesions is a growing
research topic that aims to develop tools for computer aided
diagnosis of skin cancer [6]. Reviews of researches done in
this field are given in [6] and [7].
Recently there has been an emerging trend for automatic
diagnosis of melanoma using conventional digital cameras
[8-14]. This can be applicable in web based and mobile
application as a telemedicine tool and also as a supporting
system that assists physicians. Computerized diagnosis is a
rising need due to increasing rate of incident, subjectivity of
procedure and time and cost expenses [11].
A decision support system was proposed by Alcon et al.
that takes advantage of image processing techniques for
evaluation of skin lesions [8]. It also uses some background
information of patient before the diagnosis is made.
Cavalcanti et al. proposed an automatic classification system
that consists of preprocessing, segmentation and feature
extraction steps. In order to reduce miss rate of melanoma
cases (false negative cases), a two stage classifier has been
proposed that rechecks the lesions labeled as benign [10].
Works of [9] and [10] try to estimate the four criteria of the ABCD rule by extracting a set of low level features. Amelard
et al. proposed a set of high level features that intuitively
describes ABCD characteristics [11]. Giotis et al. proposed a
computer aided system that performs some preprocessing for
enhancing the quality of the image [12]. Then, some color
and texture features of lesions are extracted automatically.
Afterward, a set of attributes are provided by the examining
physician and the final diagnosis is made by voting among
observed and automatically extracted descriptors. Examples
of commercial applications that exist in this field can be
found in [13] and [14].
Deep learning approaches have shown promising results
in some applications such as natural language processing
[15], speech recognition and recently in computer vision
areas such as object tracking [16], object detection [17], and
image classification [18]. Deep learning mechanisms can
learn set of high level features from low level ones and gain
high accuracy for classification applications without the need
for extracting handcrafted features. Especially there has been
a trend for taking advantage of superior power of deep
learning methods in medical imaging tasks [19-21].
Convolutional neural network (CNN) is a type of deep
learning method where trainable filters and pooling
operations are applied on the raw input images, extracting set
of complex high level features automatically [22].
In this paper we aim to take advantage of deep learning
methods to form an automatic diagnosis system for
melanoma detection. For this purpose the input digital
images, usually subjected to noise and illumination effects,
are preprocessed. This preprocessing effectively helps CNN
extract discriminative features from the images. Afterward,
the images are fed to a CNN architecture to classify the input
as melanoma or benign. In order to deal with the limitations
of the training dataset and relatively low number of images,
some approaches such as rotation, cropping, and resizing of
dataset images are considered that increase the number of
samples. The experimental results show that the proposed
system can outperform comparable state-of-the-art methods.
The rest of this paper is organized as follow. In Section II,
the proposed method is explained in details. Experimental
results of quantitative evaluation of our method are presented
in Section III. Section IV concludes the paper.
