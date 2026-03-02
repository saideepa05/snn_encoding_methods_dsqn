# Connect 4 Implementation

## Base Code References
- **Connect 4 Logic:** [GitHub Reference](https://github.com/neoyung/connect-4/tree/master)
- **DSQN Algorithm:** [mahmoudakl/dsrl](https://github.com/mahmoudakl/dsrl)

## Weights & Biases (WandB) Logs
- **DQN (Agent First):** [Link](https://wandb.ai/kradeero-ohio-university/experiments/runs/l5u4nvem)
- **DQN (Agent Second):** [Link](https://wandb.ai/kradeero-ohio-university/experiments/runs/sb9stdtf)
- **DSQN (Agent First):** [Link](https://wandb.ai/kradeero-ohio-university/experiments/runs/fb5l7o7r)
- **DSQN (Agent Second):** [Link](https://wandb.ai/kradeero-ohio-university/experiments/runs/usjd404z)
- **Population Encoding:** [Link](https://wandb.ai/kradeero-ohio-university/experiments/runs/w1kxmerj)
- **Count-Rate:** [Link](https://wandb.ai/kradeero-ohio-university/experiments/runs/7uenxci2)
- **TTFS:** [Link](https://wandb.ai/kradeero-ohio-university/experiments/runs/ld6axhvq)
- **ROC:** [Link](https://wandb.ai/kradeero-ohio-university/experiments/runs/2sr1653z)
- **SDR:** [Link](https://wandb.ai/kradeero-ohio-university/experiments/runs/ofy0txsa)
- **Burst:** [Link](https://wandb.ai/kradeero-ohio-university/experiments/runs/rz0eegr6)
<!--
## Training Graphs and Evaluation Results
The following graphs demonstrate the training performance over the training steps. We have evaluated the trained model on 5 different seed values (42, 52, 62, 72, 82).

### Population Encoding

<img width="1048" height="242" alt="image" src="https://github.com/user-attachments/assets/a9d318af-bfc1-49b5-920e-e02f414f39df" />

| Seed | Win+Draw | Loss | Simp | Detailed | Total Spikes | Avg % Sparsity | Avg ACs | Internal State MACs |
| :---: | :---: | :---: | :---: | :---: | :---: | :---: | :---: | :---: |
| **42** | 89 | 11 | 93.2 | 67.2 | 543.03 | 57.58 | 115,188.06 | 3,716.06 |
| **52** | 93 | 7 | 93.2 | 67.2 | 542.05 | 57.65 | 115,119.71 | 3,714.10 |
| **62** | 94 | 6 | 93.2 | 67.2 | 541.46 | 57.70 | 115,094.15 | 3,712.93 |
| **72** | 95 | 5 | 93.2 | 67.2 | 542.39 | 57.63 | 115,165.51 | 3,714.77 |
| **82** | 93 | 7 | 93.2 | 67.2 | 541.78 | 57.67 | 115,110.46 | 3,713.56 |
| **AVG** | **92.80**<br>*(±2.28)* | **7.20**<br>*(±2.28)* | **93.2** | **67.2** | **542.14** | **57.65** | **115,135.58** | **3,714.29** |


### Count-rate Encoding

<img width="1048" height="245" alt="image" src="https://github.com/user-attachments/assets/02839526-e83d-4c0d-a406-7b955baa3617" />

| Seed | Win+Draw | Loss | Simp | Detailed | Total Spikes | Avg % Sparsity | Avg ACs | Internal State MACs |
| :---: | :---: | :---: | :---: | :---: | :---: | :---: | :---: | :---: |
| **42** | 85 | 15 | 95.8 | 78.0 | 330.94 | 56.91 | 38,388.68 | 3,750.98 |
| **52** | 83 | 17 | 95.8 | 77.9 | 334.60 | 56.43 | 38,875.67 | 3,762.04 |
| **62** | 84 | 16 | 95.8 | 78.0 | 331.14 | 56.88 | 38,223.26 | 3,751.06 |
| **72** | 88 | 12 | 95.9 | 78.1 | 327.63 | 57.34 | 37,742.91 | 3,740.46 |
| **82** | 90 | 10 | 95.9 | 78.0 | 329.30 | 57.12 | 38,109.32 | 3,745.79 |
| **AVG** | **86.00**<br>*(±2.92)* | **14.00**<br>*(±2.92)* | **95.8** | **78.0** | **330.72** | **56.94** | **38,267.97** | **3,750.07** |


### TTFS (Time to First Spike)

<img width="1048" height="242" alt="image" src="https://github.com/user-attachments/assets/697c4103-9762-4db8-aa4e-638c796bd3f1" />

| Seed | Win+Draw | Loss | Simp | Detailed | Total Spikes | Avg % Sparsity | Avg ACs | Internal State MACs |
| :---: | :---: | :---: | :---: | :---: | :---: | :---: | :---: | :---: |
| **42** | 86 | 14 | 97.2 | 80.6 | 222.46 | 71.03 | 31,726.15 | 3,375.06 |
| **52** | 85 | 15 | 97.1 | 80.5 | 227.74 | 70.35 | 32,128.75 | 3,386.91 |
| **62** | 84 | 16 | 97.1 | 80.5 | 228.54 | 70.24 | 32,022.34 | 3,387.69 |
| **72** | 83 | 17 | 97.1 | 80.4 | 230.52 | 69.78 | 32,361.40 | 3,393.68 |
| **82** | 86 | 14 | 97.2 | 80.5 | 225.70 | 70.61 | 32,058.68 | 3,383.31 |
| **AVG** | **84.80**<br>*(±1.30)* | **15.20**<br>*(±1.30)* | **97.1** | **80.5** | **227.00** | **70.44** | **32,059.46** | **3,385.33** |


### ROC (Rank Order Coding)

<img width="1045" height="241" alt="image" src="https://github.com/user-attachments/assets/e62642e3-669b-42dc-9e10-d4d70f395c78" />

| Seed | Win+Draw | Loss | Simp | Detailed | Total Spikes | Avg % Sparsity | Avg ACs | Internal State MACs |
| :---: | :---: | :---: | :---: | :---: | :---: | :---: | :---: | :---: |
| **42** | 89 | 11 | 97.1 | 80.1 | 232.67 | 69.70 | 32,291.04 | 3,460.94 |
| **52** | 94 | 6 | 97.1 | 80.2 | 229.60 | 70.10 | 32,201.13 | 3,456.57 |
| **62** | 94 | 6 | 97.0 | 80.1 | 235.85 | 69.29 | 32,527.37 | 3,467.57 |
| **72** | 94 | 6 | 97.1 | 80.1 | 231.69 | 69.83 | 32,303.81 | 3,460.07 |
| **82** | 88 | 12 | 97.1 | 80.1 | 234.10 | 69.52 | 32,478.80 | 3,464.48 |
| **AVG** | **91.80**<br>*(±3.03)* | **8.20**<br>*(±3.03)* | **97.1** | **80.1** | **232.78** | **69.69** | **32,360.43** | **3,461.93** |


### SDR (Sparse Distributed Representation)

<img width="1048" height="241" alt="image" src="https://github.com/user-attachments/assets/e99b350f-9f31-4214-b829-501098cac831" />

| Seed | Win+Draw | Loss | Simp | Detailed | Total Spikes | Avg % Sparsity | Avg ACs | Internal State MACs |
| :---: | :---: | :---: | :---: | :---: | :---: | :---: | :---: | :---: |
| **42** | 94 | 6 | 93.9 | 72.5 | 483.84 | 62.20 | 81,401.95 | 3,597.67 |
| **52** | 86 | 14 | 93.7 | 71.4 | 499.57 | 60.97 | 88,568.91 | 3,629.15 |
| **62** | 88 | 12 | 93.5 | 70.9 | 514.49 | 59.81 | 91,225.04 | 3,658.98 |
| **72** | 80 | 20 | 93.2 | 70.5 | 538.87 | 57.90 | 92,230.90 | 3,707.74 |
| **82** | 78 | 22 | 93.4 | 70.9 | 525.79 | 58.92 | 90,522.92 | 3,681.58 |
| **AVG** | **85.20**<br>*(±6.42)* | **14.80**<br>*(±6.42)* | **93.54** | **71.24** | **512.51** | **59.96** | **88,789.94** | **3,655.02** |


### Burst Encoding

<img width="1047" height="241" alt="image" src="https://github.com/user-attachments/assets/6839d991-072f-46b4-a37b-91150935465c" />

| Seed | Win+Draw | Loss | Simp | Detailed | Total Spikes | Avg % Sparsity | Avg ACs | Internal State MACs |
| :---: | :---: | :---: | :---: | :---: | :---: | :---: | :---: | :---: |
| **42** | 92 | 8 | 92.7 | 74.0 | 579.95 | 54.69 | 64,931.31 | 3,789.89 |
| **52** | 93 | 7 | 92.7 | 74.0 | 579.92 | 54.69 | 64,952.80 | 3,789.83 |
| **62** | 80 | 20 | 92.7 | 74.0 | 579.84 | 54.70 | 64,912.97 | 3,789.68 |
| **72** | 90 | 10 | 92.7 | 74.0 | 579.97 | 54.69 | 64,999.59 | 3,789.94 |
| **82** | 94 | 6 | 92.7 | 74.0 | 579.99 | 54.69 | 64,989.10 | 3,789.98 |
| **AVG** | **89.80**<br>*(±5.67)* | **10.20**<br>*(±5.67)* | **92.7** | **74.0** | **579.93** | **54.69** | **64,957.15** | **3,789.86** |
- **Burst for true temporal encoding:** [Link](https://wandb.ai/kradeero-ohio-university/experiments/runs/nalrf5xu?nw=nwuserkradeero)

<img width="766" height="239" alt="image (6)" src="https://github.com/user-attachments/assets/5092cc6d-cd7f-4df6-9a7e-c07c3c7cd95d" />

 - **Burst for instantaneous encoding:** [Link](https://wandb.ai/kradeero-ohio-university/experiments/runs/fmu9xmfs?nw=nwuserkradeero)
 
<img width="773" height="245" alt="image (5)" src="https://github.com/user-attachments/assets/232b47da-55d7-4634-b5c8-eec76c36eae4" />


##### 1. Tic-Tac-Toe (Temporal Burst, $T=5$)
Uses a **True Temporal Burst** pattern where spikes are distributed over 5 time steps (e.g., `[1, 1, 1, 0, 0]`). 
*   This validates the SNN's ability to process temporal spike trains in low-dimensional state spaces.
##### 2. Connect 4 (Instantaneous Burst, $T=1$)
Uses an **Instantaneous Intensity Approximation** where the cumulative charge of a burst is injected as a scalar value in a single time step.
**Why?** Our experiments demonstrated that scaling temporal bursting to the larger Connect 4 state space caused **Gradient Instability (Thrashing)** due to noise in Backpropagation Through Time (BPTT). The instantaneous approximation eliminates this noise, ensuring stable convergence while preserving signal magnitude.

-->


