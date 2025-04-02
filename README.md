# LinuxMintDocker
Guide to install Docker on Linux Mint

#Code

sudo apt update

sudo apt install ca-certificates curl gnupg

sudo mkdir -p /etc/apt/keyrings

curl -fsSL https://download.docker.com/linux-mint/gpg -o /etc/apt/keyrings/docker.gpg

sudo apt-key add /etc/apt/keyrings/docker.gpg

sudo add-apt-repository "deb [arch=amd64] https://download.docker.com/linux-mint/ $(lsb_release -cs) $(lsb_release -c) stable"

sudo apt update

sudo apt install docker-ce docker-ce-cli containerd.io docker-compose-plugin
