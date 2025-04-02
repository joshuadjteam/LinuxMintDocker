# LinuxMintDocker
Guide to install Docker on Linux Mint

# Code

sudo apt update

sudo apt install ca-certificates curl gnupg

sudo mkdir -p /etc/apt/keyrings

curl -fsSL https://download.docker.com/linux-mint/gpg -o /etc/apt/keyrings/docker.gpg

sudo apt-key add /etc/apt/keyrings/docker.gpg

sudo add-apt-repository "deb [arch=amd64] https://download.docker.com/linux-mint/ $(lsb_release -cs) $(lsb_release -c) stable"

sudo apt update

sudo apt install docker-ce docker-ce-cli containerd.io docker-compose-plugin

# Alternative Methods

sudo apt-get update

sudo apt-get install ./docker-desktop-amd64.deb

# Last Ways

sudo apt update -y

sudo apt upgrade -y

sudo apt install ca-certificates curl gnupg

sudo mkdir -p /etc/apt/keyrings

sudo curl -fsSL https://download.docker.com/linux/ubuntu/gpg -o /etc/apt/keyrings/docker.asc

echo \
  "deb [arch=$(dpkg --print-architecture) signed-by=/etc/apt/keyrings/docker.asc] https://download.docker.com/linux/ubuntu $(lsb_release -cs) stable" | \
  sudo tee /etc/apt/sources.list.d/docker.list

sudo apt-get install docker-ce docker-ce-cli containerd.io docker-buildx-plugin docker-compose-plugin
