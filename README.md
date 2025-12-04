# SNN Encoding Methods Analysis

This repository investigates whether Deep Spiking Q-Network (DSQN) models can perform at par with standard Deep Q-Network (DQN) models in turn-based strategy games. The project focuses on evaluating different spike encoding methods to determine which strategies offer the best balance between game performance (Win Rate) and energy efficiency.

## References

### Base Code
- **Tic-Tac-Toe Logic:** [CodeLearn.io Reference](https://codelearn.io/sharing/day-ai-danh-tictactoe-voi-deep-learning)
- **Connect 4 Logic:** [GitHub Reference](https://github.com/neoyung/connect-4/tree/master)
- **DSQN Algorithm:** [mahmoudakl/dsrl](https://github.com/mahmoudakl/dsrl)
  
---

## 1. Tic-Tac-Toe Evaluation
The following section analyzes the performance of various encoding methods on the Tic-Tac-Toe environment.

### Training Dynamics (Combined Encodings)
*Comparison of Win Rates, Loss Rates, and Average Spikes across all encoding methods.*

<img width="1031" height="244" alt="ttt_encodings" src="https://github.com/user-attachments/assets/37ca4b70-f199-4e63-8744-62bddbe3e1c3" />

### Performance & Energy Metrics
Aggregated results over 5 random seeds (Mean ± Std Dev).

**Table 1: Performance and Energy Savings**
| Encoding | Win + Draw (%) | Loss (%) | Simplified Savings (%) | Detailed Savings (%) | Avg Sparsity (%) |
| :--- | :---: | :---: | :---: | :---: | :---: |
| **Population** | **99.40 ± 0.89** | 0.60 ± 0.89 | 96.8 | 76.9 | 80.45 |
| **Count Rate** | 97.00 ± 1.00 | 3.00 ± 1.00 | 97.4 | 81.1 | 83.90 |
| **TTFS** | **99.40 ± 0.89** | 0.60 ± 0.89 | **98.1** | **82.7** | **88.41** |
| **ROC** | **99.80 ± 0.45** | 0.20 ± 0.45 | **96.9** | **81.0** | 80.98 |
| **SDR** | **100.00 ± 0.00** | 0.00 ± 0.00 | 97.3 | 75.2 | 83.42 |
| **Burst** | 98.20 ± 1.10 | 1.80 ± 1.10 | 97.0 | 80.4 | 81.17 |

**Table 2: Energy Consumption Analysis**
| Encoding | Avg Spikes | Dynamic E. (Avg ACs) | Operational E. (MACs × 31) | Total Energy | Dynamic % of Total |
| :--- | :---: | :---: | :---: | :---: | :---: |
| **Population** | 250 | 36,347 | 97,650 | 133,997 | 27.13% |
| **Count Rate** | 206 | 14,720 | 94,922 | 109,642 | 13.43% |
| **TTFS** | **148** | **8,875** | **91,357** | **100,232** | **8.85%** |
| **ROC** | 244 | 12,761 | 97,247 | 110,008 | 11.60% |
| **Burst** | 241 | 16,600 | 97,092 | 113,692 | 14.60% |
| **SDR** | 212 | 48,599 | 95,325 | 143,924 | 33.77% |

---

## 2. Connect 4 Evaluation
The following section analyzes the performance of various encoding methods on the Connect 4 environment.

### Training Dynamics (Combined Encodings)
*Comparison of Win Rates, Loss Rates, and Average Spikes across all encoding methods.*

<img width="1025" height="241" alt="c4_encodings" src="https://github.com/user-attachments/assets/e88ee346-54b0-4cd0-b7b6-e6d434bb92af" />

### Performance & Energy Metrics
Aggregated results over 5 random seeds (Mean ± Std Dev).

**Table 3: Performance and Energy Savings**
| Encoding | Win + Draw (%) | Loss (%) | Simplified Savings (%) | Detailed Savings (%) | Avg Sparsity (%) |
| :--- | :---: | :---: | :---: | :---: | :---: |
| **Population** | **92.80 ± 2.28** | 7.20 ± 2.28 | 93.2 | 67.2 | 57.65 |
| **Count Rate** | 86.00 ± 2.92 | 14.00 ± 2.92 | 95.8 | 78.0 | 56.94 |
| **TTFS** | 84.80 ± 1.30 | 15.20 ± 1.30 | **97.1** | **80.5** | **70.44** |
| **ROC** | **91.80 ± 3.03** | 8.20 ± 3.03 | **97.1** | **80.1** | 69.69 |
| **SDR** | 85.20 ± 6.42 | 14.80 ± 6.42 | 93.54 | 71.24 | 59.96 |
| **Burst** | 89.80 ± 5.67 | 10.20 ± 5.67 | 92.7 | 74.0 | 54.69 |

**Table 4: Energy Consumption Analysis**
| Encoding | Avg Spikes | Dynamic E. (Avg ACs) | Operational E. (MACs × 31) | Total Energy | Dynamic % of Total |
| :--- | :---: | :---: | :---: | :---: | :---: |
| **Population** | 542 | 115,136 | 115,134 | 230,270 | 50.0% |
| **Count Rate** | 331 | 38,268 | 116,250 | 154,518 | 24.8% |
| **TTFS** | **227** | **32,059** | **104,935** | **136,994** | **23.4%** |
| **ROC** | 233 | 32,360 | 107,322 | 139,682 | 23.17% |
| **SDR** | 513 | 88,790 | 113,305 | 202,095 | 43.9% |
| **Burst** | 580 | 64,957 | 117,490 | 182,447 | 35.6% |

---

## 3. Baseline Comparison (DSQN vs. DQN)
We compared the best performing SNN configuration against a standard DQN baseline to verify that spiking networks can achieve competitive win rates.

### Tic-Tac-Toe Comparison VS random agent

<img width="682" height="239" alt="ttt_1" src="https://github.com/user-attachments/assets/0c905f1e-e5ea-4e80-901f-dbb3207636bc" /> <img width="682" height="239" alt="ttt_2" src="https://github.com/user-attachments/assets/5be594e7-35b2-41ad-964b-16a9e65b0ea7" />

### Tic-Tac-Toe Comparison VS minimax agent

<img width="692" height="251" alt="minimax_1" src="https://github.com/user-attachments/assets/002802f9-d318-4364-b9af-a57b11de2388" /> <img width="688" height="252" alt="minimax_2" src="https://github.com/user-attachments/assets/57a266b4-192d-4be3-a87a-9cc89b62baa7" />

### Connect 4 Comparison VS random agent

<img width="679" height="242" alt="c4_1" src="https://github.com/user-attachments/assets/fb167466-1d19-46f1-a916-36073985f4e1" />

<img width="689" height="241" alt="c4_2" src="https://github.com/user-attachments/assets/94ad5b43-0154-49fa-809c-def50247d34d" />


## Repository Structure 

This repository is structured to separate the experiments based on the game environment (**Tic-Tac-Toe** and **Connect 4**). Each game directory is self-contained and organized into three specific modules to facilitate reproducibility and analysis.

#### 1. Game Directories (`tictactoe/` and `connect4/`)
Both game folders follow an identical structure:

*   **`encoding/`**: This folder contains the core experiments of this research. It holds individual Jupyter Notebooks for each Spiking Neural Network (SNN) encoding method. Running these notebooks will train a DSQN agent using that specific spike encoding strategy and log the energy efficiency metrics.

*   **`dqn_dsqn/`**: This folder is dedicated to the baseline comparisons. It contains notebooks that pit a standard Deep Q-Network (DQN) against the Deep Spiking Q-Network (DSQN) to compare win-rates and learning stability.
    *   **File Naming Convention:**
        *   Files ending in **`_1`** or **`_first`** (e.g., `dqn_1.ipynb`, `dsqn_first.ipynb`) train the agent to play as **Player 1** (making the first move).
        *   Files ending in **`_2`** or **`_second`** (e.g., `dqn_2.ipynb`, `dsqn_second.ipynb`) train the agent to play as **Player 2** (making the blocking/second move).

*   **`saved_models/`**: This directory stores the pre-trained PyTorch weights (`.pth` files). These models allow you to evaluate performance or visualize gameplay without needing to retrain the agents from scratch.

#### 2. Visualization (`graphs/`)
This folder contains the scripts and generated images used to visualize the different encoding methods for better understanding. 
