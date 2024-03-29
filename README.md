# Smart-Data-Analyse
## 1. Cross Validation und Grid Search
## 2. Image Similarity

## 3. Teacher and Student Model

Based on TANG21. The basic idea is transfer learning (TL): take full advantage of old knowledge rather than train a new model from zero when getting a new similar task

The process is as follows:

Train a teacher model with the Opportunity dataset
Store the teacher model and extract the optimal parameters (weights, w)
Load the graph and weights w in the student model
Train student model with the Daphnet dataset using the weights w
Files Description:

datareader.py: read dataset
teacher.py: train a teacher model
model: contain all the information about the teacher model
student.py: train a student model
How to run?

Download Opportunity dataset (it can be downloaded from: https://archive.ics.uci.edu/ml/datasets/opportunity+activity+recognition) and Daphnet Gait dataset (it can be downloaded from: https://archive.ics.uci.edu/ml/datasets/Daphnet+Freezing+of+Gait) and put them in the corresponding folder
Run python datareader.py opp to get opportunity.h5; run python datareader.py dap to get daphnet.h5
Run python teacher.py opp using opportunity.h5 and then store all the information in the file model.
Run python student.py dap using daphnet.h5
