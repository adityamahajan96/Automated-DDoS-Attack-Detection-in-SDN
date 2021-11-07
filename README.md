# Automated DDoS Attack Detection In SDN

## Course: Advanced Computer Networks

### Overview:  
We implement a machine-learning based approach to detect Distributed Denial of Service (DDoS) attacks in the Software Defined Networking (SDN) paradigm. The network configuration has been customized using `mininet` and `pox` controller. Below topologies have been used for dataset creation.  
<img src="/Images/Topology1.JPG" alt="Topology 1" style="height: 200px; width:300px;"/> <img src="/Images/Topology2.JPG" alt="Topology 1" style="height: 200px; width:300px;"/> <img src="/Images/Topology3.JPG" alt="Topology 1" style="height: 200px; width:300px;"/>  

### Simulation of DDoS Attack using mininet

### Classification
We classify the traffic into benign (labelled as "0") and malicious (labelled as "1"). We have analyzed the results for 6 different classifiers, viz. Logistic Regression (LR), Support Vector Classifier (SVC), Ensemble Classifier (GBC), Decision Tree (DT), Artificial Neural Network (ANN) , Deep Learning (LSTM). Details about the analysis can be found in the **Analysis** section of the source code (notebook).  

### Observations
The following table shows the observed results for all the classifiers:  

N: Normal   
A: Attack  

| Algo     |   Acc |   N Prec |   A Prec |   N Rec |   A Rec |   N F-score |   A F-score |   FPR |   FNR |
|----------|-------|----------|----------|---------|---------|-------------|-------------|-------|-------|
| GNB      |  0.7  |     0.7  |     0.7  |    0.76 |    0.64 |        0.73 |        0.67 | 0.24  | 0.36  |
|----------|-------|----------|----------|---------|---------|-------------|-------------|-------|-------|
| LR       |  0.84 |     0.84 |     0.84 |    0.86 |    0.82 |        0.85 |        0.83 | 0.14  | 0.18  |
|----------|-------|----------|----------|---------|---------|-------------|-------------|-------|-------|
| SVC      |  0.98 |     0.98 |     0.97 |    0.98 |    0.98 |        0.98 |        0.97 | 0.023 | 0.024 |
|----------|-------|----------|----------|---------|---------|-------------|-------------|-------|-------|
| Ensemble |  0.99 |     0.99 |     0.99 |    0.99 |    0.99 |        0.99 |        0.99 | 0.001 | 0.001 |
|----------|-------|----------|----------|---------|---------|-------------|-------------|-------|-------|
| DT       |  1    |     1    |     1    |    1    |    1    |        1    |        1    | 0     | 0     |
|----------|-------|----------|----------|---------|---------|-------------|-------------|-------|-------|
| ANN      |  0.99 |     0.99 |     0.99 |    0.99 |    0.99 |        0.99 |        0.99 | 0.001 | 0.001 |
|----------|-------|----------|----------|---------|---------|-------------|-------------|-------|-------|
| DL       |  0.99 |     0.99 |     0.99 |    0.99 |    0.99 |        0.99 |        0.99 | 0.001 | 0.001 |
|----------|-------|----------|----------|---------|---------|-------------|-------------|-------|-------|
  



### Team:  
Dipankar Saha 2020201084  
Aditya Mahajan 2020202017  
Suman Mitra 2020202018
