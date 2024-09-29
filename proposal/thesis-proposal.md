---
title: "Detecting cardiovascular diseases with smartphones and AI"
subtitle: (working title) Thesis proposal
author: Samuel Pröll [samuel.proell@i-med.ac.at](mailto:samuel.proell@i-med.ac.at)
date: September 2024
geometry:
  - top=30mm
  - left=25mm
papersize: a4
--- 

# Introduction
Cardiovascular diseases are the leading cause of mortality worldwide, accounting
for 1.71 million deaths in 2021 in Europe alone [@EuroStat_cardiovascular_2024].
Early detection of heart disease can improve patient outcome and
reduce the burden on the health care system [@OudeWolcherink_health_2023].
At the same time, advances in sensing technology, information processing and artificial
intelligence offer new ways to identify patients at risk and diagnose diseases.
This work will explore ways to incorporate artificial intelligence into various steps
along the clinical pathway.

First, we leverage sensors available in consumer smartphones
to capture different cardiac signals. We can then apply signal processing and machine
learning to identify heart diseases. This paths the way towards solutions for
accessible cardiac screening and risk prediction.
Second, we implement and extend state-of-the-art solutions in artificial intelligence
for processing multi-modal clinical data. Utilizing modern approaches like
self-supervised pretraining and foundation models, we can build reliable and
(data-)efficient algorithms.

# State of the art
## The smartphone as a tool for cardiac screening
The smartphone has become increasingly important as a tool for health
screening [@Moses_smartphone_2022]. By now, most of the population, including the elderly own a
smartphone with capable sensors. In the literature, we find several different approaches
to obtain and interpret cardiac signals from smartphones.
In a recent study, Haddad et al. (2024) used the gyroscope and accelerometer sensors
on smartphones to record the cardiac vibrations of the chest. They are able to identify
patients with stage C heart failure with an AUC of 0.95 using basic features extracted
from the vibration signals. [@Haddad_smartphonebased_2024]
Several studies have shown that smartphone-based screening for atrial fibrillation is
possible. Rizas et al. (2022) obtained a signal of the heart rhythm through camera-based
finger PPG. Participants placed their finger on the camera module and the camera
recorded the changes in color introduced by blood volume changes with each heart
beat.&nbsp;[@Rizas_smartphonebased_2022]

Only little literature is available on using smartphones for heart auscultation. Most
studies rely on a separate (digital) stethoscope to acquire heart sound signals.
For example, Makimoto et al. (2022) showcase a deep learning-based solution for
classification of aortic valve stenosis that can run on a smartphone ($F_1=0.93$).
Phonocardiography data is recorded with a digital stethoscope and then transferred to
the app.

## Modern approaches in artificial intelligence
To build robust deep learning algorithms even from a small set of labelled data,
many researchers turn towards self-supervised learning (SSL) with unlabelled data for
pretraining.
This approach has recently seen increased attention due to the success of large language
models, which heavily rely on SSL. In SSL pretraining, a so-called pretext task is
devised, for which samples can be generated on the fly from unlabelled data. Examples
include contrastive learning, where a model needs to identify whether a pair of
augmented samples originate from the same or different instances. In other pretext
tasks, the model may be required to identify or even inverse an applied
transformation.&nbsp;[@Gui_survey_2024]

Using such techniques, researchers build towards foundation models, which offer a strong
backbone for data processing, that can be extended or fine-tuned to solve specific
tasks. An example application is given by Abbaspourazad et al. (2024) who built a
foundation model on ECG and PPG data from wearable devices. The model was able to encode
participant characteristics such as demographics and health conditions without being
specifically trained on these targets.&nbsp;[@Abbaspourazad_largescale_2024]

Extensive research in deep learning technology over the past 10+ years has yielded
many promising architectures that are suitable for multi-modal clinical data.
Moor et al. (2023) envision so-called generalist medical AI, in which any modality is
translated into tokens in a shared latent space. The stream of tokens can then be fed
into a sequence model such as a transformer.&nbsp;[@Moor_foundation_2023]

# Methods
In an effort to combine state-of-the-art deep learning with smartphone-based cardiac
signals, we must identify and leverage useful data sources.
Sensors available in most smartphones are gyroscopes and accelerometers, cameras and
microphones.
We build a smartphone application capable of acquiring data from these sensors in
a customizable manner.
Before gathering a dataset, different recording scenarios need to be devised and tested.
Preliminary explorations will reveal, which sensors are most suitable for specific tasks
and which measurement protocols are appropriate to obtain strong signals.
Multiple factors have to be considered such as sensor placement, patient position,
expected patient behavior and measurement duration.

Besides generating new data, we may also use existing data (public and internal) for
working towards improved biosignal and image processing methods. By building models
for larger datasets, we can lay the groundwork for improved outcomes on newly generated
data.
To this end, we can employ transfer learning to fine-tune the developed
models on smartphone-based data.
When designing these deep learning solutions, an important trade-off must be
considered between model performance and computational requirements.
While larger models are expected to show good performance, they also pose higher demands
on computational and memory resources.
Especially when considering the potential for on-device applications, models should be
designed as small as possible.

# Goals and next steps
The goals of this work can be summarized as follows:

- Build a dataset of smartphone-based cardiac signals, corresponding reference signals
  and patient characteristics. For this, we build a customizable smartphone application
  capable of acquiring data from on-device sensors such as accelerometers and
  microphone. 
- Implement and extend state-of-the-art models for processing multi-modal (clinical)
  data from various sources for cardiac diagnostics and risk scoring.
- Develop digital biomarkers and corresponding algorithms for smartphone-based screening
  of relevant cardiac diseases.

In order to achieve these goals, the following steps are in progress or planned for the
near future:

- Extend the literature review on both smartphone-based cardiac screening
  and state-of-the-art solutions for multi-modal data processing.
- Finalize initial development of the data acquisition application. A rough prototype
  is already built but it is missing some features regarding stability, user feedback 
  and data accessibility.
- Perform first tests to validate usability of smartphone-based biosignals. By capturing
  smartphone data in parallel with reference clinical signals (ECG, PPG, etc.), we can
  determine the usefulness of different sensors, sensor placements and recording
  scenarios. Using these results we devise recording protocols that could be applied on
  a larger scale.
- Identify suitable data sources (public and internal) and corresponding clinical
  challenges that can be addressed with modern approaches in artificial intelligence.

# References
