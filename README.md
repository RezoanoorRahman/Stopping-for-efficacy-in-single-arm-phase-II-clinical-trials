# Overview
This is the codes I used for the research work named as Stopping for efficacy in single-arm phase II clinical trials. The published article can be found at https://www.tandfonline.com/doi/full/10.1080/02664763.2021.1904846 .
In this research, a new Phase II clinical trial design has been introduced which is actually a derivative of two previously introduced clinical trial designs:

- Mander and Thompson (2010) 
- Lin and Shih (2004)

This two designs are generally extension of popular Simon's design. Simon's two stage design has the option to stop in the first stage if the response from the patiets is less than a certain threshold ie because of futility. Mander and Thompson, in addition to that, implemented a rule so that the design has an option of stopping because of efficacy, if the response is more than another threshold.

Simon considered only one target response rate in his design. Lin and Shih proposed a design that has the feasilibility to consider two target response rates based on the response from the patients in the first stage.

In our article, we proposed a design that consideres two target response rates and that the option to stop for both futility and efficacy for both target response rates in the first stage.

# Libraries Used
Throughout this research, programing language **R** is used and the list of packages those have been used are given below:
- **parallel**
- **foreach**
- **iterators**
- **doParallel**
- **tidyverse**

The associated R scripts can be found by going through: https://drive.google.com/drive/folders/1nGRsoibQEQ_fW_X_kVeq3AWfDHN3m7s0
The folder is kept private. If you require these scrips, please send me a message with proper justification.

# Brief description of the scrips
- **one_stage_sample.R** script contains the codes for computing a single stage optimal design. The other scripts has a dependency on this to bound the range of maximum values to be considered.
- **Simon.R** script contains the codes for computing Simon's two-stage design.
- **Mander_Thompson.R** script contains the codes for computing Mander and Thomspon's designs. The codes are self-written and the output results have been verified by matching with Mander and Thompson's article.
- **Lin_Shih.R** script contains the codes for computing Lin and Shih's designs. The codes are also self-written and the output results have been verified by matching with Lin and Shih's article.
- **Proposed.R** script contains codes for computing our proposed design.


# Abstract
Phase II clinical trials investigate whether a new drug or treatment has sufficient evidence of effectiveness against the disease under study. Two-stage designs are popular for phase II since they can stop in the first stage if the drug is ineffective. Investigators often face difficulties in determining the target response rates, and adaptive designs can help to set the target response rate tested in the second stage based on the number of responses observed in the first stage. Popular adaptive designs consider two alternate response rates, and they generally minimise the expected sample size at the maximum uninterested response rate. Moreover, these designs consider only futility as the reason for early stopping and have high expected sample sizes if the provided drug is effective. Motivated by this problem, we propose an adaptive design that enables us to terminate the single-arm trial at the first stage for efficacy and conclude which alternate response rate to choose. Comparing the proposed design with a popular adaptive design from literature reveals that the expected sample size decreases notably if any of the two target response rates are correct. In contrast, the expected sample size remains almost the same under the null hypothesis.
