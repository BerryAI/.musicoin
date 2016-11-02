# musicoin

This repo contains the main file structure for the musicoin app backend for blockchain data.


## How to setup genesis

Install the geth/ Ethereum packages

```
sudo apt-get install software-properties-common
sudo add-apt-repository -y ppa:ethereum/ethereum
sudo add-apt-repository -y ppa:ethereum/ethereum-dev
sudo apt-get update
sudo apt-get install ethereum
sudo apt-get install ethminer
```

`sudo su -`

`cd ~`

`git clone https://github.com/BerryAI/.musicoin.git` then enter your password

`ls -la` to check `.musicoin` exists

`geth --datadir ~/.musicoin init ~/.musicoin/musicoin_genesis.json`

`geth --datadir ~/.musicoin --networkid 55313716  --identity Musicoin --port 30303 console`

*Inside console:*

`personal.newAccount()`, with passphrase `Berry`

`eth` to check `coinbase` and `account` have been filled

`miner.start()` to start miner



### For manually adding peers to the nodes

Execute `admin.addPeer("enode://...@[ip_addr]:port")` in geth console


*For genesis node 1 and node 1b*

node 1:

address: `enode://96eb532a30efaf5e968d837207da5b3545316966ac06d30aad1a74d7e68c787e8405f6cf5dc218a5528cb2d619435bdaeb9f8cb8955df9ab9dd12ef085fe9009@104.198.70.194:30303`

admin.addPeer("enode://96eb532a30efaf5e968d837207da5b3545316966ac06d30aad1a74d7e68c787e8405f6cf5dc218a5528cb2d619435bdaeb9f8cb8955df9ab9dd12ef085fe9009@104.198.70.194:30303")

node 1b:

address: `enode://6c262c6e95f65ab0199fdd4832eab17512372a145fb057602fa322d72d331b384881cc1a0bd6e690367bc309cb38f5dbaafe9e93cee26246d83ef23f22379bef@104.197.75.174:30303`

admin.addPeer("enode://6c262c6e95f65ab0199fdd4832eab17512372a145fb057602fa322d72d331b384881cc1a0bd6e690367bc309cb38f5dbaafe9e93cee26246d83ef23f22379bef@104.197.75.174:30303")



## Running from the second node

Install the geth/ Ethereum packages

```
sudo apt-get install software-properties-common
sudo add-apt-repository -y ppa:ethereum/ethereum
sudo add-apt-repository -y ppa:ethereum/ethereum-dev
sudo apt-get update
sudo apt-get install ethereum
sudo apt-get install ethminer
```

`cd ~`

`git clone https://github.com/BerryAI/.musicoin.git` then enter your password

`ls -la` to check `.musicoin` exists

`geth --datadir ~/.musicoin init ~/.musicoin/musicoin_genesis.json`

`geth --identity Musicoin --networkid 55313716 --datadir ~/.musicoin console`

Finding initial peers is not so easy. Adding 2 static nodes above may help a new node to sync, although it seems not be a permanent solution. You can configure permanent static nodes by putting something like the following into &lt;datadir&gt;/static-nodes.json:
```
["enode://6c262c6e95f65ab0199fdd4832eab17512372a145fb057602fa322d72d331b384881cc1a0bd6e690367bc309cb38f5dbaafe9e93cee26246d83ef23f22379bef@104.197.75.174:30303",
  "enode://96eb532a30efaf5e968d837207da5b3545316966ac06d30aad1a74d7e68c787e8405f6cf5dc218a5528cb2d619435bdaeb9f8cb8955df9ab9dd12ef085fe9009@104.198.70.194:30303"
]
```
Note for Windows users: You may need to change your path from `~/.musicoin` to somewhere in your PC.

If you want to access Geth from RPC, you may need to add `--rpc --rpcapi="db,eth,net,web3,personal" --rpcport "8545" --rpcaddr "127.0.0.1" --rpccorsdomain "localhost"` with geth command. 
