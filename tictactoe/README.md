# Project References

## Base Code References
- **TicTacToe Logic:** [CodeLearn.io Reference](https://codelearn.io/sharing/day-ai-danh-tictactoe-voi-deep-learning)
- **DSQN Algorithm:** [mahmoudakl/dsrl](https://github.com/mahmoudakl/dsrl)

## Weights & Biases (WandB) Logs
- **Population Encoding:** [Link](https://wandb.ai/kradeero-ohio-university/experiments/runs/nd2pdnxk)
- **Count-Rate:** [Link](https://wandb.ai/kradeero-ohio-university/experiments/runs/dagihp0q)
- **TTFS:** [Link](https://wandb.ai/kradeero-ohio-university/experiments/runs/6ae7xe4w)
- **ROC:** [Link](https://wandb.ai/kradeero-ohio-university/experiments/runs/8t2erdo5)
- **SDR:** [Link](https://wandb.ai/kradeero-ohio-university/experiments/runs/9bu0y8po)
- **Burst:** [Link](https://wandb.ai/kradeero-ohio-university/experiments/runs/6b4rn8x7?nw=nwuserkradeero)

## Training Graphs and Evaluation results
The following graphs demonstrate the training performance over 200 steps, each step is equals to 100 episodes, showing the increase in Win+Draw rate and the decrease in Loss rate and Average Spikes. We have evaluated the trained model on 5 different seed values (42, 52, 62, 72, 82). 

**Population Encoding**: 

<img width="1042" height="239" alt="image" src="https://github.com/user-attachments/assets/3b60bf17-d524-48b1-bf20-2bfee4a9e4c1" />

| Seed | Win+Draw | Loss | Simp | Detailed | Total Spikes | Avg % Sparsity | Avg ACs | Internal State MACs |
| :---: | :---: | :---: | :---: | :---: | :---: | :---: | :---: | :---: |
| **42** | 98 | 2 | 96.8 | 76.8 | 250.96 | 80.39 | 36,486.13 | 3,151.93 |
| **52** | 100 | 0 | 96.9 | 76.9 | 249.62 | 80.50 | 36,273.33 | 3,149.24 |
| **62** | 100 | 0 | 96.8 | 76.9 | 250.00 | 80.47 | 36,299.70 | 3,149.99 |
| **72** | 100 | 0 | 96.8 | 76.8 | 251.31 | 80.37 | 36,383.99 | 3,152.62 |
| **82** | 99 | 1 | 96.9 | 76.9 | 249.17 | 80.53 | 36,291.31 | 3,148.33 |
| **AVG** | **99.40**<br>*(±0.89)* | **0.6**<br>*(±0.89)* | **96.8** | **76.9** | **250.21** | **80.45** | **36,346.89** | **3,150.42** |


**Count-rate encoding**

<img width="1052" height="244" alt="image" src="https://github.com/user-attachments/assets/4aff301b-9281-49be-8931-e3fb07150536" />

| Seed | Win+Draw | Loss | Simp | Detailed | Total Spikes | Avg % Sparsity | Avg ACs | Internal State MACs |
| :---: | :---: | :---: | :---: | :---: | :---: | :---: | :---: | :---: |
| **42** | 96 | 4 | 97.4 | 81.1 | 207.03 | 83.83 | 14,769.23 | 3,064.06 |
| **52** | 98 | 2 | 97.4 | 81.1 | 206.72 | 83.85 | 14,772.68 | 3,063.45 |
| **62** | 98 | 2 | 97.4 | 81.1 | 206.59 | 83.86 | 14,733.91 | 3,063.18 |
| **72** | 96 | 4 | 97.4 | 81.1 | 204.94 | 83.99 | 14,697.99 | 3,059.88 |
| **82** | 97 | 3 | 97.4 | 81.1 | 204.72 | 84.01 | 14,627.18 | 3,059.43 |
| **AVG** | **97.00**<br>*(±1.00)* | **3.00**<br>*(±1.00)* | **97.4** | **81.1** | **206.00** | **83.90** | **14,720.20** | **3,062.00** |


**TTFS (Time to First Spike)** 

<img width="1049" height="244" alt="image" src="https://github.com/user-attachments/assets/00072407-0aa9-48b8-bdd3-bce5a927bb55" />

| Seed | Win+Draw | Loss | Simp | Detailed | Total Spikes | Avg % Sparsity | Avg ACs | Internal State MACs |
| :---: | :---: | :---: | :---: | :---: | :---: | :---: | :---: | :---: |
| **42** | 100 | 0 | 98.1 | 82.7 | 148.77 | 88.38 | 8,877.91 | 2,947.55 |
| **52** | 99 | 1 | 98.1 | 82.7 | 150.80 | 88.22 | 8,964.72 | 2,951.61 |
| **62** | 98 | 2 | 98.1 | 82.7 | 149.36 | 88.33 | 8,918.18 | 2,948.72 |
| **72** | 100 | 0 | 98.1 | 82.7 | 147.05 | 88.51 | 8,845.32 | 2,944.10 |
| **82** | 100 | 0 | 98.2 | 82.7 | 146.10 | 88.59 | 8,768.60 | 2,942.20 |
| **AVG** | **99.40**<br>*(±0.89)* | **0.60**<br>*(±0.89)* | **98.1** | **82.7** | **148.42** | **88.41** | **8,874.95** | **2,946.84** |


**ROC (Rank Order Coding)** 

<img width="1046" height="240" alt="image" src="https://github.com/user-attachments/assets/44c1244e-1ff7-4fd8-af73-252f3ed77c8c" />

| Seed | Win+Draw | Loss | Simp | Detailed | Total Spikes | Avg % Sparsity | Avg ACs | Internal State MACs |
| :---: | :---: | :---: | :---: | :---: | :---: | :---: | :---: | :---: |
| **42** | 100 | 0 | 97.0 | 81.0 | 241.73 | 81.11 | 12,678.24 | 3,133.46 |
| **52** | 99 | 1 | 96.9 | 81.0 | 242.96 | 81.02 | 12,719.45 | 3,135.92 |
| **62** | 100 | 0 | 96.9 | 81.0 | 245.65 | 80.81 | 12,861.38 | 3,141.30 |
| **72** | 100 | 0 | 96.9 | 81.0 | 246.01 | 80.78 | 12,831.70 | 3,142.02 |
| **82** | 100 | 0 | 97.0 | 81.0 | 241.35 | 81.14 | 12,716.34 | 3,132.70 |
| **AVG** | **99.80**<br>*(±0.45)* | **0.20**<br>*(±0.45)* | **96.9** | **81.0** | **243.54** | **80.98** | **12,761.42** | **3,137.08** |


**SDR (Sparse Distributed Representation)** 

<img width="1046" height="241" alt="image" src="https://github.com/user-attachments/assets/d622acda-1179-4ff5-ae54-90a448dfdd1d" />

| Seed | Win+Draw | Loss | Simp | Detailed | Total Spikes | Avg % Sparsity | Avg ACs | Internal State MACs |
| :---: | :---: | :---: | :---: | :---: | :---: | :---: | :---: | :---: |
| **42** | 100 | 0 | 97.3 | 75.2 | 211.80 | 83.45 | 48,542.00 | 3,073.60 |
| **52** | 100 | 0 | 97.3 | 75.1 | 213.30 | 83.34 | 48,611.00 | 3,076.60 |
| **62** | 100 | 0 | 97.3 | 75.1 | 212.40 | 83.41 | 48,649.00 | 3,074.80 |
| **72** | 100 | 0 | 97.3 | 75.2 | 211.30 | 83.49 | 48,580.00 | 3,072.60 |
| **82** | 100 | 0 | 97.3 | 75.2 | 212.40 | 83.41 | 48,611.00 | 3,074.80 |
| **AVG** | **100.00**<br>*(±0.00)* | **0.00**<br>*(±0.00)* | **97.3** | **75.2** | **212.30** | **83.42** | **48,599.00** | **3,074.50** |


**Burst Encoding** 

<img width="1048" height="242" alt="image" src="https://github.com/user-attachments/assets/9e283e3c-bd80-423a-97a9-76c3a5e9192b" />

| Seed | Win+Draw | Loss | Simp | Detailed | Total Spikes | Avg % Sparsity | Avg ACs | Internal State MACs |
| :---: | :---: | :---: | :---: | :---: | :---: | :---: | :---: | :---: |
| **42** | 97 | 3 | 97.0 | 80.4 | 239.89 | 81.26 | 16,492.21 | 3,129.78 |
| **52** | 99 | 1 | 96.9 | 80.3 | 242.43 | 81.06 | 16,685.07 | 3,134.87 |
| **62** | 99 | 1 | 97.0 | 80.4 | 241.33 | 81.15 | 16,631.89 | 3,132.67 |
| **72** | 99 | 1 | 96.9 | 80.3 | 242.25 | 81.07 | 16,716.69 | 3,134.49 |
| **82** | 97 | 3 | 97.0 | 80.4 | 239.11 | 81.32 | 16,475.28 | 3,128.23 |
| **AVG** | **98.20**<br>*(±1.10)* | **1.80**<br>*(±1.10)* | **97.0** | **80.4** | **241.00** | **81.17** | **16,600.23** | **3,132.01** |



