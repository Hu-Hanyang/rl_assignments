# 1.4 Tasks
python run.py --mode train \
--env_config data/envs/dm_cheetah.yaml \
--agent_config a2/dm_cheetah_cem_agent.yaml \
--log_file output/a2/task1/log0.txt \
--out_model_file output/a2/task1/model0.pt \
--max_samples 100000000 

python run.py --mode train \
--env_config data/envs/dm_cheetah.yaml \
--agent_config a2/dm_cheetah_cem_agent.yaml \
--log_file output/a2/task1/log1.txt \
--out_model_file output/a2/task1/model1.pt \
--max_samples 100000000

tmux task1:
python run.py --mode train \
--env_config data/envs/dm_cheetah.yaml \
--agent_config a2/dm_cheetah_cem_agent.yaml \
--log_file output/a2/task1/log2.txt \
--out_model_file output/a2/task1/model2.pt \
--max_samples 100000000

tmux task12:
python run.py --mode train \
--env_config data/envs/dm_cheetah.yaml \
--agent_config a2/dm_cheetah_cem_agent.yaml \
--log_file output/a2/task1/log3.txt \
--out_model_file output/a2/task1/model3.pt \
--max_samples 100000000

python run.py --mode train \
--env_config data/envs/dm_cheetah.yaml \
--agent_config a2/dm_cheetah_cem_agent.yaml \
--log_file output/a2/task1/log4.txt \
--out_model_file output/a2/task1/model4.pt \
--max_samples 100000000

python run.py --mode train \
--env_config data/envs/dm_cheetah.yaml \
--agent_config a2/dm_cheetah_cem_agent.yaml \
--log_file output/a2/task1/log5.txt \
--out_model_file output/a2/task1/model5.pt \
--max_samples 100000000

python run.py --mode train \
--env_config data/envs/dm_cheetah.yaml \
--agent_config a2/dm_cheetah_cem_agent.yaml \
--log_file output/a2/task1/log6.txt \
--out_model_file output/a2/task1/model6.pt \
--max_samples 100000000

python run.py --mode train \
--env_config data/envs/dm_cheetah.yaml \
--agent_config a2/dm_cheetah_cem_agent.yaml \
--log_file output/a2/task1/log7.txt \
--out_model_file output/a2/task1/model7.pt \
--max_samples 100000000

plot:
test0: output/a2/task1/log0.txt  # around 130
test2: 
elite_ratio: 0.10  # 0.25, min_param_std: 0.3  # 0.1 
output/a2/task1/log2.txt  # around 361.38
output/a2/task1/log4.txt # std = 0.3, around 310.78593 +/- 0.00000
output/a2/task1/log5.txt  # std = 0.15, around 302.04952 +/- 0.00000
output/a2/task1/log6.txt  # std = 0.35, around 
output/a2/task1/log7.txt  # std = 0.3, population_size = 20

# 2.5 Tasks
python run.py --mode train \
--env_config data/envs/dm_cheetah.yaml \
--agent_config a2/dm_cheetah_pg_agent.yaml \
--log_file output/a2/task2/pg_log0.txt \
--out_model_file output/a2/task2/pg_model0.pt \
--max_samples 100000000

python run.py --mode train \
--env_config data/envs/dm_cheetah.yaml \
--agent_config a2/dm_cheetah_pg_agent.yaml \
--log_file output/a2/task2/pg_log1.txt \
--out_model_file output/a2/task2/pg_model1.pt \
--max_samples 200000000

python run.py --mode train \
--env_config data/envs/dm_cheetah.yaml \
--agent_config a2/dm_cheetah_pg_agent.yaml \
--log_file output/a2/task2/pg_log2.txt \
--out_model_file output/a2/task2/pg_model2.pt \
--max_samples 200000000

python run.py --mode train \
--env_config data/envs/dm_cheetah.yaml \
--agent_config a2/dm_cheetah_pg_agent.yaml \
--log_file output/a2/task2/pg_log2.txt \
--out_model_file output/a2/task2/pg_model2.pt \
--max_samples 100000000

python run.py --mode train \
--env_config data/envs/dm_cheetah.yaml \
--agent_config a2/dm_cheetah_pg_agent.yaml \
--log_file output/a2/task2/pg_log3.txt \
--out_model_file output/a2/task2/pg_model3.pt \
--max_samples 150000000

plot:
output/a2/task2/pg_log.txt  # around 300
test1: --max_samples 200000000  # Final value: 25808896.00, 251.33256 +/- 0.00000
test2: discount: 0.99  # killed

output/a2/task2/pg_log3.txt  # around 478.18538 +/- 0.00000

