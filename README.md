# Gensyn-Ai ![428827984-8ad5a694-e287-4d45-ba57-203f58a19714](https://github.com/user-attachments/assets/b3488e5e-2b35-4381-90b3-55e5cf40c552)
Run RL Swarm (Testnet) Node
RL Swarm is a fully open-source framework developed by GensynAI for building reinforcement learning (RL) training swarms over the internet. This guide walks you through setting up an RL Swarm node and a web UI dashboard to monitor swarm activity.

## Hardware Requirements	

- CPU: Minimum 16GB RAM (more RAM recommended for larger models or datasets).

OR

- GPU (Optional): Supported CUDA devices for enhanced performance:
    - RTX 3090
    - RTX 4090
    - A100
    - H100
    > I recommend GPUs with >=24GB vRAM.
-  **Note**: You can run the node without a GPU using CPU-only mode.
## Installation
1. **Install `sudo`**
 ```bash
 apt update && apt install -y sudo
 ```
 2. **Install other dependencies**
 ```bash
 sudo apt update && sudo apt install -y python3 python3-venv python3-pip curl wget screen git lsof nano unzip
 ```
 3. **Install Node**
 ```
 sudo apt-get update
 ```
 ```
 curl -fsSL https://deb.nodesource.com/setup_22.x | sudo -E bash -
 ```
 ```
 sudo apt-get install -y nodejs
 ```
 ```
 node -v
 ```
4. **Create a Screen session**

```bash
 screen -S gensyn
 ```

5. **Intall the swarm**
 ```bash
cd $HOME && [ -d rl-swarm ] && rm -rf rl-swarm; git clone https://github.com/andiiyan1/rl-swarm.git && cd rl-swarm
 ```

6. **Run the swarm**
```bash
 python3 -m venv .venv
 source .venv/bin/activate
 ./run_rl_swarm.sh
```
 - It will ask some questions, you should send response properly
 - ```Would you like to push models you train in the RL swarm to the Hugging Face Hub? [y/N]``` : Write `N`
7. **Detach from `screen session`**
 - Use `Ctrl + A` and then press `D` to detach from this screen session.
