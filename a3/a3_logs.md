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

### Test
python run.py --mode test \
--env_config data/envs/atari_pong.yaml \
--agent_config a3/atari_dqn_agent.yaml \
--model_file output/a3/Pong/model0.pt \
--test_episodes 20 \
--visualize

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

### Test
python run.py --mode test \
--env_config data/envs/atari_breakout.yaml \
--agent_config a3/atari_dqn_agent.yaml \
--model_file output/a3/Breakout/model0.pt \
--test_episodes 20 \
--visualize

