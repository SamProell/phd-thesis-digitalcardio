# [working title] Detecting cardiovascular diseases with smartphones and AI

## Introduction
Cardiovascular diseases are the leading cause of mortality worldwide, accounting
for 1.71 million deaths in 2021 in Europe alone[^eurostat].
Early detection of heart disease can improve patient outcome and
reduce the burden on the health care system[^health-economic].
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

## State of the art
### The smartphone as a tool for cardiac screening
The smartphone has become increasingly important as a tool for health
screening[^moses2022]. By now, most of the population, including the elderly own a
smartphone with capable sensors. In the literature, we find several different approaches
to obtain and interpret cardiac signals from smartphones.
In a recent study, Haddad et al. (2024) used the gyroscope and accelerometer sensors
on smartphones to record the cardiac vibrations of the chest. They are able to identify
patients with stage C heart failure with an AUC of 0.95 using basic features extracted
from the vibration signals. [^haddad2024]
Several studies have shown that smartphone-based screening for atrial fibrillation is
possible. Rizas et al. (2022) obtained a signal of the heart rhythm through camera-based
finger PPG. Participants placed their finger on the camera module and the camera
recorded the changes in color introduced by blood volume changes with each heart beat.
[^rizas2022]

Only little literature is available on using smartphones for heart auscultation. Most
studies rely on a separate (digital) stethoscope to acquire heart sound signals.
For example, Makimoto et al. (2022) showcase a deep learning-based solution for
classification of aortic valve stenosis that can run on a smartphone ($F_1=0.93$).
Phonocardiography data is recorded with a digital stethoscope and then transferred to
the app.

### Modern approaches in artificial intelligence
To build robust deep learning algorithms even from a small set of labelled data,
many researchers turn towards self-supervised learning (SSL) with unlabelled data for
pretraining.
This approach has recently seen increased attention due to the success of large language
models, which heavily rely on SSL. [^gui2024]
TODO more here

- SotA architectures

## Methods
First, we use sensors available in consumer smartphones to acquire cardiac signals.
Sensors available in most smartphones are gyroscopes and accelerometers, cameras and
microphones.
Several different recording scenarios are to be devised and tested.
Preliminary tests will reveal, which sensors are most suitable for specific tasks and
which measurement protocols are appropriate to gather strong signals.
Multiple factors have to be considered such as sensor placement, patient position,
expected patient behavior and measurement duration.


## Planned activities and next steps


[^eurostat]: EuroStat: Cardiovascular diseases statistics, accessed on Sep 25, 2024 at
    https://ec.europa.eu/eurostat/statistics-explained/index.php?title=Cardiovascular_diseases_statistics#Deaths_from_cardiovascular_diseases
[^health-economic]: Oude Wolcherink, M.J., Behr, C.M., Pouwels, X.G.L.V. et al. Health
    Economic Research Assessing the Value of Early Detection of Cardiovascular Disease:
    A Systematic Review. PharmacoEconomics 41, 1183–1203 (2023).
    <https://doi.org/10.1007/s40273-023-01287-2>
[^haddad2024]: Haddad, F., Saraste, A., Santalahti, K. M., P, änkäälä M., Kaisti, M., Kandolin,
      R., Simonen, P., Nammas, W., Jafarian, D. K., Koivisto, T., Knuuti, J., Mahaffey,
      K. W., & Blomster, J. I. (2024). Smartphone-Based Recognition of Heart Failure by
      Means of Microelectromechanical Sensors. JACC: Heart Failure, 12(6), 1030–1040.
      <https://doi.org/10.1016/j.jchf.2024.01.022>
[^moses2022]: Moses, J. C., Adibi, S., Wickramasinghe, N., Nguyen, L., Angelova, M., &
    Islam, S. M. S. (2022). Smartphone as a Disease Screening Tool: A Systematic Review.
    Sensors, 22(10), 3787. <https://doi.org/10.3390/s22103787>

[^rizas2022]: Rizas, K.D., Freyer, L., Sappler, N. et al. Smartphone-based screening for
    atrial fibrillation: a pragmatic randomized clinical trial. Nat Med 28, 1823–1830
    (2022). <https://doi.org/10.1038/s41591-022-01979-w>
[^gui2024]: Gui, J., Chen, T., Zhang, J., Cao, Q., Sun, Z., Luo, H., & Tao, D. (2024).
    A Survey on Self-supervised Learning: Algorithms, Applications, and Future Trends.
    In IEEE Transactions on Pattern Analysis and Machine Intelligence (pp. 1–20).
    Institute of Electrical and Electronics Engineers (IEEE).
    <https://doi.org/10.1109/tpami.2024.3415112>
