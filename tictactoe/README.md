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

## Evaluation Results
We have evaluated the results on 5 different seed values (42, 52, 62, 72, 82). Below are the specific performance metrics for **Population Encoding**:

| Seed | Win | Draw | Win+Draw | Loss | Simp | Detailed | Total Spikes | Avg % Sparsity | Avg ACs | Internal State MACs |
| :---: | :---: | :---: | :---: | :---: | :---: | :---: | :---: | :---: | :---: | :---: |
| **42** | 90 | 8 | 98 | 2 | 96.8 | 76.8 | 250.96 | 80.39 | 36,486.13 | 3,151.93 |
| **52** | 93 | 7 | 100 | 0 | 96.9 | 76.9 | 249.62 | 80.50 | 36,273.33 | 3,149.24 |
| **62** | 93 | 7 | 100 | 0 | 96.8 | 76.9 | 250.00 | 80.47 | 36,299.70 | 3,149.99 |
| **72** | 96 | 4 | 100 | 0 | 96.8 | 76.8 | 251.31 | 80.37 | 36,383.99 | 3,152.62 |
| **82** | 90 | 9 | 99 | 1 | 96.9 | 76.9 | 249.17 | 80.53 | 36,291.31 | 3,148.33 |

