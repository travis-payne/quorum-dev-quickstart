# Sample Networks

## Prerequisites

To run these tutorials, you must have the following installed:

- [Docker and Docker-compose](https://docs.docker.com/compose/install/)

| ⚠️ **Note**: If on MacOS or Windows, please ensure that you allow docker to use upto 4G of memory or 6G if running Privacy examples under the _Resources_ section. The [Docker for Mac](https://docs.docker.com/docker-for-mac/) and [Docker Desktop](https://docs.docker.com/docker-for-windows/) sites have details on how to do this at the "Resources" heading       |
| ---                                                                                                                                                                                                                                                                                                                                                                                |


| ⚠️ **Note**: This has only been tested on Windows 10 Build 18362 and Docker >= 17.12.2                                                                                                                                                                                                                                                                                              |
| ---                                                                                                                                                                                                                                                                                                                                                                                |

- On Windows ensure that the drive that this repo is cloned onto is a "Shared Drive" with Docker Desktop
- On Windows we recommend running all commands from GitBash
- [Nodejs](https://nodejs.org/en/download/) and [Truffle](https://www.trufflesuite.com/truffle) if using the DApp


## Description

npm install
npm start


Orchestrate:
```
docker-compose -f docker-compose-orchestrate-deps.yml up -d
# not sure why this is on a seperate network
docker network create deps_orchestrate
docker-compose -f docker-compose-orchestrate-besu.yml up -d
# can we create this as part of the main compose?
docker volume create --name=deps_vault-token
docker-compose -f docker-compose-orchestrate.yml up -d


```

### Stop Services and Network
`./stop.sh` stops all the docker containers created.

### Remove stopped containers and volumes
`./remove.sh` stops and removes all the containers and volumes.


##TODO:
- orchestrate with java
- orchestrate with quorum
- fix list.sh
- fix images & readme
- add monitoring for go


[INFO ] 2020-07-23 10:24:10.082 [BlockScanner-44] GethHttpServiceImpl - Geth call: eth_getBlockByNumber
[INFO ] 2020-07-23 10:24:12.092 [BlockScanner-44] GethHttpServiceImpl - Geth call: admin_peers
[INFO ] 2020-07-23 10:24:12.095 [BlockScanner-44] GethHttpServiceImpl - Geth call: eth_getBlockByNumber
[INFO ] 2020-07-23 10:24:13.972 [MessageBroker-5] GethHttpServiceImpl - Geth call: eth_getBlockByNumber
[INFO ] 2020-07-23 10:24:14.099 [BlockScanner-44] GethHttpServiceImpl - Geth call: admin_peers
[INFO ] 2020-07-23 10:24:14.104 [BlockScanner-44] GethHttpServiceImpl - Geth call: eth_getBlockByNumber
[INFO ] 2020-07-23 10:24:14.411 [MessageBroker-2] GethHttpServiceImpl - Geth call: admin_nodeInfo
[INFO ] 2020-07-23 10:24:14.416 [MessageBroker-2] GethHttpServiceImpl - Geth call: eth_mining
[INFO ] 2020-07-23 10:24:14.422 [MessageBroker-2] GethHttpServiceImpl - Geth call: net_peerCount
[INFO ] 2020-07-23 10:24:14.427 [MessageBroker-2] GethHttpServiceImpl - Geth call: eth_blockNumber
[INFO ] 2020-07-23 10:24:14.431 [MessageBroker-2] GethHttpServiceImpl - Geth call: txpool_status
[INFO ] 2020-07-23 10:24:14.435 [MessageBroker-2] GethHttpServiceImpl - Geth call: admin_peers
[INFO ] 2020-07-23 10:24:16.108 [BlockScanner-44] GethHttpServiceImpl - Geth call: admin_peers
[INFO ] 2020-07-23 10:24:16.112 [BlockScanner-44] GethHttpServiceImpl - Geth call: eth_getBlockByNumber
[INFO ] 2020-07-23 10:24:18.116 [BlockScanner-44] GethHttpServiceImpl - Geth call: admin_peers
[INFO ] 2020-07-23 10:24:18.124 [BlockScanner-44] GethHttpServiceImpl - Geth call: eth_getBlockByNumber
[INFO ] 2020-07-23 10:24:18.983 [MessageBroker-2] GethHttpServiceImpl - Geth call: eth_getBlockByNumber
[INFO ] 2020-07-23 10:24:19.440 [MessageBroker-6] GethHttpServiceImpl - Geth call: admin_nodeInfo
[INFO ] 2020-07-23 10:24:19.443 [MessageBroker-6] GethHttpServiceImpl - Geth call: eth_mining
[INFO ] 2020-07-23 10:24:19.447 [MessageBroker-6] GethHttpServiceImpl - Geth call: net_peerCount
[INFO ] 2020-07-23 10:24:19.450 [MessageBroker-6] GethHttpServiceImpl - Geth call: eth_blockNumber
[INFO ] 2020-07-23 10:24:19.454 [MessageBroker-6] GethHttpServiceImpl - Geth call: txpool_status
[INFO ] 2020-07-23 10:24:19.462 [MessageBroker-6] GethHttpServiceImpl - Geth call: admin_peers
[INFO ] 2020-07-23 10:24:20.133 [BlockScanner-44] GethHttpServiceImpl - Geth call: admin_peers
[INFO ] 2020-07-23 10:24:20.142 [BlockScanner-44] GethHttpServiceImpl - Geth call: eth_getBlockByNumber
[INFO ] 2020-07-23 10:24:22.152 [BlockScanner-44] GethHttpServiceImpl - Geth call: admin_peers
[INFO ] 2020-07-23 10:24:22.156 [BlockScanner-44] GethHttpServiceImpl - Geth call: eth_getBlockByNumber
[INFO ] 2020-07-23 10:24:23.992 [MessageBroker-3] GethHttpServiceImpl - Geth call: eth_getBlockByNumber
[INFO ] 2020-07-23 10:24:24.160 [BlockScanner-44] GethHttpServiceImpl - Geth call: admin_peers
[INFO ] 2020-07-23 10:24:24.168 [BlockScanner-44] GethHttpServiceImpl - Geth call: eth_getBlockByNumber
[INFO ] 2020-07-23 10:24:24.467 [MessageBroker-1] GethHttpServiceImpl - Geth call: admin_nodeInfo
[INFO ] 2020-07-23 10:24:24.471 [MessageBroker-1] GethHttpServiceImpl - Geth call: eth_mining
[INFO ] 2020-07-23 10:24:24.475 [MessageBroker-1] GethHttpServiceImpl - Geth call: net_peerCount
[INFO ] 2020-07-23 10:24:24.479 [MessageBroker-1] GethHttpServiceImpl - Geth call: eth_blockNumber
[INFO ] 2020-07-23 10:24:24.483 [MessageBroker-1] GethHttpServiceImpl - Geth call: txpool_status
[INFO ] 2020-07-23 10:24:24.487 [MessageBroker-1] GethHttpServiceImpl - Geth call: admin_peers
[INFO ] 2020-07-23 10:24:26.176 [BlockScanner-44] GethHttpServiceImpl - Geth call: admin_peers
[INFO ] 2020-07-23 10:24:26.180 [BlockScanner-44] GethHttpServiceImpl - Geth call: eth_getBlockByNumber
[INFO ] 2020-07-23 10:24:28.184 [BlockScanner-44] GethHttpServiceImpl - Geth call: admin_peers
[INFO ] 2020-07-23 10:24:28.192 [BlockScanner-44] GethHttpServiceImpl - Geth call: eth_getBlockByNumber
[INFO ] 2020-07-23 10:24:29.012 [MessageBroker-4] GethHttpServiceImpl - Geth call: eth_getBlockByNumber
[INFO ] 2020-07-23 10:24:29.492 [MessageBroker-2] GethHttpServiceImpl - Geth call: admin_nodeInfo
[INFO ] 2020-07-23 10:24:29.497 [MessageBroker-2] GethHttpServiceImpl - Geth call: eth_mining
[INFO ] 2020-07-23 10:24:29.502 [MessageBroker-2] GethHttpServiceImpl - Geth call: net_peerCount
[INFO ] 2020-07-23 10:24:29.505 [MessageBroker-2] GethHttpServiceImpl - Geth call: eth_blockNumber
[INFO ] 2020-07-23 10:24:29.509 [MessageBroker-2] GethHttpServiceImpl - Geth call: txpool_status
[INFO ] 2020-07-23 10:24:29.512 [MessageBroker-2] GethHttpServiceImpl - Geth call: admin_peers
[INFO ] 2020-07-23 10:24:30.199 [BlockScanner-44] GethHttpServiceImpl - Geth call: admin_peers
[INFO ] 2020-07-23 10:24:30.207 [BlockScanner-44] GethHttpServiceImpl - Geth call: eth_getBlockByNumber
[INFO ] 2020-07-23 10:24:32.216 [BlockScanner-44] GethHttpServiceImpl - Geth call: admin_peers
[INFO ] 2020-07-23 10:24:32.220 [BlockScanner-44] GethHttpServiceImpl - Geth call: eth_getBlockByNumber
[INFO ] 2020-07-23 10:24:34.018 [MessageBroker-5] GethHttpServiceImpl - Geth call: eth_getBlockByNumber
[INFO ] 2020-07-23 10:24:34.223 [BlockScanner-44] GethHttpServiceImpl - Geth call: admin_peers
[INFO ] 2020-07-23 10:24:34.232 [BlockScanner-44] GethHttpServiceImpl - Geth call: eth_getBlockByNumber
[INFO ] 2020-07-23 10:24:34.517 [MessageBroker-2] GethHttpServiceImpl - Geth call: admin_nodeInfo
[INFO ] 2020-07-23 10:24:34.525 [MessageBroker-2] GethHttpServiceImpl - Geth call: eth_mining
[INFO ] 2020-07-23 10:24:34.531 [MessageBroker-2] GethHttpServiceImpl - Geth call: net_peerCount


geth.rpcapi.list=admin,eth,debug,net,personal,web3
