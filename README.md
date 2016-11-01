# musicoin

this is the main file structure for the musicoin app.


## How to setup genesis

Execute as `sudo`:
`sudo su -`

`cd ~`

`git clone https://github.com/BerryAI/.musicoin.git` then enter your password

`ls -la` to check `.musicoin` exists

`geth --datadir ~/.musicoin/blockdata init ~/.musicoin/musicoin_genesis_1_no_allocation.json`

`rm -r ~/.musicoin/blockdata/geth`

`geth --datadir ~/.musicoin/blockdata init ~/.musicoin/musicoin_genesis_2_with_allocation.json`


`geth --datadir ~/.musicoin/blockdata --networkid 55313716  --identity Musicoin --port 30303 --nodiscover console`

`personal.newAccount()`, with passphrase `Berry`

`eth` to check `coinbase` and `account` have been filled

`miner.start()` to start miner



# Running from second node

`cd ~`

`git clone https://github.com/BerryAI/.musicoin.git` then enter your password

`ls -la` to check `.musicoin` exists

`geth --datadir ~/.musicoin/blockdata init ~/.musicoin/musicoin_genesis_2_with_allocation.json`

(A) If you do not need to specify `datadir`:

`geth --bootnodes enode://6eabaf7108c6117b77426cd65d599fa1ee6933cb41982f6eaab009e00d0490799a0cb3e754e063ceebda8dcdcb55cfeb5d11bf635e1fe5c9242b8794fa511d07@104.198.70.194:30303 --identity Musicoin --networkid 55313716 console`

OR (B) If you need to specify `datadir`:

`geth --bootnodes enode://6eabaf7108c6117b77426cd65d599fa1ee6933cb41982f6eaab009e00d0490799a0cb3e754e063ceebda8dcdcb55cfeb5d11bf635e1fe5c9242b8794fa511d07@104.198.70.194:30303 --identity Musicoin --networkid 55313716 --datadir ~/.musicoin console`


