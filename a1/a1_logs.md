# 1.3 Tasks
## 1.3.1 Train BC policies for the cheetah
python run.py --mode train \
--env_config data/envs/dm_cheetah.yaml \
--agent_config a1/dm_cheetah_bc_agent.yaml \
--log_file output/cheetah/cheetah_bc_log.txt \
--out_model_file output/cheetah/cheetah_bc_model.pt \
--max_samples 20000 

tensorboard --logdir=output/cheetah  # does not work

Try differenet hyperparameters:
1. basic (original settings)  # Final value: 19100.00, 562.26415 +/- 0.00000
2. max_samples = 30000  # sample30000, Final value: 29100.00, 615.40976 +/- 0.00000
3. max_samples = 40000  # sample40000, Final value: 39100.00, 623.27279 +/- 0.00000
4. discount0.80 + max_samples = 20000  # Final value: 19100.00, 620.25438 +/- 0.00000
5. discount0.90 + max_samples = 20000  # Final value: 19100.00, 606.89649 +/- 0.00000


## 1.3.2 Train BC policies for the walker
python run.py --mode train \
--env_config data/envs/dm_walker.yaml \
--agent_config a1/dm_walker_bc_agent.yaml \
--log_file output/walker/walker_bc_log.txt \
--out_model_file output/walker/walker_bc_model.pt \
--max_samples 20000 

Try differenet hyperparameters:
1. basic (original settings)  # Final value: 19100.00, 230.65860 +/- 0.00000
2. max_samples = 30000  # sample30000, Final value: 29100.00, 245.90623 +/- 0.00000
3. max_samples = 40000  # sample40000, Final value: 39100.00, 189.12858 +/- 0.00000
4. discount0.80 + max_samples = 20000  # Final value: 19100.00, 237.34958 +/- 0.00000
5. discount0.80 + max_samples = 30000  # Final value: 29100.00, 212.18654 +/- 0.00000
6. discount0.90 + max_samples = 20000  # Final value: 19100.00, 257.04245 +/- 0.00000
7. discount0.90 + max_samples = 30000  # Final value: 29100.00, 242.84021 +/- 0.00000