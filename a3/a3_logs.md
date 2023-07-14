# 1 Pong:
## 1.1 Try1:
Original hyper-parameters.
### Train
python run.py --mode train \
--env_config data/envs/atari_pong.yaml \
--agent_config a3/atari_dqn_agent.yaml \
--log_file output/a3/Pong/log0.txt \
--out_model_file output/a3/Pong/model0.pt \
--max_samples 3000000 

% model1: tar_net_updatae_iters: 5000 (original: 10000)
python run.py --mode train \
--env_config data/envs/atari_pong.yaml \
--agent_config a3/atari_dqn_agent.yaml \
--log_file output/a3/Pong/log1.txt \
--out_model_file output/a3/Pong/model1.pt \
--max_samples 3000000 

% model2: batch_size: 64 (original: 128)
python run.py --mode train \
--env_config data/envs/atari_pong.yaml \
--agent_config a3/atari_dqn_agent.yaml \
--log_file output/a3/Pong/log2.txt \
--out_model_file output/a3/Pong/model2.pt \
--max_samples 3000000 

% model3: init_samples: 10000 (original: 50000)
python run.py --mode train \
--env_config data/envs/atari_pong.yaml \
--agent_config a3/atari_dqn_agent.yaml \
--log_file output/a3/Pong/log3.txt \
--out_model_file output/a3/Pong/model3.pt \
--max_samples 3000000 

### Test
python run.py --mode test \
--env_config data/envs/atari_pong.yaml \
--agent_config a3/atari_dqn_agent.yaml \
--model_file output/a3/Pong/model0.pt \
--test_episodes 20  # basic: 20.1

% model1: tar_net_updatae_iters: 5000 (original: 10000)
python run.py --mode test \
--env_config data/envs/atari_pong.yaml \
--agent_config a3/atari_dqn_agent.yaml \
--model_file output/a3/Pong/model1.pt \
--test_episodes 20  # good: 20.6

% model2: batch_size: 64 (original: 128)
python run.py --mode test \
--env_config data/envs/atari_pong.yaml \
--agent_config a3/atari_dqn_agent.yaml \
--model_file output/a3/Pong/model2.pt \
--test_episodes 20  # worse: 19.65

% model3: init_samples: 10000 (original: 50000)
python run.py --mode test \
--env_config data/envs/atari_pong.yaml \
--agent_config a3/atari_dqn_agent.yaml \
--model_file output/a3/Pong/model3.pt \
--test_episodes 20  # worse: 15.65

# 2 Breakout:
## 2.1 Try1:
Original hyper-parameters.
### Train
python run.py --mode train \
--env_config data/envs/atari_breakout.yaml \
--agent_config a3/atari_dqn_agent.yaml \
--log_file output/a3/Breakout/log0.txt \
--out_model_file output/a3/Breakout/model0.pt \
--max_samples 3000000 

% model1: tar_net_updatae_iters: 5000 (original: 10000)
python run.py --mode train \
--env_config data/envs/atari_breakout.yaml \
--agent_config a3/atari_dqn_agent.yaml \
--log_file output/a3/Breakout/log1.txt \
--out_model_file output/a3/Breakout/model1.pt \
--max_samples 3000000 

% model2: batch_size: 64 (original: 128)
python run.py --mode train \
--env_config data/envs/atari_breakout.yaml \
--agent_config a3/atari_dqn_agent.yaml \
--log_file output/a3/breakout/log2.txt \
--out_model_file output/a3/breakout/model2.pt \
--max_samples 3000000 

### Test
python run.py --mode test \
--env_config data/envs/atari_breakout.yaml \
--agent_config a3/atari_dqn_agent.yaml \
--model_file output/a3/Breakout/model0.pt \
--test_episodes 20

python run.py --mode test \
--env_config data/envs/atari_breakout.yaml \
--agent_config a3/atari_dqn_agent.yaml \
--model_file output/a3/Breakout/model1.pt \
--test_episodes 20 # worse

python run.py --mode test \
--env_config data/envs/atari_breakout.yaml \
--agent_config a3/atari_dqn_agent.yaml \
--model_file output/a3/breakout/model2.pt \
--test_episodes 20  # good: 55