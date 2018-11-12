# intervalue-2.0.0-testnet

for tps test.

## Introduction  
fullnode - shard all local full nodes, get local full node list, show tps info.  
localfullnode - receive transaction messages, create events with transactions, gossip events with other nodes, consensus events and transactions, calculate tps.  
light-demo - construct transaction messages, and send to local full node.

## Manual  
### fullnode
1. config(default.config) 
statisticsInterval=3000 ***#tps statistics interval(ms)***  
statisticsBatches=1000 ***#tps statistics interval(ms)***  
ShardSize =1  
LocalFullNodeSize = 3 ***#ShardSize\*LocalFullNodeSize must equal local full node number***  
NeighborSize=3   
seed.pubIP = 172.17.2.40  
seed.port = 20000  
seed.rpcPort = 20001  
seed.httpPort = 20002  

2. run  
command: nohup java -jar seed-1.0.0-pg.jar --Ice.Config=./default.config &  

