# Lancache Monolithic for ARM32/ARM64

![Docker Pulls](https://img.shields.io/docker/pulls/jrcichra/lancachenet-monolithic?label=Monolithic) ![Docker Pulls](https://img.shields.io/docker/pulls/jrcichra/lancachenet-lancache-dns?label=Lancache-dns) ![Docker Pulls](https://img.shields.io/docker/pulls/jrcichra/lancachenet-sniproxy?label=Sniproxy) ![Docker Pulls](https://img.shields.io/docker/pulls/jrcichra/lancachenet-generic?label=Generic)

(Unofficial RPI Version) - A monolithic lancache service capable of caching all CDNs in a single instance
# Note
+ NTFS/FAT32 external drives will not work. `nginx` tries to `chown`, which doesn't play nice with Microsoft filesystems. Please use a nix filesystem such as `ext4`.
+ You may experience slower than expected cache speeds.
# Installation
- To install:
  -  If you don't already have docker and docker-compose, run `sudo apt install docker.io docker-compose`
  - `sudo git clone https://github.com/red0fireus/lancache-rpi.git`
  - `cd lancache-rpi`
  - `nano .env`
  - In the .env, follow annotations and modify LANCACHE_IP and DNS_BIND_IP to be the IP of the interface you want to expose this on. `0.0.0.0` might work but I recommend a single interface.
  - `docker-compose up -d`
+ Configure your router and/or PC to serve lancache-dns
+ Further documentation can be found at [lancache.net](https://lancache.net/)
## Test it
http://diagnostics.lancache.net/
## Actions
This repo uses Github Actions. Click the Actions tab to view the script output.

The docker images can be found on my docker hub account.
