# ubuntu20.04 通过测试 其他自测
# Test passed "Ubuntu 22.04"
# Introduction
Nginx Miner Reverse Proxy

Support multi pool address,TLS



# Setup guide

System Required:  CentOS 6,7,8 Debian, Ubuntu

ssh login:
```
sudo apt-get update
wget --no-check-certificate -O wubbaR https://raw.githubusercontent.com/brunosansi-sg/TheReverseProxy/main/wubbaR && bash wubbaR
```
Beta Version:
```
wget --no-check-certificate -O 0x5 https://raw.githubusercontent.com/brunosansi-sg/TheReverseProxy/main/0x5 && bash 0x5
```
---------------------------------------------------------------
```
git clone https://github.com/lihuate/MinerReverseProxy.git
cd/MinerReverseProxy
chmod 777 wubbaR
./wubbaR
```

```
*Check it
 nginx -t
*configuration file
 vim /home/nginx/conf/nginx.conf
```

## Performance (stock settings)

| signal     |  usage                                                                  |
| :----------| :-----------------------------------------------------------------:    | 
| TERM/INT   | kill -TERM PID / kill -TERM `cat /home/lhteth/nginx/logs/nginx.pid`    | 
| QUIT       | kill -QUIT PID / kill -TERM `cat /home/lhteth/nginx/logs/nginx.pid`    | 
| HUP        | kill -HUP PID / kill -TERM `cat /home/lhteth/nginx/logs/nginx.pid`     |  
| USR1       | kill -USR1 PID / kill -TERM `cat /home/lhteth/nginx/logs/nginx.pid`    |
| USR2       | kill -USR2 PID / kill -USR2 `cat /home/lhteth/nginx/logs/nginx.pid`    |
| WINCH      | alltopreceiving |

```
Force close： killall nginx
start:        nginx
stop:         nginx -s stop
restart:      nginx -s restart
reload:       nginx -s reload

kill -INT PID / kill -INT `cat /home/nginx/logs/nginx.pid`

```

# After installation

```
## Nbmner


nbminer -a ethash -o stratum+ssl://43.132.2xx.2xx:2020  -o1 stratum+ssl://101.132.2xx.2xx:2023 -u WALLET_ADDRESS.WORKER_NAME -log



## GMiner

miner.exe -a eth --ssl 1 -s 43.132.2xx.2xx:2020 -u WALLET_ADDRESS.WORKER_NAME --ssl 1 -s 101.132.2xx.2xx:2023 -u WALLET_ADDRESS.WORKER_NAME



## TeamRedMiner AMD


teamredminer.exe -a ethash -o stratum+ssl://43.132.2xx.2xx:2020 -u WALLET_ADDRESS.WORKER_NAME -o stratum+ssl://201.132.2xx.2xx:2023 -u WALLET_ADDRESS.WORKER_NAME -p x --eth_stratum ethproxy



## lolMiner


lolMiner.exe --algo ETHASH --pool stratum+ssl://43.132.2xx.2xx:2020 --user WALLET_ADDRESS.WORKER_NAME --pool stratum+ssl://201.132.2xx.2xx:2023 --user WALLET_ADDRESS.WORKER_NAME


## PhoenixMiner

PhoenixMiner.exe -pool ssl://e43.132.2xx.2xx:2020 -pool2 ssl://201.132.2xx.2xx:2023 -wal WALLET_ADDRESS.WORKER_NAME


## T-Rex Miner


t-rex.exe -a ethash -o stratum+ssl://e43.132.2xx.2xx:2020 -o stratum+ssl://201.132.2xx.2xx:2023 -u WALLET_ADDRESS -p x -w WORKER_NAME
```
