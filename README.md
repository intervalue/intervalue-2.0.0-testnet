# intervalue-2.0.0-testnet

for tps test.

## Introduction  
fullnode - shard all local full nodes, get local full node list, show tps info.  
localfullnode - receive transaction messages, create events with transactions, gossip events with other nodes, consensus events and transactions, calculate tps.  
light-demo - construct transaction messages, and send to local full node.

## Manual 
### env  
  ubuntu16.04, jdk1.8(sun)  
  
### fullnode  
1. config(default.config)  
  keep default.config and seed-1.0.0-pg.jar in the same path.  
  _ShardSize,LocalFullNodeSize,NeighborSize,seed.pubIP,seed.port,seed.rpcPortseed.httpPort_ are very important.
  ShardSize\*LocalFullNodeSize must be equal to total number of local full nodes.
2. run  
  command: nohup java -jar seed-1.0.0-pg.jar --Ice.Config=./default.config &  

### localfullnode   
1. config(default.config)  
  keep default.config and localfullnode-1.0.0-pg.jar in the same path.  
2. run  
command: nohup java -jar localfullnode-1.0.0-pg.jar --Ice.Config=./default.config &   

### lightnode-demo   
1. config(default.config)  
  keep default.config and light-demo-1.0.0.jar in the same path.  
2. run  
  command: nohup java -jar light-demo-1.0.0.jar --Ice.Config=./default.config &   
