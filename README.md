# Gensyn-rl-swarm let's run the rl swarm node
How to run gensyn rl swarm with vps just 4 cpu 8gb ram note : (you should use better specs vps to get rid of error) you should use it only for swarm node others would probably crash if you are running on 4CPU
# COMMANDS copy paste
we are running on low specs so first we have to make a swap file to reduce termination chances 
```bash
sudo swapoff -a
sudo rm -f /swapfile

sudo fallocate -l 8G /swapfile
sudo chmod 600 /swapfile
sudo mkswap /swapfile
sudo swapon /swapfile

swapon --show
free -h

echo '/swapfile none swap sw 0 0' | sudo tee -a /etc/fstab
```
1. Install dependencies
