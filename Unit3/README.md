### Code examples of learning to use Optuna for hyperparameter optimization

Created a modified version of hyperparams_opt.py to limit the hyperparameter optimization search space for dqn algorithm.
Example of how to use: replace original version with this
```
cp .hyperparams_opt.py /usr/local/lib/python3.11/dist-packages/rl_zoo3/hyperparams_opt.py
pythom -m rl_zoo3.train \
  --algo dqn \
  --env SpaceInvadersNoFrameskip-v4 \
  -n 1000 \
  --optimize \
  --n-trials 1000 \
  --n-jobs 1 \
  --sampler random \
  --pruner median \
  --optimize-hyperparameters \
```
