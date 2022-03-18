# covidcxr-hackathon

This is the solution of the [covidcxr-hackathon](https://ai4covid-hackathon.it) submitted by Edoardo Coppola and Damiano Ferrari. We [won](https://ai4covid-hackathon.it/accresults) the **1st prize for explainability** and the **3rd prize for accuracy**!

We would not have achieved this result without Prof. Alberto Signoroni and Dr. Mattia Savardi of the University of Brescia.

## Our approach

Our work is based on [BrixIA](https://brixia.github.io), which is an end-to-end neural network for predicting, on Chest X-rays images (CRX), a multi-regional score conveying the degree of lung compromise in COVID-19 patients.

We splitted the work into two parts. In the first one we used [BSNet](https://github.com/BrixIA/Brixia-score-COVID-19) [1] to process the images of the dataset and compute the so-called "Brixia-score" [2]. It is a scoring system which helps both quantifying and locating lung abnormalities. The Brixia-score is then used both for explainability and as an additional feature of the dataset employed in the training of a classical machine learning model. This phase, after a missing data handling strategy and a feature selection, involved several models: Decision Trees, Support Vector Machines, Extra Trees, Extreme Gradient Boosting and Random Forests. The latter category of classifiers produced the best results in terms of both balanced accuracy, sensitivity and specificity.

More details could be found on the solution description in this repository.


## The hackathon

*One of the major issues raised during the Covid-19 crisis is the additional burden on healthcare infrastructure, often nearing or surpassing treatment capacities. Automatic or semi-automatic techniques to distinguish patients that can be safely home-treated from those that are likely to require intensive care would allow for better planning and smarter allocation of available resources. Artificial Intelligence, and more specifically machine learning applied on clinical data could be a reliable answer to this demand. To this end, the Covid CXR Hackathon aims at designing effective solutions based on machine learning and data science supporting the medical doctor to formulate a Covid-19 prognosis from early chest X-ray images and clinical data collected during triage. One of the main challenges of this hackathon will be the need for processing from several different structures upon first hospitalization. This was done in near-emergency conditions during the first outbreak in Northern Italy. Hence, image quality (and format) is highly variable and clinical data, despite best intentions, is incomplete. Therefore, any developed approach will have to deal with missing data. This hackathon targets finding solutions relying on both sets of data, with a heavy emphasis on image analysis. Solutions not using CXR images will not be considered.*

*The Hackathon proposal is supported by the Labs of Learning and Intelligence Systems, and the ELLIS units of Genoa (Italian Institute of Technology and University of Genova), of University of Modena and Reggio Emilia and Technion University as well as the Bruno Kessler Foundation. The Hackathon is endorsed by Bracco Imaging and Centro Diagnostico Italiano (CDI) and the ITALIAN CINI-AIIS (National Laboratory of Artificial Intelligence and Intelligence Systems). The event is also supported by NVIDIA that will provide Computational Facilities during the hackathon.*

## Bibliography
[1] A.Signoroni, M. Savardi et al. "BS-Net: learning COVID-19 pneumonia severity on a large Chest X-Ray dataset", Medical Image Analysis, 2021

[2] A. Borghesi, R. Maroldi "COVID-19 outbreak in Italy: experimental chest X-ray scoring system for quantifying and monitoring disease progression", La radiologia medica, 2020