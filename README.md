# sci-claim-check

This repo is used to share the ready-to-open-sourced files that our group used to complete the Scientific Claim Check competation in the course of Machine Learning, Singapore Management University. 

The competation link is in: https://codalab.lisn.upsaclay.fr/competitions/2043

Our group achieved the second place of the Phase 1 (score of 0.9870) and fourth place in Phase 2 (score of 0.8054)

Scientific claim checking is a task in which the veracity of a claim is verified against sentences that support or refute this claim. In this project, the task is formulated as a 3-class classification, i.e., NOINFO (no information), SUPPORT (supporting the claim), and CONTRADICT (refuting the claim), given a claim sentence and an evidence sentence. We are required to design and train a model to predict whether a given evidence sentence supports, refutes, or is irrelevant to the given claim.  

Timeline
- 24 Feb 2022: Public leaderboard opens (max 10 submissions per day).
- 3 Mar 2022: Optional workshop to provide basics to get started on the project.
- 26 Mar 2022, 23:59 SGT: Public leaderboard closes. Private test data released (open for 2 submissions total).
- 2 Apr 2022, 23:59 SGT: Private test submission is due. Project report is due.
- 7 Apr 2022: Top teams may be invited to present their solutions in class.

## Interesting findings
the first place of phase 1 (score of 0.9930), they applied the subsampling & ensambling training techniques, which works excellent for phase 1 but very bad (score of 0.6494) for phase 2.

the first place of phase 2 (score of 0.8723), they applied the DeBERTa v3 model only to achieved the best place for larger testing dataset scenario. The pre-trained model is actually the best option considering the relatively less training data and lager testing dataset. Their performance in phase 1 is also good 0.9545 (third place).

And there is another group applied one insteresting sturcture using the emsambling training + roberta, they achieved 0.9221 of phase 1 (fourth place) and 0.8611 of phase 2 (second place). 

As for our group, we simply tested the capability of data augmentation via adding more training data to the model. (basice roberta-large, sentence pair classification)

## code explanations
The traditional models are derived and modified based on one ABSA model. https://github.com/songyouwei/ABSA-PyTorch

The basic LSTM model is from TA's tutorial

The SPC-roberta model is our self-written codes based on the huggingface tutorial of simple textual classification

For the file **Solution Sharing.pdf**, it is the presentation slide that our group used to share our group's ideas and experiment designs for the class. 
  
