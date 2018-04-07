# Quick Start

### Install docker

```bash
curl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo apt-key add -
sudo add-apt-repository "deb [arch=amd64] https://download.docker.com/linux/ubuntu $(lsb_release -cs) stable"
sudo apt-get update
apt-cache policy docker-ce
sudo apt-get install -y docker-ce
```

### Install docker compose

```bash
sudo curl -L https://github.com/docker/compose/releases/download/1.20.1/docker-compose-`uname -s`-`uname -m` -o /usr/local/bin/docker-compose
sudo chmod +x /usr/local/bin/docker-compose
```

### Clone the repo

```bash
git clone https://github.com/shouston3/node_docker.git
```

### Build the image

```bash
sudo docker build -t node-throwaway .
```

### Start the server

```bash
sudo docker-compose up --build
```

### Configure nginx

```bash
sudo apt-get install nginx
```

configure the `sudo rm /etc/nginx/sites-enabled/default` file, then

```bash
sudo nginx -s reload
```
