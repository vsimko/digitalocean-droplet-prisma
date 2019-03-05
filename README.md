# promonode-prisma-droplet
/etc/prisma config for DigitalOcean droplet

- Configured according to https://www.prisma.io/tutorials/deploy-prisma-to-digitalocean-ct12

```sh
# docker and docker-compose
curl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo apt-key add -
sudo add-apt-repository "deb [arch=amd64] https://download.docker.com/linux/ubuntu $(lsb_release -cs) stable"
sudo apt-get update
sudo apt-get install -y docker-ce
sudo curl -L https://github.com/docker/compose/releases/download/1.22.0/docker-compose-`uname -s`-`uname -m` -o /usr/local/bin/docker-compose

# docker-compose must be executable
chmod +x /usr/local/bin/docker-compose

# prisma cli is written in javascript
curl -sL https://deb.nodesource.com/setup_10.x | sudo -E bash -
sudo apt-get install -y nodejs
npm -g install prisma
```
